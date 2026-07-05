# Instrucoes de uso

Este arquivo orienta como preparar e operar a skill `merchant-onboarding-activation` em um negocio real. Ajuste nomes de sistemas, contas, politicas e limites antes de ativar automacoes.

## Requisitos especificos

- Base de clientes, plano contratado, status de onboarding, historico de atendimento e responsaveis.
- Politica de SLA, canais oficiais, limites de suporte e criterios de escalonamento.
- Acesso ao painel do produto, CRM/ERP e material de ajuda aprovado.
- Permissao explicita antes de alterar conta, plano, pagamento, dados ou configuracoes sensiveis.

## Ferramentas e acessos necessarios

- WhatsApp, helpdesk, email ou chat oficial.
- CRM/ERP para registrar chamados, health score e risco.
- Painel administrativo ou conta demo, quando autorizado.
- Base de conhecimento, tutoriais e checklist de implantacao.

## Sugestao de cron

- Health score: diario ou 2 a 3 vezes por semana.
- Onboarding: lembretes diarios enquanto houver etapa pendente.
- Suporte pendente: a cada 1 a 4 horas em horario comercial.
- Winback/retencao: semanal, com mensagem aprovada e opt-out.

## Atividades indicadas

- Responder duvidas operacionais.
- Guiar implantacao e ativacao.
- Registrar risco de churn.
- Escalar pagamentos, LGPD, contrato ou falha tecnica.

## Processo basico bem feito

1. Identificar cliente, plano, etapa, historico, ultima interacao e risco atual.
2. Classificar a demanda: duvida, bug, implantacao, uso, cobranca, contrato, churn ou oportunidade.
3. Resolver o menor proximo passo util, sem mandar lista longa de funcionalidades.
4. Quando houver tutorial, guiar por tarefa real do cliente e confirmar entendimento.
5. Registrar resposta, status, dono, prazo, risco e proximo contato.
6. Escalar bug, pagamento, contrato, LGPD, dado sensivel ou promessa comercial.
7. Fechar chamado apenas com criterio de resolucao ou proximo passo aceito.
8. Atualizar health score quando houver sinal de ativacao, bloqueio, churn, expansao ou satisfacao.
9. Criar cron para onboarding pendente, chamados vencidos, health score e winback.
10. Revisar semanalmente os motivos recorrentes e converter em tutorial, checklist ou melhoria de produto.

## Guardrails operacionais

- Comecar em modo dry-run quando a skill puder enviar mensagens, publicar conteudo, alterar dados, cobrar, cancelar, integrar sistemas ou tocar clientes.
- Usar allowlist de canais, contas, dominios e acoes permitidas.
- Separar credenciais por ambiente e nunca salvar tokens, cookies, senhas ou dados pessoais dentro da skill.
- Registrar evidencias suficientes para auditoria: entrada, decisao, acao, horario, resultado e proximo passo.
- Exigir revisao humana para acoes externas, alto volume, dados de clientes, risco juridico, financeiro, reputacional ou mudanca em producao.
