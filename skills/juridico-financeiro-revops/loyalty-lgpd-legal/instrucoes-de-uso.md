# Instrucoes de uso

Este arquivo orienta como preparar e operar a skill `loyalty-lgpd-legal` em um negocio real. Ajuste nomes de sistemas, contas, politicas e limites antes de ativar automacoes.

## Requisitos especificos

- Politicas comerciais, contratos, termos, regras de cobranca, LGPD e limites de desconto.
- Dados financeiros e pessoais apenas quando autorizados e minimizados.
- Responsavel humano para decisoes juridicas, fiscais, contabeis ou de preco sensivel.
- Historico de planos, inadimplencia, churn, upgrades e disputas.

## Ferramentas e acessos necessarios

- ERP financeiro, billing, gateway de pagamento ou planilha autorizada.
- CRM/RevOps para forecast e pipeline.
- Repositorio de contratos, termos e politicas.
- Canal de aprovacao com responsavel humano.

## Sugestao de cron

- Forecast e cobranca: diario ou semanal.
- Inadimplencia: diario em dias uteis.
- Revisao juridica/LGPD: mensal ou sob demanda.
- Nunca executar cancelamento, desconto, cobranca ou alteracao contratual sem regra e aprovacao.

## Atividades indicadas

- Revisar receita, planos e risco.
- Preparar analise juridica ou financeira.
- Sugerir proximos passos com guardrails.
- Escalar decisoes sensiveis.

## Processo basico bem feito

1. Separar tipo de demanda: preco, cobranca, contrato, LGPD, fidelidade, forecast, inadimplencia ou risco.
2. Coletar dados minimos e fonte oficial: plano, contrato, historico, valores, consentimento, status e responsavel.
3. Identificar regra aplicavel e lacunas; nao inventar interpretacao juridica, fiscal ou contabil.
4. Preparar opcoes com impacto, risco, evidencia e recomendacao.
5. Exigir aprovacao humana para desconto, cobranca, cancelamento, contrato, termo, dado pessoal ou comunicacao sensivel.
6. Registrar decisao, aprovador, data, valor, documento e proximo passo.
7. Atualizar forecast, pipeline, billing ou risco quando a decisao alterar o negocio.
8. Criar cron para inadimplencia, renovacoes, forecast, revisao de termos e riscos vencidos.
9. Manter trilha de auditoria limpa, sem expor dados pessoais desnecessarios.
10. Encerrar com status financeiro/juridico claro e proxima acao verificavel.

## Guardrails operacionais

- Comecar em modo dry-run quando a skill puder enviar mensagens, publicar conteudo, alterar dados, cobrar, cancelar, integrar sistemas ou tocar clientes.
- Usar allowlist de canais, contas, dominios e acoes permitidas.
- Separar credenciais por ambiente e nunca salvar tokens, cookies, senhas ou dados pessoais dentro da skill.
- Registrar evidencias suficientes para auditoria: entrada, decisao, acao, horario, resultado e proximo passo.
- Exigir revisao humana para acoes externas, alto volume, dados de clientes, risco juridico, financeiro, reputacional ou mudanca em producao.
