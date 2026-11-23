---
"@moonshot-ai/kap-server": minor
---

`POST /api/v1/sessions` places sessions with the implicit-project resolver: a request with only `cwd` inside a git repository joins the implicit workspace of the repository's main checkout. With `workspace_id`, `cwd` may also be another directory of the workspace root's git repository: its main checkout, a linked worktree, or a subdirectory of either, or, when the root is a subdirectory of the repository, that subdirectory in each checkout. Every other `cwd` still returns `40001`, additional directories and nested repositories included, and paths are compared after resolving symlinks. A session started away from the workspace root stays in its directory when the root changes, `Session.cwd` reports the directory the session runs in, and a session whose local `environment_cwd` is in another checkout of the root's repository uses the MCP servers of that checkout.
