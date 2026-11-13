# Issues recebidas — FitPass v1.0

Abertas pela equipe que testou o FitPass. Estão aqui do jeito que chegaram: algumas boas, algumas ruins. **Não confiem em nenhuma sem reproduzir.**

---

### #1 — [BUG] Plano trimestral cobra taxa de matrícula
**Regra:** RN05 · **Severidade sugerida:** alta
**Passos:** 1. Nome “Ana Lima”, CPF 123.456.789-09, idade 20. 2. Plano trimestral, sem estudante. 3. Simular valor.
**Esperado:** matrícula isenta, total R$ 269,70.
**Obtido:** matrícula R$ 50, total R$ 319.7.

---

### #2 — [BUG] Desconto de estudante calculado errado
**Regra:** RN06 · **Severidade sugerida:** alta
**Passos:** 1. Nome “Bruno Lima”, CPF 123.456.789-09, idade 20, estudante marcado. 2. Plano mensal. 3. Simular valor.
**Esperado:** desconto R$ 14,99, total R$ 134,91 (exemplo do documento).
**Obtido:** desconto R$ 22.49, total R$ 127.41.

---

### #3 — Estudante tá pagando menos do que devia
**Severidade sugerida:** média
Fiz a matrícula como estudante de 25 anos no plano mensal e deu R$ 127.41. Pelo documento deveria ser mais caro.

---

### #4 — [BUG] CPF falso é aceito
**Regra:** RN02 · **Severidade sugerida:** crítica
**Passos:** CPF 111.111.111-11, resto dos dados válidos, plano mensal.
**Esperado:** CPF recusado, porque não é um CPF de verdade.
**Obtido:** matrícula aceita.

---

### #5 — [BUG] Valores aparecem com ponto e sem os centavos completos
**Regra:** RNF01 · **Severidade sugerida:** baixa
**Passos:** idade 30, plano mensal, simular.
**Esperado:** `R$ 149,90`.
**Obtido:** `R$ 149.9`.

---

### #6 — [BUG] Adolescente de 13 anos não consegue se matricular
**Regra:** RN03 · **Severidade sugerida:** alta
**Passos:** idade 13, autorização marcada, plano mensal.
**Esperado:** matrícula aceita, porque tem autorização.
**Obtido:** “A matrícula é permitida a partir de 14 anos.”

---

### #7 — desconto do idoso tá estranho
**Severidade sugerida:** alta
o desconto pra idoso ta dando um valor esquisito, arruma pfv

---

### #8 — [BUG] Aluno de 14 anos com autorização é recusado
**Regra:** RN03 · **Severidade sugerida:** alta
**Passos:** idade 14, autorização do responsável marcada, plano mensal, simular.
**Esperado:** aceito.
**Obtido:** “Menores de 18 anos precisam da autorização do responsável.” (a autorização estava marcada)

---

### #9 — [BUG] Não chega e-mail de confirmação
**Severidade sugerida:** média
Confirmei a matrícula e não recebi nenhum e-mail. Todo sistema de matrícula manda e-mail.

---

### #10 — [BUG] Plano anual não cobra a taxa de matrícula
**Regra:** RN05 · **Severidade sugerida:** alta
**Passos:** idade 30, plano anual, simular.
**Esperado:** matrícula R$ 50,00.
**Obtido:** “Isenta”.

---

### #11 — [BUG] Estudante idoso recebe os dois descontos somados
**Regra:** RN06 · **Severidade sugerida:** média
**Passos:** idade 65, estudante marcado, plano anual, simular.
**Esperado:** só o maior desconto (20%): total R$ 767,04.
**Obtido:** desconto de 35%, total R$ 623.22.

---

### #12 — Trimestral mais caro que o anunciado
**Severidade sugerida:** alta
**Passos:** idade 30, plano trimestral.
**Obtido:** total R$ 319.7, aparece uma taxa de R$ 50. O site anuncia R$ 269,70.
