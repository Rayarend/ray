# Revisão independente · lote 1 · Seres Multidimensionais

**Nota editorial: 7/10.** Os dez rascunhos distinguem demonstração de caso real e mantêm um pedido por peça. O lote ainda depende de captação, fontes e validação de Ray. A nota avalia o material escrito, não alcance ou publicação.

**IDs alterados:** SN-20, SN-21, SN-22, SN-23, SN-24, SN-25, SN-26, SN-27, SN-28 e SN-29. **IDs intactos neste lote:** nenhum. Todos permanecem `rascunho`, com ID e data preservados. Os Stories das duas semanas e as 14 linhas correspondentes de `STORIES.csv` foram sincronizados; `CALENDARIO.csv` acompanha gancho, CTA, hashtags e `story_cta` dos dez posts. As palavras de DM sem entrega confirmada foram retiradas dessas linhas. Não há palavra-chave ativa nem link prometido no lote.

## Cinco problemas encontrados

1. Os CSVs ofereciam DM por FORMACAO, ARCTURIANO, CRISTAL, SAGRADO ou REIKI sem entrega temática confirmada e divergiam dos CTAs das peças.
2. O quadro 3 dos Stories vinculados repetia a mesma frase em dez dias, sem mostrar a pista particular de cada post.
3. Hashtags amplas como `#consciencia` e `#curiosidades` se repetiam em peças de recorte, citação e percepção; agora descrevem o assunto específico.
4. SN-20, SN-24, SN-25 e SN-27 tinham textos de abertura pouco informativos sem áudio ou sem conhecer a pauta. SN-24 continua condicionado ao áudio realmente captado.
5. SN-21 e SN-29 voltam à atribuição a Piccard na mesma quinzena. Os ângulos foram separados entre localizar obra/página e rastrear a cadeia de compartilhamentos, mas a falta da citação e de sua fonte limita ambos.

## Dependências de Ray

- **Oferta:** confirmar entrega, automação e destino antes de reintroduzir palavra de DM ou link; nenhuma oferta foi presumida.
- **Fala pessoal:** validar se Ray aparecerá e gravará as falas propostas. Conferir especialmente o som real de SN-24 e as cenas próprias de SN-20 e SN-22.
- **Fonte:** fornecer obra e passagem integral atribuída a Piccard (SN-21/SN-29); arquivo original e contexto do caso citado como Curitiba (SN-22); registro integral, origem e direitos do trecho de TV (SN-27); origem e local da narrativa sobre a Antártida (SN-25). Até lá, manter `[CASO A CONFIRMAR]` como nota editorial e usar apenas ilustrações ou demonstrações identificadas.

**CTA único:** sem exceções nos dez posts e nos Stories das duas semanas. O pedido é repetido entre roteiro, legenda, Stories e CSV por consistência, não soma ações diferentes. Os quatro Stories avulsos usam uma interação cada. As primeiras linhas das dez legendas têm de 54 a 81 caracteres, todas abaixo de 125; cada peça tem três hashtags temáticas.

**Validação local:** CSVs lidos com `csv.DictReader`: 61 IDs únicos no calendário e 67 datas únicas em Stories; SN-20 a SN-29 têm IDs, datas, estados e CTAs iguais aos arquivos de produção. Lint Meta nas dez peças e nos dois `STORIES.md`, excluindo `VALIDACAO.md`: zero ocorrências. Comando de reprodução: `py -c "import pathlib,re,unicodedata; p=pathlib.Path('entrega/seres-multidimensionais/producao'); fs=list(p.glob('semana-2026-11-16/SN-*.md'))+list(p.glob('semana-2026-11-23/SN-*.md'))+list(p.glob('semana-2026-11-*/STORIES.md')); s=' '.join(x.read_text(encoding='utf-8') for x in fs); s=''.join(c for c in unicodedata.normalize('NFD',s.casefold()) if unicodedata.category(c)!='Mn'); print(len(re.findall(r'amarra[cç]ao|trazer o amor de volta|\bgarantid[oa]s?\b|\bem\s+(?:\d+|[a-z]+)\s+(?:h|horas?|dias?)\b|\bfeitic[oa]s?\b|\bmagia\b',s)))"`.
