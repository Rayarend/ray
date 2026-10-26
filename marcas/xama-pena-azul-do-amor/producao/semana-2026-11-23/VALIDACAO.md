# Validação editorial · Issue #18 · semana-2026-11-23

marca_id: xama-pena-azul-do-amor
canal_instagram: @xama.pena.azul.do.amor
estado: rascunho

## Cobertura

IDs desta pasta: XN-30, XN-31, XN-32, XN-33, XN-34, XN-35, XN-36. Lote completo: XN-23 a XN-36, com 6 Reels, 4 carrosséis e 4 peças de Stories. Os dois consolidados contêm 14 blocos diários de quatro quadros. As quatro peças individuais de Stories têm copy idêntica ao bloco do dia.

Todas as linhas são `tipo_origem: original`; **nenhuma ficha remodelar-pendente** é necessária no período. Cada Reel tem três opções de gancho e storyboard, seguindo o formato das peças revisadas fornecidas como modelo. Nenhum vídeo foi assistido, renderizado ou publicado.

As dez legendas de feed têm primeira linha até 125 caracteres, total abaixo de 2.200, quatro hashtags específicas e um único CTA conferido manualmente. Os quatro carrosséis têm oito slides; capas de até seis palavras e corpos finais até 25 palavras por slide. Campos de confirmação são instruções editoriais, não texto pronto para imagem.

## Lint Meta executado

Na raiz do repositório, a busca abaixo reproduz o comando executado. Inclui os 16 arquivos de peça/Stories e exclui somente os relatórios técnicos. Resultado: **16 arquivos; zero ocorrências**. A revisão manual também conferiu promessas, atributos pessoais e a origem dos casos; a regex sozinha não valida essas questões.

```bash
python3 - <<'PY'
from pathlib import Path
import re, unicodedata
base = Path('entrega/xama-pena-azul-do-amor/producao')
files = sorted(p for week in ('semana-2026-11-16', 'semana-2026-11-23')
               for p in (base / week).glob('*.md') if p.name != 'VALIDACAO.md')
def norm(s):
    return ''.join(c for c in unicodedata.normalize('NFD', s.casefold())
                   if unicodedata.category(c) != 'Mn')
patterns = (r'amarracao', r'trazer o amor de volta', r'garantid[oa]s?',
            r'feitico', r'\bmagia\b', r'em\s+(?:24\s*h|\d+\s*dias?)')
hits = [(str(p), term) for p in files for term in patterns
        if re.search(term, norm(p.read_text(encoding='utf-8')))]
print(f'Lint Meta: {len(files)} arquivos; {len(hits)} ocorrencias; {hits}')
raise SystemExit(bool(hits))
PY
```

## Ferramentas de linguagem: resultado real

`humanize.py` e `detect.py` foram executados nas 16 peças/consolidados. Os painéis usam a copy extraída de falas, slides, legendas e quadros, sem metadados para inflar notas. Cabeçalhos e campos de máquina foram preservados. Modelo das chamadas executadas por arquivo:

```bash
python3 .agents/skills/ig-human/humanize.py ARQUIVO.md -o ARQUIVO.md --report
python3 .agents/skills/ig-human/detect.py --json < COPY_EXTRAIDA.txt
python3 .agents/skills/ig-caption/caption.py --json < LEGENDA_EXTRAIDA.txt
```

| Arquivo | Human score antes | Depois | Veredicto |
|---|---:|---:|---|
| STORIES.md | 41.2 | 41.2 | FLAGGED |
| XN-30.md | 51.6 | 53.4 | REVIEW |
| XN-31.md | 60.3 | 60.3 | REVIEW |
| XN-32.md | 27.6 | 27.6 | FLAGGED |
| XN-33.md | 52.8 | 52.8 | REVIEW |
| XN-34.md | 57.3 | 57.3 | REVIEW |
| XN-35.md | 57.0 | 57.0 | REVIEW |
| XN-36.md | 45.6 | 45.6 | FLAGGED |

**Nenhum painel retornou PASS.** No lote: 10 REVIEW e 6 FLAGGED. `detect.py` conta pronomes/contrações ingleses em VOICE e tokeniza palavras com `[A-Za-z]`, prejudicando a leitura de português; sequências curtas e campos condicionais também limitam os painéis. A nota não foi artificialmente corrigida com inglês, números inventados ou remoção de alertas. A leitura editorial manteve PT-BR, conferiu cenas concretas, clareza e variação. Os alertas não estão declarados resolvidos; o detector não certifica autoria/qualidade.

`caption.py`: dez legendas executadas, **zero FAIL**, todas REVIEW, nenhuma READY. ONE ASK não reconhece “Envie ... por DM”. HOOK IS CONCRETE usa nomes/números e também deixou aviso em XN-23, XN-27 e XN-35. As primeiras linhas dessas três mostram janela/sapato, convite que coincide com compromisso e escuta numa conversa. Os avisos foram lidos, não desativados. Conferência manual: um pedido por legenda e correspondência com a peça e os Stories. Sem URLs finais ou resposta automática presumida.

## Comparação de vizinhas

| Data | ID | Quadro/objeto principal | Ângulo |
|---|---|---|---|
| 16/11 | XN-23 | Janela abrindo e sapato | Recomeço concreto, sem agenda/caderno |
| 17/11 | XN-24 | Páginas com abas | Fonte da orientação pós-sessão |
| 18/11 | XN-25 | Xícara e caixa de escuta | Participação sem relato presumido |
| 19/11 | XN-26 | Folha desdobrada | Pergunta real a selecionar, sem print |
| 20/11 | XN-27 | Vasos separados | Companhia com espaço próprio |
| 21/11 | XN-28 | Placa que vira | Nome versus descrição do acompanhamento |
| 22/11 | XN-29 | Papel em varal | Escuta de temas, sem métricas fictícias |
| 23/11 | XN-30 | Rádio sendo baixado | Comunicação de limite, sem sumiço |
| 24/11 | XN-31 | Balões tipográficos | Perguntas sobre formato e duração |
| 25/11 | XN-32 | Microfone e rosto | Resposta real pendente |
| 26/11 | XN-33 | Ajuste de câmera | Bastidor do autor, sem cliente |
| 27/11 | XN-34 | Cartões com nomes | Comparação factual a preencher |
| 28/11 | XN-35 | Pedra e caminho | Valores propostos, sem simular ritual |
| 29/11 | XN-36 | Marcadores e enquete | Escolha de tema editorial |

Não há três vizinhas com a mesma ação/objeto. A ligação intencional entre peça e Stories do mesmo dia não constitui nova peça vizinha. Rosto aparece em vários materiais por identidade do autor, com gesto/contexto inicial diferente. A janela, o rádio e o caminho distinguem os novos Reels da recorrência de caderno/agenda nas semanas anteriores.

## Decisões e lacunas para Ray/Claude

- Para cumprir o CTA único da Issue, os convites foram alinhados a ALIVIO, CORTE e ALMAGEMEA, mesmo onde o feed do calendário cita compartilhamento/WhatsApp. CSVs intactos. XN-25 usa caixa com ALIVIO; XN-29 e XN-36 usam interação única, sem DM/link concorrente. A rotação de stickers do plano foi adaptada para não empilhar pedidos.
- XN-23 retoma somente o tema da referência própria de 08/10 identificada no TSV. Sem copiar cena, roteiro ou áudio e sem afirmar ter assistido ao vídeo ou prever desempenho novo.
- XN-24 precisa do guia pós-sessão aprovado; não houve acesso a manuscrito ou cópia dele.
- XN-26 precisa da pergunta real de 11/11 e da resposta de Ray. XN-32 depende de pergunta real anonimizada e uso autorizado. Nenhum depoimento foi inventado.
- XN-28, XN-31 e XN-34 dependem das descrições vigentes dos serviços. Não foram usados preços, etapas ou formatos históricos como oferta atual.
- XN-33 contém fala pessoal proposta que Ray precisa validar; ambiente/imagens precisam ser atuais. XN-35 sugere três valores, sem apresentá-los como escolhas já confirmadas de Ray.
- Links, horários de publicação, disponibilidade, métricas futuras e contatos qualificados não foram preenchidos. Datas das pastas são referências editoriais, não agendamentos.
- Os campos `[CASO A CONFIRMAR]` impedem gravação/arte final até preenchimento e revisão. Os rascunhos estão entregues para revisão, não liberados para publicação.
