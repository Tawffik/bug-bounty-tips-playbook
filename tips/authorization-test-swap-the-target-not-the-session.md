# Authorization test: swap the target, not the session

**Rating:** 🔥 قوية  
**Category:** IDOR, API Hacking  
**Status:** Not started  

## How It Works

في أي request authenticated، افصل بين هوية الـsession وبين object ID الموجود في الـpath/body. جرّب نفس session مع object تاني تملكه أنت. الهدف إثبات إن السيرفر بيربط القرار بالـsubject الصحيح، مش بمجرد إن المستخدم logged in.

## Payload / Code

```
Safe lab idea: Account A session + Account B test object ID. Change only a harmless field such as nickname. Confirm the change from Account B.
```

## Source

https://portswigger.net/web-security/access-control/idor

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
