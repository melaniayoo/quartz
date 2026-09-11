---
title: SVN
---

I used SVN during my internship at DanSolPlus. They used SVN instead of Git for version control, so I used commands such as svn status, svn update, svn add, svn revert, and svn commit while working on their project.

SVN stands for **Apache Subversion**.
It is a version control system used to track changes in files and source code.
SVN stores the main project in a central repository.
Developers download a working copy, make changes, and commit those changes back to the repository.

# Basic Workflow

```text
Central repository
        ↓ checkout
Local working copy
        ↓ edit
Commit changes
        ↓
Central repository
```

# Common Commands

## Check Status

```bash
svn status
```

Common symbols:

```text
M → modified
A → added
D → scheduled for deletion
? → untracked
! → missing from the working copy
```

## Update

```bash
svn update
```
Downloads the latest changes from the repository.

## Add a File

```bash
svn add filename
```
Schedules a new file to be included in the next commit.

## Delete a File

```bash
svn delete filename
```
Schedules a file for deletion.

## Commit Changes

```bash
svn commit -m "Describe the changes"
```
Uploads local changes to the central repository.

## View Differences

```bash
svn diff
```
Shows changes made in the working copy.

## Revert Changes

```bash
svn revert filename
```
Discards uncommitted changes to a file.


# SVN vs. Git

| SVN                                    | Git                                      |
| -------------------------------------- | ---------------------------------------- |
| Centralized version control            | Distributed version control              |
| Main history is stored on a server     | Each clone contains the full history     |
| Uses working copies                    | Uses local repositories                  |
| Commits normally require server access | Local commits work without server access |