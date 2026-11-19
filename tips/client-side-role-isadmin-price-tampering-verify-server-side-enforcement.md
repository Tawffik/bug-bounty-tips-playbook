# Client-side role / isAdmin / price tampering — verify server-side enforcement

**Rating:** ⭐ جيدة  
**Category:** API Hacking, Auth Bypass  
**Status:** Not started  

## How It Works

Changing client-side values such as isAdmin, role, isAuthenticated, or price matters only if the server trusts them when authorizing an action or calculating a security-sensitive value. UI-only changes are not proof of a vulnerability.

## Payload / Code

```
With an explicitly authorized test account and test data, compare the normal request with a controlled change to a client-controlled field. Verify server-side behavior using only actions and records you own. Do not modify real purchases, payments, roles, or other users' data.
```

## Source

User-provided screenshot: response manipulation / role and price fields; normalized into a server-side authorization check

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
