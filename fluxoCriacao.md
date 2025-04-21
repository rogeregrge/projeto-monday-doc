# Passo a Passo do Projeto – Integração com monday.com

---

## Início do Projeto

### Inicialização com Vite + React

```bash
npm create vite@latest projeto-monday-doc --template react
cd projeto-monday-doc
npm install
```

### Instalação do SDK da monday

```bash
npm install monday-sdk-js
```

---

## Configuração do Ambiente

### Inicialização do SDK

No componente principal (ex: `BoardItemsList.jsx`):

```js
import mondaySdk from "monday-sdk-js";

const monday = mondaySdk();
```

### Obtenção do Contexto da monday

```js
useEffect(() => {
  monday.get("context").then((res) => {
    const boardId = res.data.boardId;
    fetchBoardData(boardId);
  });
}, []);
```

---

## Criação da Query GraphQL

### Estrutura da query

```js
const query = \`
  query {
    boards(ids: \${boardId}) {
      columns {
        id
        title
      }
      items_page(limit: 50) {
        items {
          id
          name
          column_values {
            id
            text
          }
        }
      }
    }
  }
\`;

monday.api(query).then((res) => {
  setItems(res.data.boards[0].items_page.items);
  setColumns(res.data.boards[0].columns);
});
```

---

## Deploy com Vercel

###  Integração com GitHub

```bash
git init
git remote add origin https://github.com/seu-usuario/projeto-monday-doc.git
git push -u origin main
```

### Conexão com Vercel

- Importar projeto do GitHub
- Definir comandos:
  - Build: `npm run build`
  - Dev: `npm run dev`
- URL gerada:  
  `https://projeto-monday.vercel.app`

### Registro no Developer Center da monday

- Criar App
- Cadastrar URL do iframe:
  `https://projeto-monday.vercel.app`
- Configurar permissões e scopes

---

## Conclusão

- Dados do board exibidos dinamicamente
- Integração GraphQL + SDK funcionando
- Deploy automatizado com Vercel
- Projeto pronto para escalar com CI/CD e novas views
