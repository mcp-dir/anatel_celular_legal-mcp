# Instalação rápida

Anatel: Consulta Celular Legal é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_anatel_celular_legal`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Anatel: Consulta Celular Legal` / `https://api.mcp.ai/p_anatel_celular_legal`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "anatel_celular_legal": { "type": "http", "url": "https://api.mcp.ai/p_anatel_celular_legal" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=anatel_celular_legal&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9hbmF0ZWxfY2VsdWxhcl9sZWdhbCJ9)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "anatel_celular_legal": { "url": "https://api.mcp.ai/p_anatel_celular_legal" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=anatel_celular_legal&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_anatel_celular_legal%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "anatel_celular_legal": { "type": "http", "url": "https://api.mcp.ai/p_anatel_celular_legal" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_anatel_celular_legal
```

Dúvidas? [anatel_celular_legal@mcp.ai](mailto:anatel_celular_legal@mcp.ai)
