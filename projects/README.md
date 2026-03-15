# Projects

Each project has its own `.qmd` file and works as a **landing page** with:

- **What it is** — short summary
- **Why I did it** — what prompted the project
- **What I learned (or am hoping to learn)** — takeaways or goals
- **Links** — GitHub repo, docs, demo, etc.
- **Recent posts** — the 3 most recent blog posts tagged with this project

## Tagging: linking posts to projects

- In the **project** frontmatter, set `params.project-tag` to a slug (e.g. `personal-website`). That slug is the project’s tag.
- In **blog posts** (`blog/posts/*.qmd`), add that same slug to `tags`. Any post with that tag appears under “Recent posts” on the project page (up to 3, most recent first).

Example: project `projects/personal-website.qmd` has `params.project-tag: personal-website`. A post with `tags: [personal-website, Quarto, ...]` will show up on that project’s page.

## Using the template

1. Copy `_template.qmd` to `my-project-slug.qmd`.
2. Set `params.project-tag` to `my-project-slug` (usually match the filename).
3. Fill in title, date, github (and optional docs/demo), then the sections: What it is, Why I did it, What I learned, Links. The “Recent posts” chunk will list tagged posts automatically.
4. When you write a post about this project, add `my-project-slug` to that post’s `tags`.

## R dependency

The “Recent posts” block uses the R **yaml** package to read post frontmatter. Install with `install.packages("yaml")` if you don’t have it.
