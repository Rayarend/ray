---
name: rea-postagens
description: Analisa fluxos observáveis de aplicativos de postagem e converte as funcionalidades em requisitos, modelo de dados e plano de automação no n8n, com evidências e limites explícitos.
license: Uso interno de Ray Arend.
---

# REA — análise de aplicativos de postagem

Use esta skill quando Ray pedir engenharia reversa funcional, comparação de plataformas de postagem ou planejamento do próprio aplicativo conectado ao n8n. REA aqui significa **Reverse Engineering de Aplicações**: estudar comportamento acessível ao usuário para projetar uma solução original. Não copiar código, marca, interface ou elementos protegidos de terceiros.

## Entradas

- Aplicativo(s) e URLs a analisar, contas e fluxos que Ray pode acessar.
- Objetivo do aplicativo próprio: canais, aprovação, agendamento, formatos, colaboração e métricas.
- Marca e canal de destino por identificador explícito; nunca presumir que uma postagem de Seres Multidimensionais pertence ao Xamã Pena Azul do Amor.

Se faltarem aplicativos específicos, começar pelos já mencionados na conversa e por documentação pública. Pedir links ou acesso apenas para a observação que depende deles. Não pedir senha, chave ou token no chat.

## Método

1. **Mapear jornadas:** criar rascunho, adicionar mídia, legenda, canais, prévia, validação, aprovação, programação, publicação, falha, reprogramação e análise.
2. **Coletar evidência:** documentar tela/URL/data ou documentação oficial para cada função. Marcar como **observado**, **documentado**, **inferido** ou **não verificado**. Não chamar uma hipótese de funcionalidade confirmada.
3. **Decompor:** para cada jornada, registrar entrada, regra, estados, saída, exceções, permissões e responsáveis. Separar as regras do aplicativo daquelas impostas pela API oficial de cada rede.
4. **Comparar:** construir uma matriz por plataforma, com passos para o usuário, automações visíveis, limites, preços quando verificáveis e dependências externas.
5. **Projetar o aplicativo próprio:** fluxos de tela simples, estados do post, esquema de dados e eventos. Especificar como o n8n orquestra cada etapa usando APIs oficiais, com autenticação apropriada. Incluir tratamento de duplicação, tentativas, limites de API e auditoria.
6. **Priorizar:** escolher um MVP testável para uma marca e um canal; separar versões futuras. Estimar esforço apenas se houver dados suficientes.
7. **Validar:** descrever testes concretos para rascunho, aprovação, agendamento, envio, falha, recuperação, fuso horário e separação entre marcas. Nunca afirmar que publicou ou conectou contas sem evidência.

## Modelo mínimo de post

`post_id`, `marca_id`, `canal`, `conta_destino_id`, `tipo`, `midias[]`, `legenda`, `alt_text`, `estado`, `versao`, `aprovado_por`, `aprovado_em`, `programado_para_utc`, `fuso_exibicao`, `idempotency_key`, `remote_post_id`, `ultima_falha`, `tentativas`, `criado_em`, `atualizado_em`.

Estados sugeridos: `rascunho → em_revisao → aprovado → agendado → publicando → publicado`; caminhos de erro: `falha`, `cancelado`, `reagendado`. A transição para publicação exige aprovação explícita da peça e destino confirmado. Aprovação de uma marca não vale para outra.

## Entrega

- Quadro **função / evidência / estado de confirmação / regra / prioridade**.
- Jornada e modelo de dados do MVP.
- Diagrama dos fluxos n8n previstos, sem ativá-los automaticamente.
- Lista de APIs oficiais, permissões e credenciais requeridas, sem valores.
- Backlog com critérios de aceite e dúvidas ainda abertas.

Respeitar `AGENTS.md` e o registro de marcas do repositório. Não usar engenharia reversa para contornar autenticação, limites de API, acesso ou proteção de terceiros. Não conectar serviços nem publicar sem autorização e evidência do destino correto.
