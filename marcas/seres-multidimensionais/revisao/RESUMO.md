# Revisão independente | Seres Multidimensionais

**Nota editorial das peças disponíveis: 5,5/10.** Há cuidado em não transformar hipóteses em fatos e em evitar promessas de resultado. A execução perde força pela repetição de formatos e pedidos, pela distância do pilar de fenômenos da marca e pela ausência dos Reels originais em parte do lote. A nota avalia os rascunhos disponíveis, não o desempenho das publicações.

**Escopo lido:** SN-01 a SN-19, os três arquivos semanais de Stories e o calendário de 61 linhas com Stories associados. O calendário posterior a SN-19 serviu para identificar padrões; as peças SN-20 a SN-61 não estão nas três pastas de produção deste pedido.

**IDs revisados:** SN-08, SN-09, SN-10, SN-11, SN-12, SN-13, SN-14, SN-15, SN-16, SN-17, SN-18, SN-19.

**IDs sem alteração:** SN-01 a SN-07. A fonte local informa apenas data e palavra-chave; não há vídeo, tema confirmado nem legenda original. Sem esse material, um gancho específico pronto para colar inventaria o assunto. As propostas condicionais existentes continuam rascunho e precisam ser confrontadas com o Reel real.

## Cinco problemas mais frequentes

1. CTAs de Stories repetem palavras de DM sem entrega ligada ao tema e competem com enquete, quiz ou caixa na mesma sequência.
2. Ganchos e primeiras linhas genéricos contam o conteúdo antes do toque em “mais” ou deixam o assunto pouco reconhecível sem som.
3. Sete carrosséis consecutivos de autoconhecimento afastam o lote do posicionamento de mistério e fenômenos da Seres.
4. SN-15, SN-17 e SN-19 usam quase o mesmo roteiro de checagem e a mesma pergunta final; SN-16 e SN-18 repetem o CTA de detalhe.
5. Casos ainda sem documento primário levam marcadores editoriais ou datas alegadas para a copy, o que pode parecer afirmação factual na publicação.

## Cinco regras para as próximas specs

1. Registrar a imagem, o tema, a origem e a legenda do Reel existente antes de pedir uma revisão pronta para publicar; sem isso, manter a peça em rascunho.
2. Em cada Reel, especificar quadro 0, ação ou mudança até 3 segundos, texto curto legível sem áudio e fala que nomeie o assunto. Confirmar os oito pontos do checklist `virality` com o material real.
3. Planejar a sequência da semana antes de escrever: alternar fenômenos verificáveis, investigação e reflexão; não preencher dias com posts genéricos só para manter frequência.
4. Dar um único pedido por peça e um sticker de interação por sequência de Stories. Palavra de DM só com automação e entrega correspondentes confirmadas; link só com destino validado.
5. Separar instrução editorial da copy. Caso sem fonte fica como pergunta ou demonstração identificada; remover marcadores de trabalho do texto final e variar o motivo concreto de cada comentário.

**Estado:** revisão de rascunhos. Nenhuma peça foi aprovada, agendada ou publicada. As mudanças de capa, roteiro e Story são propostas para o editor aplicar aos arquivos originais após conferir arte, vídeo e automações.

**Validação:** lint Meta das versões propostas por normalização Unicode sem distinção de acento ou caixa; zero ocorrências. Comando executado nesta revisão: `py -c "import pathlib,re,unicodedata; p=pathlib.Path('entrega/seres-multidimensionais/revisao'); s='\n'.join(x.read_text(encoding='utf-8') for x in p.glob('SN-*.md')); s=''.join(c for c in unicodedata.normalize('NFD',s.casefold()) if unicodedata.category(c)!='Mn'); hits=re.findall(r'amarra[cç]ao|trazer o amor de volta|garantid[oa]s?|em\s+(?:\d+|[a-z]+)\s+(?:h|horas?|dias?)|feitic[oa]s?|magia',s); print('lint Meta:',len(hits),'ocorrencias')"`.
