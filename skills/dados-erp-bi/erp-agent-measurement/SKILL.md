---
name: "erp-agent-measurement"
description: "Agentes registram operacao no ERP com evidencias, metricas e rastreabilidade."
---

# ERP Mensuracao de Agentes

## Objetivo

Usar o ERP local como sistema de registro operacional para tudo que os agentes executam no produto. Relatorios em Markdown, memoria e mensagens de chat ajudam o contexto, mas nao substituem o ERP quando a acao gera dado mensuravel, status de processo, pendencia, risco, contato, experimento ou resultado.

## Regra central

Antes de encerrar uma tarefa relevante para a empresa, o agente deve perguntar: "qual registro mensuravel esta tarefa criou ou alterou no ERP?"

Se a tarefa afetou operacao, comercial, growth, CS, financeiro, produto, juridico, suporte, integracoes ou WhatsApp, atualizar o ERP operacional autorizado via API local/configurada ou pelos scripts existentes do ambiente.

## Quando registrar no ERP

Registrar no ERP quando houver qualquer um destes casos:

- Uma acao comercial foi preparada, executada, bloqueada ou concluida.
- Um prospect, lead, loja, parceiro ou contato ganhou novo status, score, origem, proximo passo ou evidencia.
- Uma conversa de WhatsApp ou Instagram mudou de contexto, etapa, pendencia, resposta, opt-out, erro ou necessidade de conferencia.
- Um experimento de growth foi planejado, rodado, pausado, vencido ou perdeu validade.
- Uma tarefa operacional, rotina, risco, documento, acesso, ticket ou integracao mudou de estado.
- Um evento financeiro, assinatura, pagamento, plano, MRR, trial, proposta ou checkout foi identificado.
- Um dado externo foi importado, enriquecido, auditado ou considerado inconsistente.

Nao registrar ruido: leitura sem efeito, exploracao descartada, rascunho que nao vira ativo, ou acao que nao altera decisao/status.

## Mapeamento de recursos

Usar estes recursos do ERP conforme o tipo de dado:

- `prospects`: prospeccao, fit, segmento, CNPJ, score, status, canal, proximo contato, dor, abordagem e validacao WhatsApp.
- `deals`: oportunidade comercial real, proposta, demo, valor, probabilidade e fechamento.
- `accounts`: cliente, piloto, trial, loja ativa, status de carteira, health e proxima acao.
- `subscriptions`: plano, MRR, trial, assinatura ativa, inadimplencia e renovacao.
- `waChats`: conversa WhatsApp, status local, etapa, opt-in, resumo, necessidade de conferencia no telefone.
- `waMessages`: historico local relevante, mensagem recebida/enviada, nota interna ou transcricao.
- `waDrafts`: respostas sugeridas que ainda dependem de aprovacao ou envio fora do ERP.
- `instagramLeads`: leads organicos do Instagram, status, interacoes, perfil, cidade, segmento e proximo passo.
- `instagramInteractions`: follows, curtidas, comentarios, respostas e evidencias de interacao publica.
- `outreachRuns`: rodadas de abordagem planejadas, rodando, pausadas ou concluidas.
- `experiments`: testes de growth, hipotese, metrica, prazo e resultado.
- `tasks`: tarefas operacionais executaveis por agentes.
- `routines`: rotinas recorrentes e checks executivos.
- `risks`: riscos juridicos, fiscais, produto, seguranca, operacao e mitigacao.
- `documents`: contratos, politicas, playbooks, checklists e materiais que precisam revisao/aprovacao.
- `accesses`: ferramentas, responsaveis, revisao de acesso, 5S e dependencia operacional.
- `tickets`: suporte, incidentes, bugs, severidade e resolucao.
- `productEvents`, `businessAccounts`, `commerceOrders`, `paymentEvents`: eventos vindos do produto, sincronizacoes e pagamentos.
- `cnpjEnrichments`: enriquecimento CNPJ.ws e contexto cadastral.

## Padrao minimo de registro

Todo registro novo ou alterado deve conter, quando aplicavel:

- `status`: estado atual util para dashboard.
- `updatedAt` ou data equivalente.
- `owner`: agente, pessoa ou area responsavel.
- `source`: origem do dado quando houver.
- `notes` ou campo narrativo curto com evidencia e criterio.
- `nextStep`: proximo passo concreto.
- `risk` ou `health` quando o dado afeta decisao.

Evitar campos vagos como "ver depois" sem criterio. Preferir "conferir no telefone antes de responder", "aguardar resposta humana", "bloqueado por captcha", "validar CNPJ antes de abordagem".

## WhatsApp: regra especifica

O ERP nao deve assumir que `unread` local e igual a pendencia real no telefone. Para WhatsApp:

1. Rodar ou orientar a rotina de reconciliacao `POST /api/whatsapp/reconcile-status` quando houver duvida nos indicadores.
2. Usar `waiting-us` somente para pendencia real confirmada ou status operacional intencional.
3. Usar `phone-check` quando o historico local sugere conferir no telefone antes de decidir.
4. Nao enviar follow-up sem prova visual/contextual de ausencia de resposta.
5. Registrar rascunhos em `waDrafts` quando houver resposta sugerida, sem confundir rascunho com envio.

## Antes de finalizar tarefa

Checklist obrigatorio:

- O ERP foi atualizado se houve mudanca mensuravel?
- O status escolhido ajuda o dashboard a refletir a realidade?
- A evidencia ficou clara sem expor segredo desnecessario?
- O proximo passo ficou acionavel?
- O registro nao inflou metrica falsa de cliente, lead, pendencia ou receita?

## Como agir quando nao der para atualizar

Se o ERP estiver fora do ar, registrar no arquivo de trabalho e criar uma tarefa `tasks` assim que voltar. Se houver risco de dado errado, nao inventar; registrar como `phone-check`, `review`, `blocked` ou equivalente com o motivo.

## Resultado esperado

O dashboard do ERP deve responder rapidamente:

- O que os agentes fizeram?
- O que mudou de status?
- Quais sinais comerciais existem?
- Onde ha risco, bloqueio ou pendencia?
- O que precisa de acao humana?
- Qual impacto medivel foi gerado?
