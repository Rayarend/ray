# Orquestração das marcas

## Fonte de verdade

O repositório reúne orientações e artefatos. Ele não conecta nem controla automaticamente Claude, Codex ou outros serviços de IA. Cada sessão precisa ler `AGENTS.md`, `marcas/registro.json`, a documentação da marca e sua tarefa. O repasse pode ser manual ou por ferramentas já disponíveis e autorizadas.

| Papel | Responsabilidade |
| --- | --- |
| Ray | Define marca, oferta e destino; aprova a publicação |
| Claude | Especifica tarefas e verifica as entregas |
| Codex | Executa o escopo local e entrega evidências |
| Outros agentes | Produzem ou revisam um bloco explicitamente atribuído |
| Integrador único | Controla arquivos compartilhados, resolve conflitos e integra entregas |

## Separação por marca e canal

`marcas/registro.json` é o índice central. Use os IDs `xama-pena-azul-do-amor` e `seres-multidimensionais`; seus diretórios são `marcas/<marca_id>`. Dentro de cada marca, mantenha planejamento e adaptações de Instagram, Facebook e TikTok identificáveis. Uma peça pode ter adaptações por canal; copiar a peça não transfere aprovação nem autoriza publicação em outro perfil.

Toda peça ou linha de planejamento deve identificar: `marca_id`, identificador da peça, versão, canal, destino, data planejada e estado. Registre perfil/página/conta por identificador inequívoco quando conhecido. Destino desconhecido fica pendente, sem inventar IDs. O conteúdo pode ser preparado enquanto se resolve esse dado; a pendência impede agendar/publicar.

O legado `conteudo/topo-de-funil` pertence a Seres Multidimensionais e permanece no lugar. A janela inicial de Xamã é 25/10/2026–30/11/2026, com 16 reels e 11 carrosséis. Esses números são metas do calendário, não comprovantes de publicação.

## Delegação e integração

1. O integrador transforma o pedido de Ray em uma tarefa pelo modelo, com lista exata de arquivos. Não exija nova aprovação para escolhas rotineiras já cobertas pelo pedido.
2. Atribua um dono a cada arquivo. Para execução concorrente, use ramos separados ou worktrees com base conhecida. Arquivos compartilhados ficam com o integrador; cada agente entrega sua proposta sem editá-los.
3. Distribua somente tarefas independentes. Se uma depende de decisões, arquivos ou revisão de outra, espere a entrega dessa dependência e registre sua versão.
4. O executor lê apenas as fontes necessárias, produz os artefatos autorizados e valida os critérios locais. Não chama serviços de produção. Impedimentos e necessidades fora da lista entram em `pendencias`.
5. Claude revisa o diff, a marca, os destinos e os critérios. O integrador único atualiza a base com fetch, integra as mudanças e faz rebase quando necessário, resolvendo conflitos sem apagar trabalho alheio. Revalide os arquivos afetados por conflitos.
6. Quando autorizado a enviar ao remoto, o integrador faz push sem força. Uma rejeição por divergência exige atualizar e revisar a integração; não usar `--force` nem `--force-with-lease` para contorná-la.

## Estados editoriais

| Estado | Evidência necessária |
| --- | --- |
| `ideia` | Registro da proposta e da marca |
| `rascunho` | Artefato identificável e sua versão |
| `em_revisao` | Versão submetida e responsável pela revisão |
| `aprovado` | Aprovação de Ray vinculada à versão, canais e destinos |
| `agendado` | Registro do agendador com destino, data e identificador |
| `publicado` | URL ou identificador da publicação e data efetiva |

Não avance estado por inferência. Nome de arquivo, pasta `VALIDADOS` e data passada não comprovam aprovação ou publicação. Alteração material de uma versão aprovada retorna para revisão; preserve o histórico de evidências. Aprovação para editar ou integrar o repositório não é aprovação editorial para publicar a peça.

## Repasse mínimo

Inclua no resultado ou nos arquivos autorizados: fonte utilizada (caminho e versão/commit quando disponível), evidência dos critérios verificados e limitações relevantes. Comandos não executados não aparecem como sucesso. A resposta do executor segue o JSON definido na tarefa; não copie credenciais para justificativas, exemplos ou logs.

Este repositório é público: mantenha dados de clientes e manuscritos privados em armazenamento local fora do conjunto publicado. Métricas próprias de Ray podem ser incluídas conforme a autorização existente. Os materiais podem referenciar a existência de uma fonte privada sem reproduzir seu conteúdo.
