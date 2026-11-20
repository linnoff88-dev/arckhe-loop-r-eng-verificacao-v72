# VerificaÃ§Ã£o e Evals â€” FormaÃ§Ã£o LOOP-R Engenharia (curso 1 de 6)

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


Curso aberto e gratuito do INEMA.CLUB no formato INEMA Learning v7.2, em portuguÃªs, inglÃªs e espanhol:
**https://inematds.github.io/loop-r-eng-verificacao-v72/** Â· [EN](https://inematds.github.io/loop-r-eng-verificacao-v72/en/) Â· [ES](https://inematds.github.io/loop-r-eng-verificacao-v72/es/)

Oito aulas para quem jÃ¡ usa Claude Code ou Codex no terminal: avaliador separado e cÃ©tico, critÃ©rio comando â†’ saÃ­da e o avaliador do `/goal`, testes congelados com guarda, detecÃ§Ã£o de atalho (reward hacking), conjunto de ouro com regressÃ£o, juiz por modelo calibrado, pass@k Ã— pass^k e um portÃ£o em camadas para o seu loop.

## O kit (`kit/`)

Scripts pequenos (python3 + pytest + git). Todos tÃªm um ensaio sem custo (agente, avaliador e juiz falsos) e um caminho real por variÃ¡vel (`AVALIADOR_CMD`, `--agente`, `JUIZ_CMD`) que usa `claude -p --tools ""` ou `codex exec -s read-only` pela sua assinatura.

| arquivo | aula | o que faz |
|---|---|---|
| `ensaio.sh`, `agente-falso.sh` | todas | projeto de teste com 3 testes visÃ­veis e 3 escondidos; agente falso (bom, mente, apaga, conftest, chumba) |
| `avaliar.sh`, `prompt-avaliador.md`, `avaliador-falso.sh` | 1 | avaliador separado: roda o teste por fora e manda diff + saÃ­da a outro avaliador |
| `conferir-goal.py`, `goal-ensaio.md` | 2 | roda cada critÃ©rio `comando` â†’ `saÃ­da` do goal.md |
| `guarda-testes.py` | 3 | congela testes, conftest e config do pytest fora do repo e confere |
| `atalhos.py` | 4 | testes escondidos + sinais de atalho no diff |
| `evals/` | 5, 7 | conjunto de ouro, runner com regressÃ£o, pass@k e pass^k |
| `juiz/` | 6 | rubrica sim/nÃ£o, juiz com repetiÃ§Ãµes, calibraÃ§Ã£o (concordÃ¢ncia e kappa) |
| `portao.sh` | 8 | as camadas em fila, baratas primeiro |

```bash
git clone https://github.com/inematds/loop-r-eng-verificacao-v72 ~/projetos/loop-r-eng-verificacao-v72
K=~/projetos/loop-r-eng-verificacao-v72/kit && bash $K/ensaio.sh
```

## Gerar o site

ConteÃºdo em `conteudo/<idioma>/` (JSON). O HTML Ã© gerado: `python3 gerar.py && python3 validar.py --links` (e `--lang en|es`). NÃ£o edite o HTML Ã  mÃ£o.

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>