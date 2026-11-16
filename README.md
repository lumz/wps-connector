# wps-connector

WPS 云文档连接器（WPS Cloud Document Skill）—— 一个 **SkillHub MCP** 客户端，用于读写金山文档（wps.cn）云端文档、表格、权限与导出。

> 注意：这是 **WPS 云文档技能**，与知识库无关。知识库是另一篇文章/文档内容。

## 目录

- `skills/wps-cloud-docs/` — 技能主体（SKILL.md、协议、脚本）
- `README.md` — 本说明

## 如何使用

1. 安装/启用技能：`hermes skills list` 可见 `wps-cloud-docs`
2. 认证：`scripts/wps_auth.py`（token 写入环境变量）
3. 连接：使用 MCP 客户端连接 `https://mcp-center.wps.cn/skill_hub/mcp`
4. 查看文档：`skills/wps-cloud-docs/SKILL.md` 含完整用法

## 发布

- 本地：`hermes skills publish --to github --repo lumz/wps-connector`
- 官方注册：可提交到 clawhub 或 skills.sh

## 注意

- 本技能文件中不含任何密钥/令牌
- 生产环境请使用环境变量 `${WPS_KDOCS_TOKEN}` 传入
- 无对应接口的节点标注「无此接口」；文档结构不可随意修改
