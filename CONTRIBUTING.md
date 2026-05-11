# Contributing to bsg.wtf

Thanks for helping build this community URL shortener. Keep changes focused, match **[README.md](README.md)**, and prefer small pull requests.

## Where to look first

- **[README.md](README.md)** — canonical product, API, schema, and stack for this repo.
- **[README §11](README.md#11-github-issue-breakdown)** — high-level task list and weekly targets.
- **GitHub Issues** — concrete work items: acceptance criteria, discussion, and assignment live on the issue.

If the README and an older Google Doc disagree, follow the **README** until maintainers sync the doc.

## Claiming work

1. Find an **open issue** you want to work on.
2. **Comment on that issue** asking to be assigned (or stating you are starting it, per maintainer process).
3. Wait until a maintainer **assigns the issue to you** before opening a large PR, so two people do not duplicate effort.

## Forks and branches

- **Fork** this repository to your GitHub account (do not push feature branches to the upstream repo unless maintainers give you write access).
- Create a **branch** on your fork (e.g. `feat/post-urls-handler`, `fix/canonicalize-host`).
- Open a **pull request** from your fork into the community default branch (usually `main`).

## Linking your PR to the issue

When your PR implements work for **the issue assigned to you**, put a **closing or reference keyword** and the **correct issue reference** in the PR **description** (not only in a comment), so GitHub links the work and can auto-close the issue on merge.

- **Pull requests from a fork** into this project (typical for contributors): use the **full upstream repo** form GitHub accepts, e.g. **`Closes backendstudy-group/bsg.wtf#12`** — replace **`12`** with the **issue number you were assigned** (example: `Fixes backendstudy-group/bsg.wtf#5`).
- **Same repository** (you have write access and the PR targets this repo with issues here): `Closes #12` or `Fixes #12` also works.

Always **verify the issue number** before opening the PR so you do **not** close the wrong issue.

Official reference: [Linking a pull request to an issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/linking-a-pull-request-to-an-issue).

## PR description

Include:

- **What** changed and **why**
- How a reviewer can **verify** (commands, env vars, sample requests)
- The **issue link** line above when the PR completes assigned work

## Questions and blocked work

1. Prefer a **new issue** for standalone questions, or a **comment on the existing issue** if the question is about that task.
2. If you get **no timely response**, post in the **general BSG group** channel and **tag reviewers** or other maintainers named in the README (e.g. **Reviewers** in §11).

## Community norms

- Be respectful and constructive.
- Do not commit secrets, real credentials, or personal data.

## Code expectations (Go)

When application code exists in this repo:

- Run **`go fmt ./...`** and **`go vet ./...`** before opening a PR.
- Follow **README §9** (chi, slog, pgx, goose, go-redis) unless the issue explicitly agrees a narrow exception with maintainers.
- **Tests:** follow what the **GitHub issue** asks for (and what reviewers agree in the PR). Add regression tests when fixing incorrect behavior.

## Database and migrations

- Use **goose** and SQL migrations as specified in the README and the issue.
- Keep migration up/down paths reversible; do not embed production secrets.

## Documentation

- Update **README.md** when you change public API behavior, status codes, or schema.
- Keep **diagrams** under `docs/` if you replace images; keep PNGs reasonably small.

Maintainers may request edits or smaller PRs to keep review load manageable. Thanks again for contributing.
