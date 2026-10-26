# Revisão independente — Xamã — XN-02 a XN-22

**Nota editorial das peças originais: 7/10.** Há cuidado com a política Meta, linguagem acolhedora e identificação de pendências reais. A força dos ganchos, a distinção entre peças e o alinhamento dos CTAs ainda variam. A nota é avaliação editorial, não métrica de desempenho.

**Escopo lido:** 21 peças individuais das três semanas, os três consolidados `STORIES.md`, os 21 registros correspondentes em `CALENDARIO.csv` e `STORIES.csv`, o plano editorial e as referências em `docs/instagram/xama/`. As revisões propostas são rascunhos; nenhuma peça original foi alterada.

**IDs revisados:** XN-02, XN-03, XN-04, XN-05, XN-06, XN-07, XN-08, XN-13, XN-14, XN-15, XN-16, XN-17, XN-18, XN-19, XN-20, XN-21, XN-22.

**IDs sem alteração:** XN-09, XN-10, XN-11, XN-12. Neles, a abertura já conduz à ideia central, há um pedido principal coerente e nenhuma melhora pontual justificou arquivo próprio.

## Cinco problemas mais frequentes

1. Ganchos amplos que não exploram o gesto visível no quadro 0 ou a capa do carrossel.
2. Repetição de agenda, caderno, descanso, escuta e respeito entre peças próximas, sobretudo XN-02/XN-14/XN-16/XN-20 e XN-06/XN-13/XN-21.
3. Primeira linha de legenda abstrata ou repetição da capa antes de entregar uma cena ou pergunta concreta.
4. CTA de Stories que concorre com enquete/caixa, usa palavra-chave distante do tema ou aponta a link ainda sem destino validado.
5. Formulações sobre etapas, formato, história pessoal ou visão espiritual que dependem de confirmação de Ray; XN-05 também depende do corte original.

## Cinco regras para as próximas specs

1. Especificar uma ação real já no quadro 0 e uma mudança visível antes de três segundos; na capa, usar um contraste ou uma pergunta concreta.
2. Registrar o ângulo que diferencia a peça das duas anteriores do mesmo pilar, com objeto e cena próprios quando houver material real.
3. Começar a legenda com uma frase útil nos primeiros 125 caracteres; manter uma chamada clara e coerente com o formato.
4. Associar ALIVIO a autovalor, CORTE à proposta de Cortes e ALMAGEMEA à proposta do Chamado; em Stories, escolher caixa/enquete **ou** DM como ação principal.
5. Marcar como condicionais cenas, falas, detalhes de oferta e links ainda não confirmados; nunca preencher uma lacuna com resultado, prazo, relato ou destino presumido.

## Lint Meta

Executado nas seções de copy melhorada dos arquivos `XN-*.md`, ignorando o diagnóstico editorial. A busca normaliza caixa e acento; a leitura manual verifica alegações de resultado e atribuições pessoais ao espectador. Resultado: **zero ocorrências nas versões melhoradas**.

Comando executado no PowerShell, na raiz do repositório:

```powershell
@'
from pathlib import Path
import re, unicodedata
root = Path('entrega/xama-pena-azul-do-amor/revisao')
terms = ('amarracao', 'trazer o amor de volta', 'garantido', 'feitico', 'magia')
def norm(s):
    return ''.join(c for c in unicodedata.normalize('NFD', s.casefold()) if unicodedata.category(c) != 'Mn')
hits = []
files = sorted(root.glob('XN-*.md'))
for file in files:
    copy = norm(file.read_text(encoding='utf-8').split('**Gancho', 1)[1])
    for term in terms:
        if term in copy:
            hits.append((file.name, term))
    if re.search(r'em\s+(?:24\s*h|\d+\s*dias?)', copy):
        hits.append((file.name, 'prazo'))
print(f'Lint Meta: {len(files)} revisões; {len(hits)} ocorrências; {hits}')
raise SystemExit(bool(hits))
'@ | py -
```

**Pendências para uso:** Ray deve confirmar fala e oferta em XN-07, formato online em XN-17, história real em XN-19 e visão espiritual em XN-21; conferir o corte da VSL em XN-05 e os contatos de perfil citados. Os links sem destino validado do calendário não entram nas versões propostas.
