# Instrucoes de uso

Este arquivo orienta como preparar e operar a skill `sales-agent` em um negocio real. Ajuste nomes de sistemas, contas, politicas e limites antes de ativar automacoes.

## Requisitos especificos

- Oferta, ICP, dores prioritarias, criterios de qualificacao e politicas de desconto/trial.
- CRM, planilha ou ERP para registrar etapa, dono, obje??o, follow-up e motivo de perda.
- Mensagens aprovadas para WhatsApp, Instagram, email ou telefone.
- Limites para promessas, precos, checkout, trial e escalonamento humano.

## Ferramentas e acessos necessarios

- CRM/ERP comercial.
- WhatsApp, email ou canal de atendimento autorizado.
- Agenda/calendario para follow-ups e reunioes.
- Checkout ou link de pagamento somente quando aprovado.

## Sugestao de cron

- Follow-up de leads mornos: diario em dias uteis.
- Revisao de pipeline: 1 a 2 vezes por dia.
- Reativacao: semanal, por lote pequeno e com opt-out.
- Nunca criar cron de disparo em massa sem base legal, segmentacao e aprovacao humana.

## Atividades indicadas

- Qualificar decisor e dor.
- Preparar resposta consultiva.
- Registrar obje??es e proximo passo.
- Escalar risco comercial para responsavel humano.

## Guardrails operacionais

- Comecar em modo dry-run quando a skill puder enviar mensagens, publicar conteudo, alterar dados, cobrar, cancelar, integrar sistemas ou tocar clientes.
- Usar allowlist de canais, contas, dominios e acoes permitidas.
- Separar credenciais por ambiente e nunca salvar tokens, cookies, senhas ou dados pessoais dentro da skill.
- Registrar evidencias suficientes para auditoria: entrada, decisao, acao, horario, resultado e proximo passo.
- Exigir revisao humana para acoes externas, alto volume, dados de clientes, risco juridico, financeiro, reputacional ou mudanca em producao.
