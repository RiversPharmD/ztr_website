## Project Scope & Working Agreement

This document is a **living scope and working agreement** between Zach (you) and the AI assistant (me) for the `ztr_website` project. It is versioned in git so we can see how our understanding and ambitions evolve over time.

---

### 1. Project purpose

The purpose of this project is to build and maintain a **polished personal website** that:

- Presents your work, thinking, and publications clearly to **employers, clients, and peers**.
- Serves as a **home base** for projects, long-form writing, and a curated bibliography.
- Is simple to operate, easy to extend, and pleasant to read in both light and dark modes.

The site is built with **Quarto** and deployed as a static site (currently via GitHub Pages and CI).

---

### 2. Goals for this phase (next ~2–3 months)

- **Narrative & credibility**
  - Make it immediately clear who you are, what you do, and what you are good at.
  - Highlight a small number of **projects**, **posts**, and **publications** that best represent you.

- **UX & visual design**
  - Achieve a consistent, professional look (typography, spacing, layout).
  - Implement and test **dark mode** support.

- **Features & information architecture**
  - Implement **dynamic listings** for recent posts and featured projects.
  - Establish a small, durable set of **categories/tags**.
  - Enable **RSS** and **basic search** so people can find and follow your work.

- **Deployment & workflows**
  - Make local dev (`quarto preview`) and CI/CD predictable and documented.
  - Clarify the relationship between `output-dir`, `publish-dir`, and the deployed site.

- **Shared memory**
  - Use this `scope.md` and a persistent project log in the repo root as the main coordination artifacts.

For a more detailed, tactical breakdown, see the plan file under `.cursor/plans/` (created by the AI assistant).

---

### 3. In-scope vs out-of-scope

**In scope (this phase):**

- Rewriting and expanding content on `index.qmd`, `about.qmd`, `projects.qmd`, and several additional posts/projects using the existing templates.
- Iterating on design within **Quarto + CSS** (no heavy JS frameworks).
- Implementing Quarto-native features:
  - Listings for posts and projects.
  - Categories/tags.
  - RSS and built-in search.
  - Improved citation usage and bibliography surfacing.
- Clarifying and simplifying deployment configuration and documenting common workflows in `README.md`.
- Maintaining `scope.md` and the project log as part of the normal workflow.

**Out of scope (this phase):**

- Building a custom SPA or migrating to a different framework (Next.js, Astro, etc.).
- Implementing complex backend features (user accounts, custom comment engines you host, etc.).
- Large design system work (component library, design tokens, etc.) beyond what Quarto + CSS comfortably support.

These can be revisited in a future phase if desired.

---

### 4. Roles & responsibilities (you vs AI)

**You (Zach):**

- Own the **substance**:
  - Decide which projects, posts, and publications to highlight.
  - Draft and revise narrative content (About, case studies, posts).
  - Make final calls on positioning, tone, and audience priorities.
- Review and approve meaningful changes to:
  - This `scope.md`.
  - Site-wide navigation and information architecture.
  - Visual identity (theme choices, major layout patterns).

**AI assistant:**

- Own the **scaffolding and implementation details**, within this scope:
  - Propose concrete content structures, starter copy, and refactors.
  - Implement Quarto features (listings, taxonomy, search, RSS, dark mode, CI tweaks).
  - Keep the persistent project log updated once per working session with:
    - What changed.
    - Key learnings.
    - Open questions or suggested next steps.
- Proactively suggest edits to `scope.md` when scope or priorities clearly shift.

Both of us share responsibility for keeping the repo in a healthy state (lint-free, builds passing, docs not obviously stale).

---

### 5. How scope changes

This document is **intentionally light-weight**. Scope is allowed to evolve as we learn more.

- **Changes happen via git**:
  - Any meaningful shift in goals, constraints, or responsibilities should be captured as an edit to `scope.md` in a commit/PR.
  - Short explanatory notes in commit messages or the project log are encouraged when scope changes.
- **The latest `main` version of `scope.md` is the source of truth**:
  - If other docs (e.g., the plan file or README) disagree with this file, `scope.md` wins and the others should be brought back into alignment.
- **No heavy process**:
  - Either of us can propose edits; you retain final say on direction and scope.

---

### 6. How the project log fits in

There is a separate, persistent markdown file in the repo root (working name: `project-journal.md`) that serves as:

- A **chronological log** of what happened in each working session.
- A place to record **decisions, experiments, and learnings** about how to view and evolve this project.

You can think of `scope.md` as the **current contract/charter**, and `project-journal.md` as the **lab notebook** that explains how we got here.

