# Exposed Google Maps API keys may unlock Gemini — validate model access not just Maps

**Rating:** 🔥 قوية  
**Category:** Recon, API Hacking  
**Status:** Not started  

## How It Works

بعض مفاتيح Google Maps (AIza…) المنشورة في JS قد تكون مربوطة بمشروع Cloud فيه Gemini/Generative Language مفعّل بدون قيود كافية. وجود المفتاح وحده ليس ثغرة؛ الأثر يبدأ عندما يثبت أن نفس المفتاح يستدعي models أو يتجاوز referrer/API restrictions. ابحث في: JS/source maps، Wayback، Android APKs، web assets. بعد الاستخراج اختبر فقط على نطاق مصرّح ووثّق الـAPI المفعّلة والقيود (HTTP referrer، IP، API restrictions) قبل أي بلاغ.

## Payload / Code

```
Hunt sources: JS bundles, .js.map, waybackurls, APK strings.
Pattern: AIza[0-9A-Za-z_-]{35}
Validate impact (authorized only): try Generative Language / Gemini endpoints if program allows; check Maps quotas vs other Google APIs; document restriction bypass evidence.
Tool mention: geminiHunter (community) for multi-source discovery — treat output as LEAD until impact proven.
```

## Source

Zeroday Lab / geminiHunter tip (X, Nov 2026)

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
