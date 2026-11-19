# Elmah.axd /elmah → Session cookies → Employee ATO ($6,000 escalation case)

**Rating:** 📌 للمراجعة  
**Category:** Recon, Auth Bypass  
**Status:** Not started  

## How It Works

ضيف /elmah و /elmah.axd للكلمة. لو مفتوح، ادخل Details على أي log → هتلاقي full HTTP request بما فيها session cookies. خد الكوكي وجربه على الـ main site → غالباً employee أو admin ATO. لو الـ logs فاضية، راقبها ساعات لأن ساعات بتمسح hourly.

## Payload / Code

```
https://target.com/elmah.axd
https://target.com/elmah
```

## Source

Jayesh Madnani tip – $6000 from escalating Elmah disclosure

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
