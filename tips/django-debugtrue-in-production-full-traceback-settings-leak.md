# Django DEBUG=True in production → full traceback + settings leak

**Rating:** ⭐ جيدة  
**Category:** Recon  
**Status:** Not started  

## How It Works

لما DEBUG=True، أي error بيرجع full stack + settings (SECRET_KEY أحيانًا). جرب trigger error بـ invalid input.

## Payload / Code

```
أرسل parameter غلط أو path مش موجود وشوف الـ response
```

## Source

Common misconfig (H1 reports)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
