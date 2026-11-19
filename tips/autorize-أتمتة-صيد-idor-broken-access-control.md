# Autorize — أتمتة صيد IDOR / Broken Access Control

**Rating:** 🔥 قوية  
**Category:** IDOR, Auth Bypass  
**Status:** Not started  

## How It Works

بدل ما تختبر كل endpoint يدوي للـ access control، Autorize بياخد كوكيز مستخدم أقل صلاحية وبيعيد تلقائيًا كل ريكوست بتعمله وانت متصفح بحساب أعلى، وبيقولك لو الـ endpoint اتفتح بصلاحية أقل (Bypassed). نص اكتشافات الـ IDOR بتيجي من تشغيله في الخلفية أثناء التصفح العادي.

## Payload / Code

```
1) سجّل حسابين: low-priv (victim cookies تتحط في Autorize) + high-priv تتصفح بيه
2) حط cookies حساب الـ low-priv في Autorize
3) اتصفح كل فيتشرز الحساب العالي صلاحية عادي
4) Autorize بيعيد كل ريكوست بالكوكيز الأقل صلاحية ويقارن الرد (Enforced/Bypassed!)
```

## Source

Autorize (Burp Extension) — HackByNight Real World Guide 2025

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
