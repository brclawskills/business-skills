# Instrucoes de uso

Este arquivo orienta como preparar e operar a skill `organic-multichannel-prospecting` em um negocio real. Ajuste nomes de sistemas, contas, politicas e limites antes de ativar automacoes.

## Requisitos especificos

- Conta Instagram profissional ou criador vinculada ao negocio.
- Acesso autorizado ao Instagram Web, Meta Business Suite ou Canva, conforme o fluxo.
- Lista de segmentos, pracas, hashtags, perfis-alvo, limites diarios e criterio de opt-out.
- Registro operacional para salvar evidencias, interacoes, bloqueios e proximos passos.
- CRM/ERP com campos para fonte, CNPJ, score, status, proximo passo e evidencias.
- Politica definida para uso de dados publicos, CNPJ.ws, Google Search e Google Places.

## Ferramentas e acessos necessarios

- Browser control para Instagram Web e Meta Business Suite.
- Canva quando houver criacao, revisao ou agendamento de criativos.
- Planilha, CRM ou ERP para registrar handles, status, temperatura e follow-up.
- Ferramenta de busca/pesquisa para mapear concorrentes, hashtags e perfis locais.
- Google Search via navegador para descoberta e validacao manual.
- Google Places API quando houver chave, billing e permissao do negocio.
- CNPJ.ws API publica para enriquecer CNPJs ja encontrados com confianca.

## Sugestao de cron

- Monitoramento de respostas: a cada 2 a 4 horas em horario comercial.
- Rotina organica: blocos curtos de 30 a 60 minutos, com limite de acoes por conta.
- Inteligencia de concorrencia: semanal ou quinzenal.
- Nunca criar cron que curta, siga, comente ou envie DM sem limite claro, aprovacao e criterio de parada.
- Descoberta de leads por Search/Places: diaria ou 2 a 3 vezes por semana, sem abordagem automatica.
- Enriquecimento CNPJ.ws: em lotes pequenos, com rate limit e registro de falhas.
- Higiene do CRM: semanal para deduplicar, revisar bloqueios e leads sem proximo passo.

## Atividades indicadas

- Mapear perfis e sinais publicos.
- Preparar comentarios contextuais.
- Monitorar respostas, curtidas, follows e DMs.
- Registrar evidencias e sugerir proximo toque seguro.

## Guardrails operacionais

- Comecar em modo dry-run quando a skill puder enviar mensagens, publicar conteudo, alterar dados, cobrar, cancelar, integrar sistemas ou tocar clientes.
- Usar allowlist de canais, contas, dominios e acoes permitidas.
- Separar credenciais por ambiente e nunca salvar tokens, cookies, senhas ou dados pessoais dentro da skill.
- Registrar evidencias suficientes para auditoria: entrada, decisao, acao, horario, resultado e proximo passo.
- Exigir revisao humana para acoes externas, alto volume, dados de clientes, risco juridico, financeiro, reputacional ou mudanca em producao.
