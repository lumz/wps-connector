# wps-connector

WPS 云文档连接器（WPS Cloud Document Skill）—— 一个 **SkillHub MCP** 客户端，用于读写金山文档（wps.cn）云端文档、表格、权限与导出。

## English Introduction

This skill provides **WPS cloud document read/write** capabilities via the SkillHub MCP protocol. It is a **WPS Cloud Document Skill** — not a knowledge base.

Scope
-----
- Cloud document storage with permission control
- Document creation, read, and management
- Table & document data manipulation
- Export and sharing with permission control

Not a knowledge base
---------------------
This is a runtime document skill for automation (document CRUD, tables, permission control, export). It does **not** aggregate articles, store static knowledge, or replace document APIs.

Key features
-----------
- SkillHub MCP server: `https://mcp-center.wps.cn/skill_hub/mcp`
- 638 WPS tools (read, write, sheet, PDF, permission, export)
- Authentication via `wps_auth.py` (token in env file)

Use
---
1. Install: `hermes skills list` (wps-cloud-docs)
2. Auth: `scripts/wps_auth.py` (env file)
3. Connect: MCP client -> `https://mcp-center.wps.cn/skill_hub/mcp`
4. Docs: `skills/wps-cloud-docs/SKILL.md`

Publish
-------
- Local: `hermes skills publish --to github --repo lumz/wps-connector`
- Online: submit to skills.sh / clawhub (manual)

Notes
-----
- No secrets/keys in skill files
- Use env variable `${WPS_KDOCS_TOKEN}` in production
- Nodes without an API are marked "无此流程"; do not modify the document structure
