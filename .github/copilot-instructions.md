# SysArtifacts Fork — Copilot Instructions

## Conference Directory Structure

Conference data lives in `_conferences/` using a strict naming convention:

```
_conferences/
  CONFNAME/
    CONFNAMEYEAR/
      index.md
      badges.md
      call.md
      results.md
      report.md
      organizers.md
```

- Directory names are **lowercase, no hyphens**: `osdi2024`, not `osdi-2024`.
- When adding a new conference year, **copy an existing year directory** and update
  all frontmatter and content.

## YAML Frontmatter Requirements

Every `.md` file must include:

- `title` — page title displayed in sidebar and header
- `order` — integer controlling sidebar sort order (lower = higher)

Conference-year pages should also include conference-specific metadata.

## Jekyll Conventions

- Theme: **Minimal Mistakes v4.24.0** (remote_theme)
- Markdown: Kramdown
- Collections: `_conferences` is configured as a Jekyll collection
- Plugins: `jekyll-redirect-from`, `jekyll-include-cache`
- Use `jekyll-redirect-from` frontmatter for page moves/renames.

## Guides

`chair-guide.md` and `evaluator-guide.md` contain **templated email text** and
procedural guidance for AE organizers. These are hand-maintained reference documents.
When editing, preserve the template placeholders and section structure.

## Results Pages

`results.md` files contain per-paper badge listings. These are typically populated
from HotCRP exports or manual entry. Fields: paper title, authors, badges awarded,
artifact URLs.

The artifact_analysis pipeline scrapes these files as data sources.
