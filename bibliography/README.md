# Bibliography

This directory contains bibliographic references used throughout the website. The main file is `references.bib`, which uses BibTeX format.

## Adding Citations

To cite a reference in any `.qmd` file, use the following syntax:

```markdown
[@citation-key]
```

For example:
```markdown
[@quarto2023] describes the Quarto publishing system.
```

## Adding New References

Add new references to `references.bib` using BibTeX format. Common entry types include:

- `@article` for journal articles
- `@book` for books
- `@inproceedings` for conference papers
- `@misc` for websites and other resources

Example:
```bibtex
@article{key,
  title={Title},
  author={Author, A.},
  journal={Journal Name},
  year={2024},
  doi={10.1234/example}
}
```

## Citation Styles

The website uses the Chicago citation style by default. This can be changed in `_quarto.yml` by modifying the `citation-style` parameter.

## Best Practices

1. Use unique citation keys
2. Include DOI or URL when available
3. Keep entries consistent in formatting
4. Use proper BibTeX field names
5. Include all necessary fields for the entry type 