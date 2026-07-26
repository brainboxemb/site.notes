# About This Notebook

This notebook is a Docsify-based personal technical knowledge base.

It is used to collect and organise technical information that may be useful for current and future projects.

## Purpose

The notebook provides a central place for:

- Project documentation
- Design ideas
- Software notes
- Product and supplier information
- Articles, forum discussions and videos
- DIY and workshop projects
- Daily findings
- Working conventions
- Information that should remain available for future use

The notebook is primarily a practical working document and long-term technical memory.

It is not necessary for every note to be complete or polished. Information can first be recorded briefly and later moved to a more suitable subject or project page.

## Main Structure

The main sections currently include:

```text
3d-printing/
daily/
diy/
embedded/
projects/
software/
uncategorized/
```

Information is organised by subject where possible.

## Subject Pages

Information that clearly belongs to a subject or project is stored on a dedicated page.

Examples include:

- Software documentation
- Project design considerations
- Product and supplier comparisons
- Mechanical design ideas
- Electronics information
- Workshop references
- Build instructions

Section landing pages normally use `README.md`.

## Daily Findings

Short findings that do not yet require a dedicated subject page are stored in the daily section.

These findings may include:

- YouTube videos
- Forum discussions
- Articles
- Products
- Tools
- Technical references
- Project ideas
- Small observations

Daily findings are grouped into one file per month:

```text
daily/
├── README.md
└── 2026/
    ├── 2026-07.md
    ├── 2026-08.md
    └── 2026-09.md
```

Dates use numeric ISO-style formatting:

```text
2026-07-26
```

A monthly page therefore uses a structure such as:

```markdown
# 2026-07

## 2026-07-26

### Finding Title

[Source](https://example.com/)

A short explanation of why the source or information is useful.
```

A useful finding can later be expanded into a dedicated page. The original daily entry may then link to that page.

## Writing Conventions

Pages are generally written in English.

The preferred writing style is:

- Compact
- Factual
- Easy to scan
- Limited to relevant information
- Clear about assumptions and uncertainty
- Free of unnecessary placeholder sections

Information should not be invented to make a page appear more complete.

Changing information such as prices, availability and software versions should include the date on which it was checked.

## Docsify Conventions

Absolute Docsify links are preferred for internal navigation:

```markdown
[Hinge Ideas](/projects/hub75-display/ideas/hinge)
```

Images are normally stored locally in an `_images` directory:

```markdown
![Hinge example](./_images/hinges/example-w320.webp)
```

Existing filenames and paths should be preserved when pages are updated.

When a page contains only one relevant source, the link can normally be included directly in the text instead of creating a separate one-item list.

## Use of ChatGPT

ChatGPT is used to help:

- Structure information
- Create and update Markdown pages
- Summarise useful sources
- Compare products and technical options
- Maintain consistent page layouts
- Develop repository and documentation conventions
- Convert discussions into reusable documentation

Long ChatGPT conversations eventually become difficult to continue.

A separate context page therefore contains the important information needed to continue working on this notebook in a new conversation:

- [ChatGPT Context](/chatgpt-context)

The context page should be updated when important structures, conventions or project decisions change.

## Root-Level Information

Information that applies to the entire notebook is stored directly at root level.

```text
README.md
notebook.md
chatgpt-context.md
```

The purpose of these files is:

```text
README.md            = main Docsify landing page
notebook.md          = purpose and organisation of the notebook
chatgpt-context.md   = context for continuing the work with ChatGPT
```

## Maintenance

The notebook structure may evolve as more information is added.

When an important convention changes, update:

- This notebook overview
- The ChatGPT context page
- Any affected section landing pages
- Related repository or documentation conventions

## Notes

-