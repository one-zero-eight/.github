# Contribution Guide

Hi, we are excited that you are interested in contribution!
This is a general contributing guidelines for _one-zero-eight_ projects.
Before submitting your contribution, please take a moment to read through this guide.

### How can I contribute?

There are multiple ways how you can help:

- 🐞 **Report a bug or request a feature**<br/>Go to the related repository and create a new issue for the bug/feature (go to `Issues` → `New Issue`).
- 💡 **Suggest an idea**<br/>In case you belive we lack something at Innopolis, we have a [one-zero-eight/roadmap](https://github.com/one-zero-eight/roadmap) repository, where you can open an issue to suggest your idea (your authorship will be preserved!).
- ✍️ **Send a feedback**<br/>If you have something to say about our activity, projects or anything else, you can send a feedback with [this Google Form](https://forms.gle/yqtqobmt44CB6fFW7).
- 🧑🏻‍💻 **Write code**<br/>Pick up an issue from [the board](https://github.com/orgs/one-zero-eight/projects/4) and continue reading this guide, if you want to send a pull request to one of our repositories.

## Sending Pull Request

### English only

Use English language everywhere on GitHub: in the code, comments, documentation, issues, PRs.

<details>
<summary>Why?</summary>

<br/>Most of us are Russian-speaking and we love Russian (🤍💙❤️), though we believe there are benefits of using English here:

1. **Bigger community:** there are many non-Russian speaking students studying and living in Innopolis, and everyone should be able to contribute.
2. **Open-source:** contributing to the global open-source community today is the crucial part of becoming a professional software engineer, and it's easier to so, if you use English.
3. Finally, practicing a foreign language has many benefits by itself (boosting brain activity, career benefits, etc.).
</details>

### Before you start

**For features:** before you start to work on a new feature, it's better to open a feature request issue first to discuss with the maintainers and other contributors whether the features is desired and decide on its design.
This can save time for everyone and help features to be deliveried faster.

**For small changes:** it's better to batch multiple typo fixes and small refactoring changes into one pull request to keep the commit history clean.

### Commit convention

We follow [Conventional Commits](https://www.conventionalcommits.org/) so changelogs can be auto-generated.
Use this format:

```
<type>(<optional scope>): <short description in imperative mood>
```

**Scope** is optional: name the area you touched, most probably it will be the service name or page name (`clubs`, `maps`, etc.).

- **feat** — new feature or user-visible behavior.  
  e.g. `feat(maps): add floor picker to map viewer`
- **fix** — bug fix in application logic.
  e.g. `fix(clubs): reject empty club description on update`
- **chore** — housekeeping with no user-facing behavior change (we use this often). Tooling, config,
  repo layout, small cleanups, typos in docs when you do not want a `docs:` commit.  
  e.g. `chore: update prek hook revisions`, `chore(maps): rename internal settings key`
- **docs** — documentation only (README, comments, guides).
  e.g. `docs: fix typo in contribution guide`
- **test** — add or change tests only.  
  e.g. `test(maps): cover scene list pagination`
- **refactor** — restructuring or rewriting application code for clarity or quality, with
  the same behavior as before (extract modules, rename layers, simplify control flow). Not for config,
  tooling, or repo housekeeping — use `chore` for those.  
  e.g. `refactor(clubs): split repository into read and write modules`
- **perf** — performance improvement.  
  e.g. `perf(maps): cache scene thumbnails in memory`
- **style** — formatting, whitespace, lint fixes that do not change behavior.  
  e.g. `style: apply ruff format to student_affairs routes`
- **build** — build system or dependencies (`pyproject.toml`, `uv.lock`, Docker).  
  e.g. `build: bump fastapi to 0.115.0`
- **ci** — CI config and scripts (GitHub Actions, hooks).  
  e.g. `ci: run pytest on pull request`

**feat** and **fix** are for **changes that affect runtime behavior**. When in doubt, use **chore** for
anything that does not change what users see or how the app runs.

- typo or README only → `docs: …` (not `fix: typo`)
- dependency or lockfile bump → `build: …`
- test-only PR → `test: …` or `test(scope): …`
- rewrite or reorganize service code, same behavior → `refactor(scope): …` (not `chore:`)

See the [Conventional Commits spec](https://www.conventionalcommits.org/) for details.

### Creating pull request

> If you have troubles creating a pull request, [this guide](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) might help.

It's ok to have multiple commits in a single PR, you don't need to rebase or force push anything, because we will `Squash and Merge` the PR into one commit.

**Title**

Your title should also follow the Conventional Commits. An example of a good PR title would be:

```
feat: add animated snowfall background
```

**Description**

Make sure your PR have a clear description of the changes made and the reason behind them.
If your PR closes an existing issue (e.g. #123), make sure to mention it using [built-in GitHub functionality](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue#linking-a-pull-request-to-an-issue-using-a-keyword), so it will be automatically closed once the PR gets merged:

```markdown
...

Fixes #123.
```
