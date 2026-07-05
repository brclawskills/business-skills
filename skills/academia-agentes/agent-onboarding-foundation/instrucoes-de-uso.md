# Instrucoes de uso

Este arquivo orienta como preparar e operar a skill `agent-onboarding-foundation` em um negocio real. Ajuste sistemas, politicas, permissoes e limites antes de ativar automacoes.

## Requisitos especificos

- Area do agente definida.
- Dono humano responsavel.
- Lista de sistemas autorizados.
- Politica de aprovacao humana.
- Pelo menos 3 tarefas reais para dry-run.

## Ferramentas e acessos necessarios

- Workspace de arquivos.
- ERP, CRM, board ou planilha oficial.
- Canal interno para aprovacoes.
- Acesso de leitura aos playbooks e politicas do negocio.
- Ambiente de teste ou modo dry-run.

## Sugestao de cron

- Nao criar cron antes do agente passar por dry-run.
- Criar cron inicial apenas para leitura e report, sem acao externa.
- Frequencia sugerida: diario em horario comercial para agente operacional; semanal para agente estrategico.
- Exigir registro de saida, falha, fonte lida e proximo passo.

## Atividades indicadas

- Onboarding de novo agente.
- Auditoria de agente que esta errando.
- Preparacao de agente antes de entregar a cliente.
- Revisao de permissoes antes de criar cron.

## Processo basico bem feito

1. Escrever a missao do agente em uma frase objetiva.
2. Definir dono humano, sistemas oficiais e criterio de sucesso.
3. Separar acoes de leitura, rascunho, escrita interna, envio externo e decisao sensivel.
4. Listar ferramentas autorizadas e ferramentas proibidas.
5. Preparar 3 tarefas de dry-run com entradas reais e resultado esperado.
6. Rodar dry-run e exigir evidencia de fonte, raciocinio resumido, acao proposta e risco.
7. Avaliar saida com rubrica simples: precisao, utilidade, seguranca, rastreabilidade e proximo passo.
8. Corrigir skill, contexto, permissao ou processo antes de liberar autonomia.
9. Liberar apenas o menor nivel de autonomia que resolve o problema atual.
10. Registrar versao, aprovador, data e condicoes de operacao.

## Guardrails operacionais

- Comecar em modo dry-run quando a skill puder enviar mensagens, publicar conteudo, alterar dados, cobrar, cancelar, integrar sistemas ou tocar clientes.
- Usar allowlist de canais, contas, dominios e acoes permitidas.
- Separar credenciais por ambiente e nunca salvar tokens, cookies, senhas ou dados pessoais dentro da skill.
- Registrar evidencias suficientes para auditoria: entrada, decisao, acao, horario, resultado e proximo passo.
- Exigir revisao humana para acoes externas, alto volume, dados de clientes, risco juridico, financeiro, reputacional ou mudanca em producao.
