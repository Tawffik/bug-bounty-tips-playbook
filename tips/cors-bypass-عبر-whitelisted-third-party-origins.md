# CORS Bypass عبر Whitelisted Third-Party Origins

**Rating:** 🔥 قوية  
**Category:** CSRF, General  
**Status:** Not started  

## How It Works

بعض الأنظمة بتعمل whitelist لـ domains زي GitHub Pages, CodePen, Replit للتطوير لكن بتنسى تشيلهم في Production. استضيف الـ PoC بتاعك على أي من الـ domains دي واعمل cross-origin request تتجاوز CORS لأنها موثوقة.

## Payload / Code

```
1) افحص Access-Control-Allow-Origin في الـ response headers
2) لو فيه domains زي *.github.io أو codepen.io مسموحة
3) استضيف fetch() PoC على نفس الـ domain ده واسحب البيانات
```

## Source

Intigriti Official — 31 Bug Bounty Tips 2026 (Tip 31)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
