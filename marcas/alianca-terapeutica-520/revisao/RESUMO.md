# Revisão independente · Aliança Terapêutica 520

**Nota do conjunto original: 6/10.** As peças respeitam o estado de rascunho, usam cenas próprias e evitam promessas de resultado. Perdem força pela repetição de ângulos e pelo CTA comercial em histórias que ainda não construíram essa ponte. A nota é editorial, não previsão de alcance.

**Lidos:** AL-01 a AL-13, os três arquivos semanais de Stories e o calendário/planejamento de 28/10 a 13/11. O restante do calendário foi consultado para coerência de pauta e palavras-chave, sem avaliar peças ainda não produzidas.

**IDs revisados:** AL-01, AL-02, AL-03, AL-04, AL-05, AL-06, AL-07, AL-08, AL-09, AL-10, AL-11, AL-12, AL-13; STORIES-2026-10-26, STORIES-2026-11-02, STORIES-2026-11-09.

**IDs sem alteração:** nenhum entre AL-01 e AL-13. Nos Stories, os dias 26, 27 e 30/10; 01, 02, 04 e 08/11; 10 e 12/11 não receberam nova copy. As revisões semanais indicam os dias alterados.

## Cinco problemas mais frequentes

1. `CURSOS` aparece em todo Reel, com pouca ligação explícita entre a história e a informação que a pessoa receberia.
2. Gancho nomeia a ação, mas nem sempre cria pergunta ou mudança clara antes dos 3 segundos.
3. Cenas e argumentos se repetem: gato e espaço, vento e gratidão, listas de perguntas sobre práticas.
4. Legendas de Reels resumem a cena ou explicam a intenção cedo demais; carrosséis começam por títulos genéricos.
5. Alguns Stories pedem resposta a enquete/caixa e depois DM ou link; hashtags de AL-01 a AL-03 não acompanham o assunto.

## Cinco regras para as próximas specs

1. Definir para cada Reel uma decisão visível no quadro 0 e uma mudança até 3 segundos; texto de tela com uma ideia curta.
2. Se duas peças compartilham objeto ou prática na mesma quinzena, escrever o ângulo exclusivo de cada uma antes do roteiro.
3. Abrir a legenda com detalhe concreto da história ou pergunta específica do carrossel; deixar o contexto e um CTA único depois.
4. Amarrar cada palavra-chave à entrega real: `REIKI` para conteúdo de Reiki; `CURSOS` para informações sobre práticas da formação, sem prometer atendimento ou resultado.
5. Em Stories, escolher um pedido por sequência. Enquete, caixa, quiz, DM e link contam como ações; usar sticker de link apenas com destino validado.

## Verificação

Lint Meta local, sem rede, aplicado aos arquivos das peças revisadas:

```powershell
$hits = Get-ChildItem -LiteralPath 'entrega\alianca-terapeutica-520\revisao' -Filter '*.md' -File | Where-Object { $_.Name -ne 'RESUMO.md' } | Select-String -Pattern 'amarra[cç][aã]o|trazer o amor de volta|garantid[oa]|em 24h|em [0-9]+ dias?|feiti[cç]o|magia'; $hits.Count
```

**Resultado:** `0`. Não há afirmação de atributo pessoal de quem assiste nem resultado por causa espiritual nas cópias propostas. As legendas passaram pelo analisador local de `ig-caption` e pela função de `ig-human`; ganchos e Stories foram revistos manualmente. O detector de pedidos da skill está calibrado para inglês e não reconhece imperativos em português, então o CTA único foi conferido manualmente.

**Estado:** rascunho; nenhum conteúdo foi publicado ou agendado.
