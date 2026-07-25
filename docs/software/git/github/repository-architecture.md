# GitHub Repository Architecture

This page describes the repository structure used to keep a large number of GitHub projects organised.

The structure deliberately uses small project steps, explicit repository names and repeated visual checks.

## Goals

The naming strategy should make it possible to:

- Recognise the type of a repository
- Keep experiments separated into small steps
- Connect related software and mechanical repositories
- Sort repositories chronologically
- Recognise private repositories directly from their names
- Preserve important snapshots without creating extra folders
- Store data and documents with version history and recovery options

## Repository Naming

### Structure

```text
<prefix>.<year>-<project-number>-<iteration>-<description>.<classification>
```

### Prefixes

| Prefix | Purpose |
|---|---|
| `site` | Websites and web applications |
| `code` | Software, scripts and firmware |
| `mech` | Mechanical designs, CAD files and 3D models |
| `arch` | Data, documents and other material stored for long-term preservation |

### Classification

```text
.PRV
```

The `.PRV` suffix explicitly marks a repository as private.

GitHub already displays repository visibility, but the suffix provides an additional visual check in repository lists, clone URLs, local directories and terminal output.

Renaming the repository later is acceptable when its visibility or purpose changes.

### Examples

```text
mech.2026-001-01-display-casing.PRV
code.2026-001-01-display-controller.PRV
site.2026-002-01-portfolio-web.PRV
arch.2026-003-01-display-reference-data.PRV
```

Repositories that belong to the same overall project can share the same year and project number:

```text
mech.2026-001-01-display-casing.PRV
code.2026-001-01-display-controller.PRV
```

## Small Iteration Steps

The iteration number represents a deliberately separated experiment or development step.

```text
site.2026-002-01-hugo-first-build.PRV
site.2026-002-02-hugo-content-structure.PRV
site.2026-002-03-github-pages-deployment.PRV
```

Creating separate iterations helps to:

- Keep each experiment limited in scope
- Preserve a working result before starting the next step
- Reduce the amount of unrelated history inside one repository
- Make it easier to return to an earlier approach
- Keep the repository list understandable without first reading commit history

A new iteration is not required for every small edit.

It is used when the next step should remain independently understandable or reusable.

## Archive Repositories

The `arch` prefix is used for repositories whose primary purpose is preserving data or documents.

This may include:

- Project documentation
- Reference files
- Exported data
- Historical versions
- Research material
- Configuration backups
- Files that should be protected against accidental deletion
- Material that does not belong to an active software, website or mechanical repository

Example:

```text
arch.2026-003-01-display-reference-data.PRV
```

The use of Git provides an additional recovery layer compared with ordinary cloud-storage folders.

Deleted or changed files can normally still be recovered from earlier commits, provided that the repository and its history are retained.

An archive repository is not necessarily inactive.

The `arch` prefix describes the purpose of the repository, not its current status.

## Git Tags and Snapshots

Git tags can preserve specific states inside an iteration.

### Daily Snapshot Format

```text
daily/20260101
daily/20260101-01
daily/20260101-02
```

The first tag identifies the first preserved state of the day.

Additional sequence numbers are used when multiple meaningful snapshots are created on the same day.

Daily snapshots provide small, recognisable restore points without requiring another repository.

### Milestone Tags

Descriptive milestone tags can also be used:

```text
milestone/first-working-build
milestone/mechanical-prototype
milestone/field-test
```

The two systems can be used together:

- Daily tags for chronological snapshots
- Milestone tags for recognisable project states

## GitHub Topics

GitHub Topics provide another way to filter repositories without changing their names.

### Domain Topics

- `mechanical`
- `software`
- `firmware`
- `website`
- `documentation`
- `data`
- `archive`

### Technology Topics

- `openscad`
- `java`
- `esp32`
- `raspberry-pi`
- `hugo`
- `docsify`

### Status Topics

- `active`
- `experimental`
- `paused`
- `archived`

The `archived` topic is a status and is separate from the `arch` repository prefix.

For example, an actively maintained archive repository could be:

```text
arch.2026-003-01-display-reference-data.PRV
```

with topics such as:

```text
archive
documentation
hub75
active
```

Example search:

```text
topic:mechanical
```

More specific example:

```text
topic:mechanical topic:openscad
```

## Repository Roles

Each part of the system has a separate purpose:

```text
repository name = identity, sequence and visibility check
prefix          = repository type
iteration       = separated experiment or development step
GitHub Topics   = filtering, technology and status
Git tags        = snapshots and milestones
GitHub setting  = actual public or private visibility
```

The repeated information is intentional where it provides an additional visual check or reduces the need to remember hidden context.

## Initial Convention

```text
<prefix>.<year>-<project-number>-<iteration>-<description>.PRV
```

Example:

```text
mech.2026-001-01-display-casing.PRV
```

Archive example:

```text
arch.2026-003-01-display-reference-data.PRV
```

Snapshot examples:

```text
daily/20260101
daily/20260101-01
milestone/first-working-build
```

## Notes

-