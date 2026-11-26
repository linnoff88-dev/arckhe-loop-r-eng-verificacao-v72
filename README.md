ï»¿# VerificaêÂ§êÂ£o e Evals ê¢â¬â FormaêÂ§êÂ£o LOOP-R Engenharia (curso 1 de 6)

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


Curso aberto e gratuito do INEMA.CLUB no formato INEMA Learning v7.2, em portuguêÂªs, inglêÂªs e espanhol:
**https://inematds.github.io/loop-r-eng-verificacao-v72/** êÂ· [EN](https://inematds.github.io/loop-r-eng-verificacao-v72/en/) êÂ· [ES](https://inematds.github.io/loop-r-eng-verificacao-v72/es/)

Oito aulas para quem jêÂ¡ usa Claude Code ou Codex no terminal: avaliador separado e cêÂ©tico, critêÂ©rio comando ê¢â â saêÂ­da e o avaliador do `/goal`, testes congelados com guarda, detecêÂ§êÂ£o de atalho (reward hacking), conjunto de ouro com regressêÂ£o, juiz por modelo calibrado, pass@k êâ pass^k e um portêÂ£o em camadas para o seu loop.

## O kit (`kit/`)

Scripts pequenos (python3 + pytest + git). Todos têÂªm um ensaio sem custo (agente, avaliador e juiz falsos) e um caminho real por variêÂ¡vel (`AVALIADOR_CMD`, `--agente`, `JUIZ_CMD`) que usa `claude -p --tools ""` ou `codex exec -s read-only` pela sua assinatura.

| arquivo | aula | o que faz |
|---|---|---|
| `ensaio.sh`, `agente-falso.sh` | todas | projeto de teste com 3 testes visêÂ­veis e 3 escondidos; agente falso (bom, mente, apaga, conftest, chumba) |
| `avaliar.sh`, `prompt-avaliador.md`, `avaliador-falso.sh` | 1 | avaliador separado: roda o teste por fora e manda diff + saêÂ­da a outro avaliador |
| `conferir-goal.py`, `goal-ensaio.md` | 2 | roda cada critêÂ©rio `comando` ê¢â â `saêÂ­da` do goal.md |
| `guarda-testes.py` | 3 | congela testes, conftest e config do pytest fora do repo e confere |
| `atalhos.py` | 4 | testes escondidos + sinais de atalho no diff |
| `evals/` | 5, 7 | conjunto de ouro, runner com regressêÂ£o, pass@k e pass^k |
| `juiz/` | 6 | rubrica sim/nêÂ£o, juiz com repetiêÂ§êÂµes, calibraêÂ§êÂ£o (concordêÂ¢ncia e kappa) |
| `portao.sh` | 8 | as camadas em fila, baratas primeiro |

```bash
git clone https://github.com/inematds/loop-r-eng-verificacao-v72 ~/projetos/loop-r-eng-verificacao-v72
K=~/projetos/loop-r-eng-verificacao-v72/kit && bash $K/ensaio.sh
```

## Gerar o site

ConteêÂºdo em `conteudo/<idioma>/` (JSON). O HTML êÂ© gerado: `python3 gerar.py && python3 validar.py --links` (e `--lang en|es`). NêÂ£o edite o HTML êÂ  mêÂ£o.

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>