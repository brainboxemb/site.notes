# GitHub Repository Architecture

This page describes the naming conventions used to organise GitHub repositories.

## Goals

The naming strategy should make it possible to:

- Give personal projects a unique number
- Group related repositories under one main project
- Recognise the primary repository type
- Keep websites and official forks immediately recognisable
- Mark private repositories clearly
- Preserve small development steps without creating extra repositories

## Naming Conventions

### Personal Projects

```text
<year>-<project-number>-<subproject-number>.<type>.<description>.<classification>
```

Example:

```text
2026-002-01.cad.hub75-display-enclosure.PRV
```

### Websites

Website repositories use a separate `site` prefix and are not included in the numbered personal-project sequence.

```text
site.<description>.<classification>
```

Examples:

```text
site.notes.PRV
site.hugo-step001.PRV
site.brainboxemb
```

### Official Forks

Official GitHub forks use:

```text
fork.<upstream-name>
```

Examples:

```text
fork.purecutcnc
fork.roadster
```

## Project Numbering

The numeric part of a personal project repository is:

```text
<year>-<project-number>-<subproject-number>
```

For example:

```text
2026-002-01
```

means:

```text
2026 = year in which the main project started
002  = second personal project started in that year
01   = first repository within that project
```

The project-number sequence is generic and does not restart for each repository type.

Several repositories can belong to the same project:

```text
2026-002-01.cad.hub75-display-enclosure.PRV
2026-002-02.cad.hub75-electronics-frame.PRV
2026-002-03.code.hub75-display-controller.PRV
2026-002-04.arch.hub75-reference-data.PRV
```

The subproject number identifies a separate repository. It is not a development iteration or version.

## Repository Types

| Type | Purpose |
|---|---|
| `code` | Software, scripts and firmware |
| `cad` | CAD models, parametric designs and 3D-printable parts |
| `mech` | Mechanical systems, assemblies and manufacturing information |
| `diy` | Practical construction and maker projects |
| `arch` | Data, documents and reference material stored for preservation |

The type describes the primary contents of the repository.

For example, an OpenSCAD-based enclosure repository would normally use:

```text
2026-002-01.cad.hub75-display-enclosure.PRV
```

Additional disciplines and technologies can be recorded using GitHub Topics.

## Independent Copies and Forks

An official fork remains connected to its upstream repository:

```text
fork.purecutcnc
```

A private independent copy is treated as a normal personal project:

```text
2026-006-01.code.purecutcnc-experiments.PRV
```

A local checkout of an official fork normally uses:

```text
origin   = personal GitHub fork
upstream = original repository
```

## Private Classification

Private repositories use:

```text
.PRV
```

Examples:

```text
2026-002-01.cad.hub75-display-enclosure.PRV
site.notes.PRV
```

The suffix provides an additional visual check in repository lists, local directory names, clone URLs and terminal output.

Public repositories omit `.PRV`.

## Development Tags

Daily tags preserve small chronological development steps:

```text
daily/20260101
daily/20260101-01
daily/20260101-02
```

Milestone tags identify recognisable project states:

```text
milestone/first-working-build
milestone/mechanical-prototype
milestone/field-test
```

A commit may have both a daily tag and a milestone tag.

## GitHub Topics

Topics can record disciplines, technologies and status without making repository names longer.

Examples:

```text
cad
mechanical
openscad
hub75
embedded
documentation
active
experimental
archived
```

The `archived` topic is a status and is separate from the `arch` repository type.

## Summary

```text
Personal project:
<year>-<project>-<subproject>.<type>.<description>.[PRV]

Website:
site.<description>.[PRV]

Official fork:
fork.<upstream-name>
```