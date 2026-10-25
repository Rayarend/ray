# organizar-xama-r2 — juntar conteúdo do Xamã + registrar demais contas
Repo público (Rayarend/ray), branch `organizar-xama-20261025`. Base: commit 3e32ed7. Leia AGENTS.md e operacao/ORQUESTRACAO.md.

## Objetivo
1. Trazer o planejamento de novembro do Xamã para dentro da marca, sinalizado como Xamã Pena Azul do Amor, canais Instagram + Facebook (TikTok = a criar).
2. Registrar as outras contas do Ray como marcas, para todo conteúdo futuro nascer com `marca_id` + canal.
3. Expor a skill de orquestração também para o Claude.

## Fontes (somente leitura, fora do repo)
- C:/Users/Desktop/projetos/instagram/claude-instagram/xama-pena-azul/planejamento-2026-11/{PLANEJAMENTO.md,CALENDARIO.csv,FONTES.json}

## Arquivos permitidos (lista fechada)
- marcas/xama-pena-azul-do-amor/planejamento/2026-11/PLANEJAMENTO.md, CALENDARIO.csv, FONTES.json (cópias saneadas)
- marcas/xama-pena-azul-do-amor/README.md, marca.json
- marcas/{curandeira-do-amor,igreen-brasil,alianca-terapeutica-520}/marca.json e README.md (novos)
- marcas/registro.json, marcas/README.md
- .claude/skills/orquestrar-marcas/SKILL.md (cópia de .agents/skills/orquestrar-marcas/SKILL.md)
- operacao/QUADRO.md, operacao/ENTREGA-2026-10-25.md

## Regras de conteúdo
- CALENDARIO.csv: manter as 37 linhas e colunas atuais; ACRESCENTAR no início as colunas `marca_id` (=xama-pena-azul-do-amor), `canal_instagram` (@xama.pena.azul.do.amor), `canal_facebook` (Xamã Pena Azul do Amor — página pendente de ID), `canal_tiktok` (a_criar). Status continua "planejado; não agendado".
- FONTES.json/PLANEJAMENTO.md: remover caminhos locais (C:\, /c/Users), links de edição Canva/Drive, nomes/dados de clientes e trechos de manuscrito (campos tipo capitulos, autor_nominal, cortes_vsl: trocar o conteúdo por "fonte privada local"). Métricas próprias do perfil podem ficar.
- Novas marcas (marca.json no mesmo formato do Xamã): Curandeira @curandeira.doamor; Igreen @igreen_brasil_; Aliança @aliancaterapeutica520. Facebook e TikTok = null, estado "pendente_confirmar". Nada de IDs de Composio/n8n/Drive/Metricool (repo é público).
- README do Xamã: seção "Onde está cada coisa" por tipo de material (estratégia, auditorias, reels semanais, funil Cortes/Chamado, Drive de postagem) SEM caminhos locais, dizendo que o mapa privado fica fora do repo.

## Critério de pronto
- CSV válido (py csv): 37 linhas de dados + cabeçalho, 4 colunas novas preenchidas.
- Todos os JSON carregam com `py -c "import json..."`; registro.json lista 5 marcas.
- `grep -rIE "C:\\\\|/c/Users|canva.com/design|docs.google|drive.google"` em marcas/ e .claude/ retorna vazio.
- Nenhum arquivo fora da lista alterado; conteudo/topo-de-funil intocado (Seres).

## Proibições
Sem rede, sem push, sem commit, sem .env/tokens, sem n8n/Supabase/Meta/Metricool. UTF-8 explícito; Python via `py`. Entrega: JSON do _infra/codex/schema/resultado.json.
