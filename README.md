<!--
  CYBER-SENTINEL GitHub Profile
  Professional cybersecurity engineering portfolio and product ecosystem landing page.
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

**Cyber-Sentinel is a connected cyber-defense product ecosystem built around a simple principle: knowledge, defensive engineering, and operational execution should reinforce each other without collapsing their trust boundaries.**

The ecosystem is designed for security practitioners, engineering teams, and security leaders who care about evidence, provenance, reproducibility, operational safety, offline capability, and production reality.

```text
Cyber-Sentinel
├── ATLAS       — KNOW   → Connect • Search • Investigate • Explain
├── DefenseOps  — DEFEND → Detect • Hunt • Validate • Respond • Automate
└── Skills      — APPLY  → Execute • Review • Reuse • Govern
```

The objective is not repository count. The objective is a coherent cyber-defense operating system in which **knowledge becomes engineering, engineering becomes repeatable practice, and operating results feed back into stronger knowledge and controls**.

## Product Portfolio

| Product | Role | Current maturity | Primary value |
| --- | --- | --- | --- |
| [Cyber-Sentinel-Atlas](https://github.com/cyber-sentinel/Cyber-Sentinel-Atlas) | **KNOW** | First Preview engineering readiness **READY**; Phase 5.10 Public Preview Readiness **ACTIVE / BLOCKED** | Provenance-first knowledge, deterministic investigation, verified offline content, Windows analyst workbench |
| [Cyber-Sentinel-DefenseOps](https://github.com/cyber-sentinel/Cyber-Sentinel-DefenseOps) | **DEFEND** | Public source; stable engineering baseline `0.1.0` | Detection engineering, threat hunting, validation, DFIR/IR engineering, response and automation |
| [Cyber-Sentinel-Skills](https://github.com/cyber-sentinel/Cyber-Sentinel-Skills) | **APPLY** | Public foundation / operating-model stage | Governed cybersecurity procedures and playbooks for humans and AI-assisted workflows |

Maturity labels are intentionally conservative. Passing CI, a public repository, or an engineering-ready preview is not presented as universal production readiness unless the corresponding release boundary has actually been closed.

---

## ATLAS — KNOW

### Provenance-First Cyber Defense Knowledge & Investigation Platform

ATLAS is the knowledge and investigation layer of the ecosystem. It connects security telemetry, canonical records, adversary behavior, detections, threat hunts, DFIR artifacts, relationships, and claim-level provenance into an inspectable analyst workflow.

**Core question:** *What do we know about what we are seeing — and what evidence supports it?*

Current verified engineering boundary:

```text
Phase 5.1  Product Foundation                 COMPLETE
Phase 5.2  Canonical Data Model              COMPLETE / MERGED
Phase 5.3  Source & Ingestion Core           COMPLETE / MERGED
Phase 5.4  Deterministic Search Core         COMPLETE / MERGED
Phase 5.5  Offline Pack / Shared Core        COMPLETE / MERGED / VERIFIED / FROZEN
Phase 5.6  Windows Desktop MVP               COMPLETE / MERGED / POST-MERGE VERIFIED
           ADR-0026                         ACCEPTED — Tauri 2.x
           G-D1 through G-D9                PASS / VERIFIED

FIRST PREVIEW ENGINEERING READINESS            READY
Phase 5.10 Public Preview Readiness            ACTIVE / BLOCKED
```

The Windows First Preview is built around a production Go Shared Core, deterministic SQLite + FTS5 retrieval, TUF-based verified content packs, bounded stdio IPC, claim-level provenance, explicit application-command allowlists, and a Tauri 2.x desktop host. Core investigation is offline-capable and does not depend on a default local HTTP/TCP service.

Phase 5.10 now governs the gap between an engineering-ready preview and a publicly distributable security product. Licensing, third-party redistribution, production signing/key custody, signed public packaging, and packaged accessibility acceptance remain explicit release gates; source-freshness and launch/rollback governance are controlled as machine-enforced release policy.

---

## DefenseOps — DEFEND

### Evidence-Driven Cyber Defense Engineering

DefenseOps is the defensive-engineering layer for reusable, testable, evidence-backed detections, hunts, validation assets, response content, DFIR/IR material, deception-oriented controls, and security automation.

**Core question:** *What can we detect, validate, hunt, and defend — and what evidence supports that claim?*

The current stable engineering baseline is `0.1.0`. Validation includes native Sigma, YARA, Suricata, Snort 3, and Zeek checks, positive/negative synthetic fixtures, and explicit quality maturity levels.

DefenseOps treats telemetry prerequisites, engine specificity, behavioral evidence, false positives, production constraints, rollback, and reproducibility as part of the engineering artifact—not as post-deployment documentation.

---

## Skills — APPLY

### Governed Cybersecurity Operational Skills & Playbooks

Skills is the operating-procedure layer for cybersecurity work that must be consistent, reviewable, attributable, safe, and suitable for human or AI-assisted execution without losing authorization or accountability boundaries.

**Core question:** *How should this security task be performed consistently, safely, and verifiably?*

A Skill is treated as a governed execution contract rather than a command list. It should make scope, authorization, prerequisites, procedure, evidence, failure/exit conditions, escalation, rollback, outputs, and attribution explicit.

The public `main` branch remains at foundation / operating-model maturity. A more complete Foundation v0.1 implementation exists on a separately governed review branch and remains subject to its own merge/release conditions.

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

Trust is never inherited merely because another Cyber-Sentinel repository produced an artifact. Provenance, validation, versioning, authorization, and release boundaries remain explicit at every layer.

## Engineering Principles

- **No technical claim without provenance.**
- **Detection must be measurable and testable.**
- **Security controls must survive production reality.**
- **Automation should reduce analyst workload without hiding evidence or decision boundaries.**
- **Incident response should feed back into architecture, detection, and engineering.**
- **AI output in security should be grounded, inspectable, and governed.**
- **Canonical contracts should not drift for implementation convenience.**
- **Architecture decisions should follow executable evidence, not framework preference.**
- **Production changes require explicit safety, rollback, and environment-specific validation.**

## Commercial Maturity Discipline

Cyber-Sentinel distinguishes four states deliberately:

- **Engineering ready** — defined engineering and verification gates have passed.
- **Public Preview ready** — signing, distribution, licensing, accessibility, governance, publication, and release evidence are closed.
- **Production ready** — environment-specific and never inferred from repository CI alone.
- **Public source** — improves inspectability but does not itself define licensing or commercial redistribution rights.

This distinction is intentional for security products: confidence should follow evidence, not branding.

## Professional Focus

Cyber-Sentinel reflects work across Information Security Management, SOC/THIR, Detection Engineering, Threat Hunting, DFIR, security architecture, AppSec/SSDLC/DevSecOps, defensive automation, CTI, and grounded AI-assisted security operations.

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
