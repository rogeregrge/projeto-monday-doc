# Visão Geral

## Nome do Projeto
projeto-monday – Integração com monday.com

## Objetivo

- Demonstrar, por meio de um projeto funcional, como integrar uma aplicação frontend à plataforma monday.com utilizando o SDK oficial e a API GraphQL.
- Construir toda a estrutura do projeto de forma manual, sem utilizar o `monday-cli`.
- Utilizar tecnologias modernas como React com Vite e TypeScript, com foco em modularidade, integração e deploy.

## Desenvolvedor

- Nome: Rogério Vidal 
- GitHub: [@rogeregrge](https://github.com/rogeregrge)

## Descrição Geral

- A aplicação funciona embarcada dentro da interface da monday.com, utilizando iframe.
- Utiliza o SDK da monday para obter dados contextuais do usuário e do board.
- Os dados são consultados via GraphQL com permissões definidas no ambiente de desenvolvedor.
- O projeto inclui deploy contínuo via Vercel para simular um ambiente de produção real.

## Funcionalidades Desenvolvidas

- Leitura de contexto: `boardId`, `itemId`, `userId`.
- Consumo de dados via GraphQL.
- Comunicação entre iframe e plataforma.
- Visualização de dados dentro de uma visualização customizada da monday.
- Deploy final com domínio público acessível.

## Status do Projeto

- Estrutura de código estável e modular.
- Funcionalidade de leitura testada com sucesso.
- Deploy público funcional via Vercel.
- Próximas etapas incluem: escrita de dados no board, formulários interativos e melhorias na interface.

## Link de Produção

- [https://projeto-monday.vercel.app](https://projeto-monday.vercel.app)
