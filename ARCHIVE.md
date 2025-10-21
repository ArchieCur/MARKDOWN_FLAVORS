# Archived Markdown Flavors

This document preserves information about Markdown flavors that were included in the original comparison but are no longer actively maintained or widely used.

## ExtraMark

**Status**: Student project (circa 2021)  
**Original Source**: [vimtaai's markdown-flavors comparison](https://gist.github.com/vimtaai/37c936679e8a2a2c22728f102eb7e8ae)

ExtraMark was a proposed Markdown syntax extension created as a student project. It combined features from multiple existing flavors with planned future enhancements.

### Feature Support

| Feature | Syntax | Notes |
|---------|--------|-------|
| Superscript | `^...^` | |
| Subscript | `~...~` | |
| Deletion/Strikethrough | `{--...--}` | CriticMarkup syntax |
| Insertion | `{++...++}` | CriticMarkup syntax |
| Highlight | `{==...==}` | CriticMarkup syntax |
| Footnote | `[^...]` | Planned feature |
| Task List | `- [ ] ...` | Planned feature |
| Table | ✅ | |
| Abbreviation | `*[...]: ...` | Planned feature |
| Definition List | `: ` | |

### Historical Context

ExtraMark represented an interesting attempt to create a unified Markdown syntax that incorporated:

1. **CriticMarkup conventions** for editorial markup (insertions, deletions, highlights)
2. **Common extensions** from MultiMarkdown and Pandoc
3. **Modern features** like task lists that were gaining popularity

While ExtraMark itself didn't see wide adoption, many of its proposed features have since been implemented in various Markdown flavors:

- Obsidian adopted similar highlight syntax (`==text==`)
- Task lists became standard in GitHub and GitLab
- CriticMarkup syntax is supported by MultiMarkdown and some editors

### Why It's Archived

- No evidence of active parser/implementation
- Created as an academic exercise
- Most proposed features now available in other active flavors
- Helps preserve the history of the original comparison

## Other Historical Flavors

The following flavors from the original 2021 comparison have been moved to archive status:

### Maruku
**Status**: Inactive (last update ~2016)  
**Notes**: Ruby-based parser, largely superseded by Kramdown

### Markdown2
**Status**: Maintenance mode  
**Notes**: Python implementation, limited adoption compared to Python-Markdown

### Remarkable
**Status**: Project deprecated  
**Notes**: JavaScript parser, development ceased

### Showdown
**Status**: Limited maintenance  
**Notes**: While still available, much less actively developed than other JS parsers

### Ghost
**Status**: Platform-specific  
**Notes**: Ghost CMS uses their own Markdown variant, less relevant for general comparison

### Haroopad
**Status**: Editor discontinued  
**Notes**: Desktop editor, no longer maintained

### iA Writer
**Status**: App-specific  
**Notes**: Proprietary editor, less relevant for open format comparison

### Redcarpet
**Status**: Maintenance mode  
**Notes**: Ruby library, largely superseded by other parsers

### ScholarlyMarkdown
**Status**: Specification only  
**Notes**: Academic proposal, no wide implementation

### Taiga
**Status**: Platform-specific  
**Notes**: Project management tool's internal Markdown

### Trello
**Status**: Platform-specific  
**Notes**: Limited Markdown support, platform-specific

### s9e\TextFormatter
**Status**: Niche use  
**Notes**: PHP library, limited adoption

## Criteria for Archiving

Flavors are moved to the archive when they meet one or more of:

1. **No active development** for 3+ years
2. **Superseded** by another flavor
3. **Platform-specific** with limited general applicability
4. **No parser implementation** available
5. **Minimal adoption** in the wider Markdown community

## Restoring from Archive

If a flavor becomes active again or gains significant adoption, it can be restored to the main comparison through a pull request with evidence of:

- Active development/maintenance
- Working parser/implementation
- Community adoption
- Updated feature documentation

---

**Note**: This archive helps maintain historical context while keeping the main comparison focused on currently relevant and actively maintained Markdown flavors. If you believe a flavor has been incorrectly archived, please open an issue with supporting evidence.