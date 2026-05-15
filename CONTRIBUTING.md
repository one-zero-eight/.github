# Contribution Guide

Hi, we are excited that you are interested in contribution!
This is a general contributing guidelines for _one-zero-eight_ projects.
Before submitting your contribution, please take a moment to read through this guide.

## How can I contribute?

There are multiple ways how you can help:

- 🐞 **Report a bug or request a feature**<br/>Go to the related repository and create a new issue for the bug/feature (go to `Issues` → `New Issue`).
- 💡 **Suggest an idea**<br/>In case you belive we lack something at Innopolis, we have a [one-zero-eight/roadmap](https://github.com/one-zero-eight/roadmap) repository, where you can open an issue to suggest your idea (your authorship will be preserved!).
- ✍️ **Send a feedback**<br/>If you have something to say about our activity, projects or anything else, you can send a feedback with [this Google Form](https://forms.gle/yqtqobmt44CB6fFW7).
- 🧑🏻‍💻 **Write code**<br/>Pick up an issue from [the board](https://github.com/orgs/one-zero-eight/projects/4) and continue reading this guide, if you want to send a pull request to one of our repositories.


## English only

Use English language everywhere on GitHub: in the code, comments, documentation, issues, PRs.

<details>
<summary>Why?</summary>

<br/>Most of us are Russian-speaking and we love Russian (🤍💙❤️), though we believe there are benefits of using English here:

1. **Bigger community:** there are many non-Russian speaking students studying and living in Innopolis, and everyone should be able to contribute.
2. **Open-source:** contributing to the global open-source community today is the crucial part of becoming a professional software engineer, and it's easier to so, if you use English.
3. Finally, practicing a foreign language has many benefits by itself (boosting brain activity, career benefits, etc.).
</details>

## Sending Pull Request

#### Before you start

**For features:** before you start to work on a new feature, it's better to open a feature request issue first to discuss with the maintainers and other contributors whether the features is desired and decide on its design.
This can save time for everyone and help features to be deliveried faster.

**For small changes:** it's better to batch multiple typo fixes and small refactoring changes into one pull request to keep the commit history clean.

#### Commit convention

We follow [Conventional Commits](https://www.conventionalcommits.org/) so changelogs can be auto-generated.
Use this format:

```
<type>(<optional scope>): <short description in imperative mood>
```

<details>
<summary>More info</summary>


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
</details>

See the [Conventional Commits spec](https://www.conventionalcommits.org/) for details.

#### Creating pull request

> If you have troubles creating a pull request, [this guide](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) might help.

It's ok to have multiple commits in a single PR, you don't need to rebase or force push anything, because we will `Squash and Merge` the PR into one commit.

Your **title** should also follow the Conventional Commits. An example of a good PR title would be:

```
feat: add animated snowfall background
```

Make sure your PR have a clear **description** of the changes made and the reason behind them.
If your PR closes an existing issue (e.g. #123), make sure to mention it using [built-in GitHub functionality](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue#linking-a-pull-request-to-an-issue-using-a-keyword), so it will be automatically closed once the PR gets merged:

```markdown
...

Fixes #123.
```

## Prerequisites

Before taking an issue, make sure you can do three things:

1. Use Git and GitHub.
2. Use your IDE effectively.
3. Connect your work to the assigned issue.

#### Git and GitHub

You should know how to:

- Fork or clone the repository and pull the latest changes before starting.
- Create a separate branch for your work (do not work on the default branch).
- Make small, meaningful commits with Conventional Commit messages.
- Push your branch and open a pull request.
- Update the pull request after review.
- Resolve simple merge conflicts.

Do not mix unrelated changes in one pull request.

Your commit messages and pull request titles should follow [Conventional Commits](#commit-convention).

Examples:

```text
feat(clubs): add club search by name
fix(maps): handle missing room coordinates
docs: clarify contribution guide
```

#### IDE skills

We expect contributors to know basic IDE features. You should be able to:

- Open the project correctly.
- Navigate to files and symbols.
- Search across the whole project.
- Use “Go to definition”.
- Use rename/refactor tools instead of manual search-and-replace.
- See changed files.
- View diffs before committing.
- Stage selected files or selected lines.
- Commit and push from the IDE.
- Resolve simple Git conflicts using the IDE.
- Run the project, tests, and commands from the **integrated terminal** in your IDE (do not open extra terminals outside the editor).
- Debug with breakpoints.

Using Git from the terminal is allowed, but beginners are strongly encouraged to use the IDE Git tools first. Keep one integrated terminal open in the project root so paths, virtual environments, and environment variables stay consistent. The IDE makes it easier to inspect diffs, stage only the intended changes, resolve conflicts, run tests, and debug problems before opening a pull request.

At minimum, you should know how to commit, inspect diffs, push, pull, resolve simple conflicts, run tests, and debug from your IDE.

We recommend **VS Code** as the default editor path. If you use **PyCharm**, see the PyCharm links under [Learning resources](#learning-resources).

#### Working on an assigned issue

If you are assigned to an issue, your pull request should be connected to that issue.

Before starting:

1. Read the issue carefully.
2. Ask questions in the issue comments if the task is unclear.
3. Do not start large implementation work before the expected behavior is clear.
4. Create a branch for this issue.
5. Keep the pull request focused on solving this issue only.
6. Mention the issue in the pull request description.
7. Before committing, run linter and formatter and fix any issues.
8. When you think you're done, test again, and push your changes.
9. Notify maintainers both in the issue and in the Telegram chat.

When opening the pull request, mention the issue in the description:

```markdown
Fixes #123.
```

This automatically links the pull request to the issue and closes the issue when the pull request is merged.

If your pull request only partially solves the issue, use:

```markdown
Relates to #123.
```

Do not include unrelated refactoring, formatting, or dependency updates in the same pull request unless a maintainer asks for it.


## Learning resources

#### Git and GitHub

- [Git & GitHub Crash Course for Beginners [2026]](https://www.youtube.com/watch?v=mAFoROnOfHs) — clone, branch, commit, push, pull, merge conflicts, and pull requests.

#### Pull requests

- [How to Raise a Pull Request Step by Step](https://www.youtube.com/watch?v=tWQCS5hF75w) — opening a pull request.

#### VS Code

1. [Visual Studio Code Crash Course](https://www.youtube.com/watch?v=WPqXP_kLzpo)
2. [Git & GitHub for Beginners: Complete VS Code Workflow Tutorial](https://www.youtube.com/watch?v=zInxGrvtbwA)
3. [Python in VS Code](https://www.youtube.com/watch?v=1G7U1YV01rE)
4. [How to Debug Python in VS Code](https://www.youtube.com/watch?v=7qZBwhSlfOo)

#### PyCharm

1. [Getting Started with PyCharm](https://www.youtube.com/watch?v=QJtWxm12Eo0)
2. [Introduction to Git and GitHub in PyCharm](https://www.youtube.com/watch?v=Pwku4tD6JvU)
3. [Python - Introducing the PyCharm Debugger](https://www.youtube.com/watch?v=YUUPiHPtvos)
