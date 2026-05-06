# Cloud Security Posture Management

> Part of the [worlds-biggest-software-project](https://github.com/worlds-biggest-software-project) initiative.
>
> An AI-native, open-source platform for continuous misconfiguration detection, compliance benchmarking, and drift alerting across multi-cloud environments.

Cloud Security Posture Management (CSPM) continuously inspects cloud accounts to find misconfigurations, map findings to compliance frameworks, and alert on infrastructure drift. This project targets cloud security architects, DevSecOps engineers, and GRC teams who need enterprise-grade posture visibility without the USD 300K-1M+ annual price tag of incumbent CNAPP suites.

---

## Why Cloud Security Posture Management?

- Misconfigurations account for 65-70% of cloud security incidents, yet enterprise CSPM tools such as Wiz and Prisma Cloud are typically priced at USD 300K-1M+ per year, leaving teams of 20-500 people underserved.
- Incumbents deliver findings as flat lists or require complex pricing models (Prisma Cloud) and steep learning curves; security teams handle an average of 71 incidents per week with over 25% of time spent on manual triage.
- Microsoft Defender for Cloud's free tier is Azure-centric and weaker on AWS/GCP; pure-play tools like Wiz are cloud-only with limited on-premises support.
- Open-source options such as Prowler offer no licence cost but lack runtime protection, automated remediation, and tight CIEM/DSPM integration, requiring significant engineering investment.
- Compliance evidence collection for SOC 2 and PCI currently consumes 200-400 hours per cycle; an AI-native approach can compress this to 20-40 hours.

---

## Key Features

### Multi-Cloud Posture Scanning

- Agentless API-based scanning across AWS, Azure, and GCP at minimum
- Misconfiguration detection across storage, compute, networking, identity, and database resource types
- Continuous monitoring with near-real-time alerts on posture changes
- Automatic onboarding of new cloud assets without reconfiguration

### Compliance and Reporting

- Mapping to CIS Benchmarks and NIST SP 800-53 as baseline frameworks
- Coverage for SOC 2, PCI-DSS v4.0, HIPAA, GDPR, and ISO/IEC 27001:2022 evidence
- Role-based access control for multi-team security organisations
- Dashboards summarising posture, top findings, and compliance progress

### Risk Prioritization and Attack Paths

- Risk scoring by exploitability and contextual exposure rather than flat severity lists
- Attack path analysis correlating misconfigurations, identity entitlements, network exposure, and data classification
- Prescriptive remediation guidance with code examples per finding

### Shift-Left and IaC Integration

- Terraform and CloudFormation IaC scanning for misconfigurations and policy violations
- Drift detection comparing running cloud state to IaC source of truth
- CI/CD pipeline integration for pre-merge enforcement
- Native Kubernetes security with API-based cluster discovery and workload scanning

### Data and Identity Posture

- PII and PHI discovery in cloud data stores using regex and ML classification
- Cloud Infrastructure Entitlements Management (CIEM) for IAM overgrant detection
- Container registry scanning and runtime protection capabilities

---

## AI-Native Advantage

AI enables continuous correlation of misconfiguration findings, IAM entitlements, network exposure, and data classification into an attack-path risk graph that surfaces the most dangerous combinations rather than isolated alerts. LLM-based remediation generation produces environment-specific Terraform or CloudFormation patches for one-click or automated fixes, while natural-language compliance querying lets GRC analysts ask questions such as "which S3 buckets holding PII are publicly accessible?" without learning provider query languages. Predictive drift models can flag IaC commits statistically likely to introduce misconfigurations before merge, and AI-powered compliance narration auto-generates SOC 2 or PCI evidence packages in auditor-ready format.

---

## Tech Stack & Deployment

The project targets agentless, API-based deployment across AWS, Azure, and GCP, with optional eBPF or filesystem-inspection workload coverage. Compliance mapping aligns with CIS Benchmarks, NIST SP 800-53 Rev 5, PCI DSS v4.0, ISO/IEC 27001:2022, HIPAA, and GDPR. Integration touchpoints include cloud provider SDKs, CI/CD pipelines (Terraform and CloudFormation repositories), Kubernetes APIs, and SIEM and ticketing systems. Self-hosted and SaaS deployment modes are both in scope.

---

## Market Context

The CSPM market is estimated at USD 6-7 billion in 2026, projected to reach USD 10-16 billion by 2030-2034 at a CAGR of approximately 10-15%, with Gartner projecting adoption to surpass 20% of eligible organisations in 2026. Enterprise tools (Wiz, Prisma Cloud) typically cost USD 300K-1M+ per year, while Microsoft Defender for Cloud starts at roughly USD 15/server/month and Prowler Pro from USD 299/month. Primary buyers are cloud security architects at multi-cloud enterprises, DevSecOps engineers, GRC teams automating SOC 2 and PCI evidence, and CISOs seeking board-level cloud risk dashboards.

---

## Project Status

> This project is in the **research and specification phase**.  
> Contributions, feedback, and domain expertise are welcome.

---

## Contributing

We welcome contributions from developers, domain experts, and potential users.
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Important:** All contributions must be your own original work or clearly attributed
open-source material with a compatible licence. Copyright infringement and licence
violations will not be tolerated and will result in immediate removal of the offending
contribution. If you are unsure whether a piece of code, text, or other material is
safe to contribute, open an issue and ask before submitting.

---

## Licence

Licence to be determined. See [discussion](#) for context.
