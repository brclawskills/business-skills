# Instrucoes de uso

Este arquivo orienta como preparar e operar a skill `api-webhook-integrations` em um negocio real. Ajuste nomes de sistemas, contas, politicas e limites antes de ativar automacoes.

## Requisitos especificos

- Documentacao da API, credenciais em secret manager, ambiente sandbox e contato tecnico.
- Contrato de payloads, retries, idempotencia, assinatura, logs e limites de taxa.
- Plano de rollback e criterio de aceite.
- Permissao explicita antes de alterar producao ou enviar dados reais.

## Ferramentas e acessos necessarios

- Cliente HTTP/API, ambiente sandbox, logs e monitoramento.
- Secret manager ou variaveis de ambiente.
- Repositorio/documentacao tecnica.
- Fila de incidentes ou issue tracker.

## Sugestao de cron

- Health check de integracoes: a cada 5 a 60 minutos, conforme criticidade.
- Reprocessamento: apenas com idempotencia e limite.
- Relatorio de erros: diario.
- Nunca criar cron que replique falhas em loop sem backoff e alerta.

## Atividades indicadas

- Validar contrato de API.
- Testar webhook e payload.
- Documentar erros e retries.
- Escalar falhas de producao com evidencias.

## Guardrails operacionais

- Comecar em modo dry-run quando a skill puder enviar mensagens, publicar conteudo, alterar dados, cobrar, cancelar, integrar sistemas ou tocar clientes.
- Usar allowlist de canais, contas, dominios e acoes permitidas.
- Separar credenciais por ambiente e nunca salvar tokens, cookies, senhas ou dados pessoais dentro da skill.
- Registrar evidencias suficientes para auditoria: entrada, decisao, acao, horario, resultado e proximo passo.
- Exigir revisao humana para acoes externas, alto volume, dados de clientes, risco juridico, financeiro, reputacional ou mudanca em producao.
