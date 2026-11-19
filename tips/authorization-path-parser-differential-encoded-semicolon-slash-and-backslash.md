# Authorization path parser differential — encoded semicolon, slash, and backslash

**Rating:** 🔥 قوية  
**Category:** Auth Bypass, Fuzzing, API Hacking  
**Status:** Not started  

## How It Works

A security layer and a resource handler may normalize or decode path components differently. Quarkus documented path-based authorization bypass conditions involving encoded semicolons (%3B) and encoded slashes (%2F) or backslashes (%5C), depending on the protected resource and affected version. The reusable primitive is to compare the path representation used by the policy engine with the final handler/resource selected.

## Payload / Code

```
Only in an authorized lab or explicitly in-scope target, start with a known protected test route and a negative control. Change one representation at a time: encoded semicolon, encoded slash, or encoded backslash. Compare policy decision, resolved route, and actual access. Do not treat a 200 response alone as proof; confirm protected content or a state change without exposing real data. Check affected versions and vendor fixes before testing.
```

## Source

Official Quarkus advisory GHSA-qcxp-gm7m-4j5v / CVE-2026-50559: https://github.com/advisories/GHSA-qcxp-gm7m-4j5v

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
