# Ferramentas Utilizadas

Este projeto foi desenvolvido utilizando ferramentas modernas para garantir um ambiente de desenvolvimento ágil, integrado e alinhado com práticas comuns no mercado.

---

## Desenvolvimento Frontend

- **React**  
  Biblioteca principal para construção da interface da aplicação.

- **Vite**  
  Ferramenta de build e dev server rápida, usada para substituir o CRA (Create React App).

- **TypeScript**  
  Superset do JavaScript que adiciona tipagem estática ao projeto, melhorando manutenção e segurança.

---

## Integração com a Plataforma

- **monday-sdk-js**  
  SDK oficial da monday.com utilizado para capturar contexto (`boardId`, `itemId`, etc.) e se comunicar com a plataforma.

- **GraphQL API da monday**  
  Interface de comunicação para consultar dados estruturados da conta da monday (boards, usuários, colunas, etc.).

---

## Ambientes e Deploy

- **Ngrok**  
  Ferramenta de tunelamento usada para expor o servidor local e testar a aplicação diretamente dentro da monday em ambiente de desenvolvimento.

- **Vercel**  
  Plataforma de deploy utilizada para hospedar a versão pública da aplicação, integrada ao GitHub para CI/CD automático.

---

## Versionamento

- **Git**  
  Sistema de controle de versão utilizado para organizar o código em branches e manter histórico de alterações.

- **GitHub**  
  Plataforma de hospedagem dos repositórios com controle de issues, pull requests, documentação e deploy.

---

## Organização e Documentação

- **Markdown**  
  Linguagem de marcação utilizada para escrever toda a documentação técnica do projeto.

- **GitHub Wiki (e posteriormente projeto-monday-docs)**  
  Inicialmente usada como espaço de documentação interna, depois migrada para um repositório separado com estrutura modular.

---

## Observações

- Todas as ferramentas foram escolhidas com foco em velocidade, simplicidade e aderência a projetos modernos de integração SaaS.
- A estrutura está pronta para escalar, podendo ser adaptada para uso com frameworks como Next.js, NestJS, ou deploys avançados via Docker.
