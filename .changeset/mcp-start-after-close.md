---
"@moonshot-ai/agent-core-v2": patch
---

Fix MCP servers, including session-provided ones, starting and staying up after the project or session they belong to has closed, when it closes before they finish starting: before their first load, while the environment of a stdio server is still connecting, or while its process is being spawned.
