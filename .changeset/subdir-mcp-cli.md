---
"@moonshot-ai/kimi-code": patch
---

In a subdirectory of a git repository, load project MCP servers from `.kimi-code/mcp.json` at the checkout root instead of the subdirectory; move a subdirectory's file there to keep using it. A subdirectory that already has its own project with sessions keeps reading its own file.
