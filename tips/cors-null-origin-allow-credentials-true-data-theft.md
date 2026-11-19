# CORS null origin + Allow-Credentials: true → data theft

**Rating:** 🔥 قوية  
**Category:** API Hacking  
**Status:** Not started  

## How It Works

لو الـ response بيرجع Access-Control-Allow-Origin: null مع Credentials true، تقدر من sandboxed iframe أو data: URI تسحب البيانات الحساسة.

## Payload / Code

```
Origin: null
# شوف لو ACAO: null و ACAC: true
```

## Source

Intigriti CORS advanced guide 2025/2026

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
