# Guia rápido — teste cruzado e bugtracker

Ponto de partida para a pesquisa. Não substitui as fontes: aprofundem e citem de onde tiraram.

## Teste independente (ou cruzado)

O app é testado por quem **não** o programou. Quem escreveu já sabe como deveria funcionar e tende a testar só o caminho que funciona. Outra equipe lê o requisito com olhos novos.

## Plano de teste

Documento que diz **o que** será testado, **como**, **com que dados** e **quando parar**. Partes comuns: escopo, ambiente, riscos, casos de teste, critério de saída. Normas de referência: IEEE 829 e ISO/IEC/IEEE 29119.

## Teste baseado em risco

Quando o tempo é curto, testa-se primeiro o que tem **mais chance de falhar** e **mais prejuízo se falhar** (dinheiro, dados, segurança, imagem). Risco = probabilidade × impacto.

## Técnicas de caixa preta

- **Partição de equivalência:** dividir as entradas em grupos que o sistema deve tratar igual e testar um valor de cada grupo.
- **Valor limite:** testar o valor exato onde a regra muda, e um de cada lado. Regra “a partir de 16 anos”: testar 15, 16 e 17.

## Bugtracker

Ferramenta onde os defeitos são registrados e acompanhados até o fim: GitHub Issues, Jira, Azure Boards, Redmine, Bugzilla, MantisBT.

## Relatório de defeito (Issue)

Título curto e específico · regra violada · ambiente · pré-condições · passos · dados exatos · esperado (do requisito) · obtido · evidência · severidade. **Um defeito por Issue.**

## Severidade × prioridade

- **Severidade:** o tamanho do estrago que o defeito causa. Quem testa propõe.
- **Prioridade:** a ordem em que vai ser corrigido. Quem decide é a equipe com o gerente, pensando no negócio e no prazo.
- Exemplo: um erro grave numa tela que quase ninguém usa pode ter severidade alta e prioridade baixa. Um erro de digitação no nome da empresa na página inicial pode ter severidade baixa e prioridade alta.

## Ciclo de vida do defeito

Novo → Confirmado (ou Rejeitado / Duplicado) → Em correção → Corrigido → **Retestado** → Fechado. Se o reteste falhar, a Issue é **reaberta**.

## Triagem

Reunião ou momento em que cada Issue nova é lida, reproduzida e decidida:

- **Confirmada:** reproduz e contraria o requisito.
- **Rejeitada:** o sistema faz o que o requisito diz, ou o pedido não está no requisito (aí é uma *melhoria*, não um defeito).
- **Duplicada:** o mesmo defeito já tem Issue aberta.
- **Incompleta:** falta informação para reproduzir. Pede-se o dado que falta.

## Reteste × regressão

- **Reteste:** repetir o caso que falhou, depois da correção, para confirmar que foi corrigido.
- **Regressão:** testar de novo o que **já funcionava**, para garantir que a correção não quebrou outra coisa.

## No GitHub

- Commit com `closes #4` (ou `fixes #4`) fecha a Issue 4 quando chega à branch principal.
- Labels classificam as Issues (ex.: `alta`, `baixa`).
- Fechar como *not planned* indica que a Issue foi rejeitada.
