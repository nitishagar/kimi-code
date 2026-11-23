---
"@moonshot-ai/agent-core-v2": patch
---

Start the MCP servers of a project with the first session that uses them, or with the query that lists them, instead of when the project opens, and stop them when the last one is done with them instead of when the project closes. Project readiness no longer waits for them, and the project snapshot lists them only while they are in use. The project no longer exposes its MCP servers directly: callers borrow them and give them back when they are done.
