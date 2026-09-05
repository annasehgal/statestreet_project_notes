# Questions and Blockers

---

## Open Questions

### Data

- [ ] Which features are available at campaign launch?
- [ ] Which features cause target leakage?
- [ ] Should the model only use information known before launch?
- [ ] Should campaigns outside the U.S. be excluded?
- [ ] How should missing values be handled?

### Modeling

- [ ] What should the baseline performance be?
- [ ] Which model performs best?
- [ ] Is accuracy enough?
- [ ] How should class imbalance be handled?
- [ ] Which metric should receive the most attention?

### Recommendations

- [ ] How do we translate model findings into recommendations?
- [ ] Should recommendations be rule-based?
- [ ] Should they use feature importance?
- [ ] How personalized should recommendations be?

### Deployment

- [ ] What information should the user enter?
- [ ] What should the prediction page display?
- [ ] How should probability be shown?
- [ ] How should recommendations be generated?

---

# Blockers

## Box Administrator Access

### Status

Blocked

### Description

The Box Platform App is currently disabled by the Chico State Box
administrator.

### Impact

Cannot complete authenticated end-to-end testing.

### What I Have Completed

- App creation
- OAuth configuration
- Redirect URI
- Python authentication code
- Data-access code

### Next Action

Contact Box administrator / IT support.

---

# Resolved Issues

## OAuth Redirect Parameter

### Problem

Used `redirect_url`.

### Error

`GetAuthorizeUrlOptions` did not accept `redirect_url`.

### Resolution

Changed to `redirect_uri`.

### Lesson

Check the SDK's current API rather than relying on older tutorials.
