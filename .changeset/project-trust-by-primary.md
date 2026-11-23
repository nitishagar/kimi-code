---
"@moonshot-ai/agent-core-v2": minor
---

Trust a project through its primary directory alone. A project is trusted exactly when its primary directory has a trust record, and that trust covers every session of the project wherever it runs. Trust records of additional directories, `local.toml` directories and `--add-dir` directories no longer make a project trusted, and changing a managed project's primary directory carries its trust to the new primary.
