# Situação 3 — Triar: 12 Issues e pouco tempo

**App:** FitPass (`apps/fitpass/`)

## A situação

> O FitPass foi testado por outra equipe, que abriu **12 Issues** (estão em `materiais/ISSUES-RECEBIDAS-FitPass.md`). A equipe de desenvolvimento só tem tempo para corrigir **algumas** antes da campanha de matrículas de segunda. O gerente pediu à sua equipe: **descubram quais são defeitos de verdade, joguem fora o que não é, e digam em que ordem corrigir.**

## Pesquisar (10 min)

1. O que é **triagem de defeitos**? Quem participa e o que se decide nela?
2. Quando uma Issue deve ser **rejeitada**? E quando é **duplicada**? O que fazer quando ela está **incompleta**?
3. Qual a diferença entre **severidade** e **prioridade**? Quem decide cada uma?
4. O que é **reteste** e o que é **teste de regressão**? Qual a diferença?

## Solucionar (10 min)

Escrevam em `entregas/CRITERIOS-TRIAGEM.md`:

- quando a equipe **confirma**, **rejeita**, marca como **duplicada** ou pede **mais informação**;
- como decidem a **prioridade** (o que corrigir primeiro), além da severidade.

## Aplicar (20 min)

1. Copiem `modelos/TRIAGEM.md` para `entregas/TRIAGEM-FitPass.md`.
2. Para cada uma das 12 Issues: **reproduzam no app**, com os dados que estão nela, e confiram a regra no `REQUISITOS-FitPass.md`.
3. Decidam: confirmada, rejeitada, duplicada ou incompleta, sempre com a **regra** que justifica.
4. Para as confirmadas, definam a severidade e a **ordem de correção**.
5. Registrem as **confirmadas** como Issues no repositório do grupo (**Issues → New issue → Relato de defeito**), já com a label de severidade, para a equipe de desenvolvimento começar segunda.
6. Escrevam o **plano de reteste**: para cada confirmada, o caso que vai provar que a correção funcionou.

## Mostrar na apresentação

- O placar: quantas confirmadas, rejeitadas, duplicadas e incompletas.
- Uma Issue rejeitada e a regra que mostra por quê.
- A ordem de correção e o motivo da primeira da fila.

**Entrega:** `entregas/CRITERIOS-TRIAGEM.md`, `entregas/TRIAGEM-FitPass.md`, as Issues confirmadas e `entregas/APRESENTACAO-grupo-N.md`.
