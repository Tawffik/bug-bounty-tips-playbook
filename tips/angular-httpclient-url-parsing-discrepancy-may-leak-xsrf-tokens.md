# Angular HttpClient — URL parsing discrepancy may leak XSRF tokens

**Rating:** 🔥 قوية  
**Category:** CSRF, Fuzzing, API Hacking  
**Status:** Not started  

## How It Works

Angular's HTTP client had an XSRF token leakage issue related to a URL-parsing discrepancy, described as an incomplete fix for CVE-2025-66035. The useful testing pattern is to compare how the framework classifies a request URL against how the browser/network layer resolves the final destination; token attachment must follow the intended same-origin policy.

## Payload / Code

```
In a local app using an affected Angular version, test only controlled same-origin and cross-origin URLs and observe whether the XSRF header is attached to a request that resolves cross-origin. Use a dummy token and a local receiver; do not collect real anti-CSRF tokens from production users. Read the advisory for affected/fixed versions and upgrade guidance.
```

## Source

Official Angular Advisory GHSA-jfgx-762w-99vr (2026-10-16): https://github.com/angular/angular/security/advisories/GHSA-jfgx-762w-99vr

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
