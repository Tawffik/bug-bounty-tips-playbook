# Bypass الـ WAF عبر إيجاد الـ Origin IP

**Rating:** 🔥 قوية  
**Category:** WAF Bypass  
**Status:** Not started  

## How It Works

كتير من المواقع مخبية ورا Cloudflare أو WAF تاني. لو لقيت IP السيرفر الأصلي (origin) من سجلات DNS قديمة أو certificate transparency logs (قبل ما يطبقوا الـ protection)، تقدر تتعامل مع السيرفر مباشرة بدون ما الـ WAF يشوف أي payload.

## Payload / Code

```
1) دور على الـ IP الأصلي في crt.sh أو سجلات قديمة (SecurityTrails, ViewDNS)
2) ارفع الـ request مباشرة للـ IP مع Host header = target.com
3) لو السيرفر رد عليك، اختبر الـ payloads مباشرة بدون ما يتفلتر من الـ WAF
```

## Source

Intigriti Official — 31 Bug Bounty Tips 2026 (Tip 10)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
