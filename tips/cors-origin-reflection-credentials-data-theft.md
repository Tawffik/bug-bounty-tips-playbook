# CORS origin reflection + credentials = data theft

**Rating:** 🔥 قوية  
**Category:** General  
**Status:** Not started  

## How It Works

لو Access-Control-Allow-Origin بيعكس الـ Origin و Access-Control-Allow-Credentials: true → تقدر تسرق responses من متصفح الضحية.

## Payload / Code

```
Origin: https://evil.com
(Check response headers for ACAO + ACAC)
```

## Source

Undercode + recent CVEs 2026

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
