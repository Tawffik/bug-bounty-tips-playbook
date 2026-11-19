# Casdoor — token exchange must bind JWT identity to the target organization

**Rating:** 🔥 قوية  
**Category:** Auth Bypass, API Hacking  
**Status:** Not started  

## How It Works

The reported Casdoor issue involved token exchange validating a JWT signature without verifying that the token's user belonged to the same organization as the target application. A valid token from one organization could cross an organization boundary if the missing binding check and affected versions were present.

## Payload / Code

```
For an authorized lab with two test organizations and accounts, test whether token exchange enforces both signature validity and organization/tenant membership. Use only test identities and non-sensitive scopes; record the subject, issuer, organization, target app, and resulting permissions. Do not replay real users' tokens. Advisory says affected versions were fixed in 2.387.0.
```

## Source

GitHub Advisory GHSA-c9w5-qp6m-m395 (CVE-2026-9094): https://github.com/advisories/GHSA-c9w5-qp6m-m395

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
