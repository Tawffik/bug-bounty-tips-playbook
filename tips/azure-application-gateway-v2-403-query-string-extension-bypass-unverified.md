# Azure Application Gateway v2 — 403 Query String Extension Bypass (Unverified)

**Rating:** 📌 للمراجعة  
**Category:** WAF Bypass  
**Status:** Not started  

## How It Works

Reported observation from an X post: a restricted URL returns HTTP 403, but adding a query parameter whose value contains the literal string .js (example: ?x=.js) reportedly changes the response and may allow access to the resource. The author suspects a Microsoft Azure Application Gateway v2 filtering/parsing behavior and says the cause is still being investigated. This is an unverified hypothesis, not a confirmed general bypass. Possible class to investigate: disagreement between gateway/WAF URL inspection and downstream application or routing interpretation of the query string.

## Payload / Code

```
Baseline: https://authorized-target.example/restricted-path
Comparison variant: https://authorized-target.example/restricted-path?x=.js

Only replace the placeholder with a target explicitly in scope. Compare status, redirect chain, response headers, body length/hash, and whether the actual protected resource is returned. Do not treat HTTP 200 alone as proof; check for a block page, login page, or generic error.
```

## Source

https://x.com/GodfatherOrwa/status/2114030843077259297

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
