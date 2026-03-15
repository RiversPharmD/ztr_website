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

---

## 2026-03-15 – Defining success, priorities, and meta-process

**What we did**
- Clarified a concrete \"Definition of Done\" for this 2–3 month phase and added it to `scope.md`.
- Agreed to keep a small, ordered list of **Top 5 near-term priorities** to guide what we work on next.
- Defined a lightweight cadence for reviewing `scope.md` and the rules under `.cursor/rules/`, and for logging changes in this journal.

**Key learnings / decisions**
- Success for this phase is not just \"site exists\" but:
  - Clear, concise homepage positioning.
  - Three strong project case studies and three solid posts.
  - Working dark mode, search, RSS, and dynamic listings.
  - A single, understandable deployment path.
- We will use this journal to:
  - Track not only work on the site, but also **changes to rules and scope**.
  - Capture feedback when agent behavior feels off, so rules can be refined later.
- Meta-reviews (of `scope.md` + rules) will happen roughly every **3–4 active sessions**, not on every tiny change.

**Top 5 near-term priorities (initial draft)**
1. Rewrite `about.qmd` to match the desired positioning (strong scientist, diverse skillset, human and personal).
2. Define and implement a clearer structure for `projects.qmd`, and add at least one more project case study.
3. Implement blog listings and clean up `blog/index.qmd` so it reflects real posts instead of placeholders.
4. Do an initial dark mode and typography pass using `styles.css` and `_quarto.yml` within the current theme.
5. Reconcile `_quarto.yml` `output-dir` / `publish-dir` with the GitHub Pages / CI setup and document the final approach.

**Open questions / next steps**
- Confirm or adjust the Top 5 priorities as we begin working through them.
- Implement subagent rules (`project-core`, content, design, infra) and update this journal when they are added or changed.

---

## 2026-03-15 – Structure, IA, and package alignment

**What we did**
- Aligned site structure with scope: added **Publications** to navbar, updated Home with a short positioning block, surfaced the Personal Website project on the Projects index with two placeholders, replaced manual blog links with a **Quarto listing** and “Categories coming soon.”
- **Quarto config:** Dark mode with `dark: slate`, `light: cosmo`, and `respect-user-color-scheme: true`; explicit navbar search; `site-url` set for RSS; **removed** `publish-dir: docs` (deploy via `gh-pages` branch only); footer set to 2025.
- **Deployment (B3):** Kept `output-dir: _site` for local builds; added `/_site/` to `.gitignore`; documented in README that CI builds and pushes to `gh-pages`.
- **Package/workflow bump:** GitHub Actions checkout@v4, `permissions: contents: write`, `GITHUB_TOKEN` for publish step; R 4.4.0; Quarto pinned to 1.4; README updated with deployment and version notes.

**Key learnings / decisions**
- Best practice for this repo: publish to `gh-pages` branch only; do not use `docs` on `main`.
- Blog index now uses Quarto’s native listing + feed; RSS will be at `blog/index.xml` once `site-url` is correct.

**Open questions / next steps**
- Set `site-url` in `_quarto.yml` to your real GitHub Pages URL (e.g. custom domain) if it differs from `https://zachr.github.io/ztr_website/`.
- Run `quarto preview` and click through all nav items and both themes; add more project case studies and posts per the Top 5.

---

## 2026-03-15 – Sidebar navigation (Option B)

**What we did**
- Switched from **navbar** to **sidebar** navigation in `_quarto.yml`: removed navbar, added a single docked sidebar with Home, About, Projects, Blog, Publications; search lives in the sidebar; `background: light`, `border: false`.
- Added **minimal sidebar CSS** in `styles.css`: light translucent background, thin right border, plain link styling (no button look); dark-mode–aware; minimal mobile title bar.
- Build verified with `quarto render`.

**Key learnings / decisions**
- Quarto’s sidebar uses `#quarto-sidebar`, `.sidebar-navigation`, `.sidebar-link`, etc.; theme toggle and search appear in the sidebar when there is no navbar.
- On narrow screens the sidebar collapses to a title bar; tapping it reveals the nav (drawer behavior).

**Open questions / next steps**
- **Reminder: Workshop a better name for the page.** After this sidebar design is in place, the next step is to workshop a better site title (currently “Zach’s Personal Website”). Consider options that fit the academic × personal tone (e.g. “Zach Rivers”, “Zach Rivers — Research & Writing”, or a short tagline). Update `website.title` in `_quarto.yml` and any visible labels when decided.
- Run `quarto preview` and check sidebar on desktop and mobile in both light and dark themes; tweak CSS if needed.

