# Bypass قيود الوصول بتغيير حروف الـ Path (Case Sensitivity)

**Rating:** 🔥 قوية  
**Category:** WAF Bypass, Recon  
**Status:** Not started  

## How It Works

بعض الأنظمة (case-sensitive routing) بتفرق في الرد بين الحروف الكبيرة والصغيرة في الـ path، فلو الـ lowercase محطوط أو محمي، جرّب نفس الـ path بحروف مختلفة (Camel/Mixed case) لأن الـ rule اللي بتمنع الوصول بتكون case-sensitive لكن الـ backend مش case-sensitive.

## Payload / Code

```
target[.]com/phpmyadmin/setup/index.php → 301 (راجع للوجن)
target[.]com/phpMyAdmin/setup/index.php → 200 (فتح صفحة setup مباشرة!)

phpmyadmin → 301
phpMyAdmin → 200
```

## Source

kjulius @ethical_h4ck3r_ — Credit: @GodfatherOrwa

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
