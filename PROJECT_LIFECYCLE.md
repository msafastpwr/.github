# Software Engineering & Project Governance Lifecycle

**Microsoft Student Ambassadors — FAST-NUCES Peshawar**  
*Standards for Code Quality, Architecture, Git Workflows, and Repository Maintenance*

---

## 🏗️ Philosophy & Engineering Principles

Every piece of software built under the **`github.com/msafastpwr`** umbrella is a reflection of the technical standards of FAST-NUCES Peshawar. We treat our open-source tools, chapter web portals, bots, and workshop repos with the same discipline and rigor expected in world-class software engineering organizations.

Our engineering pillars are:
1. **Simplicity over Complexity:** Avoid unnecessary frameworks, bloated dependencies, or complex build tooling where simple, elegant vanilla standards suffice.
2. **Deterministic & Deployable:** Every repository must be deployable with clear, repeatable steps documented in `README.md`.
3. **Security First:** Zero tolerance for credential leaks, hardcoded API secrets, or unvalidated user inputs.
4. **Peer Review & Mutual Accountability:** No engineer—including the President or Tech Lead—merges code directly without peer review.

---

## 🔄 The 7-Stage Project Lifecycle

```
┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│   STAGE 1    │     │   STAGE 2    │     │   STAGE 3    │     │   STAGE 4    │
│ Proposal/RFC │───► │ Architecture │───► │ Scaffolding  │───► │ Sprints & PRs│
└──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
                                                                       │
┌──────────────┐     ┌──────────────┐     ┌──────────────┐             │
│   STAGE 7    │     │   STAGE 6    │     │   STAGE 5    │             │
│ Handover/Ret.│◄─── │ Deployment   │◄─── │ Review Gates │◄────────────┘
└──────────────┘     └──────────────┘     └──────────────┘
```

---

## 1. Stage 1: Project Proposal & RFC (Request for Comments)

Before creating a new GitHub repository under `msafastpwr`:
1. Submit an issue using the [Project Proposal Template](.github/ISSUE_TEMPLATE/project_proposal.yml) or draft a short RFC document.
2. The proposal must detail:
   - **Problem Statement:** What pain point does this tool solve for FAST students, community members, or chapter operations?
   - **Target Users:** Students, event attendees, team leads, or faculty.
   - **Proposed Tech Stack & Hosting Cost:** Justification of tools (must leverage free tiers, Azure Student credits, or GitHub Pages).
   - **Project Maintainers:** Assigned Project Lead and Co-Maintainer responsible for reviewing PRs.
3. Reviewed and approved during the weekly Executive Council sync.

---

## 2. Stage 2: Tech Stack & Architectural Guidelines

We prioritize technologies that offer high longevity, zero vendor lock-in, and minimal maintenance overhead:

| Tier | Preferred Technologies | Acceptable Alternatives | When to Use |
| :--- | :--- | :--- | :--- |
| **Static Portals** | Vanilla HTML5, Modern CSS3 (`theme.css`), Vanilla JS (ES6+) | Astro, Vite | Public information portals, documentation, event landing pages. |
| **Web Applications** | Next.js, React, TypeScript, TailwindCSS | Vue.js, Svelte | Complex stateful apps, registration portals, interactive dashboards. |
| **Backend & APIs** | Node.js (Express), Python (FastAPI) | Azure Functions, Go | Microservices, data pipelines, automation endpoints. |
| **Serverless / Cloud**| **Microsoft Azure** (App Services, Functions, Cosmos DB, Blob Storage) | GitHub Pages, Vercel | Production hosting, scalable backend processing. |
| **Database** | Azure SQL, Cosmos DB (Free Tier), PostgreSQL | Supabase, SQLite | Persistent application state, registration storage. |

---

## 3. Stage 3: Repository Scaffolding & Setup Requirements

Every repository created within the `msafastpwr` organization must include the standard repository skeleton:

```
msafastpwr/<project-name>/
├── .github/
│   ├── workflows/               # Automated CI/CD (lint, test, build, deploy)
│   │   ├── ci.yml
│   │   └── deploy.yml
│   ├── PULL_REQUEST_TEMPLATE.md # Standard PR checklist
│   └── CODEOWNERS               # Mandatory code ownership assignments
├── docs/                        # Architecture decisions, setup guides, API specs
├── src/                         # Production application source code
├── tests/                       # Unit and integration test suites
├── .env.example                 # Template for required environment variables (NO SECRETS)
├── .gitignore                   # Standard gitignore (node_modules, .env, .DS_Store)
├── CONTRIBUTING.md              # Project-specific contribution guide
├── LICENSE                      # MIT License
└── README.md                    # Comprehensive quickstart & documentation
```

### Mandatory GitHub Repository Settings:
- **Default Branch:** Named `main`.
- **Branch Protection on `main`:**
  - Direct pushes forbidden.
  - Require a pull request before merging.
  - **Require at least two (2) approvals** (including designated Leads/CODEOWNERS).
  - Require status checks to pass before merging (CI build, linting).
  - Dismiss stale pull request approvals when new commits are pushed.

---

## 4. Stage 4: Sprints & Git Workflow Standards

### 4.1 Branch Naming Conventions
All branches must follow the strict taxonomy:

```
<type>/<contributor-username>-<short-description>
```

- `feat/` — A new user-facing feature (e.g., `feat/waleeja-team-page-cards`)
- `fix/` — A bug fix (e.g., `fix/mohsin-mobile-nav-toggle`)
- `docs/` — Documentation updates (e.g., `docs/rayyan-api-endpoints`)
- `refactor/` — Code refactoring without changing functionality (e.g., `refactor/subhan-css-tokens`)
- `chore/` — Routine maintenance, dependencies, or config (e.g., `chore/ci-node-upgrade`)

### 4.2 Conventional Commits
Commit messages must follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
<type>(<optional scope>): <imperative description>

[optional body explaining why this change was made]

[optional footer, e.g., Closes #42]
```

**Examples:**
- `feat(events): add dynamic filtering for past and upcoming workshops`
- `fix(theme): correct CSS variable contrast for dark mode button borders`
- `docs(readme): add Live Server setup instructions for freshmen`

---

## 5. Stage 5: Code Review & Quality Gates

Pull Requests are reviewed against four non-negotiable criteria:

### 1. Mobile Responsiveness & Layout Stability
- Must be tested across three breakpoints:
  - Mobile: `375px` – `414px` (iPhone / Android)
  - Tablet: `768px` – `1024px` (iPad)
  - Desktop: `1280px` – `1920px`
- Zero horizontal overflow scrollbars on mobile viewport widths.
- Tap targets for buttons and interactive links must be at least `44 x 44 px`.

### 2. Semantic HTML & Accessibility (a11y)
- Use appropriate semantic landmarks (`<header>`, `<main>`, `<nav>`, `<article>`, `<footer>`).
- Images must include informative `alt` text.
- Heading hierarchy (`<h1>` to `<h6>`) must be sequential; never skip levels for styling purposes.

### 3. Secret & Credential Zero-Tolerance Policy
- Pull requests are automatically scanned for leaked credentials (Azure connection strings, OpenAI keys, private student tokens).
- Leaking a secret in a pull request—even if immediately revoked—requires an immediate Git history rewrite or branch purge.

### 4. Dual-Lead Approval Policy
- For core infrastructure repositories (such as `msafastpwr.github.io`), merges require explicit approval from **both the Technical Lead and Co-Lead**.

---

## 6. Stage 6: Deployment & Monitoring

- **Continuous Deployment (CD):** Merges to `main` must trigger automated GitHub Actions workflows deploying to GitHub Pages or Azure Static Web Apps.
- **Preview Environments:** Pull Requests should ideally generate automated preview deployments (via GitHub Pages branches or Vercel preview URLs) for visual inspection before merging.
- **Uptime & Health Checks:** For backend APIs, establish lightweight uptime pings monitoring health endpoints.

---

## 7. Stage 7: Maintenance, Handover & Archival Policy

### 7.1 Annual Maintainer Handover
- Every May, during the annual leadership transition, all active repositories undergo a **Health Audit**.
- The outgoing maintainers ensure documentation is updated, dependencies are patched, and CODEOWNERS files are transferred to the incoming Technical Lead and Co-Lead.

### 7.2 Deprecation & Archival Protocol
A repository is formally archived when:
1. The project has been superseded by a newer architecture.
2. The event or competition associated with the code has concluded.
- To archive:
  - Add a clear deprecation banner to the top of `README.md` pointing to the replacement repository.
  - Set the GitHub repository state to **Read-Only / Archived**.

---

*Engineered by the Technical Team • Microsoft Student Ambassadors FAST-NUCES Peshawar*
