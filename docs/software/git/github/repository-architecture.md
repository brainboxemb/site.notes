# GitHub Repository Architecture

This page describes the repository structure used to keep a large number of GitHub projects organised.

The structure deliberately uses separate project and subproject numbers, explicit repository names and repeated visual checks.

## Goals

The naming strategy should make it possible to:

- Recognise the type of a repository
- Group related repositories under one main project
- Give each subproject its own repository and purpose
- Sort projects chronologically
- Recognise private repositories directly from their names
- Preserve small development steps in a clear and comparable way
- Store data and documents with version history and recovery options

## Repository Naming

### Structure

```text
<prefix>.<year>-<project-number>-<subproject-number>-<description>.<classification>
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
code.2026-001-02-display-controller.PRV
site.2026-002-01-portfolio-web.PRV
arch.2026-001-03-display-reference-data.PRV
```

## Projects and Subprojects

The numeric part of the repository name consists of:

```text
<year>-<project-number>-<subproject-number>
```

| Part | Purpose |
|---|---|
| `year` | The year in which the main project was started |
| `project-number` | The sequence of the main project within that year |
| `subproject-number` | A separate repository that belongs to the main project |

Each subproject has its own repository name and a clearly defined purpose.

For example:

```text
mech.2026-001-01-display-casing.PRV
code.2026-001-02-display-controller.PRV
arch.2026-001-03-display-reference-data.PRV
```

These repositories all belong to project `2026-001`:

```text
2026-001 = HUB75 display project
```

The final number identifies the individual subproject:

```text
01 = mechanical display casing
02 = display controller software
03 = reference data and documentation
```

The repository prefix may differ between subprojects because each repository can have a different type.

The subproject number does not represent a development iteration or version.

Development steps within a repository are recorded using Git commits and daily snapshot tags.

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
- Material that does not belong to a software, website or mechanical repository

Example:

```text
arch.2026-001-03-display-reference-data.PRV
```

The use of Git provides an additional recovery layer compared with ordinary cloud-storage folders.

Deleted or changed files can normally still be recovered from earlier commits, provided that the repository and its history are retained.

An archive repository is not necessarily inactive.

The `arch` prefix describes the purpose of the repository, not its current status.

## Daily Development Steps

Daily tags are used to keep small development steps recognisable, ordered and easy to compare.

### Tag Format

```text
daily/20260101
daily/20260101-01
daily/20260101-02
```

The date identifies the working day.

The first preserved state of the day uses only the date:

```text
daily/20260101
```

When multiple meaningful states are preserved on the same day, a sequence number is added:

```text
daily/20260101-01
daily/20260101-02
```

These tags make it possible to:

- Preserve small development steps
- Compare consecutive states
- Return to an earlier working state
- Keep experiments understandable
- Avoid losing overview in a long commit history
- Continue experimenting without overwriting a recognisable result

The daily tags provide the small-step structure inside each subproject repository.

## Milestone Tags

Descriptive milestone tags can be used in addition to daily tags.

Examples:

```text
milestone/first-working-build
milestone/mechanical-prototype
milestone/field-test
```

The two tag types have different purposes:

- Daily tags preserve chronological development steps
- Milestone tags identify recognisable project states

A commit may therefore have both a daily tag and a milestone tag.

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
arch.2026-001-03-display-reference-data.PRV
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
repository name   = identity, project relation and visibility check
prefix            = repository type
year              = year in which the main project started
project number    = sequence of the main project within that year
subproject number = separate repository within the main project
description       = specific purpose of the subproject
classification    = additional visual visibility check
GitHub Topics     = filtering, technology and status
Git tags          = small development steps, snapshots and milestones
GitHub setting    = actual public or private visibility
```

The repeated information is intentional where it provides an additional visual check or reduces the need to remember hidden context.

## Initial Convention

```text
<prefix>.<year>-<project-number>-<subproject-number>-<description>.PRV
```

Example main project with multiple subprojects:

```text
mech.2026-001-01-display-casing.PRV
code.2026-001-02-display-controller.PRV
arch.2026-001-03-display-reference-data.PRV
```

Daily snapshot examples:

```text
daily/20260101
daily/20260101-01
daily/20260101-02
```

Milestone example:

```text
milestone/first-working-build
```

## Notes

-