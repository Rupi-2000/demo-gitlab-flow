# GitLab Flow Demo Repository

## Purpose

This repository demonstrates GitLab Flow using a small Python FastAPI task management application.

## Application Scope

Initial version `v1.0.0` contains:

- task creation through REST API
- task completion through REST API
- listing all tasks
- listing open tasks
- SQLite database persistence
- version output
- automated tests
- CI workflow

Feature branches for priority, due dates, users, assignment, task status, bugfixes, promotion scenarios, and merge-conflict scenarios will be added later.

## Branching Strategy

GitLab Flow combines feature branches with environment branches. New work is integrated into `main`, then promoted to `staging`, and finally to `production`.

## Branch Overview

Current initial setup:

- `main`
- `staging`
- `production`

Planned later:

- `feature/add-task-priority`
- `feature/add-due-date`
- `feature/add-user-service`
- `feature/add-task-assignment`
- `feature/add-task-status`
- `bugfix/fix-task-completion`

## Promotion Flow

The planned environment promotion path is:

```text
feature branch -> main -> staging -> production
```

The initial version starts with all three environment branches pointing to the same `v1.0.0` commit.

## CI Setup

The CI workflow runs on `push` and `pull_request`.

It installs Python dependencies and runs the test suite with `python -m pytest`.

## Tags / Releases

- `v1.0.0`: initial base application

