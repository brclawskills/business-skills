# Instrucoes de uso

Este arquivo orienta como preparar e operar a skill `agent-quality-assurance` em um negocio real. Ajuste sistemas, politicas, permissoes e limites antes de ativar automacoes.

## Requisitos especificos

- Agente ou skill a ser avaliado.
- Tarefas reais ou exemplos representativos.
- Logs de execucao ou saidas em dry-run.
- Rubrica de risco do negocio.
- Dono humano para aprovar ou bloquear.

## Ferramentas e acessos necessarios

- Acesso de leitura aos outputs do agente.
- ERP, CRM, board ou arquivo onde evidencias deveriam estar.
- Logs de cron, quando houver.
- Canal interno para registrar aprovacao, bloqueio ou rebaixamento.

## Sugestao de cron

- QA semanal para agentes em producao.
- QA diario nos 3 primeiros dias apos criar cron novo.
- QA imediato apos falha de ferramenta, output ruim ou acao sensivel.
- Report mensal de qualidade por agente, departamento e tipo de erro.

## Atividades indicadas

- Certificar skill antes de entregar a cliente.
- Validar agente antes de passar de dry-run para producao.
- Auditar crons ativos.
- Investigar erro de agente.
- Criar plano de melhoria ou rebaixamento.

## Processo basico bem feito

1. Escolher agente, escopo e nivel de autonomia avaliado.
2. Separar 5 casos de teste: feliz, lacuna, sensivel, conflito de fonte e falha de ferramenta.
3. Rodar ou coletar saidas sem dar a resposta esperada ao agente.
4. Pontuar pela rubrica: precisao, fonte, utilidade, seguranca, registro, proximo passo, contexto, concisao, escalonamento e aprendizado.
5. Conferir se o sistema oficial foi atualizado ou se a recomendacao de atualizacao ficou clara.
6. Identificar falhas por categoria: contexto, ferramenta, permissao, raciocinio, registro ou processo.
7. Decidir: aprovar, aprovar com supervisao, manter em dry-run, rebaixar ou bloquear.
8. Registrar evidencia, nota, decisao, aprovador e data da proxima revisao.
9. Ajustar skill, instrucoes, permissoes ou cron conforme causa raiz.
10. Repetir teste critico antes de devolver autonomia.

## Guardrails operacionais

- Comecar em modo dry-run quando a skill puder enviar mensagens, publicar conteudo, alterar dados, cobrar, cancelar, integrar sistemas ou tocar clientes.
- Usar allowlist de canais, contas, dominios e acoes permitidas.
- Separar credenciais por ambiente e nunca salvar tokens, cookies, senhas ou dados pessoais dentro da skill.
- Registrar evidencias suficientes para auditoria: entrada, decisao, acao, horario, resultado e proximo passo.
- Exigir revisao humana para acoes externas, alto volume, dados de clientes, risco juridico, financeiro, reputacional ou mudanca em producao.
