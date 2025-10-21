# Contributing to Markdown Flavors Comparison

Thank you for helping keep this comparison accurate and up-to-date! 🎉

## How to Contribute

### Adding a New Markdown Flavor

1. **Fork the repository**
2. **Test the flavor** - Verify feature support yourself or reference official documentation
3. **Update both files**:
   - Add a row to the table in `README.md`
   - Add a row to `markdown-flavors.csv`
4. **Include in your PR**:
   - Link to official documentation
   - Version number (if applicable)
   - Date you tested
   - Any important caveats

### Updating Existing Information

If you find outdated or incorrect information:

1. **Verify the current behavior**
2. **Note what changed** (version update, new feature, etc.)
3. **Submit a PR** with:
   - What was wrong
   - What's correct now
   - Evidence (docs link, test results)
   - Version information

### Adding New Features to Track

Want to track a new Markdown feature?

1. **Check if it's widely adopted** (used by 3+ major flavors)
2. **Propose it in an issue first** to get feedback
3. **If approved**, add the column to both:
   - The comparison table in README.md
   - The CSV file
4. **Fill in data for all existing flavors**

## Contribution Guidelines

### Testing Requirements

- Test features in the actual parser/platform, not just documentation
- Note version numbers (e.g., "Pandoc 3.1.2", "marked.js 12.0.1")
- Distinguish between:
  - Native support (✅)
  - Requires extension/plugin (`*`)
  - Not supported (❌)

### Documentation Standards

When adding a flavor, include:

```markdown
| FlavorName | feature1 | feature2 | ... |
```

In the CSV:
```csv
FlavorName,syntax or No,syntax or No,...,Your notes here
```

### Syntax Examples

- Use inline code for syntax: `` `~~text~~` ``
- Show the actual syntax users would type
- If multiple syntaxes exist, show the most common: `^text^` or `^text^, <sup>text</sup>`
- Note alternatives in the "Notes" column

### Evidence Requirements

PRs should include at least one of:

- Link to official documentation
- Link to parser/implementation source code
- Test case showing the behavior
- Screenshot of rendered output

### What Makes a Good PR

✅ **Good Examples:**

```
"Add Docusaurus Markdown support - tested v3.1.0"
- Links to Docusaurus Markdown features doc
- Tested all features in a local Docusaurus site
- Notes which features require plugins
```

```
"Update GitHub math support - now supports inline $...$"
- Links to GitHub changelog announcing the change
- Shows before/after behavior
- Includes date of change
```

❌ **Avoid:**

```
"I think Flavor X supports feature Y"
- No testing or documentation
- No version information
```

## Feature Categories

Current features tracked:

### Text Formatting
- Superscript
- Subscript
- Strikethrough
- Insertion
- Highlight

### Document Structure
- Footnotes
- Task Lists
- Tables
- Callouts/Admonitions

### Advanced Features
- Wikilinks
- Mermaid diagrams
- Math (inline)
- Math (block)
- Emoji

## Column Definitions

To ensure consistency:

- **Superscript**: Text raised above baseline (x^2^)
- **Subscript**: Text lowered below baseline (H~2~O)
- **Strikethrough**: Text with line through it (~~deleted~~)
- **Insertion**: Markup for added content (critic markup)
- **Highlight**: Background color emphasis (==highlighted==)
- **Footnote**: Reference notes with `[^1]` syntax
- **Task List**: Checkbox items `- [ ]` or `- [x]`
- **Table**: Pipe-delimited tables
- **Callout/Admonition**: Styled blocks (:::, > [!], !!!)
- **Wikilinks**: Internal linking `[[page]]`
- **Mermaid**: Diagram code blocks
- **Math Inline**: LaTeX math `$...$` or `\\(...\\)`
- **Math Block**: Display equations `$$...$$` or `\\[...\\]`
- **Emoji**: `:emoji:` syntax or Unicode support

## Style Guide

### Markdown Table Formatting

- Align columns for readability
- Keep syntax examples concise
- Use ❌ for "not supported"
- Use ✅ for "native support"
- Use `` `syntax` `` for syntax examples

### CSV Formatting

- Use "No" for features not supported
- Use actual syntax string for supported features
- Use `*` suffix to indicate requires extension
- Keep notes brief (under 50 characters)

## Questions?

- **Have a question about a specific flavor?** Open an issue
- **Not sure if something is worth adding?** Open an issue to discuss
- **Found a bug in the comparison?** Open an issue or PR

## Code of Conduct

- Be respectful and constructive
- Assume good faith
- Focus on accuracy, not preference
- Credit sources and prior work

## Recognition

Contributors will be listed in the README. Significant contributions (adding multiple flavors, major updates) may be listed as co-maintainers.

---

Thank you for helping make this resource valuable to the Markdown community! 🙏