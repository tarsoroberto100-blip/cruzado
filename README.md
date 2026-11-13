# Teste cruzado — seminário

Numa empresa, o código de uma equipe é testado por **outra** equipe, e os defeitos viram registros num **bugtracker**. Hoje cada grupo recebe uma **situação real** desse trabalho, pesquisa como as empresas resolvem, monta a solução, **aplica num app de verdade** e apresenta para a turma.

## O que tem neste repositório

```
teste-cruzado/
├── README.md                     ← este arquivo
├── situacoes/                    ← uma situação por grupo
│   ├── SITUACAO-1-planejar.md     (MarmitaJá)
│   ├── SITUACAO-2-relatar.md      (QuadraLivre)
│   └── SITUACAO-3-triar.md        (FitPass)
├── apps/                         ← os 3 apps (abra o index.html no navegador)
│   ├── marmitaja/   quadralivre/   fitpass/
├── materiais/
│   ├── GUIA-RAPIDO.md             ← os conceitos de hoje em uma página
│   └── ISSUES-RECEBIDAS-FitPass.md   (só para a situação 3)
├── modelos/                      ← o que cada grupo preenche
│   ├── PLANO-DE-TESTE.md
│   ├── TRIAGEM.md
│   └── APRESENTACAO.md
├── .github/ISSUE_TEMPLATE/       ← o modelo de Issue (relato de defeito)
└── entregas/                     ← o trabalho do grupo vai aqui
```

## Passo a passo (55 minutos)

| Tempo | O que fazer |
| --- | --- |
| 0–5 min | Um integrante cria o repositório do grupo: **Use this template** → `teste-cruzado-grupo-N`, público, e adiciona os colegas em **Settings → Collaborators**. Todos leem a situação em `situacoes/`. |
| 5–15 min | **Pesquisar:** respondam às perguntas da situação. Anotem as fontes (site e link). Comecem pelo `materiais/GUIA-RAPIDO.md`. |
| 15–25 min | **Solucionar:** montem a solução que a situação pede (critério, modelo ou plano). |
| 25–45 min | **Aplicar:** usem a solução no app da situação. Tudo com valor exato e evidência (print). |
| 45–55 min | **Preparar a apresentação** com `modelos/APRESENTACAO.md`. Commit e push. |

**Como abrir o app:** depois de clonar ou baixar o repositório (Code → Download ZIP), dê dois cliques em `apps/<app>/index.html`.

## Roteiro da apresentação (5 minutos + 3 de perguntas)

1. **A situação** (30 s): qual era o problema.
2. **O que a pesquisa mostrou** (1 min): como as empresas fazem, com uma fonte.
3. **A solução do grupo** (1 min): o critério, o modelo ou o plano que vocês montaram.
4. **A aplicação** (1 min 30 s): o que aconteceu quando usaram no app. Mostrem na tela uma evidência.
5. **A lição** (1 min): o que uma equipe de testes deve fazer, e o que deve evitar.

## Regras

- O resultado esperado vem **sempre do documento de requisitos** do app, nunca do que a tela mostra.
- Valores **exatos** em todo caso de teste e em toda Issue.
- Ninguém altera o código dos apps. Hoje é dia de testar e registrar.

## Entrega

1. O que a sua situação pede, em `entregas/` (o nome do arquivo está no cartão).
2. `entregas/APRESENTACAO-grupo-N.md` (copie de `modelos/`).
3. Commit e push: `git commit -m "docs: situação N do teste cruzado"`.
