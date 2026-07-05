# Instrucoes de uso

Este arquivo orienta como preparar e operar a skill `autonomous-operation-learning` em um negocio real. Ajuste nomes de sistemas, contas, politicas e limites antes de ativar automacoes.

## Requisitos especificos

- Objetivo claro, dono do processo e criterio de pronto.
- Acesso autorizado aos sistemas citados na skill.
- Logs ou registro operacional para evidencias.
- Limites de acao externa e aprovacao humana.

## Ferramentas e acessos necessarios

- Workspace de arquivos.
- Canal de comunicacao aprovado.
- Sistema operacional do negocio.
- Ferramentas especificas mencionadas no SKILL.md.

## Sugestao de cron

- Criar cron apenas para rotinas repetitivas com criterio objetivo.
- Preferir execucao sob demanda quando houver alto risco ou necessidade de julgamento humano.
- Registrar saida e falhas sem depender de comandos locais frageis.
- Usar limites, backoff e alerta humano.

## Atividades indicadas

- Executar o procedimento da skill.
- Registrar evidencias.
- Apontar lacunas.
- Escalar decisoes sensiveis.

## Processo basico bem feito

1. Ler o estado oficial do negocio: ERP, tarefas, riscos, rotinas, indicadores e bloqueios abertos.
2. Separar fato, suposicao e decisao pendente.
3. Identificar o gargalo principal do dia: receita, operacao, produto, suporte, financeiro, juridico ou tecnologia.
4. Escolher no maximo 3 prioridades acionaveis por ciclo.
5. Para cada prioridade, definir dono, prazo, criterio de pronto e evidencia esperada.
6. Executar apenas acoes internas ou previamente aprovadas; preparar recomendacao para decisoes sensiveis.
7. Registrar no ERP ou board o que mudou, o que ficou bloqueado e o proximo passo.
8. Fechar o ciclo com resumo executivo: decisoes, riscos, metricas, pendencias e follow-up.
9. Criar cron somente para verificacoes recorrentes com fonte objetiva, como status de tarefas, rotinas vencidas, riscos, pipeline ou fechamento diario.
10. Revisar semanalmente se as rotinas ainda geram decisao util; pausar cron que apenas repete ruido.

## Guardrails operacionais

- Comecar em modo dry-run quando a skill puder enviar mensagens, publicar conteudo, alterar dados, cobrar, cancelar, integrar sistemas ou tocar clientes.
- Usar allowlist de canais, contas, dominios e acoes permitidas.
- Separar credenciais por ambiente e nunca salvar tokens, cookies, senhas ou dados pessoais dentro da skill.
- Registrar evidencias suficientes para auditoria: entrada, decisao, acao, horario, resultado e proximo passo.
- Exigir revisao humana para acoes externas, alto volume, dados de clientes, risco juridico, financeiro, reputacional ou mudanca em producao.
