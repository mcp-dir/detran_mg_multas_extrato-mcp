# Instalação rápida

DETRAN MG: Multas (Extrato) é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_detran_mg_multas_extrato`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `DETRAN MG: Multas (Extrato)` / `https://api.mcp.ai/p_detran_mg_multas_extrato`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "detran_mg_multas_extrato": { "type": "http", "url": "https://api.mcp.ai/p_detran_mg_multas_extrato" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=detran_mg_multas_extrato&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9kZXRyYW5fbWdfbXVsdGFzX2V4dHJhdG8ifQ==)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "detran_mg_multas_extrato": { "url": "https://api.mcp.ai/p_detran_mg_multas_extrato" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=detran_mg_multas_extrato&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_detran_mg_multas_extrato%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "detran_mg_multas_extrato": { "type": "http", "url": "https://api.mcp.ai/p_detran_mg_multas_extrato" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_detran_mg_multas_extrato
```

Dúvidas? [detran_mg_multas_extrato@mcp.ai](mailto:detran_mg_multas_extrato@mcp.ai)
