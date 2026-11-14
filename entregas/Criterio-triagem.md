# Critérios de triagem — FitPass v1.0

## 1. Quando a equipe confirma, rejeita, marca como duplicada ou pede mais informação

| Decisão | Quando | Exemplo no FitPass |
| --- | --- | --- |
| **Confirma** | Reproduz e o resultado contraria uma regra do requisito (RN ou RNF). | #1: trimestral cobra R$ 50,00 de matrícula, mas a RN05 isenta |
| **Rejeita** | O sistema faz o que o requisito diz, ou o pedido não está em nenhum requisito (é uma melhoria, não um defeito). | #6: 13 anos é recusado, e a RN03 só permite a partir de 14 |
| **Marca como duplicada** | É um defeito real, mas outra Issue já descreve o mesmo comportamento errado, com a mesma causa. | #12 repete o #1 |
| **Pede mais informação** | Faltam dados para reproduzir (idade, plano, estudante, valor obtido). Não se adivinha: pede-se o dado e a Issue fica em espera. | #7: não diz idade, plano nem valores |

## 2. Como decidem a prioridade (o que corrigir primeiro), além da severidade

A severidade diz o tamanho do estrago. A prioridade é a ordem de correção e leva em conta a campanha de matrículas de segunda. Perguntas, da mais importante para a menos:

1. **Mexe em dinheiro do cliente?** Cobrar a mais (reclamação, preço diferente do anunciado) vem antes de cobrar a menos.
2. **Quantas pessoas pegam o defeito na campanha?** Plano e perfil comuns pesam mais que combinação rara.
3. **Impede a venda?** Quem não consegue se matricular some da campanha.
4. **O cliente vê?** Defeito na tela de resumo, que todos olham, pesa mais.
5. **Esforço e causa em comum.** Defeitos da mesma função são corrigidos juntos, e correção de uma linha sobe na fila quando empata.

Quem decide: a equipe de desenvolvimento junto com o gerente. A equipe de testes recomenda com esses critérios.