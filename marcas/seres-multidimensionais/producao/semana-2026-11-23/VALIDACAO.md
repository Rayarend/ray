# Validação · Issue #19 · semana-2026-11-23

marca_id: seres-multidimensionais
estado: rascunho

## Cobertura

IDs desta pasta: SN-25, SN-26, SN-27, SN-28, SN-29. Lote completo: 10 peças e 14 blocos diários de quatro quadros em dois STORIES.md. Todas as linhas do período foram cobertas.

Fichas remodelar-pendente: nenhuma; não há repost/remodelar nas linhas deste período. A revisão anterior pede palavra de DM apenas com entrega e automação confirmadas. Como isso não foi fornecido, foram escolhidos CTAs de interação permitidos na Issue, repetidos entre feed e Stories. Nenhum pedido de ARCTURIANO/FORMACAO/REIKI/CRISTAL/SAGRADO foi associado artificialmente a um caso histórico. Links e contagem regressiva sem destino/horário foram omitidos. Os CSVs, virais, revisões e docs permanecem intactos. As fórmulas vêm dos títulos locais, não de uma análise de vídeos assistidos; titularidade da referência ainda requer Ray, e nenhum conteúdo é repostado.

## Validações executadas

Cobertura de IDs, datas e marca/canais; rascunho em todas as peças; 14 blocos de quatro quadros; primeiro rosto/mãos; legenda com primeira linha <=125 caracteres, total <=2.200 e 3-5 hashtags; oito slides por carrossel, capa <=6 palavras e corpo final <=25 palavras por slide; mesma ação no CTA final de peça, legenda e Stories. Campos de confirmação não são copy final. Escopo: somente as duas pastas de produção.

Lint Meta: **12 arquivos; zero ocorrências**. Comando executado na raiz, incluindo copy e instruções das peças, excluindo estes relatórios técnicos:

```bash
python3 - <<'PY'
from pathlib import Path
import re,unicodedata
root=Path('entrega/seres-multidimensionais/producao')
files=[p for w in ('semana-2026-11-16','semana-2026-11-23') for p in (root/w).glob('*.md') if p.name!='VALIDACAO.md']
patterns=('amarracao', 'trazer o amor de volta', 'garantid[oa]s?', 'em\\s+(?:24\\s*h|\\d+\\s*dias?)', 'feitico', '\\bmagia\\b')
hits=[]
for p in files:
 s=''.join(c for c in unicodedata.normalize('NFD',p.read_text(encoding='utf-8').casefold()) if unicodedata.category(c)!='Mn')
 hits.extend((str(p),t) for t in patterns if re.search(t,s))
print('Lint Meta:',len(files),'arquivos;',len(hits),'ocorrencias;',hits)
raise SystemExit(bool(hits))
PY
```

A leitura editorial também conferiu promessas e atribuições pessoais; a regex não substitui essa leitura.

## ig-human e caption.py: resultado real

Humanize aplicado a todas as peças e aos consolidados, preservando campos de máquina. Detect executado antes/depois em copy extraída de falas, tela, legendas, slides e quadros, sem metadados.

| Arquivo | Antes | Depois | Veredicto |
|---|---:|---:|---|
| SN-25.md | 53.7 | 53.7 | REVIEW |
| SN-26.md | 57.8 | 57.8 | REVIEW |
| SN-27.md | 54.5 | 54.5 | REVIEW |
| SN-28.md | 60.3 | 60.3 | REVIEW |
| SN-29.md | 57.9 | 57.9 | REVIEW |
| STORIES.md | 33.1 | 33.1 | FLAGGED |

Painéis do lote: {'REVIEW': 10, 'FLAGGED': 2}. Alertas mantidos, sem declarar PASS quando não ocorreu. O detector usa pronomes/contrações ingleses e palavras ASCII, com limitações importantes para português e textos curtos. Foram revistos concretude, naturalidade e contexto, sem inserir números ou inglês para alterar a nota.

caption.py: zero FAIL nas 10 legendas; veredictos {'REVIEW': 10}. Avisos por legenda:

- SN-25: HOOK IS CONCRETE, ONE ASK.
- SN-26: HOOK IS CONCRETE, ONE ASK.
- SN-27: ONE ASK.
- SN-28: HOOK IS CONCRETE, ONE ASK.
- SN-29: ONE ASK.

ONE ASK não reconhece todos os pedidos em português; HOOK IS CONCRETE usa nomes/números, não todos os objetos/cenas. Avisos não foram desativados: cada legenda foi conferida manualmente para um pedido e abertura concreta.

## Comparação de vizinhas e pendências

| Data | ID | Cena/objeto | Ângulo e lacuna |
|---|---|---|---|
| 2026-11-16 | SN-20 | Cortina em movimento | Descrição do ambiente versus interpretação pessoal |
| 2026-11-17 | SN-21 | Livro e marcador de página | Autoria da citação, não forma da Terra |
| 2026-11-18 | SN-22 | Lanterna e vidro com selo Demonstração | Contexto óptico; nenhuma identificação do caso |
| 2026-11-19 | SN-23 | Moldura vazada sobre composição autoral | Contexto visual, diferente da busca de autoria em SN-21 |
| 2026-11-20 | SN-24 | Relógio e áudio ambiente | Escuta, em vez da cortina visual de SN-20 |
| 2026-11-23 | SN-25 | Maquete branca identificada | Localização alegada versus origem verificável |
| 2026-11-24 | SN-26 | Porta desenhada e faixa de horário | Disponibilidade concreta, sem mecanismo sobrenatural |
| 2026-11-25 | SN-27 | Faixa de papel sobre sequência desenhada | Continuidade do vídeo, não data tratada como prova |
| 2026-11-26 | SN-28 | Feixe desenhado e camadas de texto | Experiência pessoal e explicação verificável |
| 2026-11-27 | SN-29 | Fita entre pontos de diagrama | Cadeia da atribuição, não repetição da aula de documento |

Comparação manual: não há três peças vizinhas com a mesma ação/objeto. A retomada do mesmo objeto nos Stories vinculados é intencional, não uma nova peça de feed. Nos dias avulsos, a sequência também troca o contexto visual. A recorrência de tema no calendário foi tratada com perguntas distintas, sem alterar os CSVs.

- SN-25: [CASO A CONFIRMAR] Fonte primária, local e contexto da narrativa. Não apresentar desenho, imagem gerada ou maquete como registro da Antártida.
- SN-26: Validar a proposta com Ray. Não usar exemplo de horário como agenda real, conselho individual ou promessa de efeito.
- SN-27: [CASO A CONFIRMAR] Programa, arquivo integral, data e direitos do trecho. Não inventar emissora, testemunha, fala ou acontecimento; nenhuma alegação da referência foi confirmada.
- SN-28: Ray valida a terminologia espiritual. Não incluir medida, equipamento, efeito terapêutico ou associação com Reiki não demonstrados.
- SN-29: [CASO A CONFIRMAR] Registro primário da associação. Não atribuir frase a Piccard nem discutir a forma da Terra com base em citação isolada; não há fonte para isso neste material.

Os marcadores [CASO A CONFIRMAR] são internos, nunca para narrar/mostrar ao público. Nenhum caso histórico ou fenômeno foi tratado como fato sem fonte primária. Nenhum vídeo foi assistido, cliente citado, entrega por DM prometida ou serviço externo acessado. Nada agendado/publicado; captação, fontes/consentimentos e revisão humana continuam necessários.
