# Modelo de tarefa delegada

O integrador preenche este modelo em `_infra/codex/tasks/<slug>.md` antes de delegar. Substitua os campos entre colchetes por valores concretos. Liste arquivos individualmente; diretórios e curingas não autorizam edições. Um pedido explícito e claro de Ray já autoriza preparar a tarefa dentro daquele escopo.

## Identificação

- Tarefa: [slug]
- Objetivo: [resultado observável]
- marca_id: [xama-pena-azul-do-amor ou seres-multidimensionais]
- Canais: [instagram, facebook e/ou tiktok]
- Destinos: [perfil/página/conta e ID conhecido por canal; ou pendência explícita]
- Peças/versões: [identificadores]
- Ramo: [nome do ramo]
- Base: [ramo e commit conhecido]
- Worktree/checkout: [caminho local, se aplicável]
- Responsável executor: [agente]
- Verificador: [Claude/sessão responsável]
- Integrador único: [responsável]

## Arquivos permitidos

- [caminho exato e ação: criar/editar]

## Fontes

- [caminho/URL e versão relevante; sem credenciais]
- `AGENTS.md`
- `marcas/registro.json`
- [documentação da marca]

## Critérios de pronto

- [critério observável e como verificar]
- [checagem de marca, versão, canal, destino e quantidade pertinente]
- [artefatos e evidências esperadas]

## Dependências

- [tarefa/arquivo, dono, estado e versão entregue; ou nenhuma]

## Proibições

- Não editar arquivos fora da lista; registrar necessidade em `pendencias`.
- Não chamar n8n, Supabase, Google Ads, Meta, Evolution API/WhatsApp ou WordPress.
- Não ler, imprimir ou copiar `.env`, tokens ou chaves.
- Não publicar dados de clientes ou manuscritos privados.
- Não trocar a marca do legado `conteudo/topo-de-funil` nem movê-lo.
- Não inferir aprovação a partir de `VALIDADOS` ou avançar estado sem evidência.
- [outras proibições específicas]

## Entrega

Responder em português, exclusivamente com JSON. O schema `_infra/codex/schema/resultado.json`, quando disponível, prevalece sobre este exemplo. Se não existir, usar esta estrutura e informar a ausência em `pendencias`. O executor não cria nem altera o schema sem autorização na lista de arquivos.

```json
{
  "status": "concluido",
  "resumo": "Resultado curto, fonte utilizada e evidência principal.",
  "arquivos_alterados": ["caminho/exato"],
  "comandos_rodados": ["Comando realmente executado e resultado relevante"],
  "pendencias": []
}
```

Sem schema, use `concluido`, `parcial` ou `bloqueado` conforme a entrega real. Informe limitações, fontes insuficientes e critérios não verificados em `pendencias`. Não declare publicação ou integração remota se a tarefa só produziu arquivos locais.
