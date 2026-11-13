# Situação 1 — Planejar: o que testar primeiro?

**App:** MarmitaJá (`apps/marmitaja/`)

## A situação

> O MarmitaJá vai ao ar **segunda-feira** no restaurante. A equipe que fez o app diz que “está tudo funcionando”. O dono do restaurante contratou a sua equipe para testar, mas avisou: **vocês têm só uma tarde**. Ele quer saber o que vão testar, por que essas coisas primeiro e, no fim, se o app pode ou não ir ao ar.

## Pesquisar (10 min)

1. O que é um **plano de teste**? Quais partes ele costuma ter? (Procurem pela norma IEEE 829 ou ISO/IEC/IEEE 29119.)
2. O que é **teste baseado em risco**? Como se decide o que testar primeiro quando o tempo é curto?
3. O que são as técnicas **valor limite** e **partição de equivalência**? Deem um exemplo de cada.
4. Por que é melhor o app ser testado por **outra equipe**, e não por quem o programou?

## Solucionar (10 min)

Copiem `modelos/PLANO-DE-TESTE.md` para `entregas/PLANO-DE-TESTE-MarmitaJa.md` e preencham:

- o **escopo** (o que entra e o que fica de fora);
- uma **análise de risco**: para cada regra RN01 a RN07, a chance de dar problema e o prejuízo se der (baixo, médio, alto), e a **ordem** em que vão testar;
- **10 casos de teste ou mais**, com pelo menos **3 de valor limite**, cada um com a regra, a entrada exata e o esperado tirado do requisito.

## Aplicar (20 min)

1. Executem os casos **na ordem do risco**.
2. Para cada caso, anotem o obtido e o status: Passou, Falhou ou Bloqueado.
3. Para cada caso que falhou, anotem a evidência (print) no plano.
4. Preencham o resumo: quantos passaram, quantos falharam, e a **recomendação**: o MarmitaJá pode ir ao ar segunda? Por quê?

## Mostrar na apresentação

- A tabela de risco e por que vocês escolheram aquela ordem.
- Um caso de valor limite que pegou um defeito, com o print.
- A recomendação final: vai ao ar ou não, e o que precisa ser corrigido antes.

**Entrega:** `entregas/PLANO-DE-TESTE-MarmitaJa.md` e `entregas/APRESENTACAO-grupo-N.md`.
