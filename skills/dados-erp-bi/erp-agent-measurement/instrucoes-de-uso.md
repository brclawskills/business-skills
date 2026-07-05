# Instrucoes de uso

Este arquivo orienta como preparar e operar a skill `erp-agent-measurement` em um negocio real. Ajuste nomes de sistemas, contas, politicas e limites antes de ativar automacoes.

## Requisitos especificos

- Fonte oficial de dados, dicionario de campos, owners e regras de qualidade.
- Acesso somente leitura quando possivel.
- Definicao de metricas, janelas de tempo, segmentos e criterio de verdade.
- Politica para dados pessoais, exportacoes e compartilhamento de dashboards.

## Ferramentas e acessos necessarios

- ERP, banco, planilha, BI ou data warehouse autorizado.
- Leitor de CSV/JSON e ferramenta de validacao.
- Dashboard ou relatorio operacional.
- Canal para registrar lacunas, divergencias e decisoes.

## Sugestao de cron

- Dashboards operacionais: diario.
- Conciliacao ERP/report: 1 a 4 vezes por dia, conforme criticidade.
- Auditoria de qualidade de dados: semanal.
- Alertas somente para desvios acionaveis, nao para ruido.

## Atividades indicadas

- Atualizar metricas.
- Conciliar reports com dados reais.
- Apontar lacunas e inconsistencias.
- Gerar recomendacao com impacto mensuravel.

## Guardrails operacionais

- Comecar em modo dry-run quando a skill puder enviar mensagens, publicar conteudo, alterar dados, cobrar, cancelar, integrar sistemas ou tocar clientes.
- Usar allowlist de canais, contas, dominios e acoes permitidas.
- Separar credenciais por ambiente e nunca salvar tokens, cookies, senhas ou dados pessoais dentro da skill.
- Registrar evidencias suficientes para auditoria: entrada, decisao, acao, horario, resultado e proximo passo.
- Exigir revisao humana para acoes externas, alto volume, dados de clientes, risco juridico, financeiro, reputacional ou mudanca em producao.
