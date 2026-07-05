# Instrucoes de uso

Este arquivo orienta como preparar e operar a skill `whatsapp-audio-transcription` em um negocio real. Ajuste nomes de sistemas, contas, politicas e limites antes de ativar automacoes.

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

## Guardrails operacionais

- Comecar em modo dry-run quando a skill puder enviar mensagens, publicar conteudo, alterar dados, cobrar, cancelar, integrar sistemas ou tocar clientes.
- Usar allowlist de canais, contas, dominios e acoes permitidas.
- Separar credenciais por ambiente e nunca salvar tokens, cookies, senhas ou dados pessoais dentro da skill.
- Registrar evidencias suficientes para auditoria: entrada, decisao, acao, horario, resultado e proximo passo.
- Exigir revisao humana para acoes externas, alto volume, dados de clientes, risco juridico, financeiro, reputacional ou mudanca em producao.
