# Visão Geral da API

## Introdução

A API do ASOF foi projetada seguindo os princípios RESTful, oferecendo endpoints intuitivos e bem documentados para todas as operações principais.

## Autenticação

A API utiliza autenticação via token JWT. Para obter um token:

```bash
curl -X POST https://api.asof.com/auth/token \
  -H "Content-Type: application/json" \
  -d '{"username": "seu_usuario", "password": "sua_senha"}'
```

## Formato das Requisições

Todas as requisições devem incluir:

- Header `Content-Type: application/json`
- Header `Authorization: Bearer seu_token` (exceto para autenticação)

## Endpoints Principais

### Recursos

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| GET    | /api/v1/recursos | Lista todos os recursos |
| POST   | /api/v1/recursos | Cria um novo recurso |
| GET    | /api/v1/recursos/{id} | Obtém um recurso específico |
| PUT    | /api/v1/recursos/{id} | Atualiza um recurso |
| DELETE | /api/v1/recursos/{id} | Remove um recurso |

### Exemplo de Resposta

```json
{
  "data": {
    "id": "123",
    "tipo": "recurso",
    "atributos": {
      "nome": "Exemplo",
      "descricao": "Um recurso de exemplo"
    }
  },
  "meta": {
    "timestamp": "2024-03-14T12:00:00Z"
  }
}
```

## Códigos de Status

| Código | Significado |
|--------|-------------|
| 200    | Sucesso |
| 201    | Criado com sucesso |
| 400    | Requisição inválida |
| 401    | Não autorizado |
| 403    | Proibido |
| 404    | Não encontrado |
| 500    | Erro interno |

## Rate Limiting

- 1000 requisições por hora por IP
- 10000 requisições por hora por token de API

## Webhooks

Configure webhooks para receber notificações de eventos:

```bash
curl -X POST https://api.asof.com/webhooks \
  -H "Authorization: Bearer seu_token" \
  -H "Content-Type: application/json" \
  -d '{
    "url": "https://seu-dominio.com/webhook",
    "eventos": ["recurso.criado", "recurso.atualizado"]
  }'
```

## SDKs Oficiais

- [Python SDK](https://github.com/seu-usuario/asof-python)
- [JavaScript SDK](https://github.com/seu-usuario/asof-js)
- [Go SDK](https://github.com/seu-usuario/asof-go)

## Suporte

- [Documentação Detalhada](../dev-guide/api-reference.md)
- [Exemplos de Integração](https://github.com/seu-usuario/asof-examples)
- [Status da API](https://status.asof.com) 