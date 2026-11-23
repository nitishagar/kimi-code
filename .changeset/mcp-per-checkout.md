---
"@moonshot-ai/agent-core-v2": minor
---

Give a project one set of MCP servers per git checkout. A set reads `.kimi-code/mcp.json` from, and starts stdio servers without a `cwd` in, the place the project's primary directory takes in that checkout, next to the checkout's `.mcp.json`. Sessions in a subdirectory use the set of their checkout, so a subdirectory's own `.kimi-code/mcp.json` is no longer read; sessions outside the repository keep the set of the primary directory, and a session whose directory has been deleted gets user-level servers only. The trust disclosure and the MCP registry list the set a session in that directory would use.
