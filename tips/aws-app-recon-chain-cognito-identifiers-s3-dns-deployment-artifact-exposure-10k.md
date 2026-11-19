# AWS App Recon Chain → Cognito Identifiers, S3 / DNS / Deployment Artifact Exposure ($10K Case)

**Rating:** ⭐ جيدة  
**Category:** Recon, General  
**Status:** Not started  

## How It Works

A 2025 Medium writeup reports a $10,000 bounty for an AWS configuration issue found while reviewing app client code and auth/file-management traffic. A Cognito pool identifier led to correlation of publicly readable cloud resources and deployment artifacts, exposing S3, DNS ranges and infrastructure metadata. The writeup says the researcher used passive discovery and read-only checks; payout is self-reported. The value is the correlation chain, not treating a public identifier as a secret.

## Payload / Code

```
On in-scope assets only: inspect public JS/config and observed auth/file flows for AWS region, Cognito User Pool or Identity Pool identifiers, bucket names, API base URLs and deployment references. Follow only resources linked from the authorized target and verify access with minimal read-only requests. Do not enumerate unrelated buckets, download sensitive artifacts, authenticate with discovered credentials, or modify cloud resources. Report the exact exposed resource and data category with redacted evidence.
```

## Source

https://medium.com/%40ethan_hunt/how-i-won-10k-by-finding-an-aws-misconfiguration-in-an-app-and-what-you-can-learn-990ee90b4f05 ; https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-identity-pools.html ; https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-control-block-public-access.html

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
