# 404 Subdomains — Backend errors, S3 paths, and leaked stack info

**Rating:** 🔥 قوية  
**Category:** Recon, Subdomain Enum  
**Status:** Not started  

## How It Works

Subdomains that return 404 are often ignored. Hitting a non-existent path on those hosts can still surface backend error pages, stack traces, internal paths, S3 references, or dev leftovers that never appear on the main site.

## Payload / Code

```
1) Enumerate subs → httpx
2) Keep hosts with interesting 404/500 behavior
3) Probe: /random404, /nonexistent, /.env, /debug
4) Review body for stack traces, bucket URLs, internal hostnames

Example idea:
https://test.api.target.com/random404
```

## Source

Hatem Aliyan — Bug Bounty Tip (404 pages)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
