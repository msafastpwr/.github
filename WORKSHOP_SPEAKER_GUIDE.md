# Technical Speaker & Workshop Instructor Handbook

**Microsoft Student Ambassadors — FAST-NUCES Peshawar**  
*Pedagogical Framework, Lab Architecture, & Delivery Standards for Technical Sessions*

---

## 🎯 Purpose & Philosophy

At **MSA FAST Peshawar**, our workshops are not passive lectures. We believe that **students learn best when their hands are on the keyboard, building functional software, and deploying to the cloud**.

Whether you are an internal student lead, an alumni engineering mentor, or an invited Microsoft MVP, this handbook outlines our pedagogical standards, slide deck requirements, lab repository structures, and live delivery techniques to ensure an exceptional experience for every participant.

---

## ⚖️ The 30/70 Principle: Concept vs. Code

Every technical session conducted under the MSA banner must adhere to the **30/70 rule**:

```
┌────────────────────────────────────────┬────────────────────────────────────────────────────────────────────────┐
│     30% Conceptual Architecture        │                      70% Hands-On Building & Labs                      │
│ (Problem context, system diagrams, why)│          (Live coding, terminal execution, cloud deployment, Q&A)      │
└────────────────────────────────────────┴────────────────────────────────────────────────────────────────────────┘
```

- **Avoid the "Slide Marathon":** Never spend more than 15–20 continuous minutes on conceptual slides before opening an IDE, terminal, or cloud console.
- **Problem-First Framing:** Introduce every concept by demonstrating the concrete problem it solves before introducing the syntax.

---

## 📊 Presentation Deck Standards

All workshop decks must uphold our visual identity as specified in [`BRAND_GUIDELINES.md`](BRAND_GUIDELINES.md):

### 1. Slide Format & Aspect Ratio
- **Widescreen 16:9 (`1920 x 1080 px`):** Standard for all FAST campus projectors and video recording monitors.
- **Branded Master Template:** Utilize the official MSA FAST Peshawar slide template (featuring official logo lockups, Segoe UI / Inter typography, and clean dark/light themes).

### 2. Slide Content Rules
- **Minimum Font Sizes:**
  - Slide Titles: **36pt – 44pt**
  - Section Headers: **28pt – 32pt**
  - Body Text & Bullet Points: **20pt – 24pt** (Strictly avoid font sizes below 18pt)
- **Code on Slides:**
  - Never display unformatted, screenshot-based code snippets.
  - Use high-contrast syntax highlighting (e.g., VS Code Dark+ theme).
  - Limit code snippets on a single slide to **maximum 8–10 lines**. Highlight only the critical lines under discussion.
- **Mandatory Slide Structure:**
  1. **Title Slide:** Workshop Title, Speaker Name, Title, and Date.
  2. **Learning Objectives:** Bulleted outcomes (*"By the end of this session, you will deploy..."*).
  3. **Architecture / Concept Flow:** High-level diagram showing how pieces fit together.
  4. **The Live Build:** Guided hands-on implementation.
  5. **Troubleshooting & Gotchas:** Common pitfalls beginners encounter.
  6. **Where to Go Next:** Direct links to **Microsoft Learn** modules, documentation, and certifications.
  7. **Q&A & Connect:** Speaker LinkedIn/GitHub and chapter links.

---

## 💻 Workshop Repository Architecture

Every technical session must have a companion open-source repository published under the **`github.com/msafastpwr`** organization at least **48 hours prior** to the event:

### Standard Repository Layout

```
msafastpwr/workshop-<topic-name>/
├── .devcontainer/               # Optional: Dev container for instant Codespaces launch
│   └── devcontainer.json
├── starter-code/                # Clean starter boilerplate for participants
│   ├── src/
│   ├── package.json / requirements.txt
│   └── .env.example
├── completed-solution/          # Fully functional, working reference implementation
│   ├── src/
│   └── ...
├── docs/
│   ├── SETUP_GUIDE.md           # Step-by-step local machine prerequisite installation
│   └── CHEATSHEET.md            # Quick reference commands and syntax
├── slides/
│   └── presentation.pdf         # Exported slide deck
├── LICENSE                      # MIT License
└── README.md                    # Primary workshop guide
```

### Essential Requirements for `README.md`:
1. **Prerequisites Checklist:** Exact software versions needed (e.g., Node.js v20 LTS, Python 3.11+, Git 2.40+, Azure CLI).
2. **5-Minute Quickstart:** Commands to clone the repo, install dependencies, and run the development server.
3. **Lab Steps with Code Explanations:** Step-by-step numbered walkthrough with expected terminal outputs.
4. **Common Errors & Fixes:** Address campus-specific issues (e.g., university proxy configurations, Windows PATH errors).

---

## ☁️ Cloud Sandboxes & Azure Student Subscriptions

- **Avoid Billing Friction:** Ensure hands-on labs do **not** incur unexpected credit exhaustion for attendees.
- **Leverage Free Tiers & Sandboxes:**
  - Direct students to [Microsoft Learn Interactive Sandboxes](https://learn.microsoft.com/) which provide free, temporary Azure environments requiring zero credit cards.
  - Utilize Azure Free Tier services (e.g., Azure App Service Free F1, Azure Functions Consumption Tier, Azure Cosmos DB Free Tier).
- **GitHub Codespaces:** Whenever possible, enable GitHub Codespaces on the workshop repository so students on low-spec laptops or with permission restrictions on lab PCs can develop directly inside their browser with zero local installation.

---

## 🎙️ Live Delivery & Pedagogical Best Practices

### 1. Terminal & Editor Readability
- **Zoom In:** Press `Ctrl + =` (or `Cmd + =`) in VS Code and terminal windows until the font size is clearly legible from the **back row of the computer lab**. Recommended terminal font size: **18px – 20px**.
- **Clear Terminal Prompts:** Use a clean, distraction-free shell prompt. Run `clear` frequently to keep active commands at the top of the screen where attendees in the back can see them above other heads.

### 2. Live Coding Etiquette
- **Narrate Keystrokes:** Explain *why* you are writing a piece of code before you type it.
- **Embrace and Normalize Errors:** When you encounter a bug or typo during live coding, do not panic! Treat it as a teaching opportunity. Walk the audience through reading the stack trace and diagnosing the fix.
- **Do NOT Copy-Paste Massive Blocks:** Avoid pasting 50 lines of boilerplate from a scratchpad without walking through what each block does.

### 3. Pacing & Checkpoint Signaling
Establish explicit check-in checkpoints throughout the workshop:
> *"Give me a quick thumbs-up if your local server is running on localhost:3000... Great! If your terminal is showing an error, keep your hand raised and our Technical Team TAs will come assist you right now."*

### 4. Roving Teaching Assistants (TAs)
- Before the session, brief the **2–4 Technical Team core members** assigned as roving TAs.
- When an attendee hits a local syntax error, Git conflict, or environment bug, a TA quietly squats beside their desk to resolve it without interrupting the flow of the speaker's presentation.

### 5. Inclusivity & Respectful Communication
- **Eliminate Demeaning Vocabulary:** Strictly avoid words like *"obviously"*, *"simply"*, *"it's trivial"*, or *"just write this"*. What is trivial to an experienced developer can be intimidating to a freshman writing their first function.
- **Validate Questions:** Respond to all student questions with encouragement (*"That's a fantastic question, especially when working with asynchronous code..."*).
- **Gender & Background Inclusivity:** Proactively encourage questions from diverse attendees, ensuring female participants feel equally heard and supported in line with our **Her Tech Wing** ethos.

---

## 📦 Post-Workshop Deliverables Checklist

Within **24 hours** of workshop completion, the speaker must submit to the Technical Lead:
- [ ] Final, validated code committed to the public `msafastpwr` workshop repository.
- [ ] Presentation slides exported to PDF and added to the repository `slides/` directory.
- [ ] Curated list of 3–5 **Microsoft Learn** modules for follow-up study.
- [ ] Brief summary of common questions or hurdles observed during the session to feed into our community FAQ.

---

*Authored by the Technical & Academic Wing • Microsoft Student Ambassadors FAST-NUCES Peshawar*
