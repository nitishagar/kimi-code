---
"@moonshot-ai/agent-core-v2": patch
"@moonshot-ai/kap-server": patch
---

Report a file root that does not exist as not found (`40409` on the KAP file endpoints) when its parent is reached through a symlink, instead of as escaping the session (`41304`).
