# Daily Project Log

---

## September 5, 2026

### Focus

Box data integration / programmatic data access.

### What I Did

- Created a Box Platform App for the project.
- Configured OAuth 2.0 authentication.
- Configured the localhost OAuth callback:
  `http://localhost:3000/callback`
- Added Box credentials to a local `.env` file.
- Added the Box folder ID and dataset filename as configuration.
- Added dependencies to `requirements.txt`.
- Created `utils/box_client.py`.
- Implemented the Box OAuth authorization flow.
- Created `utils/data_access.py`.
- Implemented logic to:
  1. retrieve the configured Box folder,
  2. find the configured CSV file,
  3. download the file,
  4. load the CSV with pandas.
- Used persistent token storage for the OAuth authentication flow.
- Started the Flask server locally.
- Tested the Box authorization flow.
- Initially encountered an error caused by using the wrong parameter name.
- Corrected `redirect_url` to `redirect_uri`.
- Successfully reached the Box authorization page.
- Discovered that the Box Platform App is disabled by the Chico State administrator.

### Technical Details

#### Authentication

Used OAuth 2.0 rather than storing a Box username/password.

#### Configuration

Sensitive credentials are stored locally in `.env`.

The repository should not contain:

- Box client secret
- OAuth access token
- OAuth refresh token
- `.env`

The repository can contain:

- Box folder ID
- dataset filename
- `.env.example`

#### Data Flow

Current intended architecture:

    Box
      ↓
    OAuth authentication
      ↓
    Box API
      ↓
    Specific Box folder
      ↓
    Kickstarter CSV
      ↓
    Python
      ↓
    pandas DataFrame

### Why I Did This

The Kickstarter dataset itself is publicly available, but the team's
shared copy is stored in Box.

I wanted to make data access programmatic and reproducible instead of
requiring a person to manually download the CSV.

This also provides experience with an enterprise-style cloud data
workflow involving authentication, API access, configuration, and
programmatic ingestion.

### What I Learned

- OAuth 2.0 authentication
- Box Platform Apps
- Box API / Python SDK
- Persistent token storage
- Flask routes
- OAuth redirect URIs
- Environment variables
- Secret management
- Programmatic file discovery
- Downloading cloud files from Python
- Loading downloaded data into pandas

### Problems / Errors

#### Error 1

Used:

`redirect_url`

The SDK expected:

`redirect_uri`

Result:

`TypeError: GetAuthorizeUrlOptions.__init__() got an unexpected keyword argument 'redirect_url'`

### Fix

Changed the parameter to:

`redirect_uri`

### Error 2

Box authorization page reported that the application was disabled by
the administrator.

### Diagnosis

This appears to be an account/administrator-level Box restriction,
not a Python implementation problem.

### Blocker

Need Chico State Box administrator approval/enabling of the Platform
App before the complete end-to-end flow can be tested.

### What I Would Say in a Presentation

> I built a programmatic Box-to-Python ingestion workflow using OAuth 2.0
> so the team's shared dataset could be accessed reproducibly rather than
> manually downloaded.

### What I Would Say in an Interview

> One of my contributions was building the data-access layer. I
> configured a Box OAuth integration, separated credentials from the
> code using environment variables, and wrote Python utilities to
> locate and download the project's dataset from a specific Box folder.
> During implementation I also had to troubleshoot the OAuth redirect
> configuration and distinguish an application-level error from an
> administrator-side access restriction.

### Next Steps

- Resolve Box administrator access.
- Test authenticated file listing.
- Test CSV download.
- Test pandas loading.
- Connect authenticated Box client to the data-access module.
- Determine how this fits into the team's broader preprocessing pipeline.

---
