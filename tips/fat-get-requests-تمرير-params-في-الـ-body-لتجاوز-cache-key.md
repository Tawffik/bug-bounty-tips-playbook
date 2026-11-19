# Fat GET Requests — تمرير Params في الـ Body لتجاوز Cache Key

**Rating:** 🔥 قوية  
**Category:** WAF Bypass, API Hacking  
**Status:** Not started  

## How It Works

بعض السيرفرات (خصوصًا Ruby/PHP/بعض الـ frameworks) بتقرا الباراميترات من body بتاع ريكوست GET كمان. الكاش بيعمل الـ cache key على الـ URL/query فقط ومبيشوفش الـ body، فالقيمة اللي في الـ body تعتبر unkeyed input. ده بيديك مدخل مخفي تسمّم بيه الكاش أو تتجاوز فلاتر الـ WAF اللي بتفحص الـ query string بس.

## Payload / Code

```
GET /search?q=test HTTP/1.1
Host: target.com
Content-Length: 24

q=<script>alert(1)</script>
// بعض الـ frameworks بتقرا الـ params من body الـ GET، بينما الكاش بيعمل key على query string بس
```

## Source

SecurityCipher — Web Cache Poisoning Playbook 2026

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
