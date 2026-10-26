# Validação · Issue #20 · semana-2026-11-16

marca_id: alianca-terapeutica-520
estado: rascunho

## Cobertura

IDs desta pasta: AL-14, AL-15, AL-16, AL-17, AL-18. Lote completo: 10 peças e 14 blocos diários de quatro quadros em dois STORIES.md. Todas as linhas do período foram cobertas.

Fichas remodelar-pendente: nenhuma; não há repost/remodelar nas linhas deste período. A Issue permite interação como CTA: os carrosséis mantêm salvar; três Reels de natureza usam comentário ou salvar; Reels de animal fazem ponte explícita para informação geral da formação com CURSOS. O pedido final é o mesmo entre Reel/carrossel, legenda e Stories. Sem link não validado, sticker concorrente, promessa de entrega automática ou informação de currículo/preço presumida. Hashtags foram ajustadas ao assunto real, sem editar os CSVs. Não há repost/remodelar no período; seis recriar, dois modelar e dois originais. Só fórmula de referências, sem assistir, transcrever ou copiar seus vídeos.

## Validações executadas

Cobertura de IDs, datas e marca/canais; rascunho em todas as peças; 14 blocos de quatro quadros; primeiro rosto/mãos; legenda com primeira linha <=125 caracteres, total <=2.200 e 3-5 hashtags; número de slides conforme calendário e modelos da marca, capa <=6 palavras e corpo final <=25 palavras por slide; mesma ação no CTA final de peça, legenda e Stories. Campos de confirmação não são copy final. Escopo: somente as duas pastas de produção.

Lint Meta: **12 arquivos; zero ocorrências**. Comando executado na raiz, incluindo copy e instruções das peças, excluindo estes relatórios técnicos:

```bash
python3 - <<'PY'
from pathlib import Path
import re,unicodedata
root=Path('entrega/alianca-terapeutica-520/producao')
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
| AL-14.md | 53.2 | 53.2 | REVIEW |
| AL-15.md | 57.0 | 57.0 | REVIEW |
| AL-16.md | 53.0 | 53.0 | REVIEW |
| AL-17.md | 59.1 | 59.1 | REVIEW |
| AL-18.md | 55.4 | 55.4 | REVIEW |
| STORIES.md | 34.5 | 34.5 | FLAGGED |

Painéis do lote: {'REVIEW': 10, 'FLAGGED': 2}. Alertas mantidos, sem declarar PASS quando não ocorreu. O detector usa pronomes/contrações ingleses e palavras ASCII, com limitações importantes para português e textos curtos. Foram revistos concretude, naturalidade e contexto, sem inserir números ou inglês para alterar a nota.

caption.py: zero FAIL nas 10 legendas; veredictos {'REVIEW': 10}. Avisos por legenda:

- AL-14: HOOK IS CONCRETE, ONE ASK.
- AL-15: ONE ASK.
- AL-16: HOOK IS CONCRETE, ONE ASK.
- AL-17: HOOK IS CONCRETE, ONE ASK.
- AL-18: HOOK IS CONCRETE, ONE ASK.

ONE ASK não reconhece todos os pedidos em português; HOOK IS CONCRETE usa nomes/números, não todos os objetos/cenas. Avisos não foram desativados: cada legenda foi conferida manualmente para um pedido e abertura concreta.

## Comparação de vizinhas e pendências

| Data | ID | Cena/objeto | Ângulo e lacuna |
|---|---|---|---|
| 2026-11-16 | AL-14 | Livro fechado no colo e gato à distância | Companhia sem exigir resposta; não repetir televisão de AL-09 |
| 2026-11-17 | AL-15 | Frasco fechado e rótulo ilustrativo | Informação do produto antes da escolha |
| 2026-11-18 | AL-16 | Gota no vidro e áudio real | Escuta, sem história de tempestade pessoal |
| 2026-11-19 | AL-17 | Balões de fala e marcador de leitura | Clareza antes de continuar, sem repetir lista de objetos de AL-12 |
| 2026-11-20 | AL-18 | Mão contida no próprio joelho e passagem livre | Respeito à aproximação; diferente da companhia de AL-14 |
| 2026-11-23 | AL-19 | Tecido preso no varal e vento real | Oração como expressão, sem repetir folha/caderno de AL-11 |
| 2026-11-24 | AL-20 | Pêndulo imóvel em suporte, sem medição | Proposta versus alcance da interpretação |
| 2026-11-25 | AL-21 | Guarda-chuva secando | Ação prática depois da chuva, não escuta da gota em AL-16 |
| 2026-11-26 | AL-22 | Mão aberta e balão de interrupção | Combinar parada e retomada, distinto da compreensão em AL-17 |
| 2026-11-27 | AL-23 | Caixa limpa com saída livre | Preparar espaço sem exigir uso; distinto de AL-14 e AL-18 |

Comparação manual: não há três peças vizinhas com a mesma ação/objeto. A retomada do mesmo objeto nos Stories vinculados é intencional, não uma nova peça de feed. Nos dias avulsos, a sequência também troca o contexto visual. A recorrência de tema no calendário foi tratada com perguntas distintas, sem alterar os CSVs.

- AL-14: [CASO A CONFIRMAR] Captação própria ou autorizada ainda não fornecida. Não encenar caso de sofrimento ou depoimento. Não atrair, conter ou dirigir o animal; se ele sair, adaptar a cena. Ray confirma proposta da formação e resposta manual ao pedido, sem automação presumida.
- AL-15: Ray valida os termos com pessoa habilitada antes da produção final. Não inserir fórmula, diluição, ingestão, recomendação a animais/crianças ou alegação de saúde. Não foi confirmado módulo específico na oferta atual.
- AL-16: [CASO A CONFIRMAR] Captação autoral de chuva e autorização de quem aparecer. Não simular notícia de evento climático, sofrimento ou efeito de saúde. Não gravar em condição de risco; se não houver chuva real, adiar a captação, sem chamar outro áudio de registro local.
- AL-17: Ray valida a formulação e as condições reais das práticas apresentadas. Não há protocolo de sessão fornecido nem promessa de estado emocional. Não vincular a uma terapia que o calendário não nomeia.
- AL-18: [CASO A CONFIRMAR] Filmagem própria/autorizada. Não forçar toque, aproximação ou permanência do animal; pausar captação se necessário. Ray confirma informação atual da formação e resposta ao comentário. Não usar o gesto como atestado de caráter ou qualificação.

Os marcadores [CASO A CONFIRMAR] são internos, nunca para narrar/mostrar ao público. Nenhum caso histórico ou fenômeno foi tratado como fato sem fonte primária. Nenhum vídeo foi assistido, cliente citado, entrega por DM prometida ou serviço externo acessado. Nada agendado/publicado; captação, fontes/consentimentos e revisão humana continuam necessários.
