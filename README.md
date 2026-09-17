<!--
  CYBER-SENTINEL GitHub Profile
  Maintained as a professional cybersecurity engineering portfolio and ecosystem landing page.
-->

<p align="center">
  <img src="./assets/cyber-sentinel-banner-new.png" alt="Cyber-Sentinel — Ali RahimDabagh" width="100%" />
</p>

<p align="center">
  <strong>Security Leadership • Cyber Defense Architecture • Evidence-Driven Engineering</strong>
</p>

<p align="center">
  SOC & THIR • Detection Engineering • DFIR • Security Architecture • AppSec & DevSecOps • AI Security • Defensive Automation
</p>

---

## Cyber-Sentinel

**Cyber-Sentinel is a connected cyber-defense engineering ecosystem built around one operating idea: knowledge, defensive engineering, and execution procedures should reinforce each other without collapsing their trust boundaries.**

It is designed as a professional security engineering portfolio and product family for practitioners, engineering teams, and security leaders who care about evidence, reproducibility, operational safety, provenance, and production reality.

The ecosystem currently consists of three contract-separated product layers:

```text
Cyber-Sentinel
├── ATLAS       — KNOW   → Connect • Search • Investigate • Explain
├── DefenseOps  — DEFEND → Detect • Hunt • Validate • Respond • Automate
└── Skills      — APPLY  → Execute • Review • Reuse • Govern
```

The objective is not repository count. The objective is a coherent operating system for cyber defense in which **knowledge can become engineering, engineering can become repeatable practice, and operational results can feed back into better knowledge and controls**.

## Current Product Portfolio

| Product | Role | Current maturity | Primary value |
| --- | --- | --- | --- |
| [Cyber-Sentinel-Atlas](https://github.com/cyber-sentinel/Cyber-Sentinel-Atlas) | **KNOW** | **First Preview engineering readiness: READY**; public release remains Pre-preview / unreleased | Provenance-first knowledge, deterministic investigation, verified offline content, analyst workbench |
| [Cyber-Sentinel-DefenseOps](https://github.com/cyber-sentinel/Cyber-Sentinel-DefenseOps) | **DEFEND** | Public source repository; stable baseline `v0.1.0` | Detection engineering, threat hunting, validation, DFIR/IR engineering, response and automation |
| [Cyber-Sentinel-Skills](https://github.com/cyber-sentinel/Cyber-Sentinel-Skills) | **APPLY** | Public foundation stage | Governed, reusable cybersecurity procedures and playbooks for humans and AI-assisted workflows |

Maturity labels are intentionally conservative. A public repository, passing CI, or successful preview build is not presented as GA or universal production readiness unless the relevant release boundary has actually been closed.

---

## ATLAS — KNOW

### Provenance-First Cyber Defense Knowledge & Investigation Platform

ATLAS is the knowledge and investigation product of the ecosystem. It connects security telemetry, canonical records, adversary behavior, detections, threat hunts, DFIR artifacts, defensive context, relationships, and claim-level provenance into an inspectable analyst workflow.

**Core question:** *What do we know about what we are seeing — and what evidence supports it?*

### Current engineering state

```text
Phase 5.1  Product Foundation                 COMPLETE
Phase 5.2  Canonical Data Model              COMPLETE / MERGED
Phase 5.3  Source & Ingestion Core           COMPLETE / MERGED
Phase 5.4  Deterministic Search Core         COMPLETE / MERGED
Phase 5.5  Offline Pack / Shared Core        COMPLETE / MERGED / POST-MERGE VERIFIED / FROZEN
Phase 5.6  Windows Desktop MVP               COMPLETE / MERGED / POST-MERGE VERIFIED
  5.6.0   Environment / Core Boundary       COMPLETE / VERIFIED
  5.6.1   Executable Candidate Builds       COMPLETE / VERIFIED
  5.6.2   Hard Gates / Desktop Selection    COMPLETE / VERIFIED
           G-D1 through G-D9                PASS / CLOSED
           ADR-0026                         ACCEPTED — Tauri 2.x
  5.6.3   First Preview UI                  COMPLETE / MERGED / VERIFIED
  5.6.4   Packaging / Clean-Windows Smoke   COMPLETE / MERGED / POST-MERGE VERIFIED

FIRST PREVIEW READY — ENGINEERING READINESS
Public binary release — PRE-PREVIEW / UNRELEASED
```

PR #39 merged the Phase 5.6 implementation to `main` at `70afc6fdb9e5ce88afdb0dd4de139aa659606f1e`. Post-merge package run `35133827422` completed successfully on that release baseline. PR #41 subsequently synchronized the public README and authoritative project-state documents; current ATLAS `main` is `d839bb366dbbd10282f6b6da70000d2fa4aaf826`.

The First Preview is an engineering-ready, unsigned portable Windows artifact. Production Authenticode signing, installer/public-distribution hardening, third-party licensing/redistribution closure, broader accessibility review, source freshness policy, and public launch criteria remain **Phase 5.10 — Public Preview Readiness** work.

### Accepted architecture

- canonical schema contract `1.0.0` using JSON Schema Draft 2020-12;
- exactly seven canonical `AtlasRecord` families;
- deterministic exact-before-lexical retrieval using SQLite + FTS5;
- TUF-based pack trust, trusted-time, and highest-seen rollback protection;
- verified `.atlaspack` runtime with immutable generations and Last Known Good semantics;
- production Shared Core implemented in Go;
- bounded child-process stdio IPC via `atlas-core --serve-stdio`;
- no default local HTTP/TCP/WebSocket listener and no hidden network fallback;
- Windows desktop host selected as Tauri 2.x through frozen, evidence-based evaluation;
- explicit application command allowlists and CSP `connect-src 'none'`;
- adjacent SHA-256-bound `atlas-core.exe` sidecar;
- fail-closed sidecar integrity handling and verified recovery;
- unsigned First Preview packaging boundary, with production signing deferred to Public Preview readiness.

The First Preview UI implements offline global search, canonical record detail, relationship and graph navigation, source/provenance visibility, verified pack state, pack update, safe rollback/recovery visibility, diagnostics, and UTC/system-local/Tehran-Jalali presentation.

ATLAS remains intentionally **offline-first, evidence-first, and fail-closed**.

---

## DefenseOps — DEFEND

### Production-Aware Cyber Defense Engineering

DefenseOps is the defensive-engineering layer for reusable, testable, evidence-backed detections, hunts, validation assets, response content, DFIR/IR engineering material, deception-oriented controls, and security automation.

**Core question:** *What can we detect, validate, hunt, and defend — and what evidence supports that claim?*

The current stable baseline is `v0.1.0`. Its validation model includes native Sigma, YARA, Suricata, Snort, and Zeek checks, positive/negative synthetic fixtures, and explicit quality maturity levels.

DefenseOps is deliberately production-conscious: telemetry prerequisites, false positives, engine/language specificity, validation maturity, rollback, reproducibility, and deployment constraints are treated as part of the engineering artifact rather than afterthoughts.

DefenseOps is a public source repository. No project `LICENSE` is currently published, so public visibility must not be interpreted as a reuse or redistribution grant.

---

## Skills — APPLY

### Governed Cybersecurity Operational Skills & Playbooks

Skills is the reusable operating-procedure layer for cybersecurity work that should be explicit enough to execute consistently, review technically, attribute correctly, improve over time, and consume safely in human or AI-assisted workflows.

**Core question:** *How should this security task be performed consistently, safely, and verifiably?*

A Skill is treated as a governed execution contract rather than a command list. It should make scope, authorization, prerequisites, procedure, evidence, failure conditions, rollback/escalation, expected outputs, and attribution clear.

The repository is currently at foundation stage. It is public, but no project `LICENSE` is presently published; public visibility must not be interpreted as a reuse or redistribution grant.

---

## Ecosystem Operating Loop

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

`VALIDATE`, `AUTOMATE`, and `EVOLVE` are operating outcomes and feedback stages, not separate repositories.

Controlled content may move between products, but trust is never inherited merely because another Cyber-Sentinel repository produced an artifact. Provenance, validation, versioning, authorization, and release boundaries remain explicit.

---

## Engineering Principles

- **No technical claim without provenance.**
- **Detection must be measurable and testable.**
- **Security controls must survive production reality.**
- **Automation should reduce analyst workload without hiding evidence or decision boundaries.**
- **Threat intelligence is valuable when it changes a defensive decision.**
- **Incident response should feed back into architecture, detection, and engineering.**
- **AI output in security should be grounded, inspectable, and governed.**
- **Canonical contracts should not drift for implementation convenience.**
- **Security engineering should be reproducible, documented, reviewable, and rollback-aware.**
- **Architecture decisions should follow executable evidence, not framework preference.**

## Commercial Maturity Discipline

Cyber-Sentinel uses explicit maturity boundaries rather than marketing shorthand:

- **Engineering ready** means the defined engineering and verification gates have passed.
- **Public preview ready** additionally requires signing, distribution, licensing, accessibility, release governance, and publication criteria.
- **Production ready** is environment-specific and cannot be inferred from repository CI alone.
- **Public source visibility** does not grant reuse or redistribution rights when no project license has been published.

This distinction is intentional for security products: confidence should follow evidence, not branding.

## Professional Focus

Cyber-Sentinel reflects work across:

- Information Security Management and cyber-defense strategy;
- SOC and THIR operating models;
- Detection Engineering and threat hunting;
- Digital Forensics and Incident Response;
- security architecture and defense-in-depth;
- AppSec, SSDLC, and DevSecOps;
- security automation and orchestration;
- AI-assisted defensive workflows and grounded security knowledge systems.

### Security technologies and platforms

`Splunk` `Wazuh` `MISP` `Sigma` `YARA` `Sysmon` `Zeek` `Suricata` `SOAR` `CTI` `SentinelOne` `ESET Inspect` `FortiGate` `FortiWeb` `Palo Alto` `F5 BIG-IP` `PAM` `DLP` `IAM`

### Engineering technologies

`Go` `Python` `PowerShell` `Bash` `Rust` `Git/GitHub Actions` `SQLite/FTS5` `Tauri` `Docker` `Kubernetes` `REST APIs` `JSON` `YAML`

### Frameworks and standards

`MITRE ATT&CK` `MITRE D3FEND` `MITRE CAR` `NIST CSF` `NIST SP 800-61` `CIS Controls` `ISO/IEC 27001` `OWASP`

---

## Maintainer

**Ali RahimDabagh**

Information Security Manager • Cyber Defense Architect

15+ years across security operations, incident response, threat hunting, digital forensics, security architecture, security engineering, and security leadership.

---

<p align="center">
  <strong>Know. Defend. Apply. Evolve.</strong>
</p>

<p align="center">
  <sub>Cyber-Sentinel • Evidence-Driven Security Leadership & Cyber Defense Engineering</sub>
</p>
