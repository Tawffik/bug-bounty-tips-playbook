# Bypass الدفع بالـ Test Cards المنسية في Production

**Rating:** ⭐ جيدة  
**Category:** General  
**Status:** Not started  

## How It Works

بعض المطورين بينسوا يشيلوا test cards بتاعة payment gateways (Stripe, PayPal) في الـ Production. لو اشتغلت، ممكن تعمل orders بدون ما تتخصم فلوس.

## Payload / Code

```
jarrib cards معروفة زي: 4242 4242 4242 4242 (Stripe test card) على الـ production checkout
```

## Source

Intigriti Official — 31 Bug Bounty Tips 2026 (Tip 22)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
