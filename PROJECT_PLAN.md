# Pre-GDHF Technical Workshop — Master Project Plan & Execution Tracker
Two-day applied digital immunization workshop governance, work breakdown structure, critical path schedule, and action tracker
**To:** Pre-GDHF Workshop Steering Group (OHS-SF & WHO)  
**From:** Fred Hersch & Roy Munge (OHS-SF) | Carl Leitner & Diana Wijayanti (WHO)  
**Date:** October 19, 2026  
**Primary Sources:** [Workshop Agenda Slides](https://docs.google.com/presentation/d/157ICNv27xEB80z2SJHi1S5_XT5GEeHrmGD1igOw16DQ/edit?slide=id.p4#slide=id.p4) | [User Journeys & Technical Requirements Doc](https://docs.google.com/document/d/1x30S9zc93lvHqoh8VkKKGNU31JvXVh85pnaqgIeD47M/edit?tab=t.0#heading=h.i0qefgnmrgri) | Workshop Sync Records (Oct 9, Oct 14, Oct 16, 2026)

## 1. Executive Summary & Governance Structure

| Track / Surface | Primary Accountability | Core Purpose & Scope | Target Cohort & Participants |
| :--- | :--- | :--- | :--- |
| **Technical & Implementer Track** | **OHS-SF Lead:** Roy Munge (Nawi Tech)<br>**OHS-SF Co-Lead:** Fred Hersch<br>**WHO Tech Lead:** Carl Leitner | Hands-on FHIR data modeling, StructureMap transformation, GDHCN cryptographic verification, and multiplatform application assembly (OHS Player web & tablet, offline Android CHW). | Software developers, FHIR implementers, Interoperability Lab engineers (Thailand, Indonesia, Malaysia, Laos, Cambodia), and technical partners (AeHIN, CSIRO, OpenFn). |
| **Policy & Decision-Maker Track** | **WHO Lead:** Diana Wijayanti<br>**WHO Co-Leads:** Garrett Mehl, Alvin Marcelo (AeHIN) | Cross-border trust frameworks, Digital Public Infrastructure for Health (DPI-H) reference architectures, data-sharing agreements, and regional governance of unmapped domestic vaccine codes. | Ministry of Health planners, national digital health directors, and international development partners. |
| **Joint Plenary & Vignette** | **Joint Co-Chairs:** Fred Hersch (OHS-SF), Carl Leitner (WHO) | Unified end-to-end clinical storyline connecting foreign delivery, CHW discovery, primary clinic verification, and multi-member cross-border travel ("One Family, One Phone"). | Combined technical and policy cohorts (Day 1 Opening, Day 1 Closing Synthesis, Day 2 Final Connected Demo). |

The two-day Pre-GDHF workshop (November 30 – December 1, 2026, Bangkok) provides an applied, vendor-neutral learning environment leading directly into the Global Digital Health Forum. The programme connects high-level policy deliberation with tangible technical verification by anchoring both cohorts in a shared patient journey.

### Track Governance & RACI Matrix

| Workstream Component | Responsible (R) | Accountable (A) | Consulted (C) | Informed (I) |
| :--- | :--- | :--- | :--- | :--- |
| **Overall Workshop Delivery & Cadence** | Diana Wijayanti, Carl Leitner (WHO) | WHO (Carl Leitner, Garrett Mehl) | Fred Hersch, Roy Munge (OHS-SF), Mark Landry, Alvin Marcelo | Wider GDHF Steering Committee |
| **Clinical Vignette Script (J1–J4.1)** | Fred Hersch | Fred Hersch | Carl Leitner, Roy Munge | Country delegations |
| **KMP QR Verification Library** | Carl Leitner, Jose Costa Teixeira | Carl Leitner | Roy Munge, Jing Tang | Technical participants |
| **Mobile & Web Demo Applications** | Roy Munge, Jing Tang | Roy Munge (OHS-SF) | Fred Hersch, Carl Leitner | WHO technical leads |
| **Test Payloads & Mock VHL Issuer** | Ritika Rawlani, Jose Costa Teixeira | Carl Leitner | Roy Munge | Interoperability labs |
| **FHIR Implementation Guide (IG)** | Roy Munge, Carl Leitner | Roy Munge | Ritika Rawlani, Jose Costa Teixeira | HL7 / AeHIN |
| **Day 1 Code Labs & Scaffolding** | Fred Hersch, Roy Munge | Fred Hersch | CSIRO, OpenFn | Technical participants |
| **Policy Curriculum & Breakouts** | Diana Wijayanti, Garrett Mehl | Garrett Mehl (WHO) | Mark Landry, Alvin Marcelo | MoH leaders |
| **Country Delegations & Logistics** | Alvin Marcelo, Diana Wijayanti | Diana Wijayanti (WHO) | Mark Landry | Thailand MoH host team |

## 2. Master Work Breakdown Structure (WBS) & Task Tracker

| ID | Track | Workstream | Task Description & Scope | Owner(s) | Priority | Due Date | Status | Deliverable / Verification Criteria |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **TECH-01** | Technical | Clinical Vignette | Finalize step-by-step clinical vignette script (J1–J4.1) | Fred Hersch | P0 | 2026-10-21 | In Progress | Validated sequence flow connecting newborn Hep B, CHW referral, clinic GDHCN check, and multi-member travel. |
| **TECH-02** | Technical | Issuance Demo | Produce simulated vaccine issuance demo video & paper cards | Carl Leitner | P1 | 2026-10-24 | In Progress | Pre-recorded issuance video and pre-printed sample QR cards. Eliminates live UI/printer dependencies on site. |
| **TECH-03** | Technical | Test Data & Keys | Provision test payloads, DEV keys & single-vaccine IPS | Ritika Rawlani, Carl Leitner | P0 | 2026-10-20 | In Progress | Signed DVC payloads (Country A vs B unmapped codes) and single-vaccine IPS embedded QR payloads. |
| **TECH-04** | Technical | QR & Crypto Lib | Transcode & build Kotlin Multiplatform (KMP) QR validator | Carl Leitner, Jose Costa Teixeira | P0 | 2026-10-23 | In Progress | Kotlin/Rust cross-compiled library for HCERT/DVC extraction and DEV trust list signature checking on Android & Web. |
| **TECH-05** | Technical | CHW Mobile App | Build offline-first CHW Android referral application | Roy Munge | P0 | 2026-10-28 | In Progress | Android OHS app scanning QR to read unverified vaccine metadata, registering newborn, and generating clinic referral. |
| **TECH-06** | Technical | Clinic EMR Verifier | Build clinic EMR verifier & schedule calculation engine | Roy Munge, Jing Tang | P0 | 2026-11-04 | Not Started | OHS Player web / tablet app scanning paper QR, verifying GDHCN digital signature, and calculating due routine vaccines. |
| **TECH-07** | Technical | Family Wallet | Build "One Family, One Phone" multi-member Android wallet | Roy Munge | P1 | 2026-11-10 | Not Started | Lightweight Android app segregating family profiles (father medications via IPS, child DVCs) with separate VHL passcodes. |
| **TECH-08** | Technical | VHL Middleware | Prototype mock VHL issuer & OpenFn packaging pipeline | Jose Costa Teixeira, Roy Munge | P1 | 2026-11-06 | Not Started | Lightweight mock VHL issuer on ITB/GCP using OpenFn to fetch/package FHIR resources without heavy Docker containers. |
| **TECH-09** | Technical | Implementation Guide | Publish formal WHO Implementation Guide (IG) with BPMN | Roy Munge, Carl Leitner | P1 | 2026-11-06 | In Progress | Formal IG on WHO GitHub repository specifying data models, terminology value sets, and clinical workflow diagrams. |
| **TECH-10** | Technical | Audit & Consent | Configure FHIR AuditEvent & Privacy Consent Framework | Roy Munge, Carl Leitner | P2 | 2026-11-12 | Not Started | OHS Info Gateway telemetry logging access events and family consent records for cross-border data requests. |
| **TECH-11** | Technical | Day 1 Code Labs | Assemble Day 1 "Partially Assembled Lego Kit" code labs | Fred Hersch, Roy Munge | P0 | 2026-11-14 | Not Started | Pre-packaged modules: FHIR foundations, Folio LLM schema mapping, StructureMap templates, and validation exercises. |
| **TECH-12** | Technical | Day 2 Practicum | Configure Day 2 interoperability stations & test scripts | Roy Munge, Carl Leitner | P1 | 2026-11-18 | Not Started | Stations 1–3 run-of-show (source-to-FHIR, use & update, test & exchange) plus optional WHO-ITB ICVP test harness. |
| **TECH-13** | Technical | Rehearsal | Execute full end-to-end technical rehearsal | Roy Munge, Fred Hersch, Carl Leitner | P0 | 2026-11-25 | Not Started | Dry run of complete pipeline including offline fallbacks, failure recovery, station handoffs, and live demonstration. |
| **POL-01** | Policy | Curriculum | Finalize Policy & Decision-Maker track detailed agenda | Diana Wijayanti, Garrett Mehl | P0 | 2026-10-25 | In Progress | Structured sessions on cross-border data-sharing agreements, DPI-H reference architectures, and connectathon labs. |
| **POL-02** | Policy | Keynote Framing | Confirm high-level speakers (HL7 President Rachel Dunc) | Mark Landry, Diana Wijayanti | P1 | 2026-10-24 | In Progress | Formal invitations to HL7 leadership and CSIRO regional capacity representatives for Day 1 opening perspective. |
| **POL-03** | Policy | Country Outreach | Lock country delegations & interoperability lab teams | Alvin Marcelo, Mark Landry | P0 | 2026-10-28 | In Progress | Confirmed attendee cohorts from Thailand MoH, Indonesia SATUSEHAT, Malaysia MoH, Laos, and Cambodia. |
| **POL-04** | Policy | Readiness Survey | Deploy participant advance readiness profile survey | Diana Wijayanti, Fred Hersch | P1 | 2026-10-30 | Not Started | Survey assessing attendee FHIR/API experience, preferred languages, and device limits to set lab scaffolding ratios. |
| **POL-05** | Policy | Trust Governance | Draft cross-border trust framework briefing paper | Carl Leitner, Garrett Mehl | P1 | 2026-11-10 | Not Started | Policy briefing detailing GDHCN trust list governance, bilateral data agreements, and unmapped vaccine code policies. |
| **POL-06** | Policy | Country Showcases | Lock partner country showcase slots (Malaysia IPS demo) | Alvin Marcelo, Diana Wijayanti | P1 | 2026-11-12 | Not Started | Scheduled live presentations of operating national FHIR registries and cross-border IPS patient summary exchanges. |
| **POL-07** | Policy | Summit Handoff | Draft policy recommendations for ASEAN ministerial dialogue | Mark Landry, Garrett Mehl | P1 | 2026-11-20 | Not Started | Policy brief synthesizing workshop evidence and lab commitments for presentation at the main GDHF summit. |
| **JOINT-01** | Joint | Governance | Maintain weekly multi-stakeholder workshop syncs | Carl Leitner, Fred Hersch, Diana Wijayanti | P0 | 2026-10-21 | Done | Recurring Wednesday syncs established (WHO, OHS-SF, Nawi, AeHIN, regional partners); next meeting Oct 21 at 13:00 CEST. |
| **JOINT-02** | Joint | Plenary Framing | Design Day 1 Opening Plenary & joint storyline framing | Fred Hersch, Carl Leitner | P1 | 2026-11-08 | Not Started | Joint session grounding technical and policy cohorts in the shared cross-border patient vignette before breakout tracks. |
| **JOINT-03** | Joint | Daily Synthesis | Structure Day 1 synthesis & shared evidence review | Fred Hersch, Diana Wijayanti | P1 | 2026-11-15 | Not Started | Joint 16:15–17:00 checkpoint where technical teams present mappings, validation results, and issue logs to planners. |
| **JOINT-04** | Joint | Grand Demo | Direct Day 2 connected end-to-end demonstration | Roy Munge, Carl Leitner, Fred Hersch | P0 | 2026-11-22 | Not Started | Integrated live demonstration moving from community referral to clinic GDHCN verification and cross-border travel. |

## 3. Critical Path Milestones & Phase Schedule

| Phase & Milestone | Target Window | Key Activities & Deliverables | Primary Exit Criteria |
| :--- | :--- | :--- | :--- |
| **Phase 1: Architecture & Scoping** | Oct 9 – Oct 23 | Align technical journeys (J1–J4.1); transcode KMP QR validator; seed single-vaccine IPS test data. | Signed vignette script; working KMP extraction prototype; test payloads available on GitHub. |
| **Phase 2: Core Asset Development** | Oct 24 – Nov 6 | Build offline CHW Android app; deploy clinic EMR verifier; publish formal WHO IG; deploy participant readiness survey. | CHW app reads QR metadata offline; clinic app verifies GDHCN signatures; readiness survey closed. |
| **Phase 3: Integration & Testbed** | Nov 7 – Nov 20 | Deploy mock VHL issuer & OpenFn packaging; build "One Family, One Phone" wallet; package Day 1 code labs; draft policy briefs. | Family wallet resolves multi-member VHLs; Day 1 lab repos verified clean; policy briefs approved. |
| **Phase 4: Rehearsal & Scaffolding** | Nov 21 – Nov 27 | Conduct full technical dry run with failure injection; pre-provision participant endpoints and local caches. | Successful end-to-end rehearsal; offline fallback USB/local images validated. |
| **Phase 5: Workshop Delivery** | Nov 28 – Dec 1 | Deliver Day 1 (Foundations & Mapping) and Day 2 (Interoperability Practicum & Plenary Demo); compile issue log. | Working multi-station demo executed; policy findings delivered to GDHF ministerial session. |

## 4. Technical Architecture & Key Design Decisions (OHS-SF)

| Component Layer | Architectural Choice & Implementation Path | Strategic Rationale & Operational De-Risking |
| :--- | :--- | :--- |
| **Issuance Workflow** | Simulated issuance via pre-recorded video and pre-printed sample QR cards. | Eliminates live printer hardware jams, badge-maker networking errors, and complex UI data-entry delays on site. |
| **QR Code Payload** | Self-contained single-vaccine IPS payload embedded directly inside the QR code. | Eliminates runtime external URL lookups and dependency on live foreign national registries during the demo. |
| **Crypto Verification** | Unified Kotlin Multiplatform (KMP) library transcoded from Python REST validator. | Single shared codebase supports native Android (CHW app / tablet EMR) and web client verification without server round-trips. |
| **VHL Issuance & Hosting** | Lightweight mock Verifiable Health Link (VHL) issuer on GCP/ITB using OpenFn. | Avoids heavy Docker infrastructure and orchestrator overhead; provides lightweight packaging of FHIR bundles. |
| **Family Travel Modeling** | Three independent QR codes, VHLs, and IPS records (father, mother, infant) on a single device. | Reflects realistic multi-person border clearance while demonstrating "One Family, One Phone" household device sharing. |
| **Frontline CHW Scope** | Lightweight QR scan to extract unverified vaccine metadata; clinic referral creation. | Focuses CHWs on community recording and linkage to care; reserves formal cryptographic trust verification for clinic EMR. |
| **Code Lab Format** | "Partially assembled Lego kit" exercises (steps 3, 7, 11) with recorded final assemblies. | Prevents Gradle dependency download stalls, CPU compilation bottlenecks, and out-of-memory errors seen in Kigali. |

## 5. Policy & Governance Architecture (WHO)

| Policy Domain | Focus Areas & Discussion Questions | Targeted Policy Output / Artifact |
| :--- | :--- | :--- |
| **Cross-Border Trust** | How do ministries establish bilateral recognition for routine immunization certificates outside the IHR Yellow Card? | Briefing on GDHCN trust list onboarding and bilateral health data exchange frameworks. |
| **Terminology Discrepancies** | When Country A codes Hep B differently from Country B, who resolves mapping conflicts at the border? | Regional governance charter for unmapped domestic vaccine code reconciliation committees. |
| **Consent & Privacy** | What legal frameworks govern parent/guardian consent when sharing dependent records internationally? | Implementation guidance on FHIR Privacy Consent Framework (PCF) and AuditEvent logging. |
| **DPI-H Architecture** | How do open digital public goods (Open Health Stack, OpenMRS, OpenFn) prevent vendor lock-in? | Reference architecture brief mapping national digital health platforms to DPI-H building blocks. |
| **Regional Capacity** | How can interoperability labs in Thailand, Indonesia, and Malaysia maintain sustained connectathon capacity? | Multi-country interoperability capacity roadmap presented at the main GDHF conference. |

## 6. Tracker Modality Recommendation & Tooling Architecture

To address the project management needs across OHS-SF (Roy, Fred) and WHO (Carl, Diana, Alvin), three primary tracker modalities were evaluated:

| Modality | Strengths | Limitations | Strategic Fit & Recommendation |
| :--- | :--- | :--- | :--- |
| **Interactive Standalone Web-App (`tracker.html`)** | Instant visual dashboard; interactive status updating; dynamic filtering by track, owner, priority; built-in CSV/JSON export; zero server dependency; works offline. | State stored locally in browser `localStorage` unless exported/committed to repo. | **Primary Recommended Tool for Leads.** Built and delivered directly in the workspace (`scratch/tracker.html`). |
| **Collaborative Google Sheet** | Real-time multi-user simultaneous editing; familiar to non-technical MoH and WHO policy leads; built-in comment threads. | Can become disorganized without strict column validation; lacks automated visual sprint velocity KPIs. | **Recommended Secondary Tool for Multi-Stakeholder Syncs.** Can be instantly populated using the Web-App CSV export. |
| **Buganizer / GitHub Project Board** | Deep issue tracking; code commit linkages; institutional task auditing (e.g. Buganizer Component 2042386). | High overhead for senior policy stakeholders who lack Google corporate or GitHub access. | **Recommended for Technical Sub-Task Execution.** Use for daily engineering tracking by OHS-SF and Nawi teams. |

### Delivered Interactive Web Application (`tracker.html`)

A complete, self-contained interactive web application has been authored and placed in the project scratch space:
- **File Location:** `file:///usr/local/google/home/fredhersch/.gemini/jetski/brain/b65a503c-70f0-4ae6-8ab5-08d31db3e45f/scratch/tracker.html`
- **Features Included:**
  1. **Executive KPI Dashboard:** Real-time completion percentage, status breakdown bar (Done, In Progress, Blocked, Not Started), and track-specific counters.
  2. **Track-Specific Tabs:** Instant toggling between All Tracks, Technical Track (OHS-SF & WHO Tech Lead), Policy Track (WHO), and Joint & Plenary.
  3. **Multi-Dimensional Filtering:** Real-time search by keyword, status, priority (P0/P1/P2), and task owner.
  4. **Dynamic Item Management:** Modal forms to add new plan items, edit existing tasks, inline status dropdowns, and item deletion.
  5. **Persistence & Data Interoperability:** Automatic persistence via browser `localStorage`, one-click **Export to CSV** (for immediate Google Sheets import), **Export to JSON**, and factory reset.
- **How to Launch:** Open `scratch/tracker.html` directly in any web browser, or serve locally with `python3 -m http.server 8080 --directory .../scratch/`.

## 7. Open Questions to Resolve on Next Call (Wednesday, Oct 21)

The following three architectural and curriculum open questions are slated for resolution during the upcoming WHO / OHS-SF coordination call on Wednesday, October 21 at 13:00 CEST / 19:00 SGT:

***Open Question 1 (Curriculum Structure):*** *Should the clinical vignette run compactly on Day 2 following Day 1 foundations, or be introduced in the Day 1 opening plenary to anchor every subsequent lab and policy discussion? (Recommendation: Frame in Day 1 Opening, unpack during Day 1 afternoon, and execute end-to-end on Day 2).*

***Open Question 2 (Edge Verification Boundary):*** *Should the CHW mobile application perform offline GDHCN digital signature verification directly in the household, or extract unverified metadata to create a clinic verification referral? (Recommendation: Follow the Oct 16 consensus—extract metadata and refer to clinic, keeping the CHW flow lightweight).*

***Open Question 3 (Day 2 Station Facilitation):*** *Which regional partner lead will facilitate the Day 2 ICVP/GITB test station if country teams request yellow card testing? (Recommendation: Carl Leitner to lead with Jose Costa Teixeira providing testbed support).*

## 8. Immediate Action Items

1. **Circulate Tracker to Co-Leads**: Share `tracker.html` and the CSV export with Roy Munge (OHS-SF) and Carl Leitner / Diana Wijayanti (WHO) ahead of the Wednesday sync.
2. **Convene Weekly Coordination Sync**: Host the next workshop planning sync on Wednesday, October 21 at 13:00 CEST / 19:00 SGT, onboarding Alvin Marcelo and Mark Landry.
3. **Review Single-Vaccine IPS Test Data**: Validate Ritika Rawlani's single-vaccine IPS payload on Monday, October 20, confirming compatibility with the baby vaccination storyline.
4. **Inspect KMP QR Validator Library**: Review Carl Leitner and Jose Costa Teixeira's Kotlin Multiplatform library build by Wednesday, October 23, for integration into Roy Munge's Android demo app.
5. **Resolve Day 1 & Day 2 Open Questions**: Table Open Questions 1–3 at the start of the Wednesday sync to lock down run-of-show and station owners.
