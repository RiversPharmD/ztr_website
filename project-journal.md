## Project Journal

This file is a **persistent log** of work on `ztr_website`. It is meant to be:

- A **chronological changelog** of what we did in each working session.
- A **lab notebook** for decisions, experiments, and why we chose certain paths.
- A **meta guide** for how to think about the project as it evolves.

Entries are appended over time and kept under version control so we can see how the project and our thinking change.

---

### Entry template (for future sessions)

For each working session, we’ll roughly follow this structure:

```markdown
## YYYY-MM-DD – Short session title

**What we did**
- ...

**Key learnings / decisions**
- ...

**Open questions / next steps**
- ...
```

We don’t have to be rigid, but this format should keep entries short, scannable, and useful.

---

## 2026-03-15 – Rebooting the project and defining scope

**What we did**
- Reviewed the existing Quarto-based site structure, content, and deployment setup.
- Clarified high-level goals for the next 2–3 months:
  - Strengthen narrative and credibility across Home, About, Projects, Blog, and Publications.
  - Improve UX and visual design, including dark mode.
  - Implement dynamic listings, basic taxonomy, RSS, and search.
  - Simplify and document deployment and local dev workflows.
- Agreed to treat this repo as the **source of truth** for both content and process, including AI collaboration.
- Created two root-level artifacts:
  - `scope.md` – a living scope and working agreement.
  - `project-journal.md` – this persistent journal.

**Key learnings / decisions**
- The site already has strong building blocks (bibliography, a detailed personal-website project page, and a long-form blog post), but many top-level pages are still scaffolds.
- We want an **aggressive** 2–3 month scope and are willing to invest in substantial new writing/content.
- The audience is mixed (employers, clients, peers), so we will optimize for **general credibility** rather than a single narrow persona.
- We will use `scope.md` and this journal as **primary coordination tools** to reduce the context the AI needs to hold in its head and to make intent and history inspectable.

**Open questions / next steps**
- Refine the exact positioning and tone for the homepage and About page (e.g., which domains to emphasize first).
- Decide which additional projects and posts should be prioritized for new case studies and blog entries.
- Implement the first wave of changes outlined in the current high-level plan:
  - Rewrite `index.qmd`, `about.qmd`, and `projects.qmd` with real content.
  - Set up basic listings for posts and projects.
  - Begin UX and visual refinements and introduce dark mode.

---

## 2026-03-15 – Establishing design principles

**What we did**
- Added a global Cursor rule at `.cursor/rules/website-design.mdc` to capture website and blog design principles.
- Encoded a hybrid **academic × notebook** design tone: serious, structured, and citation-friendly, but still personal and human.
- Documented accessibility and readability expectations (strong contrast, semantic structure, comfortable typography) and Quarto/CSS conventions.

**Key learnings / decisions**
- We want design decisions to be **explicit and reusable**, so future changes to Quarto pages and `styles.css` can follow the same principles without re-deriving them.
- Design will be guided by three core ideas:
  - Content-first and calm.
  - Academic enough to signal scientific rigor.
  - Personal enough to show who you are beyond your CV.
- Accessibility is important but we will aim for **strong, practical standards** rather than perfectionism.

**Open questions / next steps**
- As we iterate on `index.qmd`, `about.qmd`, and `projects.qmd`, we may refine these principles and update the rule file.
- We still need to make concrete theme and typography choices (e.g., final font stack, exact heading sizes) within these high-level guidelines.

