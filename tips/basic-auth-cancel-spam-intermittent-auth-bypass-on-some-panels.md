# Basic Auth cancel spam — intermittent auth bypass on some panels

**Rating:** 📌 للمراجعة  
**Category:** Auth Bypass  
**Status:** Not started  

## How It Works

في بعض لوحات login القديمة، إلغاء نافذة Basic Auth عدة مرات قد يُسقط الجلسة إلى حالة authenticated أو يكشف محتوى محمي بسبب خطأ في منطق التحدي. نادر وغير مضمون؛ وثّق بدقة إن نجح ولا تعتمد عليه كمنهج أساسي.

## Payload / Code

```
Open protected path → browser Basic Auth prompt → Cancel 3–4 times → observe whether body/admin UI leaks.
Prefer reproducing with raw HTTP (empty Authorization / repeated 401 handling) for a clean PoC.
```

## Source

mahmoud tip (X) — cancel basic auth 3–4 times

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
