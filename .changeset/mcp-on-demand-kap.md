---
"@moonshot-ai/kap-server": patch
---

Start the MCP servers of a workspace with its first open session and stop them when the last one closes. Requests that leave a session closed, such as forking, archiving, or deleting one that is not open, no longer start them.
