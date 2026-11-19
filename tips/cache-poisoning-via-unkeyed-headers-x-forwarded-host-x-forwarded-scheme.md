# Cache Poisoning via Unkeyed Headers (X-Forwarded-Host / X-Forwarded-Scheme)

**Rating:** 🔥 قوية  
**Category:** API Hacking, XSS, General  
**Status:** Not started  

## How It Works

Inject a header the cache does not key on but the application uses for redirects, absolute URLs, or asset generation (X-Forwarded-Host, X-Forwarded-Scheme, X-Original-URL, etc.). If the response is cached with your injected value, subsequent users receive poisoned content (open redirect, XSS, or wrong origin). One request can affect many users.

## Payload / Code

```
X-Forwarded-Host: evil.com
X-Forwarded-Scheme: http
X-Original-URL: /evil

Then force cache hit and observe Location / script src / link tags reflecting the poisoned host.
```

## Source

Twitter/X @gustavorobertux — Bug Bounty Tip #19/30 Cache poisoning (Nov 2026) + classic PortSwigger patterns

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
