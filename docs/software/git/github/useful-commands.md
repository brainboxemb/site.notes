# Useful GitHub Commands

This page contains useful Git and GitHub commands for recurring repository-management tasks.

## Clone a Repository Manually

Open the parent directory in the Visual Studio Code terminal:

```powershell
cd C:\projects
```

Clone the repository with an explicit GitHub username:

```powershell
git clone https://username@github.com/username/repository-name.git
```

Example:

```powershell
git clone https://github-user@github.com/github-user/cad.2026-002-01-hub75-display-enclosure.PRV.git
```

Open the cloned repository in Visual Studio Code:

```powershell
cd cad.2026-002-01-hub75-display-enclosure.PRV
code .
```

Verify the remote:

```powershell
git remote -v
```

Including the username in the HTTPS URL makes the intended GitHub account explicit.

Authentication is still handled separately, normally through Git Credential Manager.

## Update Origin After Renaming a GitHub Repository

When a repository is renamed on GitHub, the remote URL in an existing local checkout may still contain the old repository name.

Check the current remote:

```powershell
git remote -v
```

Update `origin`:

```powershell
git remote set-url origin https://github.com/username/new-repository-name.git
```

When using an explicit GitHub username in the URL:

```powershell
git remote set-url origin https://username@github.com/username/new-repository-name.git
```

For SSH:

```powershell
git remote set-url origin git@github.com:username/new-repository-name.git
```

Verify and test the new remote:

```powershell
git remote -v
git fetch origin
```

Example:

```powershell
git remote set-url origin https://github.com/username/site.2026-001-01-hugo-step001.PRV.git
```

## Notes

GitHub may redirect the old repository URL after a rename, but updating the local remote keeps the configuration clear and current.


## Create a Tag Using the GitHub Web Interface

GitHub does not provide a prominent standalone button for creating a tag in the normal repository view.

A tag can be created through the release interface:

1. Open the repository on GitHub.
2. Open **Releases**.
3. Select **Draft a new release**.
4. Enter the required tag name.
5. Select **Create new tag** and choose the target branch or commit.
6. Publish the release.

The release can be deleted afterwards while keeping the tag.

When deleting the release, do not select the option to also delete the associated tag.

This video demonstrates the process:

[YouTube — Create a Git Tag Using the GitHub Web Interface](https://www.youtube.com/watch?v=ktGLZDy3oc0)

This method can be useful for creating tags such as:

```text
daily/20260729
milestone/first-working-build
```