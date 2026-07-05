# Instrucoes de uso

Este arquivo orienta como preparar e operar a skill `agent-graduation-levels` em um negocio real. Ajuste sistemas, politicas, permissoes e limites antes de ativar automacoes.

## Requisitos especificos

- Inventario de agentes ativos.
- Lista de ferramentas e permissoes por agente.
- Historico de saidas, erros e aprovacoes.
- Dono humano por agente ou departamento.
- Criterios de risco do negocio.

## Ferramentas e acessos necessarios

- ERP, CRM ou board com historico.
- Logs de execucao, cron ou chat.
- Gestor de acesso ou lista de permissoes.
- Canal de aprovacao humana.

## Sugestao de cron

- Revisao semanal de nivel dos agentes.
- Revisao diaria apenas para agentes nivel 3 ou maior em rotina critica.
- Alerta imediato quando houver falha de cron, acao externa indevida ou erro de registro.
- Report mensal de agentes promovidos, rebaixados e bloqueados.

## Atividades indicadas

- Definir autonomia de agente novo.
- Aprovar criacao de cron.
- Liberar escrita em CRM/ERP.
- Auditar agente que errou.
- Montar trilha de capacitacao por departamento.

## Processo basico bem feito

1. Listar agentes e o trabalho real que cada um executa.
2. Classificar nivel atual por evidencia, nao por intencao.
3. Conferir ferramentas, permissoes, crons e canais externos.
4. Comparar autonomia atual com o nivel permitido.
5. Definir lacunas de capacitacao: contexto, ferramenta, criterio, seguranca, escrita ou decisao.
6. Rodar teste controlado do proximo nivel apenas quando o nivel atual estiver estavel.
7. Promover com escopo, prazo, limites, rollback e aprovador.
8. Rebaixar ou bloquear quando houver erro grave ou repetido.
9. Registrar matriz de nivel por agente e revisar semanalmente.
10. Medir valor gerado: tempo economizado, qualidade, risco reduzido, receita, SLA ou aprendizado.

## Guardrails operacionais

- Comecar em modo dry-run quando a skill puder enviar mensagens, publicar conteudo, alterar dados, cobrar, cancelar, integrar sistemas ou tocar clientes.
- Usar allowlist de canais, contas, dominios e acoes permitidas.
- Separar credenciais por ambiente e nunca salvar tokens, cookies, senhas ou dados pessoais dentro da skill.
- Registrar evidencias suficientes para auditoria: entrada, decisao, acao, horario, resultado e proximo passo.
- Exigir revisao humana para acoes externas, alto volume, dados de clientes, risco juridico, financeiro, reputacional ou mudanca em producao.
