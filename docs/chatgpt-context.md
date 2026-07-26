# ChatGPT Context

This page contains the general context needed to continue working on this Docsify notebook in a new ChatGPT conversation.

## Purpose

This is a personal technical notebook built with Docsify.

It contains project notes, software information, design ideas, references, daily findings and repository conventions.

Notebook pages are generally written in English. Discussion with ChatGPT is usually in Dutch.

## Docsify Version

The notebook currently uses Docsify 4.

Docsify 5 is still a prerelease and is currently available as a release candidate. Migration can be considered after a stable Docsify 5 release is available.

## Working Method

When updating an existing page, the current page content should normally be included in the conversation.

ChatGPT should use the supplied page as the source for:

- Existing structure
- Current wording
- Filenames
- Links
- Image paths
- Previously recorded decisions

This context page contains only general conventions. It does not reproduce the contents of the complete notebook.

## Writing Style

Notebook pages should be:

- Compact
- Factual
- Easy to scan
- Written in clear English
- Limited to relevant information
- Clear about assumptions and uncertainty

Do not invent facts, dimensions, prices, features or conclusions.

Avoid vague placeholder sections unless they have a concrete purpose.

When a complete page is requested, return the complete Markdown page in one copyable block.

## Markdown Output

When a page contains fenced code blocks, wrap the complete page in four backticks so that nested code blocks remain intact.

## Docsify Conventions

Section landing pages normally use:

```text
README.md
```

Use absolute Docsify links for internal navigation:

```markdown
[Hinge Ideas](/projects/hub75-display/ideas/hinge)
```

Images are normally stored locally in an `_images` directory.

Preserve existing filenames, links and image paths unless a change is explicitly agreed.

## Root-Level Files

```text
README.md
notebook.md
chatgpt-context.md
```

Their purposes are:

```text
README.md            = main Docsify landing page
notebook.md          = purpose and organisation of the notebook
chatgpt-context.md   = general context for a new ChatGPT conversation
```

## Daily Findings

Short findings such as videos, forum discussions, articles and technical references are stored by month.

Example:

```text
daily/
└── 2026/
    └── 2026-07.md
```

Dates use numeric ISO-style formatting:

```text
2026-07-26
```

## Repository Naming

The general GitHub repository naming convention is:

```text
<prefix>.<year>-<project-number>-<subproject-number>-<description>.<classification>
```

Private repositories use:

```text
.PRV
```

Current prefixes include:

```text
proj = complex multidisciplinary project
site = standalone website or web application
code = standalone software, scripts or firmware
cad  = standalone CAD model or 3D-printable design
mech = standalone mechanical system or assembly
diy  = standalone maker or construction project
arch = data and documents stored for preservation
fork = official GitHub fork
```

The prefix acts as a first visual filter.

The `proj` prefix is used when the shared identity of a complex project is more important than the technical discipline of an individual repository.

The subproject number identifies a separate repository within the same main project. It is not a development iteration.

Small development states inside a repository may use tags such as:

```text
daily/20260101
daily/20260101-01
```

## Starting a New Chat

A new conversation can start with:

```text
I am maintaining a Docsify 4-based personal technical notebook.

Please follow the conventions in chatgpt-context.md.

Notebook content is generally written in English, while discussion may be in Dutch.

Keep pages compact and factual.
Use absolute Docsify links.
Preserve existing filenames, links and image paths.
Do not invent facts or conclusions.
Return complete Markdown pages when requested.

I will provide the existing page that needs to be updated.
```

## Maintenance

Update this page only when general notebook conventions or working methods change.

Project-specific information should remain on the corresponding project or subject pages.