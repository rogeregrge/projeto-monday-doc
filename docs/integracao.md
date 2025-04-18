# Integração com a monday.com

## SDK Utilizado

- Biblioteca: `monday-sdk-js`
- Repositório oficial: [https://github.com/mondaycom/monday-sdk-js](https://github.com/mondaycom/monday-sdk-js)

## Instalação

```bash
npm install monday-sdk-js
```

## Permissões Necessárias

As permissões foram definidas no painel de desenvolvedor da monday.com, e são necessárias para que a aplicação consiga interagir com os dados da conta:

- `boards:read` – Leitura de estruturas de board.
- `users:read` – Acesso a dados do usuário logado.
- `updates:write` – Envio de atualizações no board (ainda não implementado).

## Leitura de Contexto

A aplicação utiliza o método `get("context")` para capturar dados contextuais como `boardId`, `itemId`, `userId`, etc.

### Exemplo de código:

```ts
import mondaySdk from "monday-sdk-js";

const monday = mondaySdk();

monday.get("context").then((res) => {
  const boardId = res.data.boardId;
  console.log("Board ID:", boardId);
});
```

## Requisições via GraphQL

A comunicação com a API da monday é feita utilizando o método `monday.api()` com queries GraphQL customizadas. Isso permite consultar itens, colunas e metadados do board diretamente da aplicação.

### Exemplo de consulta:

```ts
monday.api(`query {
  me {
    name
  }
}`);
```

## Observações

- A estrutura da aplicação foi criada manualmente, sem uso do comando `monday-cli scaffold`.
- Toda a configuração (URLs de redirecionamento, permissões, visualizações) foi realizada diretamente no painel de desenvolvedor da monday.com.
- A aplicação é incorporada por meio de iframe dentro da interface do board.

