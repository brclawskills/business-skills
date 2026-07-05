# Instrucoes de uso

Este arquivo orienta como preparar e operar a skill `commercial-conversion-os` em um negocio real. Ajuste nomes de sistemas, contas, politicas e limites antes de ativar automacoes.

## Requisitos especificos

- Posicionamento, ICP, oferta, biblioteca de provas, guardrails juridicos e tom de marca.
- Calendario editorial, canais, formatos, metricas e aprovador humano.
- Acesso aos ativos visuais, brand kit, blog/CMS, Canva ou ferramenta de video quando aplicavel.
- Criterio claro para publicar, agendar, pausar ou revisar criativos.

## Ferramentas e acessos necessarios

- CMS/blog, Canva, editor de video/imagem ou gerador autorizado.
- Analytics, Search Console, CRM ou planilha de metricas.
- Biblioteca de assets, provas, depoimentos e referencias aprovadas.
- Ferramentas de pesquisa de palavras-chave, concorrentes e tendencias.

## Sugestao de cron

- Calendario editorial: semanal.
- Revisao de desempenho de conteudo: semanal ou quinzenal.
- QA de criativos antes de publicar: sob demanda, nunca totalmente automatico.
- Monitoramento de campanhas: diario enquanto campanha estiver ativa.

## Atividades indicadas

- Criar pauta e copy.
- Revisar criativos e claims.
- Publicar/agendar com aprovacao.
- Analisar performance e gerar proxima hipotese.

## Guardrails operacionais

- Comecar em modo dry-run quando a skill puder enviar mensagens, publicar conteudo, alterar dados, cobrar, cancelar, integrar sistemas ou tocar clientes.
- Usar allowlist de canais, contas, dominios e acoes permitidas.
- Separar credenciais por ambiente e nunca salvar tokens, cookies, senhas ou dados pessoais dentro da skill.
- Registrar evidencias suficientes para auditoria: entrada, decisao, acao, horario, resultado e proximo passo.
- Exigir revisao humana para acoes externas, alto volume, dados de clientes, risco juridico, financeiro, reputacional ou mudanca em producao.
