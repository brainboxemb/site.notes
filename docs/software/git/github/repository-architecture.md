# GitHub Repository Architecture

This page describes the repository structure used to keep a large number of GitHub repositories organised.

The structure deliberately uses recognisable prefixes, separate project and subproject numbers, explicit visibility markers and small Git-tagged development steps.

## Goals

The naming strategy should make it possible to:

- Recognise the repository type immediately
- Group related repositories under one main project
- Give each subproject its own repository and purpose
- Keep complex multidisciplinary projects together
- Sort projects chronologically
- Recognise private repositories directly from their names
- Distinguish official GitHub forks from independent repositories
- Preserve small development steps in a clear and comparable way
- Store data and documents with version history and recovery options

## Repository Naming

### Structure

```text
<prefix>.<year>-<project-number>-<subproject-number>-<description>.<classification>
```

The classification suffix is omitted when it does not apply.

### Prefixes

| Prefix | Purpose |
|---|---|
| `proj` | Complex projects consisting of multiple related disciplines or subprojects |
| `site` | Standalone websites and web applications |
| `code` | Standalone software, scripts and firmware |
| `cad` | Standalone CAD models, parametric designs and 3D-printable parts |
| `mech` | Standalone mechanical systems and assemblies |
| `diy` | Standalone construction and maker projects |
| `arch` | Data, documents and other material stored for long-term preservation |
| `fork` | Official GitHub forks that remain connected to an upstream repository |

The prefix acts as a first visual filter.

A specific prefix is used when a repository can be clearly classified on its own. The `proj` prefix is used when the relationship between several repositories is more important than their individual technical discipline.

### Private Classification

```text
.PRV
```

The `.PRV` suffix explicitly marks a repository as private.

GitHub already displays repository visibility, but the suffix provides an additional visual check in:

- Repository lists
- Clone URLs
- Local directory names
- Terminal output
- Scripts and configuration files

Renaming a repository later is acceptable when its visibility or purpose changes.

A public repository does not use the `.PRV` suffix.

### Examples

```text
proj.2026-001-01-hub75-display-enclosure.PRV
proj.2026-001-02-hub75-electronics-frame.PRV
proj.2026-001-03-hub75-controller.PRV

cad.2026-002-01-router-roof-mount.PRV
code.2026-003-01-deployment-tools.PRV
diy.2026-004-01-folding-workbench.PRV
site.2026-005-01-portfolio-web.PRV
arch.2026-001-04-hub75-reference-data.PRV

fork.2026-006-01-purecutcnc
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
proj.2026-001-01-hub75-display-enclosure.PRV
proj.2026-001-02-hub75-electronics-frame.PRV
proj.2026-001-03-hub75-controller.PRV
arch.2026-001-04-hub75-reference-data.PRV
```

These repositories all belong to project `2026-001`:

```text
2026-001 = HUB75 display project
```

The final number identifies the individual subproject:

```text
01 = display enclosure
02 = electronics frame
03 = controller
04 = reference data
```

The subproject number does not represent a development iteration or software version.

Development steps within a repository are recorded using Git commits and daily snapshot tags.

## Complex Projects

The `proj` prefix is used when a project contains multiple disciplines or several closely related subprojects.

Examples include projects that combine:

- Mechanical construction
- CAD designs
- Electronics
- Embedded software
- Documentation
- Test infrastructure
- Deployment tooling

All main repositories belonging to such a project use the `proj` prefix.

Example:

```text
proj.2026-001-01-hub75-display-enclosure.PRV
proj.2026-001-02-hub75-electronics-frame.PRV
proj.2026-001-03-hub75-controller.PRV
```

The specific discipline can be recorded using GitHub Topics:

```text
mechanical
cad
electronics
software
embedded
hub75
```

Using the shared `proj` prefix keeps the related repositories visually grouped and recognisable.

Supporting repositories may still use another prefix when their purpose is clearly different.

For example, a repository used primarily to preserve reference material can use `arch` while retaining the same project number:

```text
arch.2026-001-04-hub75-reference-data.PRV
```

## Standalone Repositories

A more specific prefix is used when a repository is not part of a complex multidisciplinary project.

Examples:

```text
cad.2026-002-01-router-roof-mount.PRV
code.2026-003-01-deployment-tools.PRV
diy.2026-004-01-folding-workbench.PRV
site.2026-005-01-portfolio-web.PRV
```

Practical distinction:

```text
cad  = digital design or 3D-printable part
mech = mechanical system or assembly
diy  = practical physical build project
code = standalone software, firmware or scripts
site = standalone website or web application
proj = complex project where the shared project identity is most important
```

## Archive Repositories

The `arch` prefix is used for repositories whose primary purpose is preserving data or documents.

This may include:

- Project documentation
- Reference files
- Exported data
- Historical versions
- Research material
- Configuration backups
- Datasheets
- Images and measurements
- Files that should be protected against accidental deletion
- Material that does not belong in an active software, website or mechanical repository

Example:

```text
arch.2026-001-04-hub75-reference-data.PRV
```

Using Git provides an additional recovery layer compared with ordinary cloud-storage folders.

Deleted or changed files can normally still be recovered from earlier commits, provided that the repository and its history are retained.

An archive repository is not necessarily inactive.

The `arch` prefix describes the purpose of the repository, not its current status.

## Fork Repositories

The `fork` prefix is used for official GitHub forks.

An official fork remains connected to the original repository through GitHub's fork network.

### Naming

```text
fork.<year>-<project-number>-<subproject-number>-<upstream-name>
```

Example:

```text
fork.2026-006-01-purecutcnc
```

The upstream project name should remain recognisable in the repository description.

A fork of a public repository is public and therefore does not use the `.PRV` suffix.

### Fork Name

A fork can be given a different repository name while it is being created on GitHub.

The renamed fork remains connected to the original upstream repository.

The fork can therefore follow this naming convention while preserving the official fork relationship.

### Local Remotes

A local checkout of a fork normally uses:

```text
origin   = personal GitHub fork
upstream = original repository
```

Example:

```text
origin    https://github.com/username/fork.2026-006-01-purecutcnc.git
upstream  https://github.com/PureCutCNC/purecutcnc.git
```

When the `upstream` remote is missing, it can be added manually:

```powershell
git remote add upstream https://github.com/PureCutCNC/purecutcnc.git
```

Verify the remotes:

```powershell
git remote -v
```

Fetch changes from the original repository:

```powershell
git fetch upstream
```

### Independent Private Copy

A private copy that is not part of the official GitHub fork network uses a normal repository-type prefix instead:

```text
code.2026-006-01-purecutcnc-experiments.PRV
```

The distinction is:

```text
fork = official GitHub fork connected to upstream
code = independent software repository
```

An independent private copy may be more suitable when:

- Private experiments are required
- Changes are not intended to be contributed upstream
- The project will diverge substantially
- The official GitHub fork relationship is not useful

## Daily Development Steps

Daily tags are used to keep small development steps recognisable, ordered and easy to compare.

The daily tags provide the small-step structure inside each subproject repository.

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

The repository and subproject numbers identify where the work belongs.

The daily tags identify the smaller development states inside that repository.

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

GitHub Topics provide another way to classify and filter repositories without changing their names.

### Domain Topics

Possible domain topics include:

```text
project
mechanical
cad
diy
software
firmware
website
documentation
data
archive
fork
electronics
embedded
```

### Technology Topics

Possible technology topics include:

```text
openscad
java
esp32
raspberry-pi
hugo
docsify
hub75
```

### Status Topics

Possible status topics include:

```text
active
experimental
paused
archived
```

The `archived` topic is a status and is separate from the `arch` repository prefix.

For example, an actively maintained archive repository could be:

```text
arch.2026-001-04-hub75-reference-data.PRV
```

with topics such as:

```text
archive
documentation
hub75
active
```

A complex project repository could use:

```text
project
mechanical
cad
hub75
active
```

An actively maintained fork could use:

```text
fork
software
cnc
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
prefix            = first visual filter and repository type
year              = year in which the main project started
project number    = sequence of the main project within that year
subproject number = separate repository within the main project
description       = purpose of the repository or recognisable upstream name
classification    = additional visual visibility check
GitHub Topics     = discipline, technology and status
Git tags          = small development steps, snapshots and milestones
GitHub setting    = actual public or private visibility
```

The repeated information is intentional where it provides an additional visual check or reduces the need to remember hidden context.

## Initial Convention

```text
<prefix>.<year>-<project-number>-<subproject-number>-<description>.<classification>
```

Complex project examples:

```text
proj.2026-001-01-hub75-display-enclosure.PRV
proj.2026-001-02-hub75-electronics-frame.PRV
proj.2026-001-03-hub75-controller.PRV
arch.2026-001-04-hub75-reference-data.PRV
```

Standalone repository examples:

```text
cad.2026-002-01-router-roof-mount.PRV
code.2026-003-01-deployment-tools.PRV
diy.2026-004-01-folding-workbench.PRV
site.2026-005-01-portfolio-web.PRV
```

Official public fork example:

```text
fork.2026-006-01-purecutcnc
```

Independent private copy example:

```text
code.2026-006-01-purecutcnc-experiments.PRV
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