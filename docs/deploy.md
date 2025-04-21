## 🚀 Deploy e Entrega

### 🧪 Ambiente de Desenvolvimento Local

A aplicação é executada localmente utilizando **Vite**, com a porta padrão `3000`.

Durante as primeiras etapas do desenvolvimento, foi utilizado **ngrok** para expor a aplicação local e testá-la no ambiente real da monday.com. No entanto, esse método foi substituído por um fluxo mais estável com deploy contínuo via Vercel (veja abaixo).

> ❌ **Ngrok - obsoleto para este projeto**  
> - Criava uma URL pública temporária para testes.  
> - Exigia atualização manual da URL no painel de desenvolvedor da monday.com a cada nova sessão.  
> - Útil apenas para testes locais rápidos.  
> - **Não é mais utilizado atualmente.**

---

### ✅ Novo Fluxo com Vercel (CI/CD Básico)

Atualmente, o deploy é feito automaticamente via [Vercel](https://vercel.com), que está integrado ao repositório GitHub do projeto.

**Etapas:**

1. Desenvolve e testa localmente com:
   ```bash
   npm run dev
   ```

2. Faz o push para a branch `main`:
   ```bash
   git push origin main
   ```

3. O Vercel realiza o **build** e o **deploy automático**.

4. A URL gerada é pública e estável, configurada no painel de desenvolvedor da monday.com como origem da aplicação.

---

### 🌐 URL pública de produção

```
https://projeto-monday.vercel.app
```

Essa URL é usada como:
- **iframe** dentro do board
- Endpoint de visualização da app configurado no Developer Center da monday.com

---

### ✅ Checklist de Verificação de Deploy

- [x] Leitura do contexto (`boardId`, `itemId`) funcionando corretamente  
- [x] Respostas da API GraphQL recebendo os dados esperados  
- [x] Layout responsivo renderizado corretamente dentro do iframe  
- [x] Nenhum erro nos logs do console  
- [x] Publicação e acesso via domínio público da Vercel  

---

### 💡 Considerações

- A aplicação é compatível com múltiplos ambientes de execução.  
- O uso do Vercel elimina a necessidade do `ngrok` e permite deploy contínuo.  
- O fluxo atual já está adaptado para **CI/CD** básico.  
- A estrutura modular permite escalar a aplicação para múltiplas views, automações ou integrações futuras.
