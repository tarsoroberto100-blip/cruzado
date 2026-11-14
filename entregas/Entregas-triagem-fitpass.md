# Triagem das Issues — FitPass v1.0

**Integrantes:** Tarso, Jefferson

Decisões: **Confirmada** · **Rejeitada** · **Duplicada de #N** · **Incompleta**

| Issue | Reproduzimos? (dados usados) | Decisão | Regra que justifica | Severidade final | Prioridade (1 = primeiro) |
| --- | --- | --- | --- | --- | --- |
| #1 | Sim. Ana Lima, CPF 123.456.789-09, 20 anos, trimestral, sem estudante → matrícula R$ 50, total R$ 319.7 | **Confirmada** | RN05: matrícula isenta no trimestral. Esperado R$ 269,70 (RN07) | Alta | **1** |
| #2 | Sim. Bruno Lima, 20 anos, estudante, mensal → desconto R$ 22.49, total R$ 127.41 | **Confirmada** | RN06: desconto só sobre o plano (15% de 99,90 = R$ 14,99), nunca sobre a matrícula. Esperado total R$ 134,91 (exemplo do documento) | Alta | **2** |
| #3 | Sim. 25 anos, estudante, mensal → R$ 127.41 (mesmo resultado do #2) | **Duplicada de #2** | RN06: mesma causa do #2 (desconto aplicado também sobre a matrícula). Esperado R$ 134,91 | — | — |
| #4 | Sim. CPF 111.111.111-11, demais dados válidos → aceito | **Rejeitada** | RN02: o sistema confere **só o formato** (11 números). 111.111.111-11 tem 11 números, então aceitar está certo. Validar dígitos seria uma melhoria | — | — |
| #5 | Sim. 30 anos, mensal → "R$ 99.9", "R$ 50" e "R$ 149.9" | **Confirmada** | RNF01: todo valor no formato `R$ 0,00`. Esperado `R$ 149,90` (e `R$ 99,90`, `R$ 50,00`) | Baixa | **5** |
| #6 | Sim. 13 anos, autorização marcada, mensal → "A matrícula é permitida a partir de 14 anos." | **Rejeitada** | RN03: matrícula só a partir de 14 anos. A autorização não vale para menores de 14. A mensagem também cumpre a RNF02 | — | — |
| #7 | **Não.** A Issue não traz idade, plano, valor obtido nem valor esperado | **Incompleta** | Sem dados não há como comparar com RN06. (Em teste exploratório, idoso de 65 anos no mensal deu desconto R$ 29.98 em vez de R$ 19,98: mesma causa do #2. Só vira duplicada se o autor confirmar o cenário) | — | — |
| #8 | Sim. 14 anos, autorização marcada, mensal → "Menores de 18 anos precisam da autorização do responsável." | **Confirmada** | RN03: a partir de 14 anos, com autorização, a matrícula é aceita. Esperado total R$ 149,90. Causa: o limite está em "idade <= 14" | Alta | **4** |
| #9 | Não se aplica (não há passos nem regra) | **Rejeitada** | Nenhuma RN nem RNF fala de e-mail de confirmação. Não está no requisito, então é uma **melhoria** para o gerente decidir | — | — |
| #10 | Sim. 30 anos, anual → matrícula "Isenta", total R$ 958.8 | **Rejeitada** | RN05: matrícula é **isenta** nos planos trimestral e anual. O app está certo; o esperado da Issue contraria o requisito | — | — |
| #11 | Sim. 65 anos, estudante, anual → desconto 35% (R$ 335.58), total R$ 623.22 | **Confirmada** | RN06: os descontos não se somam, vale só o maior (20%). Esperado desconto R$ 191,76 e total R$ 767,04 | Média | **3** |
| #12 | Sim. 30 anos, trimestral → matrícula R$ 50, total R$ 319.7 | **Duplicada de #1** | RN05: mesmo defeito do #1 (taxa no trimestral). Esperado R$ 269,70 | — | — |

## Placar

| Confirmadas | Rejeitadas | Duplicadas | Incompletas |
| --- | --- | --- | --- |
| 5 (#1, #2, #5, #8, #11) | 4 (#4, #6, #9, #10) | 2 (#3 → #2, #12 → #1) | 1 (#7) |