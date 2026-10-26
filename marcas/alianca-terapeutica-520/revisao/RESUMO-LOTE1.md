# Revisão independente · lote 1 · Aliança Terapêutica 520

**Nota editorial: 7,5/10.** AL-14 a AL-23 têm cenas próprias propostas, legendas concretas, um pedido por peça e limites explícitos. A nota considera os roteiros em rascunho; não mede desempenho nem valida material que ainda não foi gravado.

**IDs alterados:** AL-14, AL-15, AL-16, AL-17, AL-18, AL-19, AL-20, AL-21, AL-22, AL-23; Stories de 16 a 29/11. **IDs intactos no lote:** nenhum. Estado, IDs e datas foram preservados. Os dois CSVs foram sincronizados apenas nas linhas do período.

## Cinco problemas encontrados

1. Os Reels de gato repetiam proximidade e espera; em AL-14 e AL-23 o animal podia nem aparecer no quadro inicial. Agora os objetos e a decisão humana aparecem no mesmo plano, sem dirigir o animal.
2. A primeira tela de AL-16 dependia da fala para revelar que a cena era chuva. Agora nomeia a cena sem som.
3. Terceiros quadros dos Stories de 16 a 27/11 repetiam a mesma frase genérica, mesmo em conteúdos de aroma, radiestesia ou pausa. Foram ligados ao detalhe real de cada pauta.
4. Parte das hashtags descrevia espiritualidade e bem-estar genéricos em vez de frasco, pêndulo, pausa ou guarda-chuva. Foram alinhadas ao assunto de cada peça.
5. Calendário e CSV de Stories ainda traziam CTAs e sequências anteriores à produção, inclusive DM/link onde a peça pede salvar ou comentar. Foram alinhados aos arquivos semanais.

## Dependências do Ray

- **Oferta:** confirmar proposta atual da formação, práticas incluídas e resposta manual para pedidos `CURSOS`; os carrosséis não confirmam currículo, serviço ou protocolo.
- **Fala pessoal:** aprovar a frase de oração de AL-19 e qualquer fala em primeira pessoa antes da gravação; sem atribuir experiência pessoal não fornecida.
- **Fonte:** fornecer captações próprias/autorizadas de animal, chuva, vento e cenas propostas; validar termos técnicos de aromaterapia e radiestesia com pessoa habilitada. Até lá, permanecem os avisos `[CASO A CONFIRMAR]` nas peças dependentes de gravação.

## Verificação local

Comando de lint Meta, excluindo `VALIDACAO.md` por citar os termos da regra:

```powershell
rg -n -i 'amarra[cç][aã]o|trazer o amor de volta|garantid[oa]|em 24h|em [0-9]+ dias?|feiti[cç]o|magia' entrega/alianca-terapeutica-520/producao/semana-2026-11-16 entrega/alianca-terapeutica-520/producao/semana-2026-11-23 -g '!VALIDACAO.md'
```

Resultado: **zero ocorrências** (código 1 do `rg`). Revisão manual: nenhuma promessa de resultado por causa espiritual nem afirmação de atributo pessoal do espectador. CSVs lidos em UTF-8 com `csv.DictReader`: IDs e datas iguais à versão anterior; AL-14 a AL-23 com legenda até 125 caracteres na primeira linha, três a cinco hashtags, CTA e `story_cta` iguais ao quadro final; palavras-chave do período limitadas a `CURSOS` ou vazias. **Exceções de CTA único: nenhuma** nas peças e sequências semanais. Stories avulsos têm uma caixa, enquete ou quiz cada, sem segundo pedido. Nenhum conteúdo foi publicado ou agendado.
