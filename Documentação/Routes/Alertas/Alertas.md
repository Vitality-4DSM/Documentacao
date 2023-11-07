
# API de Gerenciamento de Alertas

Esta é uma documentação simples para a API de Gerenciamento de Alertas. A API permite criar, recuperar, atualizar e excluir alertas no sistema.

## Rotas:
- Rotas Usada para fazer as requisições:
   - routes.use("/alert", alert);
### Criar um Alerta

- **Método HTTP:** POST
- **URL:** `/`.alert
- **Descrição:** Cria um novo alerta.
- **Permissão:** Somente administradores podem criar alertas.

### Obter um Alerta por ID

- **Método HTTP:** GET
- **URL:** `/get`.alert
- **Descrição:** Obtém informações sobre um alerta com base em seu ID.
- **Permissão:** Público.

### Obter Todos os Alertas

- **Método HTTP:** GET
- **URL:** `/`.alert
- **Descrição:** Obtém uma lista de todos os alertas.
- **Permissão:** Público.

### Atualizar um Alerta

- **Método HTTP:** PUT
- **URL:** `/`.alert
- **Descrição:** Atualiza um alerta com base em seu ID.
- **Permissão:** Somente administradores podem atualizar alertas.

### Deletar um Alerta

- **Método HTTP:** DELETE
- **URL:** `/:id`.alert
- **Descrição:** Remove um alerta com base em seu ID.
- **Permissão:** Somente administradores podem excluir alertas.

### Resposta para Solicitações Desconhecidas

- **Descrição:** Todas as solicitações que não correspondem a nenhuma das rotas acima receberão uma resposta padrão indicando que a solicitação é desconhecida.

## Exemplos de Uso

Aqui estão alguns exemplos de como usar as rotas da API:

### Criar um Alerta

```bash
POST / HTTP/1.1
Content-Type: application/json
Authorization: Bearer <token>

{
  "valor": 30, // Valor do Alerta
  "sinal": "+", // Sinal da Operação 
   "fk_parametro": 1 // Identificador do Parametro
}
```
### Get por ID
```bash
GET /get HTTP/1.1
Content-Type: application/json

{
  "id": 123
}
```

### Atualizando um Alerta
```bash
GET /get HTTP/1.1
Content-Type: application/json
{
  "id": 123
  "Campo": "Nova_valor"      
}
```

### Delete de um Alerta
```bash
DELETE /123 HTTP/1.1   // ID passado pela URL
Authorization: Bearer <token>
```