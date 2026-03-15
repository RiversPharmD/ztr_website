## Project Journal

Log of work on `ztr_website`. **Newest entry first.** Keep entries short: what we did, any decisions, and open next steps. Details live in `scope.md`, `.cursor/rules/`, and the repo.

---

## 2026-03-15

**Done**
- Set site title to "Zach Rivers, PharmD, PhD" everywhere; added content prompting questions for About and Homepage (`meta/content-prompting-questions.md`).
- Homepage: relaxed intro (clinician-scientist, real-world data, site purpose, hobby projects); simplified sections to Posts, Projects, Papers & writing (one-line + link).
- Enforced straight quotes only: normalized repo, added `.cursor/rules/quotes-style.mdc`.
- Project landing pages: each project has What it is, Why, What I learned, Links, and **Recent posts** (3 most recent blog posts with matching tag). Tagging: `params.project-tag` on project = slug; add same slug to post `tags` to link them. Template in `projects/_template.qmd`; README in `projects/README.md`. R chunk uses `yaml` to read post frontmatter.
- Placeholder projects added: MTG cards, Legos, Cooking (no external links). Projects index updated. Blog template and building-my-personal-website post use `personal-website` tag.
- Sidebar nav (no navbar), minimal sidebar CSS, build verified.

**Decisions**
- Publish to `gh-pages` only; `output-dir: _site`. Design and process live in `scope.md` and `.cursor/rules/`.
- Project slug = tag that links posts to that project’s page.

**Next**
- Fill About from prompting questions. Run `quarto preview`, check sidebar and project pages. Add posts with project tags to test Recent posts.

---

*Add new entries above this line (newest first).*
