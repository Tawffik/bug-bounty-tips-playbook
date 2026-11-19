# AI support chatbot that renders model output in DOM → XSS → session theft / ATO

**Rating:** 🔥 قوية  
**Category:** XSS, Auth Bypass  
**Status:** Not started  

## How It Works

شركات كثيرة تضيف chatbot دعم بدون تدقيق مخرجات النموذج. لو البوت يفك payload (base64/URL-decode) ويعرض الناتج في DOM بدون sanitization، تحصل على XSS مخزّن أو منعكس عبر قناة المحادثة. سلسلة شائعة: XSS → سرقة cookies/tokens أو OAuth cookie-downgrade → account takeover. القاعدة: أي مخرجات LLM تُرسَم في الصفحة = سطح هجوم. اختبر على برامج مصرّح بها فقط، بأدلة (request/response + DOM proof) من غير إضرار بالمستخدمين.

## Payload / Code

```
1) Find in-scope AI/chat/support endpoints
2) Send encoded XSS (base64, HTML entities, markdown that becomes HTML)
3) Confirm bot decodes and DOM reflects/executes
4) Escalate only with proof: cookie access, token leak, or auth action in same origin
Heuristic: "If it renders in the DOM, treat it as injectable until proven sanitized."
```

## Source

Patrickbatman writeup tip (X) — AI bot decoded base64 XSS into DOM

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
