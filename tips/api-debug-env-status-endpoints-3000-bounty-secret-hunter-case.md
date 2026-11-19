# API Debug /env /status endpoints → $3,000 Bounty (Secret Hunter case)

**Rating:** 🔥 قوية  
**Category:** Recon, API Hacking  
**Status:** Not started  

## How It Works

كثير APIs بتسيب /debug أو /env أو /_debug أو /health مع verbose mode. بيرجع environment variables كاملة. استخدم ffuf بقائمة debug endpoints.

## Payload / Code

```
ffuf -u https://target.com/api/FUZZ -w debug_endpoints.txt -mc 200
# قائمة: debug, env, status, health, _debug, actuator/env
```

## Source

Undercode Testing writeup – $3,000 paid

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
