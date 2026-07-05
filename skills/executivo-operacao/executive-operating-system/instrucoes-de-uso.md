# Instrucoes de uso

Este arquivo orienta como preparar e operar a skill `executive-operating-system` em um negocio real. Ajuste nomes de sistemas, contas, politicas e limites antes de ativar automacoes.

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

## Guardrails operacionais

- Comecar em modo dry-run quando a skill puder enviar mensagens, publicar conteudo, alterar dados, cobrar, cancelar, integrar sistemas ou tocar clientes.
- Usar allowlist de canais, contas, dominios e acoes permitidas.
- Separar credenciais por ambiente e nunca salvar tokens, cookies, senhas ou dados pessoais dentro da skill.
- Registrar evidencias suficientes para auditoria: entrada, decisao, acao, horario, resultado e proximo passo.
- Exigir revisao humana para acoes externas, alto volume, dados de clientes, risco juridico, financeiro, reputacional ou mudanca em producao.
