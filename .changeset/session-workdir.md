---
"@moonshot-ai/agent-core-v2": minor
---

Give each session its own working directory. A new local session that starts away from its project's primary directory records that directory as its `environmentCwd` and stays there; one that starts in the primary directory follows it, as before. Instructions, skills, agents and `local.toml` come from the session's own directory, sessions in another checkout or a subdirectory of the repository also get the project's additional directories, and a broken `local.toml` in one checkout no longer fails the sessions of another. A session whose directory has been deleted can still be opened, archived and deleted. Add a listing of the sessions of one directory's implicit project that run in that directory, and report the session directory in export manifests.
