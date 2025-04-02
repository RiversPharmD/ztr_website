# Personal Academic Website

This repository contains the source code for my personal academic website, built using Quarto. The website serves as a platform to showcase my research, publications, and professional journey in the fields of pharmacogenomics, health economics, and cancer research.

## Structure

```
.
├── _quarto.yml          # Quarto configuration file
├── index.qmd           # Homepage
├── bibliography/       # Bibliography and publications
│   └── published_works.qmd
├── blog/              # Blog posts
│   └── posts/         # Individual blog post files
├── projects/          # Project documentation
│   └── index.qmd      # Project listing
├── images/           # Image assets
│   ├── blog/         # Blog-specific images
│   └── projects/     # Project-specific images
└── references.bib    # Bibliography database
```

## Features

- **Publications**: Comprehensive list of academic publications and research work
- **Blog**: Platform for sharing thoughts and insights on research and healthcare
- **Projects**: Documentation of research projects and their outcomes
- **Bibliography**: Organized collection of academic references
- **Responsive Design**: Mobile-friendly layout

## Getting Started

### Prerequisites

- [Quarto](https://quarto.org/docs/get-started/) installed on your system
- Git for version control

### Local Development

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ztr_website.git
   cd ztr_website
   ```

2. Preview the website locally:
   ```bash
   quarto preview
   ```

3. Build the website:
   ```bash
   quarto render
   ```

## Deployment

This website is deployed using GitHub Pages with a custom GitHub Actions workflow. The deployment process:

1. **Build Environment Setup**
   - Installs R 4.3.0
   - Sets up TinyTeX for PDF generation
   - Installs required R packages (rmarkdown, knitr, tidyverse, DT)
   - Uses caching to speed up subsequent builds

2. **Site Generation**
   - Builds the site using Quarto
   - Processes R code blocks
   - Generates citations and references
   - Deploys to the `gh-pages` branch

3. **Monitoring**
   - Workflow status is monitored through GitHub Actions
   - Failed builds trigger notifications
   - Cache status is tracked for build performance

### Deployment Workflow

The site is deployed using the "Publish Quarto Website" workflow, which:
- Runs automatically on pushes to `main`
- Can be triggered manually from the Actions tab
- Handles all R dependencies and Quarto-specific requirements
- Uses caching to optimize build times

### Troubleshooting

If the site fails to deploy:
1. Check the Actions tab for error messages
2. Verify R package installation logs
3. Ensure all dependencies are properly specified
4. Check for any R code errors in the source files

## Contributing

This is a personal website repository. While it's public, it's primarily maintained for my own use. If you notice any issues or have suggestions, feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For questions or comments about the website or its content, please reach out through the appropriate channels listed in my profile.