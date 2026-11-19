# 200 OK is not proof of BOLA

**Rating:** 🔥 قوية  
**Category:** IDOR, API Hacking  
**Status:** Not started  

## How It Works

الـstatus code لوحده مش finding. لازم تثبت إن response رجّع object مختلف أو إن state اتغيّر فعلاً. قارن body/headers/length، وبعدها اعمل verification من مالك object في حساب تاني تملكه.

## Payload / Code

```
Use a harmless canary value in a lab and verify it from the second controlled account. Treat redirects, generic success JSON, and identical empty bodies as inconclusive.
```

## Source

https://portswigger.net/burp/documentation/desktop/testing-workflow/vulnerabilities/access-controls

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
