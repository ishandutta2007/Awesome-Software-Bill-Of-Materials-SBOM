# Awesome-Software-Bill-Of-Materials-SBOM

# Awesome-Software-Bill-Of-Materials-SBOM

## Top Software Bill of Materials (SBOM) Tools Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Software Composition Analysis, CycloneDX/SPDX Generation & Vulnerability Intelligence*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Software Bill of Materials (SBOM)**. These tools generate, manage, and analyze SBOMs — machine-readable inventories of software components, dependencies, and licenses — enabling organizations to understand their supply chain, respond to vulnerabilities, and meet regulatory requirements like EO 14028 and the EU Cyber Resilience Act.

**Examples** include Black Duck, Sonatype Lifecycle, Mend.io, Snyk Open Source, FOSSA, Revenera FlexNet, Anchore Enterprise, Cybellum, Finite State, and Legit Security (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, spec-compliant SBOM generation, and transparent dependency analysis — ideal for security teams prioritizing data sovereignty, developers building supply chain pipelines, and organizations that need verifiable evidence without relying solely on commercial SaaS platforms.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Black Duck (Synopsys)](https://www.blackduck.com/)**  
  **The reference enterprise SCA and SBOM platform**, named a Leader in the **2026 Gartner Magic Quadrant for Software Supply Chain Security**. **Import third-party SBOMs and generate SPDX and CycloneDX SBOMs** containing open source, proprietary, and commercial dependencies with customizable fields for industry, regulatory, or customer requirements. **Multiple scan technologies** combine package dependencies, CodePrint, snippet, binary, and container analysis to identify components in any programming language. **Malware detection** via ReversingLabs technology detects suspicious files and malicious packages post-build. **AI/ML model detection** uncovers integrated AI models, their origin, license obligations, and whether they've been significantly retrained. **Regulatory alignment** covers EO 14028, NTIA, FDA, SSDF, and EU CRA. **Gartner Peer Insights reviewers** praise comprehensive SBOM generation and enterprise integration.

- **[Sonatype Lifecycle & SBOM Manager](https://www.sonatype.com/)**  
  **The system of record for software artifacts** built on 15+ years of curated OSS intelligence from Maven Central and OSS Index. **SAGE (Sonatype Air-Gapped Environment)** packages Lifecycle, Nexus Repository, SBOM Manager, and Nexus Firewall with SAGE Data Services for **fully disconnected federal environments** — no external network calls, continuous compliance with NIST SSDF, EO 14028, and CISA BOD 22-01. **SBOM Manager** generates SBOMs directly from binaries and container images, critical when source code is unavailable, and continuously monitors them against new CVEs, KEV items, and license changes. **Central Mirror** provides a point-in-time snapshot of Maven Central for high-throughput builds entirely within the enclave. **Policy-as-code governance** enforces KEV-aware prioritization, license compliance, and security risk thresholds directly in CI/CD pipelines. **The air-gapped choice for defense, intelligence, and federal civilian programs**.

- **[Mend.io](https://www.mend.io/)**  
  **Unified governance for the software you write and the AI you build.** **Mend AI** provides **AI Bill of Materials (AIBoM)** — goes beyond traditional SBOM by scanning **human-written and AI-generated code, open source libraries, and proprietary components** into a comprehensive machine-readable inventory in SPDX and CycloneDX formats. **AI component detection** covers models, frameworks, agents, RAGs, MCPs, and shadow AI. **System prompt hardening** detects and assesses system prompts against best practices. **AI red teaming** uses prebuilt and custom tests across prompt injection, hallucination, and social engineering. **Reachability analysis** with VEX data identifies whether application code can reach vulnerable components. **Automated dependency updates** keep SBOMs continuously current as components change. **VEX incorporation** adds exploitability context to each component automatically. **Regulatory alignment** covers EO 14028, EU CRA, and CISA submission. **The AI-native choice** for organizations building with or on AI models.

- **[Snyk Open Source](https://snyk.io/product/open-source-security/)**  
  **Developer-first SCA with CLI and API-driven SBOM generation.** The **`snyk sbom` command** generates CycloneDX v1.4-1.6 (JSON/XML) and SPDX v2.3 (JSON) documents from package manager manifests. **`--unmanaged`** generates SBOMs for projects without manifest files. **`--all-projects`** auto-detects all projects in monorepos and produces a single SBOM. **`--dev`** includes development-only dependencies. **`--prune-repeated-subdependencies`** removes duplicate sub-dependencies. **`--allow-incomplete-sbom`** continues generation when some projects fail to resolve. **Snyk REST API** endpoint retrieves SBOM documents for continuously monitored projects with Snyk-specific metadata including org, project, and target IDs. **Best for developer-first workflows** wanting SBOM generation as part of the normal CLI and CI experience.

- **[FOSSA](https://fossa.com/)**  
  **Recognized as a significant SCA solution in The Forrester Wave™**, achieving **highest scores in license risk management and SBOM criteria**. **Automated NOTICE file recreation** and **FDA compliance support**. **SBOM policy feature** enforces SBOM standards for compliance and security. **C/C++ scanning and SBOM generation** support enhances software supply chain security for systems programming. **Best for license-compliance-heavy organizations** where NOTICE files and obligations management matter.

- **[Revenera FlexNet Code Insight](https://www.revenera.com/)**  
  **Single integrated solution for open source license compliance and security.** **14 million+ components** with support for **25+ languages and 70+ extensions**. **Vulnerability data from multiple sources** including NVD and Secunia Research. **Discovers all open source in source code, binaries, containers, build dependencies, subcomponents, modified and partial open source components**. **Patented scan and analysis flexibility** for varying business needs. **Policy enforcement and approval automation** with usage and remediation guidance. **Proactive and continuous monitoring** of newly discovered vulnerabilities in current and shipped products. **REST API framework** for custom integrations with build tools, CI/CD, SCM, and artifact repositories. **Best for organizations needing deep license obligation management** alongside security.

- **[Anchore Enterprise](https://anchore.com/)**  
  **Market leader in SCA for cloud-native platforms** with **Anchore SBOM** providing centralized SBOM management including **"Bring Your Own SBOMs"**. **Imports SBOMs in SPDX (2.1-2.3), CycloneDX (1.0-1.6), and Syft native formats**. **Validates uploaded SBOM quality** against schema standards. **Anchore Score** prioritizes vulnerabilities based on CVSS, EPSS, and CISA KEV data. **Flagship customers include NVIDIA, Cisco, US Navy, and Department of Defense**. **Best for container and cloud-native security** with existing Anchore deployments.

- **[Legit Security](https://www.legitsecurity.com/)**  
  **Continuous compliance and SBOM with alignment to regulatory frameworks.** **Maps security guardrails to specific regulations** including ISO 27001, SSDF, FedRAMP, SLSA, NIST, SOC 2, PCI DSS, and CISA Attestation. **Real-time compliance violation monitoring** with automated reporting. **Creates SBOMs and signed software attestations** in all regulated formats. **Best for organizations needing continuous compliance evidence** rather than point-in-time SBOM exports.

- **[Cybellum](https://cybellum.com/)**  
  **Product security platform with Cyber Digital Twins™** for connected device manufacturers. **Product SBOM management** orchestrates the entire SBOM process from merging to validation to collaboration. **Automotive, medical, and industrial sector focus** with pre-built mapping to **50+ standards**. **FDA compliance support** for medical device SBOM validation. **Best for embedded, IoT, and connected device manufacturers**.

- **[Finite State](https://finitestate.io/)**  
  **AI-first product security platform purpose-built for connected device manufacturers.** **Scans source code, binaries, third-party components, and firmware** from one platform. **130+ binary formats, 30+ architectures, 18+ programming languages**. **Consolidates third-party and legacy supplier SBOMs** into a single source of truth. **Reachability analysis** pinpoints truly exploitable vulnerabilities. **Prioritization based on EPSS, KEV, network exposure, exploit maturity, and license risk** with auto-resolution of unreachable findings. **Best for IoT and embedded systems** with complex binary and firmware analysis needs.

## Open-Source GitHub Projects

- **[Syft (Anchore)](https://github.com/anchore/syft)**  
  **One of the most widely deployed open-source SBOM generators** — Apache 2.0 licensed, 5,000+ GitHub stars. **Scans container images, filesystems, and archives** with broad ecosystem coverage across dozens of language ecosystems and OS package managers (apt, apk, rpm). **Generates both SPDX and CycloneDX output** out of the box — CycloneDX 1.2-1.7 (JSON/XML) and SPDX 2.2-3.0 (JSON) and SPDX tag-value 2.1-2.3. **Integrates cleanly with Grype** (Anchore's vulnerability scanner) and standard CI pipelines via a well-maintained GitHub Action. **`syft <image> -o <format>`** specifies output format and version. **Best for teams wanting a dedicated SBOM generator** with strong multi-ecosystem coverage and Anchore's backing.

- **[Trivy (Aqua Security)](https://github.com/aquasecurity/trivy)**  
  **Vulnerability scanner that grew into a capable SBOM generator** — supports both CycloneDX and SPDX for container images, filesystems, and Kubernetes clusters. **Because vulnerability scanning and SBOM generation share the same package-detection engine**, Trivy is practical for teams wanting one tool doing both jobs rather than stitching two together. **Fast, very active development, large user base**. **SBOM output is somewhat secondary to its scanning mission**, so some CycloneDX/SPDX edge-case fields and metadata completeness lag behind tools built primarily as SBOM generators. **Best for teams already using Trivy for scanning** who want SBOM generation without adding another tool.

- **[cdxgen (CycloneDX)](https://github.com/CycloneDX/cdxgen)**  
  **Dedicated CycloneDX generator** maintained under the CycloneDX project umbrella with **unusually broad language support**. **The reference implementation for CycloneDX format** from the project that maintains the specification. **Best for teams committed to CycloneDX** wanting a generator from the specification maintainers.

- **[Microsoft sbom-tool](https://github.com/microsoft/sbom-tool)**  
  **Microsoft's open-source SBOM generator** supporting SPDX format for source and build artifacts. **Best for .NET and Microsoft-centric development environments**.

- **[SPDX Tools](https://github.com/spdx/tools-golang)**  
  **Official SPDX tools** for generating, validating, and manipulating SPDX documents. **Best for teams needing strict SPDX compliance**.

- **[Tern](https://github.com/tern-tools/tern)**  
  **Software composition analysis tool and Python library** that generates SBOMs for container images and Dockerfiles. **Layer-by-layer view of container contents** in human-readable, JSON, HTML, and SPDX formats. **Best for container-focused SBOM generation** with a focus on layer transparency.

### Additional Strong Open-Source Options

- **Grype** — Anchore's vulnerability scanner that pairs with Syft SBOMs for continuous monitoring.
- **Dependency-Track** — Open-source SBOM analysis platform that consumes SBOMs and continuously monitors components for vulnerabilities with policy enforcement and license compliance.
- **OpenVEX** — Vulnerability Exploitability eXchange specification and tooling for machine-readable exploitability assessments that complement SBOMs.
- **Sigstore** — Digital signing and verification for software artifacts, providing the provenance layer that makes SBOMs verifiable.

**Frameworks for building custom systems**: Combine **Syft** for spec-compliant SBOM generation from containers and filesystems, **Trivy** for unified vulnerability scanning and SBOM output, **cdxgen** for dedicated CycloneDX generation with broad language support, **Dependency-Track** for continuous SBOM-based monitoring, and **Sigstore** for artifact signing and provenance verification — to build a complete self-hosted SBOM pipeline from generation through continuous monitoring and signed attestation.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- SBOM tools differ significantly in format support, ecosystem coverage, and deployment constraints. **Syft and Trivy are the most widely deployed open-source generators** with dual CycloneDX and SPDX support. **Trivy's SBOM output is secondary to its scanning mission** — edge-case metadata completeness may lag dedicated generators. **Sonatype SAGE is the only offering with a fully air-gapped architecture** for classified environments. **Mend's AIBoM and Black Duck's AI model detection** address the emerging need to inventory AI/ML components. **License compliance tools like FOSSA and Revenera** excel at NOTICE file generation and obligation tracking beyond basic SBOM generation. **Anchore's "Bring Your Own SBOM"** imports and validates third-party SBOMs in SPDX 2.1-2.3 and CycloneDX 1.0-1.6.
- Self-hosted open-source solutions require proper integration with existing CI/CD pipelines, vulnerability database updates, and ongoing monitoring of SBOM quality and completeness.

---

**Made for security engineers, DevSecOps teams, supply chain architects, and developers building SBOM and software composition analysis platforms.**  
Let's make software bill of materials more open, spec-compliant, and actionable.
