# Azure DevOps Public Project Review → Pipeline Metadata & Accidental Secret Exposure

**Rating:** ⭐ جيدة  
**Category:** Recon, API Hacking  
**Status:** Not started  

## How It Works

Public Azure DevOps projects and repository/build surfaces may expose pipeline YAML, build logs, test outputs, artifacts, deployment configuration, or identifiers that reveal how a target deploys. The highest-signal angle is accidental disclosure inside an artifact or log (for example, a credential accidentally printed in a failed build), not simply finding a public project. This is distinct from GitHub Actions workflow injection already covered in Notion. Public-project visibility can be intentional, and program policies differ sharply.

## Payload / Code

```
Passive-first, in-scope workflow: identify the organization's official Azure DevOps tenant from public references; inspect only publicly accessible project/repository/build pages and artifacts; review pipeline YAML, recent failed-build logs, test reports, coverage output, and downloadable build artifacts for secrets or private deployment data. Do not guess or access private project IDs, use stolen credentials, trigger builds, or test credentials against live services. If a suspected secret appears, capture a redacted proof and report it; do not use it.
```

## Source

https://www.microsoft.com/en-us/msrc/bounty-azure-devops ; https://microsoft.github.io/zerotrustassessment/docs/workshop-guidance/devsecops/DS_076 ; https://bugbounty.info/Attack-Surface/CI-CD/Secret-Leakage

---

_Synced from Notion: Bug Bounty Tips and Tricks. Authorized testing only._
