---
name: orquestrar-marcas
description: Organiza e delega trabalho de conteúdo entre IAs para as marcas de Ray, com escopo por arquivo, revisão e repasse entre Instagram, Facebook e TikTok. Use ao coordenar múltiplos agentes ou integrar entregas de marcas; não executa publicação em serviços externos.
---

# Orquestrar marcas

Leia `AGENTS.md`, `operacao/ORQUESTRACAO.md` e `marcas/registro.json` a partir da raiz do repositório. Carregue somente a documentação da marca e as fontes necessárias. Cada IA precisa acessar essas fontes por conta própria; esta skill não cria conexão automática entre serviços.

1. Identifique a marca por `marca_id`, os canais e os destinos. Não confunda o legado `conteudo/topo-de-funil` de Seres com Xamã. Dados ausentes viram pendências explícitas; prepare o que não depende deles.
2. Como integrador, derive a tarefa do pedido autorizado de Ray usando `operacao/TAREFA-MODELO.md` e grave-a em `_infra/codex/tasks/<slug>.md`. Inclua arquivos exatos, dono, ramo, fontes, dependências e critérios. Como executor delegado, limite-se à tarefa recebida.
3. Delegue apenas blocos independentes, um dono por arquivo, em ramos separados ou worktrees. Se não houver ferramenta de agentes, entregue os arquivos de tarefa para repasse manual e não alegue tê-los despachado. Reserve arquivos compartilhados ao integrador único.
4. Exija entrega com fonte, evidência e limitações no JSON da tarefa. Claude verifica escopo e conteúdo; Ray aprova publicação da versão e dos destinos. `VALIDADOS` não comprova aprovação.
5. Integre somente entregas revisadas. Atualize a base com fetch/rebase quando necessário, confira conflitos e faça push não forçado apenas quando o envio estiver autorizado. Agendamento/publicação permanecem pendentes até haver evidência externa.

O executor entrega artefatos locais e não chama produção. Nunca leia `.env`, tokens ou chaves. Mantenha dados de clientes e manuscritos privados fora deste repositório público; a autorização para métricas próprias de Ray não cobre terceiros. Não crie novas confirmações para trabalho já autorizado.
