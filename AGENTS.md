# Operação do Ray Arend

Ray define marca, oferta e destino e aprova publicação. Claude especifica e verifica. Codex executa tarefas delimitadas; outros agentes recebem escopos próprios. Consulte [a orquestração](operacao/ORQUESTRACAO.md) e `marcas/registro.json` antes de produzir conteúdo de uma marca.

## Escopo de execução

- Toda execução delegada parte de `_infra/codex/tasks/<slug>.md`, preparado com [o modelo](operacao/TAREFA-MODELO.md). O integrador pode preparar a tarefa a partir do pedido explícito de Ray, sem inventar uma nova etapa de confirmação.
- Edite somente os arquivos exatos autorizados. Se precisar de outro, registre em `pendencias`; não o edite. Um único responsável escreve cada arquivo por vez.
- O executor não chama n8n, Supabase, Google Ads, Meta, Evolution API/WhatsApp ou WordPress. Entrega scripts, JSON e demais artefatos; Claude conduz o acionamento autorizado em outra etapa.
- Nunca leia, imprima ou copie `.env`, tokens ou chaves. Scripts usam variáveis de ambiente sem registrar seus valores.
- Este repositório é público. Dados de clientes, manuscritos privados e credenciais permanecem locais. Ray autorizou publicar suas próprias métricas; isso não autoriza expor dados de terceiros.
- Use português em comentários e resumos. Leia e grave texto com UTF-8 explícito. No Windows use `py` ou o caminho completo do Python; não use `python`/`pip` crus. PowerShell 5.1 não aceita `??` nem `&&`. Para JSON use Python/Node, sem depender de `jq` ou `psql`.

## Marca e evidência

Use `marca_id`, canais e identificadores explícitos de destino. Nunca deduza aprovação pelo nome `VALIDADOS`. Não mova nem reatribua `conteudo/topo-de-funil`: esse legado pertence a Seres Multidimensionais. Trabalho para Xamã Pena Azul do Amor fica separado em `marcas/xama-pena-azul-do-amor`; Seres usa `marcas/seres-multidimensionais`.

A entrega do executor contém apenas JSON com `status`, `resumo`, `arquivos_alterados`, `comandos_rodados` e `pendencias`, conforme o schema da tarefa (`_infra/codex/schema/resultado.json`, quando disponível). Informe verificações realmente executadas e limitações. Sem schema disponível, use o exemplo do modelo e registre a ausência.
