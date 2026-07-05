---
name: "conecta-operacao-autonoma-aprendizado"
description: "Execucao atomica sem metade"
---

# Atualizacao: Missao Atomica e Fechamento Mensuravel

## Regra central

Quando uma missao operacional for iniciada, ela deve ter criterio de aceite numerico, checkpoint curto e fechamento verificavel. Nunca tratar "agendado", "rodando", "em andamento" ou "sem historico visivel" como entrega.

## Antes de iniciar

1. Definir objetivo concreto: quantidade, entidade, canal, risco e limite.
2. Definir unidade atomica maxima:
   - prospeccao externa: lotes de 5 a 10 touchpoints;
   - alteracao de ERP/dados: uma entidade ou colecao por lote;
   - documentos/materiais: um arquivo ou pacote por lote;
   - integracao/bug: uma falha reproduzida, uma correcao, uma validacao.
3. Definir criterio de pronto: evidencias no ERP, memoria, arquivo, Workboard ou log.
4. Definir criterio de parada: captcha, UI ambigua, risco reputacional, falta de credencial, erro repetido, limite financeiro ou falta de prova.

## Durante a execucao

- Registrar progresso depois de cada lote, nao so no final.
- Se uma execucao ficar mais de 5 minutos sem novo progresso mensuravel, considerar suspeita.
- Se ficar mais de 10 minutos sem progresso, abrir plano de retomada: checar estado, reduzir lote, trocar rota ou bloquear com motivo.
- Nao iniciar bloco seguinte enquanto o bloco anterior estiver sem fechamento, exceto se houver decisao explicita de paralelismo seguro.
- Se precisar adiar um bloco seguinte para terminar o anterior, registrar o adiamento e o motivo.

## Fechamento obrigatorio

Ao encerrar, responder sempre:

- Meta original.
- Feito real.
- Evidencia/onde foi registrado.
- Faltante, se houver.
- Causa do faltante.
- Proxima acao com prazo ou responsavel.

## Proibido

- Inflar metricas com tarefas apenas mapeadas.
- Contar intencao/agendamento como execucao.
- Deixar job grande rodando sem checkpoint e sem retomada.
- Dizer "feito" quando falta parte do criterio de aceite.

## Aplicacao imediata ao Conecta

Para sprint comercial, cada bloco deve fechar com contagem real por tipo: follows, likes, comentarios, DMs, WhatsApp, respostas e bloqueios. O ERP e a memoria devem bater. Se o browser ou cron travar, dividir em microlotes e concluir/registrar cada lote antes de seguir.
