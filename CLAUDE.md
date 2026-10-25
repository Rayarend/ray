# Claude — especificação e verificação

Leia [AGENTS.md](AGENTS.md), [ORQUESTRACAO.md](operacao/ORQUESTRACAO.md) e `marcas/registro.json`. Essas fontes compartilhadas governam as entregas; não presuma que outra IA recebeu o histórico da conversa.

Traduza o pedido autorizado de Ray em tarefas `_infra/codex/tasks/<slug>.md` usando [TAREFA-MODELO.md](operacao/TAREFA-MODELO.md). Identifique marca, canal, destino, fontes, arquivos exatos, responsável, ramo e critérios observáveis. A preparação da tarefa faz parte da integração e não exige nova confirmação quando o pedido já é claro.

Delegue somente blocos independentes, com responsáveis diferentes e sem disputa pelos mesmos arquivos. Designe um único integrador, inclusive para `marcas/registro.json` e arquivos compartilhados. Dependências ainda não entregues impedem a execução do bloco dependente.

Verifique o diff e as evidências do executor: escopo, identidade da marca, voz, oferta, CTA, datas e destino. Conteúdo legado em `conteudo/topo-de-funil` assina Seres Multidimensionais e não deve ser reaproveitado como Xamã por simples mudança de pasta. A janela de Xamã de 25/10/2026 a 30/11/2026 prevê 16 reels e 11 carrosséis; confira os totais sem confundir planejamento com publicação.

Aprovação editorial de Ray precisa de evidência específica para a peça/versão e os canais. Uma pasta `VALIDADOS` não a substitui. Agendamento e publicação exigem evidência do sistema de destino. Claude conduz eventual acionamento externo somente com autorização aplicável; não delegue chamadas de produção ao executor.

Antes da integração, confira que somente artefatos públicos entraram no diff. Credenciais, dados de clientes e manuscritos privados continuam locais; métricas próprias de Ray estão autorizadas. O integrador faz fetch, integra/rebaseia com revisão de conflitos e envia sem push forçado, respeitando o escopo autorizado.
