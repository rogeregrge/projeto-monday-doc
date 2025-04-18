# Deploy e Entrega

## Ambiente de Desenvolvimento Local

- A aplicação é executada localmente utilizando Vite, com a porta padrão `3000`.
- Para testes em ambiente real da monday.com, foi utilizado `ngrok` para criar uma URL pública temporária.
- O iframe da aplicação deve ser registrado no painel de desenvolvedor da monday.com com a URL gerada.

### Passos para rodar localmente

1. Iniciar a aplicação local:
```bash
npm run dev
```

2. Criar um túnel com ngrok:
```bash
ngrok http 3000
```

3. Copiar a URL pública do ngrok (ex: `https://xxxx.ngrok.io`) e configurar na seção de URLs da aplicação no painel da monday.

---

## Ambiente de Produção

- O deploy da aplicação foi realizado utilizando a plataforma [Vercel](https://vercel.com).
- A URL de produção está registrada no painel da monday como endpoint principal da app.
- Todos os testes funcionais foram realizados com a aplicação publicada.

### URL pública de produção

- [https://projeto-monday.vercel.app](https://projeto-monday.vercel.app)

---

## Checklist de Verificação de Deploy

- [x] Leitura do contexto (`boardId`, `itemId`) funcionando corretamente
- [x] Respostas da API GraphQL recebendo os dados esperados
- [x] Layout responsivo renderizado corretamente dentro do iframe da monday
- [x] Nenhum erro nos logs do console
- [x] Publicação e acesso via domínio público da Vercel

---

## Considerações

- A aplicação é compatível com múltiplos ambientes (ngrok e Vercel).
- O fluxo de deploy pode ser facilmente adaptado para CI/CD, caso necessário.
- A estrutura modular permite escalar a aplicação para múltiplas visualizações ou automações no futuro.
