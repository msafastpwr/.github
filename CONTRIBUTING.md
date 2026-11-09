# Contributing to MSA FAST-NUCES Peshawar

First off, thank you for considering contributing to **Microsoft Student Ambassadors (MSA) FAST-NUCES Peshawar**! 🎉

Whether you're fixing a typo in documentation, building a feature for our website, submitting a lab exercise for an upcoming workshop, or sharing learning materials, your contributions help empower the entire student developer community.

---

## 📜 Code of Conduct

All contributors and participants are expected to adhere to our [Code of Conduct](CODE_OF_CONDUCT.md). Please read it to understand our community standards and expectations.

---

## 🚀 How Can I Contribute?

### 1. Reporting Bugs & Issues
- Before opening a new issue, check existing open issues to avoid duplicates.
- Use our structured [Bug Report Template](.github/ISSUE_TEMPLATE/bug_report.yml) to provide detailed reproduction steps, browser/OS environment, and screenshots if applicable.

### 2. Suggesting Features & Enhancements
- Have an idea for the chapter portal, an automation script, or a workshop topic?
- Submit a proposal using our [Feature Request Template](.github/ISSUE_TEMPLATE/feature_request.yml) or [Workshop Request Template](.github/ISSUE_TEMPLATE/workshop_request.yml).

### 3. Submitting Code or Documentation
- Look for issues labeled `good first issue` or `help wanted`.
- Comment on the issue to let others know you are working on it.

---

## 🔄 Development Workflow

Follow this standard Git workflow for all repositories under `msafastpwr`:

### 1. Fork or Clone
Clone the repository to your local machine:
```bash
git clone https://github.com/msafastpwr/<repository-name>.git
cd <repository-name>
```

### 2. Create a Feature Branch
Create a descriptive branch off `main`:
```bash
# For a new feature:
git checkout -b feature/event-countdown-timer

# For a bug fix:
git checkout -b fix/mobile-navbar-overflow

# For documentation:
git checkout -b docs/update-workshop-readme
```

### 3. Make Your Changes
- Keep changes focused and atomic.
- Respect existing styling and architecture (e.g., in `msafastpwr.github.io`, adhere to the vanilla architecture, avoiding external heavy dependencies or modifying shared locked base files without lead consensus).
- Ensure code is well-commented and clean.

### 4. Commit Your Work
We recommend following the [Conventional Commits](https://www.conventionalcommits.org/) specification:
- `feat: add upcoming workshop preview to home page`
- `fix: resolve responsive alignment issue in footer on mobile`
- `docs: add instructions for running the email script locally`
- `style: format css according to style guide`
- `chore: update organization links and badges`

### 5. Submit a Pull Request
1. Push your branch to GitHub.
2. Open a Pull Request targeting the `main` branch.
3. Fill out the [Pull Request Template](.github/PULL_REQUEST_TEMPLATE.md) completely, referencing any related issue (e.g., `Closes #12`).
4. Wait for maintainer feedback and reviews. Maintainers may request tweaks before approval.

---

## 🧪 Quality & Standards Checklist

Before submitting a Pull Request, please ensure:
- [ ] Code runs without errors or console warnings.
- [ ] Responsive design has been tested across mobile, tablet, and desktop viewports.
- [ ] Accessibility standards are respected (meaningful `alt` text for images, semantic HTML elements).
- [ ] Sensitive secrets (API keys, personal student contact info, passwords) are **never** committed to version control.

---

## 🌟 Thank You!

Every contribution—big or small—makes a real impact on our campus community. Happy coding!
