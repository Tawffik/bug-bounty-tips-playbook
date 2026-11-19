# Excessive API fields + GDPR/CCPA framing لرفع الـ Severity

**Rating:** 🔥 قوية  
**Category:** API Hacking, General  
**Status:** Not started  

## How It Works

لما الـ API بيرجع fields زيادة (address, phone, SSN last4, internal notes)، اكتب التقرير مع ذكر GDPR/CCPA risk و business impact (identity theft, regulatory fines). ده بيرفع الـ severity من Low/Medium لـ High في كتير من البرامج.

## Payload / Code

```
قارن الـ UI fields مع الـ raw JSON response
```

## Source

ToxSec Medium + Intigriti privacy guidance

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
