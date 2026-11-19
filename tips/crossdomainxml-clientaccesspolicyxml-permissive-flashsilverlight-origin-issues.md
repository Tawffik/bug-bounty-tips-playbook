# crossdomain.xml / clientaccesspolicy.xml permissive → Flash/Silverlight origin issues

**Rating:** 📌 للمراجعة  
**Category:** Recon  
**Status:** Not started  

## How It Works

لو الملف بيسمح لأي domain (*)، ممكن يستخدم في بعض الـ legacy attacks أو كـ info disclosure عن الـ allowed origins.

## Payload / Code

```
https://target.com/crossdomain.xml
https://target.com/clientaccesspolicy.xml
```

## Source

Older but still checked in some programs

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
