# Contributing to MediAssist

## 1. Start from an issue
Every change starts as a GitHub Issue. Use the **Bug report**, **Feature request** or **Change request** template.
Changes to reminder scheduling, caregiver alerts, authentication, Firebase rules or dependencies are **critical-area** changes and need an impact analysis in the issue.

## 2. Branch
```bash
git switch main
git pull --rebase origin main
git switch -c feature/<issue#>-<short-desc>   # or fix/, hotfix/, docs/, test/, chore/, ci/
```
Keep a branch to at most 2 working days and about 400 changed lines. Split larger work, or hide it behind a feature flag.

## 3. Commit
Use [Conventional Commits](https://www.conventionalcommits.org/): `feat:`, `fix:`, `docs:`, `test:`, `chore:`, `ci:`.
Write an imperative subject of 50 characters or fewer, and explain *why* in the body.

## 4. Open a pull request
```bash
git push -u origin feature/<issue#>-<short-desc>
```
Open the PR against `main`, fill in the template, and write `Closes #<issue#>`.

## 5. Merge rules (enforced on `main`)
- No direct pushes or force-pushes to `main`.
- The `ci` check must pass and the branch must be up to date.
- All review conversations must be resolved.
- Critical-area PRs need a second reviewer, or a 12-hour wait before self-merge while the project has one developer, plus a test on a physical device.
- Use **Squash and merge** only. The branch is deleted automatically.

## 6. Hotfixes
Branch `hotfix/<issue#>-<desc>` from `main`, keep the fix minimal, open an expedited PR (CI still required), then tag a PATCH release.

## 7. Releases
Tag `main` with an annotated SemVer tag (`git tag -a v1.2.0 -m "Release 1.2.0"` then `git push origin v1.2.0`). The `release.yml` workflow builds and publishes the release.
