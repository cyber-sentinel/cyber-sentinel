<!--
  CYBER-SENTINEL
  Public ecosystem landing page.
  Visual assets are intentionally modular so product-specific artwork can be replaced later
  without changing the product architecture or maturity statements.
-->

<p align="center">
  <img src="./assets/cyber-sentinel-banner-new.png" alt="Cyber-Sentinel — Evidence-Driven Cyber Defense Ecosystem" width="100%" />
</p>

<p align="center">
  <strong>KNOW • DEFEND • APPLY • EVOLVE</strong>
</p>

<p align="center">
  Provenance-First Knowledge • Detection Engineering • Threat Hunting • DFIR • Defensive Validation • Security Automation • Governed Operational Skills
</p>

---

# Cyber-Sentinel

**Cyber-Sentinel is an evidence-driven cyber-defense product ecosystem for turning trusted security knowledge into validated defensive engineering and repeatable operational practice.**

It is being built for security teams that need investigation, detection, response, automation, and AI-assisted workflows to remain **inspectable, attributable, testable, versioned, and operationally bounded**.

Cyber-Sentinel is not designed as a collection of disconnected repositories. Each product owns a distinct contract:

```text
Cyber-Sentinel
│
├── ATLAS       — KNOW
│   Connect • Search • Investigate • Explain
│
├── DefenseOps  — DEFEND
│   Detect • Hunt • Validate • Respond • Automate
│
└── Skills      — APPLY
    Execute • Review • Reuse • Govern

                 ↓
       VALIDATE • AUTOMATE • EVOLVE
                 ↺
```

> **Product thesis:** Security knowledge should become defensible engineering; defensible engineering should become repeatable operating practice; operational outcomes should feed back into better knowledge, detections, controls, and procedures.

<!-- FUTURE VISUAL SLOT:
     assets/ecosystem-architecture.png
     Recommended: international product architecture illustration showing KNOW / DEFEND / APPLY
     with a restrained cyber-intelligence visual language.
-->

## Product Portfolio

| Product | Mission | Current maturity | Primary value |
| --- | --- | --- | --- |
| [Cyber-Sentinel ATLAS](https://github.com/cyber-sentinel/Cyber-Sentinel-Atlas) | **KNOW** | Windows First Preview engineering-ready; Public Preview closure active | Provenance-first knowledge, deterministic search, investigation, relationships, verified offline packs |
| [Cyber-Sentinel DefenseOps](https://github.com/cyber-sentinel/Cyber-Sentinel-DefenseOps) | **DEFEND** | Stable engineering baseline `0.1.0`; controlled public-source maturity | Detection engineering, hunting, validation, DFIR/IR engineering, response and automation |
| [Cyber-Sentinel Skills](https://github.com/cyber-sentinel/Cyber-Sentinel-Skills) | **APPLY** | Foundation / operating-model stage | Governed procedures and playbooks for consistent human and AI-assisted execution |

Maturity labels are intentionally conservative. A public repository, passing CI, or a successful preview build is not presented as GA or universal production readiness unless the relevant release, security, legal, and operational boundaries are actually closed.

---

# ATLAS — KNOW

## Provenance-First Cyber Defense Knowledge & Investigation Platform

ATLAS is the knowledge and investigation layer of Cyber-Sentinel.

Its core question is:

> **What do we know about what we are seeing — and what evidence supports it?**

ATLAS connects telemetry, canonical records, adversary behavior, defensive context, investigation pivots, detections, hunts, DFIR artifacts, relationships, and claim-level provenance into one analyst workflow.

### Current Windows product state

- canonical schema `1.0.0` with exactly seven AtlasRecord families;
- deterministic exact-before-lexical search using SQLite + FTS5;
- TUF-based content-pack trust, trusted-time and anti-rollback controls;
- production Shared Core implemented in Go;
- bounded child-process stdio IPC;
- Tauri 2.x Windows desktop;
- no default local HTTP/TCP/WebSocket listener;
- verified portable Windows engineering package;
- clean-Windows Search → Record → Graph → Provenance acceptance;
- verified resolution of Windows Security Event ID `4688` and Sysmon Event ID `1`;
- fail-closed TUF target-tamper rejection;
- Public Preview release closure still gated by licensing, redistribution, production signing, exact-package evidence, and executable accessibility review.

### Approved ATLAS product family

```text
ATLAS
│
├── ATLAS Desktop
│    ├── Windows       ← current release-critical surface
│    ├── Linux
│    └── macOS
│
├── ATLAS CLI
│    ├── Windows
│    ├── Linux
│    └── macOS
│
├── ATLAS Web
│
├── ATLAS PWA
│    └── iOS Safari
│
├── ATLAS API
│
└── ATLAS Mobile
     ├── iOS
     └── Android
```

The iOS Safari PWA is a dedicated installable web experience for iPhone/iPad. Desktop and Android browser use are covered by the normal Web surface rather than separate PWA products. Native iOS and Android are distinct application surfaces with their own runtime, signing, privacy, and distribution controls.

### Approved Windows Security Corpus scope

ATLAS is moving from a small engineering-fixture pack to a measurable Windows security knowledge corpus.

The approved mandatory corpus scope includes:

- Microsoft-Windows-Security-Auditing / Security;
- Microsoft Sysmon;
- PowerShell Operational;
- Windows Defender native operational/security telemetry;
- AppLocker;
- WMI Activity;
- Task Scheduler Operational;
- Remote Desktop / Terminal Services;
- Windows Firewall / Windows Filtering Platform;
- DNS Client / DNS Server where applicable;
- Service Control Manager and service/process persistence telemetry;
- additional persistence-relevant Windows providers admitted through explicit source/version/provenance review.

A provider counts as covered only when authoritative source identity, normalization, canonical records, claims/provenance, search projections, pack inclusion, and acceptance evidence are present. Merely having a parser or source profile does not count as product coverage.

### ATLAS operating model

```text
Authoritative Sources
        ↓
Acquisition + Immutable Snapshot
        ↓
Normalization + Lineage
        ↓
Canonical Records
        ↓
Claims + Provenance
        ↓
Deterministic Search + Relationships
        ↓
Verified .atlaspack
        ↓
Analyst Investigation
        ↓
Evidence-backed defensive context
```

<!-- FUTURE VISUAL SLOT:
     assets/atlas-product-family.png
     Recommended: desktop / CLI / Web / iOS PWA / API / Mobile family map.
-->

---

# DefenseOps — DEFEND

## Evidence-Driven Cyber Defense Engineering

DefenseOps owns the engineering lifecycle around defensive content.

Its core question is:

> **What can we detect, validate, hunt, and defend — and what evidence supports that claim?**

DefenseOps is designed around production-conscious defensive engineering:

- Detection-as-Code;
- Hunt-as-Code;
- multi-engine detection validation;
- positive and negative synthetic fixtures;
- telemetry prerequisites;
- explicit engine/query-language identity;
- false-positive and blind-spot analysis;
- response engineering;
- DFIR/IR engineering content;
- deception-oriented defensive assets;
- rollback and deployment constraints;
- measurable quality maturity.

Current validated tooling includes Sigma, YARA, Suricata, Snort, Zeek and multiple SIEM/EDR query families where technically applicable.

DefenseOps does not replace ATLAS knowledge ownership and does not treat a syntactically valid rule as automatically production-safe.

<!-- FUTURE VISUAL SLOT:
     assets/defenseops-engineering-loop.png
     Recommended: Design → Review → Test → Validate → Deploy → Measure → Tune → Retire.
-->

---

# Skills — APPLY

## Governed Cybersecurity Operational Skills & Playbooks

Skills owns reusable operating methods.

Its core question is:

> **How should this security task be performed consistently, safely, and verifiably?**

A Cyber-Sentinel Skill is not merely a command list. It is intended to make the following explicit:

- purpose and authorized scope;
- prerequisites and dependencies;
- inputs;
- ordered procedure;
- decision points;
- evidence and verification;
- stop/escalation conditions;
- rollback/recovery;
- outputs;
- references and attribution;
- version history.

Skills is designed for humans first and AI-assisted execution where appropriate. Machine readability does not remove authorization, human oversight, or accountability.

<!-- FUTURE VISUAL SLOT:
     assets/skills-operating-contract.png
     Recommended: Authorized Task → Bounded Skill → Execution → Evidence → Review → Outcome.
-->

---

# Ecosystem Operating Loop

<p align="center">
  <img src="./assets/process-flow.png" alt="Cyber-Sentinel operating loop — KNOW, DEFEND, APPLY, VALIDATE, AUTOMATE, EVOLVE" width="100%" />
</p>

```text
Authoritative Sources / Telemetry / Security Knowledge
                         │
                         ▼
                  ATLAS — KNOW
        Connect • Search • Investigate • Explain
                         │
             evidence / defensive context
                         ▼
               DefenseOps — DEFEND
       Detect • Hunt • Validate • Respond • Automate
                         │
              repeatable operating method
                         ▼
                  Skills — APPLY
          Execute • Review • Reuse • Govern
                         │
                         ▼
          VALIDATE → AUTOMATE → EVOLVE
                         │
                         └──────────────↺
                    feedback into knowledge,
                 engineering and procedures
```

Trust is not inherited merely because another Cyber-Sentinel repository produced an artifact. Provenance, validation, versioning, authorization, and release boundaries remain explicit at every product boundary.

---

# Engineering & Trust Principles

1. **No technical claim without provenance.**
2. **Deterministic retrieval precedes optional semantic or AI augmentation.**
3. **Detection must be measurable and testable.**
4. **Automation must not hide evidence or decision boundaries.**
5. **Security controls must survive production reality.**
6. **Offline and restricted environments are first-class design conditions where relevant.**
7. **Canonical contracts do not drift for implementation convenience.**
8. **Trust, signing, update, rollback, and release boundaries are explicit.**
9. **Human accountability remains intact in AI-assisted operations.**
10. **Product maturity follows executable evidence, not marketing language.**

---

# Enterprise / International Product Direction

Cyber-Sentinel is being engineered for professional security environments that value:

- SOC and THIR investigation consistency;
- deterministic, evidence-backed analyst workflows;
- Detection Engineering and Threat Hunting at scale;
- DFIR and incident-driven defensive improvement;
- restricted/offline operational environments;
- defensible provenance and version lineage;
- security-content supply-chain controls;
- product-level release discipline;
- cross-platform delivery without duplicating canonical truth;
- AI-assisted workflows grounded in verifiable security context.

Target users include SOC analysts, incident responders, threat hunters, DFIR practitioners, detection/security engineers, purple teams, security architects, platform/security engineering teams, and security leaders building governed cyber-defense capabilities.

---

# Product Maturity Model

Cyber-Sentinel uses explicit maturity language:

| State | Meaning |
| --- | --- |
| **Foundation** | Product model and governance are established; broad operational coverage is still forming |
| **Engineering Ready** | Defined implementation and engineering verification gates have passed |
| **Public Preview Ready** | Release-specific licensing, redistribution, signing, packaging, accessibility, security and publication gates have passed |
| **Production Deployment** | Environment-specific approval after customer/organization validation and change control |

Public repository visibility does **not** automatically grant redistribution rights where a project license has not been published.

---

# Current Delivery Priorities

```text
ATLAS Windows Public Preview closure
        ↓
ATLAS Windows Security Corpus expansion
        ↓
ATLAS CLI
        ↓
ATLAS Web + iOS Safari PWA
        ↓
ATLAS Public API
        ↓
ATLAS Linux / macOS Desktop
        ↓
ATLAS Native iOS / Android
        ↓
Broader Cyber-Sentinel ecosystem integration
```

DefenseOps and Skills evolve in parallel under their own evidence and governance boundaries.

---

# Security Domains

Cyber-Sentinel spans engineering work across:

- SOC / THIR;
- Detection Engineering;
- Threat Hunting;
- DFIR / Incident Response;
- Cyber Defense Architecture;
- Threat Intelligence;
- Security Automation / SOAR;
- AppSec / SSDLC / DevSecOps;
- IAM / PAM / network and endpoint security;
- cloud/container security knowledge;
- AI-assisted security operations;
- governance-aware operational security.

### Selected technologies and ecosystems

`Go` `Python` `PowerShell` `Bash` `Rust` `SQLite/FTS5` `Tauri` `GitHub Actions` `Docker` `Kubernetes`

`Splunk` `Wazuh` `MISP` `Sigma` `YARA` `Sysmon` `Zeek` `Suricata` `Snort`

`MITRE ATT&CK` `MITRE D3FEND` `MITRE CAR` `NIST CSF` `NIST SP 800-61` `CIS Controls` `ISO/IEC 27001` `OWASP`

---

# Repository Map

- **KNOW:** [Cyber-Sentinel-Atlas](https://github.com/cyber-sentinel/Cyber-Sentinel-Atlas)
- **DEFEND:** [Cyber-Sentinel-DefenseOps](https://github.com/cyber-sentinel/Cyber-Sentinel-DefenseOps)
- **APPLY:** [Cyber-Sentinel-Skills](https://github.com/cyber-sentinel/Cyber-Sentinel-Skills)

---

## Maintainer

**Ali RahimDabagh**

Information Security Manager • Cyber Defense Architect

---

<p align="center">
  <strong>Know. Defend. Apply. Evolve.</strong>
</p>

<p align="center">
  <sub>Cyber-Sentinel • Evidence-Driven Cyber Defense Engineering</sub>
</p>
