# 404 response → check for exposed config or repository paths

**Rating:** ⭐ جيدة  
**Category:** Recon  
**Status:** Not started  

## How It Works

صفحة 404 عادية قد تساعد في ملاحظة سلوك routing غير متوقع، لكنها لا تعني أن الملفات بجوارها موجودة. اختبر المسارات الشائعة على أصل الموقع فقط وداخل النطاق، وسجّل status code وحجم الاستجابة ومحتواها. لا تفترض أن حالة المكافأة المذكورة قابلة للتعميم.

## Payload / Code

```
https://target.com/some/404/path/.git/config
https://target.com/some/404/path/.env
```

## Source

InfoSec Write-ups — الرابط الأصلي يحتاج إضافة للتحقق من الحالة المذكورة

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
