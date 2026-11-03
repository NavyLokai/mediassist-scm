# MediAssist — SCM Repository

**Navy Lokai · Adm. No. 672415 · USIU-Africa**

MediAssist is an Android medication-reminder app for elderly users, with a Firebase backend and a caregiver dashboard. This repository holds the app and its Software Configuration Management (SCM) work.

## Branching strategy: GitHub Flow
- `main` is the only long-lived branch. It is protected and always releasable.
- All work happens on short-lived branches named `<type>/<issue#>-<short-description>`, for example `feature/12-snooze-reminder` or `fix/18-duplicate-alert`.
- Types: `feature`, `fix`, `hotfix`, `docs`, `test`, `chore`, `ci`.
- Branches live at most 2 working days, merge via pull request with squash-merge only, and are deleted after merge.
- Releases are SemVer tags on `main` (`v0.1.0`, `v1.0.0`, …).

See [CONTRIBUTING.md](CONTRIBUTING.md) for the full workflow.

## Coursework documents
| Week | Deliverable |
|------|-------------|
| 1 | [SCM requirements](docs/week1-scm-requirements.pdf) |
| 2 | [SCM / artifact-tracking database design](docs/week2-scm-database-design.pdf) |
| 3 | [Branching strategy and SCM plan](docs/week3-scm-plan.pdf) |
