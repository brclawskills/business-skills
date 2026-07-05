# Instrucoes de uso

Este arquivo orienta como preparar e operar a skill `video-tour` em um negocio real. Ajuste nomes de sistemas, contas, politicas e limites antes de ativar automacoes.

## Requisitos especificos

- Conta demo ou ambiente seguro, com dados ficticios.
- Roteiro, objetivo, publico, telas permitidas e telas proibidas.
- Ferramenta de gravacao, narracao, legenda e edicao autorizada.
- Checklist para ocultar dados pessoais, financeiros, tokens e informacoes internas.

## Ferramentas e acessos necessarios

- Browser ou app do produto em ambiente demo.
- Gravador de tela, editor de video, Canva/CapCut ou equivalente.
- Ferramenta de TTS/narracao e gerador de SRT/VTT quando aplicavel.
- Pasta de saida para roteiro, audio, legenda, storyboard e relatorio.

## Sugestao de cron

- Geralmente usar sob demanda, nao cron recorrente.
- Criar cron apenas para revisar demos antigas, links quebrados ou videos pendentes.
- Para tours recorrentes, agendar checklist semanal de atualizacao do roteiro.
- Nunca automatizar gravacao/publicacao sem revisao visual humana.

## Atividades indicadas

- Mapear fluxo e telas.
- Gerar roteiro e narracao.
- Gravar demo com dados seguros.
- Entregar pacote de edicao e checklist de qualidade.

## Processo basico bem feito

1. Definir objetivo, publico, canal, duracao, mensagem principal e criterio de qualidade.
2. Usar ambiente demo, conta teste ou dados ficticios; nunca gravar dados reais sem autorizacao.
3. Mapear telas permitidas, telas proibidas, jornada, cortes e pontos de zoom/destaque.
4. Criar roteiro narrado com frases curtas e beneficio claro.
5. Preparar storyboard ou lista de cenas antes de gravar.
6. Gerar ou gravar audio, legenda e video em formatos editaveis.
7. Revisar visualmente o arquivo final: enquadramento, audio, legenda, dados sensiveis, ritmo e clareza.
8. Salvar pacote completo: roteiro, video, audio, SRT/VTT, instrucoes de edicao, capa e relatorio.
9. Criar cron apenas para revisao de videos antigos, links quebrados, demos desatualizadas ou backlog de tutoriais.
10. Publicar somente apos QA e aprovacao quando houver marca, cliente real, claim comercial ou canal externo.

## Guardrails operacionais

- Comecar em modo dry-run quando a skill puder enviar mensagens, publicar conteudo, alterar dados, cobrar, cancelar, integrar sistemas ou tocar clientes.
- Usar allowlist de canais, contas, dominios e acoes permitidas.
- Separar credenciais por ambiente e nunca salvar tokens, cookies, senhas ou dados pessoais dentro da skill.
- Registrar evidencias suficientes para auditoria: entrada, decisao, acao, horario, resultado e proximo passo.
- Exigir revisao humana para acoes externas, alto volume, dados de clientes, risco juridico, financeiro, reputacional ou mudanca em producao.
