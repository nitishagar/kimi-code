---
"@moonshot-ai/agent-core-v2": minor
---

Resolve implicit projects by git repository. A directory whose own implicit project already has sessions, archived ones included, keeps that project. Any other directory inside a git repository joins the implicit project of the repository's main checkout, unless the main checkout is the home directory or one of its ancestors, or an existing implicit project for it has since moved its primary directory elsewhere; every other directory gets its own implicit project as before. The main checkout is read from disk without running git: a linked worktree joins it only when its back pointer and common directory match, a forged or unreadable `.git` keeps the directory in its own project, and `core.bare` and `core.worktree` are also read from `config.worktree`. Every entry that creates implicit projects goes through this resolver, and lookups by directory that only read no longer register a project.
