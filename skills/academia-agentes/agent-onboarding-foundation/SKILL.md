---
name: "agent-onboarding-foundation"
description: "Onboarding de agentes de negocio: contexto minimo, ferramentas, limites, dry-run, evidencias e passagem segura para operacao."
---

# Agent Onboarding Foundation

Use esta skill para preparar um agente antes de coloca-lo para operar em uma empresa real. O objetivo e evitar agente solto, sem contexto, sem limite, sem ferramenta certa e sem criterio de qualidade.

## Resultado esperado

Ao final do onboarding, o agente deve ter:

- missao clara;
- area e dono humano responsavel;
- fontes oficiais de contexto;
- ferramentas autorizadas;
- acoes proibidas;
- criterio de pronto;
- formato de evidencia;
- modo dry-run validado;
- regra de escalonamento humano;
- primeiro cron ou rotina sob demanda, quando fizer sentido.

## Processo de onboarding

1. Definir a missao do agente em uma frase: "este agente existe para..."
2. Definir a fronteira: o que ele pode decidir sozinho, o que pode apenas recomendar e o que nunca deve fazer.
3. Mapear fontes oficiais: ERP, CRM, board, planilha, inbox, analytics, arquivos, API, browser ou canal.
4. Mapear ferramentas: leitura, escrita, envio, publicacao, integracao, navegador, cron e memoria.
5. Criar o kit de contexto minimo: produto, ICP, oferta, politicas, playbooks, exemplos bons e exemplos ruins.
6. Definir registro operacional: onde o agente deixa status, evidencia, proximo passo e bloqueio.
7. Rodar 3 a 5 tarefas em dry-run sem acao externa.
8. Revisar as saidas com rubrica simples: utilidade, precisao, seguranca, rastreabilidade e proximo passo.
9. Ajustar skill, ferramentas, permissao e exemplos.
10. Liberar apenas a menor autonomia util: primeiro leitura, depois rascunho, depois alteracao interna, depois cron, depois acao externa com aprovacao.

## Kit de contexto minimo

Antes de rodar, reunir:

- objetivo do negocio e prioridade atual;
- publico-alvo ou tipo de cliente;
- oferta, planos, politicas e restricoes;
- linguagem aprovada;
- sistemas oficiais e campos importantes;
- exemplos de decisao correta;
- exemplos de erro que devem ser evitados;
- limites de volume, horario, canal e risco;
- contato humano para aprovacao.

Se algo essencial faltar, o agente deve registrar lacuna e propor como obter, nao inventar.

## Modo dry-run

No dry-run, o agente pode:

- ler fontes autorizadas;
- preparar plano;
- simular acao;
- gerar rascunho;
- apontar risco;
- sugerir registro de ERP/CRM;
- explicar o que faria e por que.

No dry-run, o agente nao pode:

- enviar mensagem externa;
- publicar conteudo;
- alterar dado de cliente;
- disparar cobranca;
- criar promessa comercial;
- executar mudanca em producao;
- criar cron recorrente sem aprovacao.

## Saida padrao do onboarding

Ao concluir, entregar:

```text
Agente:
Missao:
Dono humano:
Fontes oficiais:
Ferramentas autorizadas:
Acoes permitidas:
Acoes proibidas:
Registro operacional:
Checklist de dry-run:
Riscos:
Primeira rotina recomendada:
Status: aprovado / ajustar / bloqueado
```

## Quando ler referencias

- Leia `references/onboarding-checklist.md` quando precisar criar ou auditar o plano de onboarding de um agente.

## Guardrails

- Nunca liberar autonomia por confianca subjetiva; exigir evidencia de dry-run.
- Nunca misturar credencial pessoal com credencial operacional sem regra clara.
- Nunca usar memoria ou chat como unica fonte se existe ERP/CRM oficial.
- Nunca permitir acao externa sem canal, limite, aprovacao e rollback definidos.
- Quando o agente errar, reduzir autonomia antes de aumentar instrucao.
