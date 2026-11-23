---
"@moonshot-ai/kimi-code": patch
---

`kimi -c`, the session picker, `kimi session list`, `kimi fork` and `kimi export` now use only sessions that ran in the current directory, no longer sessions of desktop projects opened at or containing it; use `kimi session list --all` or `kimi -r <id>` to reach those.
