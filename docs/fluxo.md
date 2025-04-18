# Fluxo de Desenvolvimento

## Organização Geral

- O projeto segue uma abordagem baseada em Kanban.
- As tarefas são organizadas por estágios de progresso: backlog, desenvolvimento, revisão, testes e finalização.
- O fluxo foi pensado para refletir a realidade de uma entrega contínua com validações locais e testes em ambiente real da monday.com.

---

## Etapas do Fluxo

1. **Planejamento**
   - Definição do escopo da funcionalidade.
   - Levantamento de permissões e dados necessários da API da monday.

2. **Desenvolvimento**
   - Implementação da funcionalidade com React + Vite.
   - Criação dos componentes e consumo da API GraphQL.
   - Leitura de contexto via SDK (`monday-sdk-js`).

3. **Testes Locais**
   - Execução local via Vite.
   - Tunelamento com ngrok para testar diretamente dentro do iframe da monday.com.
   - Simulação de diferentes boards e usuários para validar o comportamento.

4. **Revisão**
   - Verificação do funcionamento de ponta a ponta.
   - Testes de comportamento, validação de permissões e logs de erro.

5. **Deploy**
   - Publicação via Vercel.
   - Atualização das URLs de produção no painel da monday.
   - Testes finais com o app publicado.

---

## Boas Práticas Aplicadas

- Commit semântico para cada mudança de escopo.
- Uso de branches organizadas por tipo de tarefa (`feature/*`, `bugfix/*`).
- Modularização do código para facilitar manutenção e expansão.
- Anotações em cada etapa do desenvolvimento no README ou Wiki.

---

## Observações

- O fluxo permite testar rapidamente a aplicação sem necessidade de aprovação formal da monday.com (em modo de desenvolvedor).
- A estrutura é adaptável para times, podendo ser expandida com ferramentas como Jira, Trello ou Linear.

