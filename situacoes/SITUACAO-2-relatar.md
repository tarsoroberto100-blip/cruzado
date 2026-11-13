# Situação 2 — Relatar: “tá dando erro na reserva”

**App:** QuadraLivre (`apps/quadralivre/`)

## A situação

> A equipe que programou o QuadraLivre recebeu esta mensagem de um testador: **“tá dando erro na reserva, às vezes cobra errado, às vezes some, arruma aí”**. Eles passaram uma tarde tentando e **não conseguiram reproduzir nada**. O gerente decidiu: a partir de hoje, todo defeito vai para o **bugtracker** (as Issues do GitHub), num formato que qualquer pessoa consiga reproduzir. A sua equipe vai criar esse padrão e mostrar que ele funciona.

## Pesquisar (10 min)

1. O que é um **bugtracker**? Citem 3 ferramentas usadas no mercado (o GitHub Issues é uma).
2. Quais campos um **bom relatório de defeito** precisa ter? Por que cada um importa?
3. Qual a diferença entre **severidade** e **prioridade**? Deem um exemplo de defeito com severidade alta e prioridade baixa.
4. O que é o **ciclo de vida de um defeito** (novo, confirmado, em correção, corrigido, retestado, fechado)?

## Solucionar (10 min)

1. Abram o modelo de Issue que já vem no repositório (`.github/ISSUE_TEMPLATE/defeito.md`) e comparem com o que pesquisaram. Falta algum campo? Melhorem o modelo e façam commit.
2. No repositório do grupo, criem as **labels** de severidade: `crítica`, `alta`, `média` e `baixa` (**Issues → Labels → New label**), e escrevam em `entregas/CRITERIOS-SEVERIDADE.md` quando usar cada uma.
3. Reescrevam a mensagem do testador (“tá dando erro na reserva…”) e expliquem por que ela não pode ser reproduzida.

## Aplicar (20 min)

1. Testem o QuadraLivre contra o `REQUISITOS-QuadraLivre.md`: horários, preços, horário nobre, sócio, conflito de horário e o F5.
2. Para cada defeito encontrado, abram **uma Issue** no repositório do grupo: **Issues → New issue → Relato de defeito**, com passos, dados exatos, esperado do requisito, obtido, print e label de severidade.
3. Meta: **4 Issues ou mais**, uma por defeito.
4. Teste final do padrão: peçam a um colega de **outro grupo** que leia uma Issue e reproduza o defeito sem fazer nenhuma pergunta.

## Mostrar na apresentação

- A mensagem original do testador ao lado da Issue de vocês.
- A Issue mais bem escrita, aberta na tela.
- O resultado do teste com o colega de outro grupo: ele conseguiu reproduzir?

**Entrega:** as Issues no repositório, `entregas/CRITERIOS-SEVERIDADE.md` e `entregas/APRESENTACAO-grupo-N.md`.
