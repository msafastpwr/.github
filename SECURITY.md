# Security Policy

The **Microsoft Student Ambassadors (MSA) FAST-NUCES Peshawar** chapter takes the security and integrity of our software repositories, automation tools, student datasets, and web portals seriously.

---

## 🔒 Supported Repositories & Scope

Security updates and active vulnerability monitoring apply to the latest commit on the `main` branch of all active repositories under [`msafastpwr`](https://github.com/msafastpwr), including:

| Repository | Status |
| :--- | :--- |
| `msafastpwr.github.io` | Active |
| `.github` | Active |
| Community tooling & workshop starter kits | Active |

---

## 🚨 Reporting a Vulnerability

If you discover a security vulnerability, sensitive data exposure, or leaked credential within any repository, website, or infrastructure managed by MSA FAST Peshawar, please **do not open a public issue**. Publicly disclosing security flaws puts our community, systems, and user data at risk.

Instead, please report the vulnerability confidentially:

1. **Email:** Send full details to **[msp.pwr@nu.edu.pk](mailto:msp.pwr@nu.edu.pk)**.
2. **Subject Line:** Include `[SECURITY REPORT] <Short Description>` in the subject line.
3. **Report Contents:**
   - Detailed description of the vulnerability.
   - Affected repository, branch, URL, or script.
   - Step-by-step reproduction instructions or Proof-of-Concept (PoC).
   - Potential impact of the issue.
   - Your contact details for coordination and acknowledgment.

We will acknowledge receipt of your report within **48 hours** and provide regular updates on triage and mitigation.

---

## 🛡️ Best Practices for Contributors

To preserve community security, contributors must observe the following rules:

- **Never Commit Secrets:** Do not commit API keys, personal access tokens (PATs), Google Cloud/Azure service account keys, OAuth secrets, database connection strings, or environment files (`.env`).
- **Protect Student Data:** Never commit unanonymized rosters, roll numbers, phone numbers, or academic records.
- **Dependency Hygiene:** Ensure any third-party libraries or CDNs used are verified, pinned, and free from known vulnerabilities.
- **Immediate Invalidation:** If credentials or sensitive student data are accidentally pushed, immediately revoke/rotate the affected credentials and contact the maintainers to purge the commit history.
