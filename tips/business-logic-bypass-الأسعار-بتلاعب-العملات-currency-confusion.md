# Business Logic: Bypass الأسعار بتلاعب العملات (Currency Confusion)

**Rating:** 🔥 قوية  
**Category:** General  
**Status:** Not started  

## How It Works

الأنظمة اللي بتتعامل مع أكتر من عملة بتستخدم exchange rate function. لو مفيش تحقق كويس، جرّب تغيّر العملة لعملة أضعف (زي INR أو JPY) وشوف هل السعر النهائي بيتحسب صح ولا لأ — ممكن تشتري بسعر أقل بكتير من قيمة المنتج الحقيقية.

## Payload / Code

```
لو فيه param اسمه currency أو lang بيتحكم في الـ pricing، جرّب:
currency=INR بدل currency=USD (مع نفس السعر الرقمي)
وشوف هل السيرفر بيحول العملة صح أو لأ
```

## Source

Intigriti Official — 31 Bug Bounty Tips 2026 (Tip 20)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
