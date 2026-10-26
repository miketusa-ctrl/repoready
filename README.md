# RepoReady Lite — free, MIT (5 workflows)

By **Harlo** (formerly Digital Promo Hub). Not affiliated with GitHub, Inc.

**Demo CI:** https://github.com/miketusa-ctrl/repoready-demo (public; Node/Python/Go green)

**Download:** grab `RepoReady-Lite.zip` from this repo's Releases page.

5 CI-verified, SHA-pinned GitHub Actions workflows + repo hygiene. MIT licensed.

| File | What it does | Secrets / setup |
|---|---|---|
| `.github/workflows/ci-node.yml` | Node.js test matrix | none |
| `.github/workflows/ci-python.yml` | Python test matrix | none |
| `.github/workflows/ci-go.yml` | Go test matrix | none |
| `.github/workflows/release-on-tag.yml` | GitHub Release on v* tag | none (uses GITHUB_TOKEN, contents: write) |
| `.github/workflows/stale.yml` | Mark/close stale issues and PRs | none |

No-project-file safe: Node/Go jobs skip gracefully when `package.json`/`go.mod` is absent; Python falls back to `unittest`.

## Install
Copy the `.github/` folder (and `SECURITY.md`, `CONTRIBUTING.md`) into your repo root, commit, push. Workflows run on next push/PR.

## Customize
- Versions: edit the `matrix` lists (Node/Python/Go).
- Branch: replace `main` under `on.push.branches`.
- Every action is pinned to a full commit SHA with the version tag in a trailing comment; Dependabot (`.github/dependabot.yml`, weekly npm/pip/gomod/github-actions) keeps pins fresh.
- Hygiene: issue forms (`.github/ISSUE_TEMPLATE/`), `PULL_REQUEST_TEMPLATE.md`, `SECURITY.md`, `CONTRIBUTING.md`.

Support: digitalpromohub.support@gmail.com

## Want more? Paid tiers
- **RepoReady Pro — $19** (24 workflows: CodeQL, Pages deploy, Dependabot auto-merge, changelog, labeler, Docker publish, lint suites, link/license/secret checks...): https://miketusa.gumroad.com/l/repoready-pro
- **RepoReady Team — $39** (team license): https://miketusa.gumroad.com/l/repoready-team

## License
MIT — see `LICENSE`. GitHub and GitHub Actions are trademarks of GitHub, Inc.; this project is not affiliated with or endorsed by GitHub, Inc.
