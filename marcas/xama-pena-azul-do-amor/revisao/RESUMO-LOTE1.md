# Revisão independente · lote 1 · XN-23 a XN-36

**Nota editorial: 8/10.** Os rascunhos preservam o tom da marca e assinalam lacunas factuais. A nota avalia apenas o material editorial, não prevê desempenho nem libera publicação. As partes condicionais continuam em estado `rascunho`.

**Peças alteradas:** XN-23, XN-24, XN-25, XN-26, XN-28, XN-30, XN-31, XN-33, XN-34 e XN-35. Cada arquivo registra no topo “Revisão lote 1: o que mudou”.

**Peças intactas:** XN-27, XN-29, XN-32 e XN-36. Seus roteiros já tinham uma cena ou pergunta específica e um pedido único. Os registros correspondentes dos dois CSVs foram alinhados aos roteiros; em XN-32, o gancho do calendário deixou de afirmar que uma pergunta é frequente sem fonte.

## Cinco problemas encontrados

1. Ganchos de XN-23, XN-26, XN-28 e XN-33 mostravam movimento, mas a fala ou o texto não identificava imediatamente o assunto.
2. XN-30 mandava uma reflexão sobre limites para a sessão de Cortes; ALIVIO agora nomeia a conversa sobre autovalor e limites.
3. XN-24 e XN-31 dependem de guia ou oferta atual para responder às perguntas; as capas foram concretizadas, mas os campos `[CASO A CONFIRMAR]` impedem arte final.
4. Os CTAs, hashtags e quadros dos CSVs ainda descreviam links, WhatsApp ou interações adicionais ausentes nas peças. Foram sincronizados para os 14 IDs, sem mudar datas ou estado.
5. XN-35 usava uma pedra sem conexão clara com o assunto. A mesa e a cadeira mostram uma conversa reconhecível; os três valores continuam como sugestões a confirmar com Ray.

## Dependências de Ray

- **Oferta:** descrição vigente, formato e limites de Cortes e Chamado para XN-24, XN-28, XN-31 e XN-34. Não preencher slides ou falas condicionais com preço, etapa ou duração presumidos.
- **Fala pessoal:** validar a descrição em primeira pessoa de XN-33 e escolher ou substituir os três valores sugeridos em XN-35. Confirmar disponibilidade de resposta manual aos DMs previstos.
- **Fonte:** guia pós-sessão aprovado para XN-24; pergunta real de 11/11 e resposta para XN-26; pergunta anonimizada e autorizada e resposta atual para XN-32. Sem isso, os campos marcados não são copy publicável.

## Validação

Lint Meta nas 14 peças `XN-*.md`, sem incluir `VALIDACAO.md`: **0 ocorrências** de termos proibidos ou prazo no padrão testado. Comando executado na raiz, em PowerShell, com leitura UTF-8 e normalização de acento/caixa:

```powershell
@'
from pathlib import Path
import re, unicodedata
root = Path('entrega/xama-pena-azul-do-amor/producao')
files = [p for w in ('semana-2026-11-16', 'semana-2026-11-23') for p in (root/w).glob('XN-*.md')]
def norm(s):
    return ''.join(c for c in unicodedata.normalize('NFD', s.casefold()) if unicodedata.category(c) != 'Mn')
hits = []
for p in files:
    s = norm(p.read_text(encoding='utf-8'))
    hits += [(p.name, t) for t in ('amarracao', 'trazer o amor de volta', 'garantido', 'feitico', 'magia') if t in s]
    if re.search(r'em\s+(?:24\s*h|\d+\s*dias?)', s): hits.append((p.name, 'prazo'))
print('Lint Meta:', len(files), 'peças;', len(hits), 'ocorrências;', hits)
raise SystemExit(bool(hits))
'@ | py -
```

Os dois CSVs foram lidos como CSV UTF-8: XN-23 a XN-36 têm IDs, datas e estado `rascunho` correspondentes, quatro quadros por Story e o mesmo `story_cta` nos dois arquivos. Palavras-chave usadas: **ALIVIO**, **CORTE**, **ALMAGEMEA**. XN-29 e XN-36 usam apenas caixa/enquete, sem palavra-chave. **Exceções de CTA duplo: nenhuma** nas peças; quando há Reel ou carrossel com Stories vinculados, o pedido se repete nas duas superfícies como uma ação por peça.

`ig-human` não encontrou trocas lexicais, tipográficas ou caracteres invisíveis nas dez legendas. O linter `ig-caption`, voltado a CTAs em inglês, marcou `ONE ASK` como aviso para o verbo português “Envie”; a conferência em português verificou um pedido por legenda, primeira linha de até 125 caracteres e 3–5 hashtags relacionadas ao tema.
