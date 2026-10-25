<!--
  CYBER-SENTINEL
  Public ecosystem landing page.
  Product repositories remain authoritative for implementation and release state.
-->

<p align="center">
  <img src="./assets/cyber-sentinel-banner-new.png" alt="Cyber-Sentinel — Evidence-Driven Cyber Defense Ecosystem" width="100%" />
</p>

<h1 align="center">Cyber-Sentinel</h1>
<p align="center"><strong>Evidence-Driven Cyber Defense Engineering</strong></p>
<p align="center">KNOW • DEFEND • APPLY • VALIDATE • AUTOMATE • EVOLVE</p>

<p align="center">
  <a href="https://github.com/cyber-sentinel/Cyber-Sentinel-Atlas"><img alt="ATLAS — KNOW" src="https://img.shields.io/badge/ATLAS-KNOW-2563eb"></a>
  <a href="https://github.com/cyber-sentinel/Cyber-Sentinel-DefenseOps"><img alt="DefenseOps — DEFEND" src="https://img.shields.io/badge/DefenseOps-DEFEND-dc2626"></a>
  <a href="https://github.com/cyber-sentinel/Cyber-Sentinel-Skills"><img alt="Skills — APPLY" src="https://img.shields.io/badge/Skills-APPLY-7c3aed"></a>
  <a href="https://github.com/cyber-sentinel/Cyber-Sentinel-AION"><img alt="AION — INTERACT" src="https://img.shields.io/badge/AION-INTERACT-0f766e"></a>
  <img alt="Provenance First" src="https://img.shields.io/badge/engineering-provenance--first-0f766e">
  <img alt="Offline Aware" src="https://img.shields.io/badge/architecture-offline--aware-334155">
</p>

Cyber-Sentinel is a contract-separated cyber-defense ecosystem for turning **trusted knowledge** into **validated defensive engineering** and then into **repeatable operating practice**. The goal is not to accumulate rules, notes, or automation fragments; it is to make security work attributable, testable, reviewable, and operationally defensible.

> **Product thesis:** Security knowledge should become defensible engineering. Defensible engineering should become repeatable operating practice. Operational evidence should feed back into better knowledge, detections, controls, and procedures.

## Ecosystem at a Glance

| Product | Role | Core question | Current public maturity |
| --- | --- | --- | --- |
| [**ATLAS**](https://github.com/cyber-sentinel/Cyber-Sentinel-Atlas) | **KNOW** | What do we know about what we are seeing — and what evidence supports it? | Engineering-ready Windows First Preview; MVP-2 candidate validated; Public Preview still gated |
| [**DefenseOps**](https://github.com/cyber-sentinel/Cyber-Sentinel-DefenseOps) | **DEFEND** | What can we detect, hunt, validate, and defend — and what evidence supports that claim? | Stable engineering baseline `0.1.0`; no published GitHub Release/tag |
| [**Skills**](https://github.com/cyber-sentinel/Cyber-Sentinel-Skills) | **APPLY** | How should a security task be performed consistently, safely, and verifiably? | Foundation v0.1 under controlled review; official release not authorized |
| [**AION**](https://github.com/cyber-sentinel/Cyber-Sentinel-AION) | **INTERACT** | How should grounded cybersecurity context be presented and accessed through visual, voice, and bilingual interaction? | Visual/voice engineering in a stacked Draft PR series; native runtime and Product Acceptance pending |

<p align="center">
  <img src="./assets/ecosystem-overview.svg" alt="Cyber-Sentinel ecosystem: ATLAS KNOW, DefenseOps DEFEND, Skills APPLY, with validation and feedback" width="100%" />
</p>

## Engineering Status Snapshot — 2026-10-25

This is a **dated GitHub engineering snapshot**, not a live process monitor or a release announcement. Product repositories and approved Product Owner evidence remain authoritative; in-progress local Codex activity cannot be inferred from Git commits alone.

| Product | Latest reviewed engineering evidence | Next acceptance boundary |
| --- | --- | --- |
| **ATLAS** | [MVP-2 remediation Draft PR #231](https://github.com/cyber-sentinel/Cyber-Sentinel-Atlas/pull/231), head `d4a1c45ac46c`; [Foundation Hygiene #40185293219](https://github.com/cyber-sentinel/Cyber-Sentinel-Atlas/actions/runs/40185293219) succeeded on that revision | Exact-candidate Windows UX, offline/pack, localization and Product Owner review remain distinct from CI; no public release |
| **DefenseOps** | `main` retains the `0.1.0` engineering baseline; [Draft PR #13](https://github.com/cyber-sentinel/Cyber-Sentinel-DefenseOps/pull/13) proposes `AGENTS.md` and has successful [Repository Hygiene #39992078480](https://github.com/cyber-sentinel/Cyber-Sentinel-DefenseOps/actions/runs/39992078480) | Final governance review, merge authorization, platform-specific deployment validation; no release |
| **Skills** | [Foundation Draft PR #1](https://github.com/cyber-sentinel/Cyber-Sentinel-Skills/pull/1) adds five offline built-in Skills; [exact-head Foundation #40067596169](https://github.com/cyber-sentinel/Cyber-Sentinel-Skills/actions/runs/40067596169) passed four Linux/Windows matrix jobs | Branch-protection GOV-001 verified in PR evidence; README merge conflict, final review and owner merge/release authorization still open |
| **AION** | [Synthetic bilingual ASR diagnostic Draft PR #29](https://github.com/cyber-sentinel/Cyber-Sentinel-AION/pull/29) at `595150e04b05`; latest exact-head [AION Foundation #39607007924](https://github.com/cyber-sentinel/Cyber-Sentinel-AION/actions/runs/39607007924) failed before visible steps | Confirm CI root cause and approved runner/budget, real offline voice/runtime evidence, license clearance and Product Acceptance |

Successful synthetic tests or public visibility **do not** certify Production, authorize release, or transfer Product Owner approval between build candidates.

## ATLAS — KNOW

**Provenance-First Cyber Defense Knowledge & Investigation Platform**

ATLAS is the governed knowledge and analyst-investigation layer. It connects telemetry records, canonical entities, relationships, adversary behavior, defensive context, investigation pivots, and claim-level provenance while preserving source identity and trust boundaries.

### Current verified position

| Boundary | State |
| --- | --- |
| Microsoft-Windows-Security-Auditing | **423/423 encyclopedia-grade — COMPLETE** |
| Sysmon 15.22 | **30/30 encyclopedia-grade — COMPLETE** |
| PowerShell Operational | **43/43 in the validated MVP-2 candidate** |
| Integrated MVP-2 runtime corpus | **502/502 clean-Windows runtime acceptance** |
| Deterministic retrieval | SQLite + FTS5, exact-before-lexical |
| Verified content delivery | `.atlaspack` + TUF trust model |
| Shared Core | Go / bounded child-process stdio |
| Windows Desktop | Tauri 2.x; offline-first engineering preview |
| Product Owner interactive review | **PENDING** for the current MVP-2 candidate |
| Public Preview | **BLOCKED / fail-closed** until release gates close |

The PowerShell and `502/502` figures describe the current validated MVP-2 candidate workstream, not a claim that every item is already merged into the public `main` release authority. The global Windows denominator also remains intentionally unfrozen while additional mandatory telemetry families are brought under controlled coverage.

### ATLAS delivery family

`Desktop (Windows / Linux / macOS)` • `CLI` • `Web` • `PWA` • `API` • `Mobile`

Windows Desktop is the current release-critical surface. The other surfaces are approved delivery scope, not released-product claims.

## DefenseOps — DEFEND

**Evidence-Driven Cyber Defense Engineering**

DefenseOps treats defensive content as an engineering lifecycle rather than a rule collection. It owns detections, hunts, validation assets, DFIR/IR engineering material, response content, deception-oriented controls, and defensive automation with explicit telemetry, engine, evidence, tuning, and rollback requirements.

Current baseline highlights:

- Detection-as-Code and Hunt-as-Code;
- Sigma, YARA, Suricata, Snort and Zeek validation where applicable;
- SIEM/EDR query engineering with explicit backend identity;
- positive/negative synthetic validation fixtures;
- false-positive, blind-spot and deployment-boundary analysis;
- Hunt → Detection → Validation → Operational feedback.

A CI-green rule is evidence of a defined validation contract — **not** automatic production authorization.

## Skills — APPLY

**Governed Cybersecurity Operational Skills & Playbooks**

Skills converts analyst know-how into bounded operational contracts. A substantive Skill is expected to make purpose, authorization, prerequisites, inputs, procedure, decision points, evidence, stop conditions, rollback, outputs, references, and version history explicit.

The active Foundation v0.1 workstream is under controlled review and is intentionally separated from release authority. Human accountability, environment-specific authorization, and evidence requirements remain mandatory even when a procedure is machine-readable or AI-assisted.

## AION — INTERACT

**Grounded Visual and Bilingual Voice Interaction**

[AION](https://github.com/cyber-sentinel/Cyber-Sentinel-AION) owns the versioned Entity/visual-state experience, bounded Persian/English interaction contracts, accessibility fallbacks, and product-adapter boundary. It is a **supporting interaction layer, not a second authoritative cybersecurity knowledge engine**. ATLAS remains authoritative for its source-backed security facts, search and investigation content.

Current Visual, Session, Adapter and offline Voice/ASR/TTS work is managed in stacked Draft PRs. Synthetic quality diagnostics and framework tests are engineering evidence; hardware-native operation, redistribution, Product Owner acceptance and release remain separately gated. The ATLAS integration target is **one application window and one end-user executable**, not an extra AION installer.

## Engineering Principles

1. **No material technical claim without provenance.**
2. **Deterministic evidence precedes optional semantic augmentation.**
3. **Detection and defensive content must be measurable and testable.**
4. **Automation must preserve evidence and decision boundaries.**
5. **Security controls must survive production reality.**
6. **Offline and restricted environments are first-class design conditions where relevant.**
7. **Canonical contracts do not drift for implementation convenience.**
8. **Trust, update, rollback, signing, and release boundaries are explicit.**
9. **Human accountability remains intact in assisted operations.**
10. **Product maturity follows executable evidence, not marketing language.**

## Where the Products Meet

| Flow | Contract |
| --- | --- |
| ATLAS → DefenseOps | Evidence-backed knowledge and context may inform defensive engineering; origin alone never grants production authority |
| DefenseOps → Skills | Validated engineering artifacts may become repeatable procedures; Skills does not redefine detection ownership |
| Skills → ATLAS | Operational outcomes and lessons may become governed knowledge only through ATLAS provenance and validation boundaries |
| AION ↔ Product Core | Versioned, bounded product adapters communicate grounded results and state; AION never becomes the source of cybersecurity truth |
| All products | Versioning, attribution, authorization, review, and release authority remain explicit |

## Primary Security Domains

`SOC / THIR` • `Detection Engineering` • `Threat Hunting` • `DFIR / Incident Response` • `Threat Intelligence` • `Security Automation / SOAR` • `Cyber Defense Architecture` • `AppSec / SSDLC / DevSecOps` • `IAM / PAM` • `Endpoint / Network / Cloud / Container Security`

### Selected technologies and frameworks

`Go` `Python` `PowerShell` `Bash` `Rust` `SQLite/FTS5` `Tauri` `GitHub Actions` `Docker` `Kubernetes`

`Splunk` `Wazuh` `MISP` `Sigma` `YARA` `Sysmon` `Zeek` `Suricata` `Snort`

`MITRE ATT&CK` `MITRE D3FEND` `MITRE CAR` `NIST CSF` `NIST SP 800-61` `CIS Controls` `ISO/IEC 27001` `OWASP`

## Maturity Model

| State | Meaning |
| --- | --- |
| **Foundation** | Product contracts and governance exist; operational coverage is still forming |
| **Engineering Ready** | Defined implementation and engineering-verification gates have passed |
| **Public Preview Ready** | Release-specific security, licensing, redistribution, packaging, accessibility, signing, and publication gates have passed |
| **Production Deployment** | Environment-specific approval after customer/organization validation and change control |

Public source visibility, passing CI, or an engineering preview is **not** represented as GA or universal production readiness.

## Repositories

- **KNOW** — [Cyber-Sentinel-Atlas](https://github.com/cyber-sentinel/Cyber-Sentinel-Atlas)
- **DEFEND** — [Cyber-Sentinel-DefenseOps](https://github.com/cyber-sentinel/Cyber-Sentinel-DefenseOps)
- **APPLY** — [Cyber-Sentinel-Skills](https://github.com/cyber-sentinel/Cyber-Sentinel-Skills)
- **INTERACT** — [Cyber-Sentinel-AION](https://github.com/cyber-sentinel/Cyber-Sentinel-AION)

---

<p align="center"><strong>Ali RahimDabagh</strong></p>
<p align="center">Information Security Manager • Cyber Defense Architect</p>
<p align="center"><strong>Know. Defend. Apply. Evolve.</strong></p>
