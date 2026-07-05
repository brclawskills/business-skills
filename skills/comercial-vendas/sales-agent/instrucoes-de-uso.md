# Instrucoes de uso

Este arquivo orienta como preparar e operar a skill `sales-agent` em um negocio real. Ajuste nomes de sistemas, contas, politicas e limites antes de ativar automacoes.

## Requisitos especificos

- Oferta, ICP, dores prioritarias, criterios de qualificacao e politicas de desconto/trial.
- CRM, planilha ou ERP para registrar etapa, dono, objecao, follow-up e motivo de perda.
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
- Registrar objecoes e proximo passo.
- Escalar risco comercial para responsavel humano.

## Processo basico bem feito

1. Trabalhar apenas leads com fonte, fit minimo, canal permitido e proximo passo definido.
2. Antes do contato, ler segmento, dor provavel, evidencia publica, historico e restricoes.
3. Abrir conversa com contexto curto e pergunta diagnostica; nao despejar pitch.
4. Descobrir decisor, dor, urgencia, processo atual e impacto economico.
5. Registrar objecoes, temperatura, etapa, canal e data do proximo contato.
6. Propor demo, trial, diagnostico, checkout ou reuniao somente quando houver fit e permissao.
7. Escalar preco, desconto, contrato, promessa sensivel ou excecao para responsavel humano.
8. Descartar apenas com motivo claro: opt-out, sem fit, duplicado, numero errado, sem resposta apos cadencia curta ou risco.
9. Criar cron para revisao de pipeline, follow-ups vencidos e leads sem proximo passo.
10. Medir conversao por origem, segmento, mensagem, etapa e objecao; ajustar uma variavel por vez.

## Guardrails operacionais

- Comecar em modo dry-run quando a skill puder enviar mensagens, publicar conteudo, alterar dados, cobrar, cancelar, integrar sistemas ou tocar clientes.
- Usar allowlist de canais, contas, dominios e acoes permitidas.
- Separar credenciais por ambiente e nunca salvar tokens, cookies, senhas ou dados pessoais dentro da skill.
- Registrar evidencias suficientes para auditoria: entrada, decisao, acao, horario, resultado e proximo passo.
- Exigir revisao humana para acoes externas, alto volume, dados de clientes, risco juridico, financeiro, reputacional ou mudanca em producao.
