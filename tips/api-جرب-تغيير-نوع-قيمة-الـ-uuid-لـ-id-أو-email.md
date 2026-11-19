# API: جرّب تغيير نوع قيمة الـ UUID لـ ID أو Email

**Rating:** ⭐ جيدة  
**Category:** API Hacking, IDOR  
**Status:** Not started  

## How It Works

لما endpoint بيقبل UUID كـ identifier، جرّب تبعتله ID رقمي أو إيميل بدل الـ UUID. بعض الباكيندات بتعمل CASE على أكتر من نوع identifier في نفس الاستعلام، وده ممكن يفتح مسارات وصول تانية.

## Payload / Code

```
/api/user/a8ae-1322-ac09-8f90
/api/user/1
/api/user/user@a.test

SQL موازي محتمل في الباكيند:
SELECT * FROM subscribers WHERE
  CASE
    WHEN $1 > 0 THEN id = $1
    WHEN $2 != '' THEN uuid = $2::UUID
    WHEN $3 != '' THEN email = $3
  END;
```

## Source

Anton @thercem an

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
