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

## Processo basico bem feito

1. Ler documentacao da API, limites, autenticacao, payloads, webhooks e ambiente sandbox.
2. Definir contrato de dados: campos obrigatorios, tipos, exemplos, erros, retries e idempotencia.
3. Guardar credenciais apenas em secret manager ou variaveis de ambiente.
4. Testar primeiro em sandbox com payload minimo e payload realista.
5. Registrar request, response, status, latency, correlation id e erro.
6. Implementar backoff, limite de taxa, timeout, assinatura/verificacao e logs.
7. Preparar rollback e criterio de aceite antes de producao.
8. Monitorar health check, fila, falhas, duplicidades e reprocessamentos.
9. Criar cron para health check, relatorio de erros e reprocessamento idempotente controlado.
10. Nunca criar loop automatico que reenvie falha sem limite, alerta e criterio de parada.

## Guardrails operacionais

- Comecar em modo dry-run quando a skill puder enviar mensagens, publicar conteudo, alterar dados, cobrar, cancelar, integrar sistemas ou tocar clientes.
- Usar allowlist de canais, contas, dominios e acoes permitidas.
- Separar credenciais por ambiente e nunca salvar tokens, cookies, senhas ou dados pessoais dentro da skill.
- Registrar evidencias suficientes para auditoria: entrada, decisao, acao, horario, resultado e proximo passo.
- Exigir revisao humana para acoes externas, alto volume, dados de clientes, risco juridico, financeiro, reputacional ou mudanca em producao.
