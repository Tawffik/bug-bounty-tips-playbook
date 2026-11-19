# Blind SSRF Detection عبر Interactsh

**Rating:** 🔥 قوية  
**Category:** SSRF  
**Status:** Not started  

## How It Works

لو الـ SSRF مش بترجع أي رد في الـ response (blind)، استخدم سيرفر out-of-band زي Interactsh للتأكد من وجود الثغرة عبر أي DNS/HTTP callback يوصلك.

## Payload / Code

```
1) تنصيب: go install -v github.com/projectdiscovery/interactsh/cmd/interactsh-client@latest
2) تشغيل: interactsh-client -server oast.pro -n 5
3) حط الـ subdomain اللي طلعتلك مكان الـ URL المستهدف في الـ request
4) أي callback يرجع = تأكيد وجود الثغرة
```

## Source

Redfox Security 2026

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
