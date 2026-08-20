---
name: anatel_celular_legal-mcp
description: Skill da REST API do Anatel: Consulta Celular Legal na MCP.AI: 1 endpoint em /api/anatel_celular_legal. Anatel: Consulta Celular Legal, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Anatel: Consulta Celular Legal — REST API skill

Você tem acesso à **Anatel: Consulta Celular Legal** REST API na MCP.AI.

> Anatel: Consulta Celular Legal, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/anatel_celular_legal
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/anatel_celular_legal/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"imei":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/anatel_celular_legal/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `anatel_celular_legal_consultar`

Anatel: Consulta Celular Legal, consulta em fonte oficial. _(POST /api/anatel_celular_legal/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `imei` | string | Sim | Parâmetro de consulta "imei". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_anatel_celular_legal` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
