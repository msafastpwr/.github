# `.github` — Central Organization Governance & Community Health

**Microsoft Student Ambassadors — FAST-NUCES Peshawar**  
*The central governance, policy documentation, and community standard repository for the [`msafastpwr`](https://github.com/msafastpwr) organization.*

---

## 🏛️ Repository Overview & Purpose

This repository serves two foundational purposes across **`github.com/msafastpwr`**:

1. **Organization-Wide Community Health Defaults:** GitHub automatically inherits default files (`CODE_OF_CONDUCT.md`, `CONTRIBUTING.md`, `SECURITY.md`, `SUPPORT.md`, `LICENSE`, and issue/PR templates) defined here across **all** current and future repositories within the `msafastpwr` organization.
2. **Master Organizational Documentation Hub:** Houses the complete constitutional, operational, brand, and engineering standards governing all executive officers, department leads, and student ambassadors.
3. **Public Organization Profile:** Contains the profile header artwork and landing page markdown rendered publicly at [github.com/msafastpwr](https://github.com/msafastpwr).

---

## 📚 Organization Documentation Suite

Click on any document below to view the full policy, playbook, or guidelines:

```
                                  ┌──────────────────────────────────────────────┐
                                  │      msafastpwr Master Documentation         │
                                  └──────────────────────┬───────────────────────┘
                                                         │
         ┌────────────────────────┬──────────────────────┼──────────────────────┬────────────────────────┐
         │                        │                      │                      │                        │
         ▼                        ▼                      ▼                      ▼                        ▼
┌──────────────────┐    ┌──────────────────┐   ┌──────────────────┐   ┌──────────────────┐     ┌──────────────────┐
│  Governance &    │    │  Operations &    │   │  Engineering &   │   │  Brand & Media   │     │  Community &     │
│  Constitution    │    │  Campus SOPs     │   │  Code Standards  │   │  Visual Identity │     │  Health Files    │
└──────────────────┘    └──────────────────┘   └──────────────────┘   └──────────────────┘     └──────────────────┘
```

### 1. 🏛️ Governance, Strategy & People
- **[GOVERNANCE.md](GOVERNANCE.md):** The Supreme Chapter Constitution. Details mission, organizational chart, executive mandates, voting protocols, attendance rules, and succession lifecycles.
- **[ONBOARDING.md](ONBOARDING.md):** Comprehensive 30-Day Onboarding Handbook for newly inducted core members, covering account setups, Microsoft Learn profiles, Azure for Students, and department tracks.
- **[ROADMAP.md](ROADMAP.md):** Annual Strategic Roadmap and Objectives & Key Results (OKRs) spanning Fall 2026 through Summer 2027.
- **[COMMUNITY_ROSTER.md](COMMUNITY_ROSTER.md):** Complete official leadership directory for the 2026–2027 tenure (Executive Body, Technical Team, Her Tech Wing, Media, Events, Outreach, and Graphics).
- **[HER_TECH_WING_CHARTER.md](HER_TECH_WING_CHARTER.md):** Dedicated charter for the **Her Tech Wing**, defining initiatives, study circles, and safe-space protections for female engineers at FAST Peshawar.

### 2. 🎪 Campus Operations & External Relations
- **[EVENT_MANAGEMENT_SOP.md](EVENT_MANAGEMENT_SOP.md):** 5-Phase Standard Operating Procedure for organizing workshops, bootcamps, and hackathons on the FAST-NUCES Peshawar campus.
- **[COMMUNICATION_POLICY.md](COMMUNICATION_POLICY.md):** Communication Channel Matrix, spokesperson protocols, and standardized email templates for administration room bookings, corporate sponsorships, and speaker invites.
- **[WORKSHOP_SPEAKER_GUIDE.md](WORKSHOP_SPEAKER_GUIDE.md):** Pedagogical standards, slide deck templates, the 30/70 hands-on rule, and lab repository architectures for workshop conductors.

### 3. 💻 Engineering & Software Standards
- **[PROJECT_LIFECYCLE.md](PROJECT_LIFECYCLE.md):** The 7-Stage Software Engineering Lifecycle governing all repositories (RFC, tech stack standards, branch protection, Conventional Commits, and Dual-Lead review).
- **[CONTRIBUTING.md](CONTRIBUTING.md):** Universal contributor guidelines detailing fork-and-PR workflows, local Live Server preview setup, and code quality expectations.
- **[SECURITY.md](SECURITY.md):** Vulnerability disclosure policy, credential leak protocols, and secret management standards.

### 4. 🎨 Brand Identity & Community Health
- **[BRAND_GUIDELINES.md](BRAND_GUIDELINES.md):** Visual Identity Standards, approved color palettes (Microsoft Blue `#0078D4`, Accent Cyan, Red, Green, Yellow), Segoe UI / Inter typography, and social media asset dimensions.
- **[CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md):** Community standards and graduated enforcement ladder adapted from Contributor Covenant v2.1.
- **[SUPPORT.md](SUPPORT.md):** Directory of community help desks, WhatsApp channels, Discord servers, and executive escalation contacts.
- **[LICENSE](LICENSE):** Standard MIT Open Source License.

---

## 🗂️ File Directory Structure

```
.github/
├── profile/
│   ├── README.md                 # Public profile rendered on github.com/msafastpwr
│   └── Banner_MSA.jpeg           # Official chapter banner graphic
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.yml        # Structured bug report issue form
│   │   ├── feature_request.yml   # Feature proposal issue form
│   │   ├── workshop_request.yml  # Community workshop topic request form
│   │   ├── project_proposal.yml  # Open-source project proposal form
│   │   └── config.yml            # Community support links and template chooser
│   └── PULL_REQUEST_TEMPLATE.md  # Standard pull request checklist & verification
│
├── BRAND_GUIDELINES.md           # Visual identity, colors, typography, asset specs
├── CODE_OF_CONDUCT.md            # Contributor Covenant v2.1 community health standard
├── COMMUNICATION_POLICY.md       # Comms matrix, spokesperson rules, official email templates
├── COMMUNITY_ROSTER.md           # 2026–2027 Executive Body & Department Directory
├── CONTRIBUTING.md               # Universal organization-wide contributing guidelines
├── EVENT_MANAGEMENT_SOP.md       # Campus event operations SOP & administration checklists
├── GOVERNANCE.md                 # Supreme Constitution & Organizational Bylaws
├── HER_TECH_WING_CHARTER.md      # Women in Tech inclusion charter & program framework
├── LICENSE                       # MIT Open Source License
├── ONBOARDING.md                 # 30-Day New Member Onboarding Handbook
├── PROJECT_LIFECYCLE.md          # Software development lifecycle & engineering standards
├── README.md                     # Central documentation index (this file)
├── ROADMAP.md                    # Annual Strategic Roadmap & OKRs (2026–2027)
├── SECURITY.md                   # Vulnerability disclosure & secret management policy
├── SUPPORT.md                    # Community support channels & escalation directory
└── WORKSHOP_SPEAKER_GUIDE.md     # Instructor guide, 30/70 rule, and lab repository layout
```

---

## ⚙️ Maintenance & Pull Request Workflow

1. Any changes to constitutional policies, brand guidelines, or community templates must be submitted via a Pull Request to this repository.
2. Major modifications to [`GOVERNANCE.md`](GOVERNANCE.md) or [`HER_TECH_WING_CHARTER.md`](HER_TECH_WING_CHARTER.md) require formal approval from the Executive Council and written concurrence of **Faculty Advisor Sir Samin Ahmed**.
3. All PRs must adhere to our [Conventional Commits](https://www.conventionalcommits.org/) standards.

---

## 🔗 Official Organization Channels

| Channel | Destination |
| :--- | :--- |
| 🌐 **Official Website** | [msafastpwr.github.io](https://msafastpwr.github.io) |
| 💼 **LinkedIn** | [linkedin.com/company/msafastpwr](https://www.linkedin.com/company/msafastpwr/) |
| 📸 **Instagram** | [@msafastpwr](https://www.instagram.com/msafastpwr/) |
| 💬 **WhatsApp Community** | [Join Community Group](https://chat.whatsapp.com/LoL1SKxYWUQ97wsRcZ0qcW) |
| 🔗 **Linktree** | [linktr.ee/msafastpwr](https://linktr.ee/msafastpwr) |
| ✉️ **Official Email** | [msp.pwr@nu.edu.pk](mailto:msp.pwr@nu.edu.pk) |
| 📍 **Campus** | FAST-NUCES Peshawar, Industrial Estate, Hayatabad, Peshawar, Pakistan |

---

<div align="center">
<sub>Microsoft Student Ambassadors · FAST-NUCES Peshawar Chapter</sub><br/>
<b>Learn together. Build together. Make an impact.</b>
</div>
