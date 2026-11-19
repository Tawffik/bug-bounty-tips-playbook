# CSRF في GraphQL Targets

**Rating:** ⭐ جيدة  
**Category:** CSRF  
**Status:** Not started  

## How It Works

GraphQL مالوش فيها حماية مدمجة ضد CSRF. لو لقيت طلب بيغير حالة بدون token، والـ backend بيقبل content-type غير JSON، تقدر تعمل CSRF form عادي ليه.

## Payload / Code

```
1) لاقي mutation بيغير حالة مش محتاج token
2) غيّر content-type من application/json إلى application/x-www-form-urlencoded
3) اعمل form html بتبعت الـ mutation body مباشرة
```

## Source

Intigriti Official — 31 Bug Bounty Tips 2026 (Tip 30)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
