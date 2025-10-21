# Markdown Flavors Comparison

A living comparison of syntax extensions across popular Markdown flavors and parsers.

## About This Project

This comparison helps developers, technical writers, and documentation maintainers understand which Markdown features are supported by different parsers and platforms. Whether you're choosing a Markdown flavor for a new project or migrating documentation, this resource provides a quick reference.

### Original Work

This project builds upon the excellent work by [@vimtaai](https://github.com/vimtaai) from their [markdown-flavors.md](https://gist.github.com/vimtaai/37c936679e8a2a2c22728f102eb7e8ae) comparison (2021). We've updated it for 2025 with modern flavors, new features, and community contributions.

**Note:** The original comparison included **ExtraMark**, a student project that has been archived here for historical reference.

## Feature Support Matrix

| Flavor | Superscript | Subscript | Strikethrough | Insertion | Highlight | Footnote | Task List | Table | Abbreviation | Definition List | Alerts | Callout/Admonition | Wikilinks | Mermaid | Math | Math Block | Emoji |
|--------|-------------|-----------|---------------|-----------|-----------|----------|-----------|-------|-------------|----------------|--------|-------------------|-----------|---------|------|------------|-------|
| **CommonMark** | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| **GitHub (GFM)** | ❌ | ❌ | `~~text~~` | ❌ | ❌ | ❌ | `- [ ]` | ✅ | ❌ | ❌ | `> [!NOTE]` | ❌ | ❌ | ✅ | ❌ | `$$...$$` | `:emoji:` |
| **GitLab** | ❌ | ❌ | `~~text~~` | `{+text+}` | ❌ | `[^1]` | `- [ ]` | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | `$...$` | ` ```math ` | `:emoji:` |
| **Obsidian** | ❌ | `~text~` | `~~text~~` | ❌ | `==text==` | `[^1]` | `- [ ]` | ✅ | ❌ | ❌ | `> [!note]` | ✅ | `[[page]]` | ✅ | `$...$` | `$$...$$` | `:emoji:` |
| **Discord** | ❌ | ❌ | `~~text~~` | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | `:emoji:` |
| **Pandoc** | `^text^` | `~text~` | `~~text~~` | ❌ | ❌ | `[^1]` | ❌ | ✅ | `*[...]:` | `: ` | ❌ | `::: info` | ❌ | ❌ | `$...$` | `$$...$$` | `:emoji:` |
| **MultiMarkdown** | `^text^` | `~text~` | `{--text--}` | `{++text++}` | `{==text==}` | `[^1]` | ❌ | ✅ | `*[...]:` | `: ` | ❌ | ❌ | ❌ | ❌ | `\\(...\\)` | `\\[...\\]` | ❌ |
| **Kramdown** | ❌ | ❌ | ❌ | ❌ | ❌ | `[^1]` | ❌ | ✅ | `*[...]:` | `: ` | ❌ | ❌ | ❌ | ❌ | `$$...$$` | `$$...$$` | ❌ |
| **Python-Markdown** | `^text^` * | `~text~` * | `~~text~~` * | ❌ | `==text==` * | `[^1]` | `- [ ]` * | ✅ | `*[...]:` * | `: ` * | ❌ | `!!! note` * | `[[page]]` * | ❌ | ❌ | ❌ | `:emoji:` * |
| **Marked.js** | ❌ | ❌ | `~~text~~` * | ❌ | ❌ | ❌ | `- [ ]` * | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | `:emoji:` * |
| **R Markdown** | `^text^` | `~text~` | `~~text~~` | ❌ | ❌ | `[^1]` | ❌ | ✅ | ❌ | ❌ | ❌ | `::: callout` | ❌ | ✅ | `$...$` | `$$...$$` | `:emoji:` |
| **MDX** | ❌ | ❌ | `~~text~~` * | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| **Quarto** | `^text^` | `~text~` | `~~text~~` | ❌ | ❌ | `[^1]` | `- [ ]` | ✅ | ❌ | `: ` | ❌ | `::: callout` | ❌ | ✅ | `$...$` | `$$...$$` | `:emoji:` |
| **Markdown Extra** | ❌ | ❌ | ❌ | ❌ | ❌ | `[^1]` | ❌ | ✅ | `*[...]:` | `: ` | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |

**Legend:**
- ✅ = Supported natively
- `syntax` = Syntax example
- ❌ = Not supported
- `*` = Requires extension/plugin

## Feature Descriptions

### Text Formatting Extensions

- **Superscript**: Text displayed above the normal line (e.g., x^2^)
- **Subscript**: Text displayed below the normal line (e.g., H~2~O)
- **Strikethrough**: Text with a line through it (deleted/deprecated content)
- **Insertion**: Markup for inserted/added content (often used with CriticMarkup)
- **Highlight**: Background highlighting for emphasis

### Semantic Syntax Features

These features provide meaningful structure for accessibility, AI parsing, and semantic HTML:

- **Abbreviation**: Define abbreviations with `*[HTML]: Hypertext Markup Language` - improves accessibility and helps readers understand acronyms
- **Definition List**: Key-value pairs using `: ` syntax - useful for glossaries, term definitions, and structured metadata
- **Alerts** (GitHub-specific): Styled notification blocks using `> [!NOTE]`, `> [!WARNING]`, `> [!IMPORTANT]` syntax - similar to callouts but with standardized types
- **Callout/Admonition**: Styled blocks for notes, warnings, tips using various syntaxes (`::: note`, `> [!note]`, `!!! note`) - helps organize information by importance/type

### Document Structure

- **Footnote**: Reference notes at the bottom of the document
- **Task List**: Interactive checkboxes for to-do items
- **Table**: Structured tabular data

### Advanced Features

- **Wikilinks**: Internal document linking with `[[page]]` syntax
- **Mermaid**: Diagram and flowchart generation
- **Math**: Inline mathematical expressions (LaTeX)
- **Math Block**: Display mathematical equations (LaTeX blocks)
- **Emoji**: Support for `:emoji:` syntax or Unicode

## Flavor-Specific Notes

### CommonMark
The base specification that many flavors extend. Intentionally minimal to ensure broad compatibility.

### GitHub Flavored Markdown (GFM)
GitHub's implementation, widely used in README files, issues, and pull requests. Added support for math blocks in 2022 and Alerts in 2023.

### Obsidian
Optimized for knowledge management with strong support for internal linking, callouts, and community plugins that extend functionality.

### Python-Markdown
Highly extensible through its extension system. Most advanced features require installing specific extensions.

### Pandoc
Swiss-army knife of document conversion. Extensive feature support for academic and technical writing.

### Quarto
Modern scientific and technical publishing system built on Pandoc, popular in data science.

### MDX
Allows JSX components in Markdown, primarily used with React-based documentation sites.

## Contributing

We welcome contributions! This is a living document that should reflect the current state of Markdown parsers.

### How to Contribute

1. **Fork this repository**
2. **Add or update flavor information** in both:
   - `README.md` (the comparison table)
   - `markdown-flavors.csv` (the data file)
3. **Include in your PR**:
   - Link to official documentation
   - Version number (if applicable)
   - Date tested
4. **Submit a pull request**

### Guidelines

- Test features yourself or provide documentation links
- Include version numbers for parsers (e.g., "Marked.js v12.0.0")
- Note if a feature requires plugins/extensions
- Be specific about syntax variations
- Update both the table and CSV file

## Data Format

The machine-readable data is available in `markdown-flavors.csv` for programmatic access.

## Version History

- **2025-01-22**: Added GitHub Alerts, Abbreviations, Definition Lists; reorganized features into semantic categories (thanks to [@saeris](https://reddit.com/user/saeris) for terminology feedback)
- **2025-01**: Updated comparison with modern flavors (Obsidian, Quarto, MDX), new features (callouts, wikilinks, emoji)
- **2021-06**: Original comparison by [@vimtaai](https://github.com/vimtaai)

## Related Resources

- [CommonMark Spec](https://commonmark.org/)
- [GitHub Flavored Markdown Spec](https://github.github.com/gfm/)
- [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown)
- [Markdown Guide](https://www.markdownguide.org/)

## License

This comparison is released under CC0 1.0 Universal (Public Domain). The original work by vimtaai was also released under CC0.

---

**Maintainers**: Looking for maintainers to help keep this up-to-date. Open an issue if interested!

**Last Updated**: January 22, 2025
