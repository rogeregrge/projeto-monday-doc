# projeto-monday-docs

Documentação completa do projeto [projeto-monday](https://github.com/rogeregrge/projeto-monday), que demonstra como integrar aplicações externas à plataforma monday.com utilizando React, Vite, GraphQL e o SDK oficial da monday.

## Badges

- [![Vercel](https://vercel.com/button)](https://projeto-monday.vercel.app/)
- [![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)  
- ![Made with React](https://img.shields.io/badge/made%20with-react-61DAFB?logo=react&logoColor=white)

---

## Seções

- [Visão Geral](docs/VisaoGeral.md)
- [Integração com a monday](docs/integracao.md)
- [Deploy e Entrega](docs/deploy.md)
- [Fluxo de Desenvolvimento](docs/fluxo.md)
- [Ferramentas Utilizadas](docs/ferramentas.md)      


---

## Visão Geral

- Projeto desenvolvido de forma independente com foco em aprendizado técnico.
- Integração direta com a plataforma monday.com sem uso do `monday-cli`.
- App embarcado dentro da monday utilizando iframe e o SDK oficial.
- Deploy publicado e testado em ambiente real.

---

## Integração com a monday.com

- SDK utilizado: `monday-sdk-js`
- API: GraphQL com permissões:
  - `boards:read`
  - `users:read`
  - `updates:write`
- Exemplo de leitura de contexto:
```ts
monday.get("context").then(res => {
  const boardId = res.data.boardId;
});
```

---

## Estrutura do Projeto

```
/src
  /components       → Componentes reutilizáveis
  /views            → Telas (MainView, SettingsView, etc.)
  /utils            → Funções auxiliares
  index.tsx         → Entry point da aplicação
```

---

## Fluxo de Desenvolvimento

- Desenvolvimento local com Vite e ngrok
- Integração com ambiente de desenvolvedor da monday
- Testes e validações contextuais (board, item, usuário)
- Deploy final via Vercel

---

## Deploy e Entrega

- Deploy realizado via [Vercel](https://vercel.com)
- URL de produção: [https://projeto-monday.vercel.app](https://projeto-monday.vercel.app)
- Configuração de URL feita diretamente no painel de desenvolvedor da monday.com
- Processo validado com conta real de testes

---

## Padrões e Organização

- Commits semânticos (`feat`, `fix`, `docs`, etc.)
- Uso de GitFlow (`main`, `dev`, `feature/*`, `bugfix/*`)
- Código modular, reutilizável e tipado com TypeScript
- Organização por responsabilidade: views, components, utils

---

## Ferramentas Utilizadas

- React + Vite
- Javascript
- monday-sdk-js
- GraphQL
- Ngrok
- Vercel (produção)
- Git + GitHub

---

Desenvolvido por **Rogério Vidal**  
GitHub: [@rogeregrge](https://github.com/rogeregrge)
