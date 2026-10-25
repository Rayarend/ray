# organizar-xama-r3 — revisar, integrar e publicar no GitHub
Repo Rayarend/ray. Branch local `organizar-xama-20261025` (commits 3e32ed7 + 48311b5, sobre db754a0). Leia AGENTS.md e operacao/ORQUESTRACAO.md.
origin/main avançou 2 commits (fbf77b9, 44ffd8d) que só mexem em conteudo/topo-de-funil (Seres).

## Objetivo
1. Revisar os 2 commits locais contra os critérios abaixo; corrigir só o que falhar.
2. Escrever operacao/ENTREGA-2026-10-25.md (o que foi organizado, pendências) e atualizar operacao/QUADRO.md (5 marcas, estado de cada uma).
3. `git fetch`, rebase da branch sobre origin/main, push sem força para main.

## Arquivos permitidos
operacao/ENTREGA-2026-10-25.md, operacao/QUADRO.md, e correções pontuais em marcas/**, .claude/skills/orquestrar-marcas/SKILL.md, .gitignore.

## Critério de pronto
- CALENDARIO.csv do Xamã: 37 linhas, 16 REEL, 11 CARROSSEL, colunas marca_id/canal_instagram/canal_facebook/canal_tiktok preenchidas.
- registro.json com 5 marcas; todos os JSON de marcas/ carregam.
- `grep -rIE "C:/|/c/Users|drive.google|docs.google|canva.com/design|Downloads"` em marcas/, operacao/, .claude/ = vazio.
- conteudo/topo-de-funil sem alteração vinda desta branch.
- ENTREGA lista pendências do Ray: ID da página Facebook do Xamã, criar TikTok, logos (brand-kit/logos vazio), Facebook/TikTok das outras 4 marcas.
- Push aceito sem --force/--force-with-lease; se rejeitar, fetch+rebase de novo, nunca forçar.

## Proibições
Não publicar em rede social, não chamar n8n/Supabase/Meta/Metricool, não ler .env, não mexer em conteudo/topo-de-funil. Python via `py`, UTF-8. Entrega: JSON do _infra/codex/schema/resultado.json.
