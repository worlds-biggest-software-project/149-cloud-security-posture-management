# Cloud Security Posture Management — Feature & Functionality Survey

> Candidate #149 · Researched: 2026-05-03

## Solutions Analysed

| Tool | Type | Licence / Model | URL |
|------|------|-----------------|-----|
| Wiz | Commercial SaaS CNAPP | Usage-based subscription | https://www.wiz.io/ |
| Prisma Cloud (Palo Alto Networks) | Commercial SaaS CNAPP | Credit-based consumption model | https://www.paloaltonetworks.com/prisma/cloud |
| Microsoft Defender for Cloud | Commercial SaaS / Free tier | Free foundational; Defender plans ~$15/server/month | https://learn.microsoft.com/en-us/azure/defender-for-cloud/ |
| Orca Security | Commercial SaaS CNAPP | Subscription (undisclosed) | https://orca.security/ |
| Lacework FortiCNAPP (Fortinet) | Commercial SaaS CNAPP | Subscription (undisclosed) | https://www.fortinet.com/products/forticnapp |
| Tenable Cloud Security (formerly Tenable.cs) | Commercial SaaS CSPM | Per-resource subscription | https://www.tenable.com/products/tenable-cloud-security |
| Prowler | Open source with SaaS option | Free (Apache 2.0 licence); Prowler Pro SaaS from $299/month | https://prowler.com/ |
| Aikido Security | Commercial SaaS, developer-first | Free Developer plan; Basic plan from ~$300/month | https://www.aikido.dev/ |

## Feature Analysis by Solution

### Wiz

**Core features**
- Agentless CSPM with scanning across AWS, Azure, GCP, OCI, Alibaba Cloud, VMware vSphere, and Kubernetes via cloud provider APIs
- Security Graph maps resources, identities, vulnerabilities, and network exposure into attack paths to prioritize toxic risk combinations
- Wiz Code: CI/CD scanning with 1-click fix PRs for infrastructure-as-code vulnerabilities
- Wiz Cloud: Runtime agentless protection with CSPM, CWPP, CIEM, and DSPM capabilities
- Wiz Defend: eBPF-based runtime protection for workloads
- Data Security & AI Protection: Scans actual content of buckets and databases to detect PII, PCI, and PHI using regex and ML-based pattern matching
- Shadow AI detection: Discovers unmanaged AI models, training datasets, and AI API endpoints

**Differentiating features**
- Security Graph technology that contextualizes findings into attack paths rather than flat vulnerability lists
- AI-SPM for discovering Shadow AI and unmanaged ML infrastructure
- Agentic security platform (SecOps and Remediation agents in 2025 public preview)
- Unified detection from code through cloud to runtime within single platform

**UX patterns**
- Rapid agentless deployment model requiring only cloud API permissions
- AI-augmented risk prioritization driven by attack path context
- 1-click PR generation for IaC remediation

**Integration points**
- Cloud provider APIs (AWS, Azure, GCP, OCI, Alibaba, vSphere)
- CI/CD pipeline integration for shift-left scanning
- Custom webhooks and likely third-party tooling connections

**Known gaps**
- Limited on-premises support despite agentless architecture
- High price point ($300K+/year enterprise) limits SME adoption

**Licence / IP notes**
- Proprietary commercial licence; no known patent encumbrances identified in public domain

---

### Prisma Cloud (Palo Alto Networks)

**Core features**
- Unified CNAPP bundling CSPM, CWPP, CIEM, DSPM, code security, cloud network security, and web application/API security
- CSPM module detects misconfigurations (publicly accessible storage, overly permissive security groups, unencrypted databases, disabled audit logging)
- Compliance engine maps findings to regulatory frameworks and generates auditor reports
- Code security module built on Checkov (open-source IaC scanner; Palo Alto acquired Bridgecrew in 2021)
- CWPP covers full workload lifecycle from CI vulnerability scanning to production runtime defense
- Container security: image scanning, runtime monitoring, and Kubernetes compliance checks
- Over 100 auto-remediation policies with customization capability
- Multi-cloud support: AWS, Azure, GCP, OCI, Alibaba Cloud, IBM Cloud

**Differentiating features**
- Broadest integrated CNAPP feature set across code, cloud, and runtime in single platform
- Checkov-based IaC scanning with 2 million+ downloads and extensive policy library
- Auto-remediation across 100+ policies with custom rule support
- Merger with Cortex CDR in Q3 FY25 (late 2025) introduces AI-powered capabilities

**UX patterns**
- Unified console for code-to-cloud security visibility
- Progressive policy complexity from built-in library to custom policies
- Single login/authentication across entire CNAPP platform

**Integration points**
- Checkov open-source ecosystem (2 million+ downloads)
- Multi-cloud provider APIs
- CI/CD pipeline tooling
- SIEM and ticketing system integrations

**Known gaps**
- Complex pricing model and steep learning curve reported in user reviews
- Overwhelming feature breadth can challenge SME onboarding

**Licence / IP notes**
- Proprietary commercial licence; Checkov component is Apache 2.0 licence (open source)
- No known patent encumbrances identified

---

### Microsoft Defender for Cloud

**Core features**
- Free Foundational CSPM enabled by default for all Azure subscriptions
- Paid Defender CSPM plan adds advanced features: AI security posture, attack path analysis, risk prioritization
- Agentless discovery for Kubernetes clusters (API-based detection of architecture and workloads)
- Agentless container vulnerability assessments for images in registries
- Sensitive data discovery using smart sampling to identify managed data resources containing PII/PHI
- Cloud infrastructure entitlement management (CIEM) for identity governance
- Multi-cloud support: Azure (native), AWS (cross-cloud), GCP (preview Cloud Logging ingestion available 2025-2026)
- Attack Path analysis showing OAuth app compromises and lateral movement across environments

**Differentiating features**
- Strong native Azure integration and free foundational tier lower initial cost barrier
- Attack Path visualization for OAuth-based lateral movement (2025-2026 capability)
- Sensitive data discovery with automatic smart sampling (no 100% scan overhead)
- CIEM visibility into permission usage across cloud environments

**UX patterns**
- Free-to-paid conversion model (foundational → Defender plans)
- Risk prioritization via Attack Path context
- Government cloud customer support (2025-2026 GA)

**Integration points**
- Azure Security Center and Sentinel integration (native)
- AWS and GCP APIs for cross-cloud visibility
- Microsoft Entra (formerly Azure AD) for identity context
- Log Analytics workspace for data aggregation

**Known gaps**
- AWS/GCP coverage noticeably weaker than pure-play multi-cloud tools
- CIEM features lag behind dedicated CIEM platforms
- Foundational tier provides limited actionability

**Licence / IP notes**
- Proprietary commercial Microsoft licence
- No known patent encumbrances identified

---

### Orca Security

**Core features**
- Agentless-first platform using patented SideScanning™ technology
- SideScanning reconstructs workload file systems in read-only virtual view without agent deployment
- Covers all major workload types: Linux/Windows VMs, containers/container images, serverless functions
- CSPM with misconfigurations detection
- CWPP with runtime behaviour analysis
- CIEM for identity entitlements and access rights
- DSPM for data security posture
- Container security and API security
- AWS Security Hub integration with OCSF support (June 2025 enhancement)
- Full risk profile delivery in under 24 hours

**Differentiating features**
- Zero-touch SideScanning™ technology requires no agents, rules, or policies
- Covers all cloud asset types including infrastructure resources (storage buckets, VPCs, KMS keys)
- Automatic onboarding of new assets without reconfiguration
- Generative AI for simplified security investigations and remediation workflows

**UX patterns**
- Minutes-to-deployment model (no agent installation orchestration)
- AI-assisted investigation and remediation guidance
- No network packets or code execution in target environment

**Integration points**
- AWS Security Hub with OCSF support (2025)
- Multi-cloud provider APIs
- Cloud infrastructure resources (S3, VPCs, KMS, etc.)
- Likely CI/CD and ticketing system integrations

**Known gaps**
- Smaller ecosystem and partner network compared to Wiz
- Limited public information on specific remediation automation capabilities

**Licence / IP notes**
- Proprietary commercial licence; SideScanning™ is patented technology
- Patent status should be clarified before adopting similar scanning approaches

---

### Lacework FortiCNAPP (Fortinet)

**Core features**
- Polygraph Data Platform mapping cloud behaviours for baseline-and-anomaly detection
- Zero-touch workload protection (no rules, no policies, no logs required for breach detection)
- Behaviour-based threat detection via Polygraph deviation analysis from normal activity
- CSPM, CWPP, CIEM, CDR (Cyber Deception & Response), code security, DSPM, and Kubernetes security
- Multi-cloud support: AWS, Azure, GCP, OCI, Kubernetes
- Polygraph applies to users, workloads, and applications

**Differentiating features**
- Polygraph zero-touch anomaly detection without manual rule engineering
- 2025 SC Award for Best Cloud Workload Protection Solution
- Named Leader in Overall, Market, and Innovation in KuppingerCole 2025 CNAPP Leadership Compass
- Behaviour-based approach captures novel threats not covered by static policies
- Fortinet integration enables security fabric extensibility (post-acquisition 2024)

**UX patterns**
- Unsupervised learning baseline of normal behaviour
- Anomaly alerts without false-positive rule tuning overhead
- Behaviour correlation across users, workloads, and applications

**Integration points**
- Fortinet security fabric products (post-acquisition)
- Multi-cloud provider APIs
- Kubernetes API and container runtime integration

**Known gaps**
- Fortinet acquisition (August 2024) created roadmap uncertainty initially, though recent awards and categorizations suggest stability
- Limited public data on specific IaC scanning and compliance mapping breadth

**Licence / IP notes**
- Proprietary commercial Fortinet licence
- Polygraph technology may be patent-pending; recommend legal review if adopting similar statistical behaviour models

---

### Tenable Cloud Security (formerly Tenable.cs)

**Core features**
- Agentless CSPM with IaC scanning for drift detection
- Terraform, CloudFormation, and Kubernetes IaC scanning for misconfigurations and policy violations
- "Drift as Code" capability identifying new resources and configuration changes
- Policy as Code for detecting and remediating policy violations
- Remediation as Code reverts vulnerable changes to propagate safe changes to IaC
- Multi-cloud support (AWS, Azure, GCP implied from Accurics heritage)
- Compliance framework mapping

**Differentiating features**
- Exceptional IaC/drift detection coverage (Accurics heritage)
- Drift detection compares running cloud infrastructure against IaC templates that created it
- Policy as Code and Remediation as Code integrate infrastructure definition and runtime state

**UX patterns**
- Drift detection alerts on configuration divergence from IaC source of truth
- Policy-driven remediation feedback to IaC templates
- Integration with enterprise CI/CD and ticketing systems

**Integration points**
- Terraform and CloudFormation repositories
- Kubernetes manifests
- Enterprise CI/CD systems
- Ticketing and change management platforms

**Known gaps**
- Narrower workload protection compared to comprehensive CNAPP platforms (Wiz, Prisma Cloud)
- Limited public information on runtime or network security capabilities
- Smaller market presence than leaders

**Licence / IP notes**
- Proprietary Tenable commercial licence
- Accurics acquisition (October 2021) intellectual property now Tenable-owned
- No known patent encumbrances identified

---

### Prowler

**Core features**
- Open-source cloud security assessment for AWS, Azure, GCP, and Kubernetes
- 400+ security checks mapped to CIS Benchmarks, NIST 800, NIST CSF, CISA, FedRAMP, PCI-DSS, GDPR, HIPAA, and other frameworks
- Multi-framework compliance: Industry standards, regulatory (RBI, FedRAMP, PCI-DSS, NIS2), privacy (GDPR, HIPAA, FFIEC), cloud-specific (AWS FTR, Well-Architected, BSI C5)
- Continuous monitoring to maintain compliance with industry standards and custom frameworks
- Prowler Autonomous Fixer provides guided remediation steps
- Attack Paths feature extends AWS scans with Neo4j graph combining cloud inventory with findings
- Prowler App/Cloud: web-based interface for running scans and visualizing results
- Written in Python using AWS SDK (Boto3), Azure SDK, and GCP API Python Client
- Prowler Pro SaaS option from $299/month

**Differentiating features**
- Zero licence cost (Apache 2.0 open source)
- Community-driven development with active maintenance
- Autonomous Fixer guidance for remediation without scripting
- Attack Paths with Neo4j graph integration (AWS-specific)
- Extensive multi-framework compliance mapping (40+ frameworks)

**UX patterns**
- CLI-first approach suitable for engineering-centric teams
- Scan results visualization via web app (Prowler Cloud)
- Framework-based findings navigation and filtering
- Community contribution model

**Integration points**
- Cloud provider SDKs and APIs
- CI/CD pipeline integration via Python package
- Neo4j graph database for Attack Paths
- Cartography integration for cloud inventory

**Known gaps**
- No runtime protection or vulnerability scanning (CSPM-only focus)
- Requires engineering expertise for deployment and interpretation
- Autonomous Fixer provides guidance but not automated remediation
- Limited CIEM, DSPM, or advanced detection capabilities

**Licence / IP notes**
- Apache 2.0 open-source licence (free to use, modify, and distribute)
- No licence compatibility issues with most cloud projects
- Prowler Pro SaaS tier is proprietary but leverages open-source core

---

### Aikido Security

**Core features**
- Developer-first unified security platform covering code to runtime
- SAST (Static Application Security Testing), DAST (Dynamic Application Security Testing)
- IaC scanning (infrastructure-as-code)
- Container scanning
- Secrets detection
- Open source licence scanning (SCA)
- CSPM (Cloud Posture Management)
- Runtime protection
- AI-powered triage and auto-fix recommendations
- Automatic SBOM generation
- Exploitability filtering: vulnerabilities prioritized by actual risk and usage in code
- Free Developer plan (2 users, 10 repos, 1 domain, 1 cloud, 250k monthly requests)
- Basic plan from $300/month (10 users, 100 repos, 3 clouds, full SAST/DAST)
- Pro plan from $600/month (adds API scanning, malware detection, IDE plugins)

**Differentiating features**
- Developer-centric with "minutes" onboarding for small teams
- Exploitability filtering reduces alert fatigue
- AI-driven false-positive reduction
- Integrated SAST/DAST/IaC/CSPM stack for startups/SMEs
- Free tier removes entry barrier for small teams

**UX patterns**
- Developer-friendly remediation guidance
- Integrated IDE plugins (Pro tier)
- AI triage reduces manual false-positive filtering
- Lightweight onboarding suitable for 2–50 person teams

**Integration points**
- Git repositories (GitHub, GitLab, etc.)
- CI/CD pipelines
- IDE plugins (VS Code, etc. in Pro tier)
- Slack notifications (implied from developer-first approach)

**Known gaps**
- Limited enterprise governance and compliance framework breadth
- Smaller team and community compared to established vendors
- Pro plan required for advanced capabilities (API scanning, malware)

**Licence / IP notes**
- Proprietary Aikido commercial licence (SaaS)
- No known patent encumbrances identified

---

## Cross-Cutting Feature Themes

### Table-Stakes Features

Any CSPM project in this category must provide:

- **Multi-cloud CSPM scanning** across at least AWS, Azure, and GCP
- **Misconfiguration detection** for common cloud resource types (storage, compute, networking, identity)
- **Compliance framework mapping** to at least CIS Benchmarks and NIST SP 800-53
- **Continuous monitoring** of cloud infrastructure posture changes in near-real-time
- **Risk prioritization** (not flat vulnerability lists) — at minimum by severity, ideally by exploitability or context
- **Visual dashboards** showing security posture summary, top risks, and compliance progress
- **Remediation guidance** per finding, ideally with prescriptive steps or code examples
- **Role-based access control** for multi-team security organisations
- **Audit logging and compliance reporting** for SOC 2, PCI-DSS, HIPAA, GDPR evidence

### Differentiating Features

Capabilities that separate leading solutions from commoditised competitors:

- **Attack path analysis** — contextualizing findings into end-to-end attack chains rather than isolated misconfigurations (Wiz, Microsoft, Lacework, Prowler)
- **Agentless workload scanning** — deep visibility into VM/container posture without agent deployment (Wiz, Orca, Prisma Cloud)
- **Zero-touch anomaly detection** — unsupervised learning of normal cloud behaviour to flag deviations without hand-crafted rules (Lacework Polygraph)
- **IaC drift detection** — comparing running cloud state against infrastructure-as-code source of truth (Tenable, Prisma Cloud)
- **Data security posture** — automatic classification and discovery of PII/PHI in cloud data stores (Wiz, Prisma Cloud, Orca)
- **AI-powered remediation** — generating environment-specific Terraform/CloudFormation patches, not just guidance (Wiz, Orca with AI, Aikido)
- **Identity entitlements management** — visualising permission overgrant and lateral movement paths (Orca, Tenable Ermetic heritage, Wiz)
- **Container and Kubernetes security** — registry scanning, runtime monitoring, policy enforcement (Prisma Cloud, Wiz, Aikido)
- **Shift-left integration** — CI/CD scanning of IaC and code before deployment (Wiz, Prisma Cloud, Aikido)
- **Open-source ecosystem** — free baseline scanning with optional SaaS layer (Prowler, leverages Checkov)
- **Developer-centric UX** — fast onboarding, low friction, minimal configuration for teams <100 people (Aikido)

### Underserved Areas / Opportunities

Gaps in the market where a new entrant or existing player could add differentiated value:

- **SME affordability** — Enterprise CSPM tools command $300K–1M+/year. Gaps below $50–100K/year for teams 20–500 people. (Aikido and Prowler Pro address this partially.)
- **Fully automated remediation** — Most tools provide guidance; few offer one-click or automatic fixes without manual approval workflows. (Wiz and Tenable offer partial automation; most require manual review.)
- **Custom compliance framework definition** — Existing tools map to CIS/NIST/PCI/GDPR but lack frictionless ways to build org-specific policies tied to business context.
- **Multi-vendor identity correlation** — Most CIEM modules handle single-cloud identity; cross-cloud (AWS IAM + Azure AD + GCP workload identity) correlation is rare and manual.
- **Real-time incident playbook integration** — No tool yet tightly integrates posture findings with incident response playbooks to execute remediations tied to specific attack scenarios.
- **Supply-chain risk posture** — No integrated CSPM + software bill-of-materials (SBOM) + container provenance tracking in a single platform yet.
- **Kubernetes-native CSPM** — Most tools treat K8s as an afterthought; no pure Kubernetes-native CSPM exists yet with deep workload/namespace/policy awareness.
- **Natural-language compliance query** — No tool yet allows "show me all S3 buckets holding PII that are public" without SQL-like query language or framework mapping.

### AI-Augmentation Candidates

Manual and rule-based features where AI could provide meaningfully better results than existing approaches:

- **Intelligent attack path prioritization** — AI models correlating misconfiguration chains, entitlement overgrants, network exposure, and data classification to score "toxic" combinations. (Wiz Security Graph + AI agents partially address this.)
- **Predictive drift detection** — ML models learning an organisation's change velocity and infrastructure patterns to flag IaC commits statistically likely to introduce misconfigurations before merge. (None currently, opportunity for pre-commit enforcement.)
- **Automated compliance narrative generation** — LLMs auto-generating SOC 2 Control 7.1 or PCI-DSS 3.2.4 compliance evidence in auditor-ready format (email logs, access reviews, change records) reducing evidence collection from 200+ hours to <20. (Wiz and Orca hint at this with "AI-powered" investigations.)
- **Natural-language policy authoring** — Letting security analysts write policies in English ("block publicly accessible databases unless approved") and having AI translate to cloud-native IaC and runtime rules. (None exist yet.)
- **Context-aware vulnerability prioritization** — AI filtering CSPM + vulnerability scan + exploit intelligence + threat intelligence to surface only findings that could actually be exploited in the specific cloud architecture. (Aikido's exploitability filtering is closest.)
- **Shadow IT and rogue workload detection** — ML models detecting anomalous resource creation patterns, unusual data flows, or unmanaged IAM roles not in IaC. (Wiz AI-SPM for Shadow AI is a prototype.)
- **Cross-cloud entitlement correlation** — Graph-based AI models mapping identity chains across AWS IAM + Azure AD + GCP workload identity + on-premises AD to detect lateral movement opportunities. (No integrated solution exists yet.)

## Legal & IP Summary

All commercial solutions reviewed are proprietary closed-source SaaS offerings with no identified copyright, licensing, or patent conflicts. Prowler is Apache 2.0 open source, compatible with most cloud projects. Prisma Cloud's code security module is built on Checkov (Apache 2.0 open source, acquired by Palo Alto Networks); no license compatibility issues identified.

**Patent considerations:** Orca's SideScanning™ and Lacework's Polygraph technology are proprietary/patent-pending. Organizations adopting similar approaches (scanning workload filesystems without agents, or unsupervised behaviour baseline models) should conduct independent legal review to avoid infringement risk.

No material was omitted due to copyright or licensing uncertainty; all information sourced from public product pages, documentation, or credible third-party reviews.

## Recommended Feature Scope

Based on the cross-cutting analysis above, here is a prioritised feature scope for a new CSPM entrant:

**Must-have (MVP)**
- Multi-cloud CSPM scanning (AWS, Azure, GCP minimum; agentless API-based preferred to reduce deployment friction)
- Misconfiguration detection across 5–10 common resource types per cloud (storage, compute, networking, identity, databases)
- CIS Benchmarks and NIST SP 800-53 compliance mapping
- Risk prioritization (at minimum: exploitability, context from network/identity exposure)
- Continuous monitoring with near-real-time alerts
- Remediation guidance (prescriptive steps + code examples) per finding
- RBAC and compliance reporting for SOC 2 / PCI-DSS / HIPAA
- Dashboard showing posture summary, top findings, compliance progress

**Should-have (v1.1)**
- IaC scanning + drift detection (Terraform, CloudFormation) to shift-left misconfiguration prevention
- Agentless workload scanning (VM/container filesystem inspection or runtime behaviour baseline)
- Attack path analysis to contextualize finding chains
- Data security posture (PII/PHI discovery in cloud data stores using regex + ML classification)
- AI-assisted remediation generation (environment-specific Terraform/CloudFormation patches)
- One-click or automated remediation approval workflows
- Native Kubernetes security (API-based cluster discovery, workload scanning, policy enforcement)
- Developer-friendly CI/CD pipeline integration

**Nice-to-have (backlog)**
- Cloud infrastructure entitlements management (CIEM) for IAM overgrant detection
- Container registry scanning + runtime protection
- Kubernetes network policy recommendations
- Custom compliance framework definition UI
- Natural-language compliance querying (e.g., "S3 buckets holding PII that are public")
- Incident response playbook integration (auto-trigger remediations for specific attack scenarios)
- Shadow AI/IT detection via anomalous resource creation patterns
- Multi-vendor identity correlation (cross-cloud lateral movement analysis)
- Predictive IaC drift detection (flag commits statistically likely to introduce misconfigurations)
