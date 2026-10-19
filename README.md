# Pre-GDHF Technical Workshop — Project Plan & Action Tracker

Applied digital immunization workshop governance, work breakdown structure, critical path schedule, and interactive execution tracker for the Pre-GDHF Workshop in Bangkok (November 30 – December 1, 2026).

---

## Overview

The **Pre-GDHF Technical Workshop** is a two-day applied programme on FHIR data modeling, schema mapping, cryptographic trust verification, and interoperability testing, leading directly into the **Global Digital Health Forum (GDHF 2026)**.

The workshop connects high-level digital health policy and trust governance with tangible technical implementation through a shared clinical vignette (routine newborn immunization, frontline referral, clinic verification, and multi-member cross-border travel).

### Leadership & Track Ownership

* **Technical & Implementer Track**:
  * **OHS-SF Lead:** Roy Munge (Nawi Tech)
  * **OHS-SF Co-Lead:** Fred Hersch (OHS-SF / Google DeepMind)
  * **WHO Tech Lead:** Carl Leitner (WHO)
* **Policy & Decision-Maker Track**:
  * **WHO Lead:** Diana Wijayanti (WHO)
  * **WHO Co-Leads:** Garrett Mehl (WHO), Alvin Marcelo (AeHIN), Mark Landry (WHO)
* **Joint Plenary & Grand Demonstration**:
  * **Joint Co-Chairs:** Fred Hersch (OHS-SF), Carl Leitner (WHO)

---

## Features of the Interactive Tracker (`index.html`)

* **Visual KPI Dashboard**: Live tracking of overall progress percentage, progress bar (Done, In Progress, Blocked, Not Started), and track-specific counts.
* **Track Filtering**: Instant tabs for **All Tracks**, **Technical Track (OHS-SF & WHO)**, **Policy Track (WHO)**, and **Joint & Plenary**.
* **Dynamic Search & Multi-Filters**: Filter by Status, Priority (P0, P1, P2), Owner, or free-text search across titles, workstreams, and notes.
* **In-Browser Item Management**: Add new tasks via modal form, edit existing items, or update status dropdowns in real time.
* **Local Persistence**: State automatically persists to browser `localStorage` (`pre_gdhf_workshop_tracker_v2`).
* **Interoperability & Data Portability**: One-click **Export to CSV** (for immediate Google Sheets import) and **Export to JSON** (for backups or programmatic sync).

---

## Quick Start

### 1. View Locally in Browser

Simply open `index.html` directly in your web browser:
```bash
# macOS
open index.html

# Linux
xdg-open index.html
```

Or run a local HTTP server:
```bash
python3 -m http.server 8080
```
Then navigate to `http://localhost:8080/`.

### 2. Host on GitHub Pages (Instant Zero-Config Deployment)

1. Push this repository to GitHub.
2. In your GitHub repository, navigate to **Settings** > **Pages**.
3. Under **Build and deployment** > **Branch**, select `main` and folder `/(root)`, then click **Save**.
4. GitHub Pages will publish the live interactive tracker at:
   `https://<your-username>.github.io/<repo-name>/`

---

## Repository Structure

```text
├── index.html            # Standalone interactive action tracker web application
├── PROJECT_PLAN.md       # Comprehensive master project plan, RACI matrix & schedule
├── tracker_seed.json     # Pre-compiled JSON seed data (24 core tasks)
├── tracker_seed.csv      # Pre-compiled CSV export for Google Sheets / Excel
└── README.md             # Project documentation and deployment guide
```

---

## Primary References

* [Project Plan & RACI Matrix](PROJECT_PLAN.md)
* [WHO Pre-GDHF User Journeys & Technical Requirements](https://docs.google.com/document/d/1x30S9zc93lvHqoh8VkKKGNU31JvXVh85pnaqgIeD47M/edit)
* [Thailand Technologist Workstream Detailed Agenda Slides](https://docs.google.com/presentation/d/157ICNv27xEB80z2SJHi1S5_XT5GEeHrmGD1igOw16DQ/edit)
