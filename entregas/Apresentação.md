# Apresentação — Situação 3

**Integrantes: Tarso e jefferson

## 1. A situação

O FitPass, sistema de matrícula da Academia Movimento, foi testado por outra equipe, que abriu **12 Issues**. A equipe de desenvolvimento só consegue corrigir algumas antes da campanha de matrículas de segunda. O gerente pediu: quais são defeitos de verdade, quais jogar fora e em que ordem corrigir.

## 2. O que a pesquisa mostrou

(Esta parte está nos slides do grupo.)

## 3. A solução do grupo

Um fluxo de decisão em ordem: (1) dá para reproduzir? Se não, **incompleta**. (2) Reproduzimos e conferimos no **requisito**: se o sistema está certo ou o pedido não está no documento, **rejeitada**. (3) Se é defeito, já existe Issue igual? **Duplicada**; senão **confirmada**.
Prioridade pensando na campanha de segunda: (1) dinheiro cobrado do cliente, (2) quantas pessoas pegam o defeito, (3) impede a venda, (4) o cliente vê, (5) esforço e causa em comum.

## 4. A aplicação no app

Reproduzimos as 12 Issues com os dados escritos nelas e conferimos cada uma no `REQUISITOS-FitPass.md`.

**Placar:** 5 confirmadas · 4 rejeitadas · 2 duplicadas · 1 incompleta.

- **Rejeitada, para mostrar na tela: #10** (plano anual deveria cobrar matrícula). Mostrar 30 anos, anual: o app mostra "Isenta", e a **RN05** diz que a matrícula é isenta no trimestral e no anual. O esperado da Issue estava errado.
- **Duplicadas:** #3 é do #2 e #12 é do #1. **Incompleta:** #7, sem idade, plano nem valores.
- **Ordem de correção:** #1 → #2 → #11 → #8 → #5.
- **Primeira da fila (#1):** o trimestral cobra R$ 50,00 a mais que o anunciado (R$ 319,70 em vez de R$ 269,70). É dinheiro do cliente, aparece em duas Issues e a campanha vai vender esse plano.
- **Evidência para mostrar na tela:** print do resumo com Ana Lima, 20 anos, trimestral (Matrícula R$ 50 e Total R$ 319.7).
- Também mostrar o contraste de severidade e prioridade: #8 tem severidade alta, mas fica em 4º porque afeta só quem tem 14 anos.

## 5. A lição

Uma equipe de testes deve:
- reproduzir antes de decidir e conferir sempre no requisito, nunca na tela nem na opinião de quem abriu a Issue;
- pedir o dado que falta em vez de rejeitar ou adivinhar;
- juntar duplicadas e corrigir juntos os defeitos da mesma causa;
- registrar as confirmadas com valores exatos e planejar reteste e regressão.

E deve evitar:
- aceitar Issue como verdadeira só porque está bem escrita (o #6, o #4 e o #10 pareciam defeitos e não eram);
- confundir melhoria com defeito (#4 e #9);
- achar que severidade alta significa prioridade 1.

## 6. Fontes

Tema	Fonte	Link
Triagem	bug0	https://bug0.com/knowledge-base/defect-triage
Triagem, rejeitada e duplicada	C# Corner (Defect Triage in Software Testing)	https://www.c-sharpcorner.com/article/defect-triage-in-software-testing
Severidade × prioridade	Marker.io	https://marker.io/blog/bug-severity-vs-priority
Severidade × prioridade, quem decide	TestMu AI	https://www.testmuai.com/blog/bug-severity-vs-priority-in-testing-with-examples/
Reteste × regressão	Testomat.io	https://testomat.io/blog/regression-testing-vs-retesting/
Geral, incompleta e ciclo do defeito	Guia rápido do repositório	materiais/GUIA-RAPIDO.md

Extras, se quiserem mais fontes

Tema	Fonte	Link
Triagem e quem participa	Atomic Object (How Do You Triage Software Bugs?)	https://spin.atomicobject.com/bug-triage/
Triagem, passo a passo da reunião	C# Corner (Defect Triage Meeting)	https://www.c-sharpcorner.com/article/defect-triage-meeting-in-software-testing
Reteste × regressão	QATestLab	https://blog.qatestlab.com/regression-and-confirmation-testing-what-is-the-difference/