# Exposed .env على subdomain = $250–$10k+ (Easy $250 case + higher)

**Rating:** 🔥 قوية  
**Category:** Recon  
**Status:** Not started  

## How It Works

بعد subfinder + httpx، شغّل ffuf/dirsearch على .env و .env.backup و .env.local. في حالة exam proctoring موقع طلع .env وخد $250. في fintech طلع Stripe + AWS = آلاف.

## Payload / Code

```
ffuf -u https://FUZZ.target.com/.env -w subs.txt -mc 200
dirsearch -u https://sub.target.com -e env,bak,sql -t 30
```

## Source

Abhijeet Kumawat writeup ($250) + multiple fintech cases $500–$10k+

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
