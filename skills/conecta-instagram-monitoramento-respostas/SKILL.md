---
name: "conecta-instagram-monitoramento-respostas"
description: "Monitorar sinais do Instagram orgânico e decidir follow-up seguro."
---

# Conecta Instagram Monitoramento De Respostas

## Objetivo

Monitorar sinais gerados pela prospecção orgânica no Instagram, registrar evidências no ERP e decidir follow-up seguro quando uma empresa curtir, responder ou demonstrar interesse.

## Escopo

Usar para:

- checar notificações do Instagram do Conecta;
- verificar respostas ou curtidas em comentários feitos pelo perfil `fidelizaconectaclube`;
- atualizar `instagramLeads`, `instagramInteractions` e `prospects` no ERP local;
- propor ou enviar DM apenas quando houver sinal explícito e contexto adequado.

Não usar para:

- DM fria em massa;
- responder automaticamente sem leitura contextual;
- insistir em perfil que ignorou ou reagiu negativamente;
- contornar limites, captcha, bloqueio ou aviso do Instagram.

## Fontes De Sinal

Prioridade:

1. Notificações do Instagram Web/Chrome aberto no perfil do Conecta.
2. Post onde o Conecta comentou, procurando resposta direta ao comentário.
3. Perfil da empresa, buscando mudança recente de follow/curtida/resposta.
4. Registro local `instagramInteractions` para saber o que foi comentado e onde.

Sinais:

- `liked-us`: empresa ou perfil relacionado curtiu nosso comentário.
- `replied`: empresa respondeu ao nosso comentário.
- `followed-back`: empresa seguiu o Conecta.
- `dm-inbound`: empresa mandou DM.
- `negative`: resposta negativa, crítica, pedido para parar ou indício de incômodo.

## Cadência Segura

- Checar 2 a 4 vezes por dia em horário comercial.
- Não ficar atualizando a tela em loop.
- Não abrir perfis pessoais de clientes/seguidores.
- Não usar automação agressiva de scroll ou clique.
- Se houver aviso, captcha, lentidão estranha ou bloqueio, parar e registrar risco.

## Fluxo Operacional

1. Ler `memory/YYYY-MM-DD.md` e `instagramInteractions` do ERP para identificar comentários recentes.
2. Abrir Instagram Web no Chrome já logado no perfil do Conecta, sem trocar conta/perfil.
3. Checar notificações visíveis.
4. Para cada sinal:
   - confirmar que vem de perfil comercial/local ou da empresa alvo;
   - capturar/registrar o tipo de sinal;
   - atualizar `instagramLeads.status`;
   - criar `instagramInteractions` com `type` apropriado;
   - atualizar o prospect correspondente.
5. Se houver resposta pública, ler o contexto antes de responder.
6. Se a empresa pediu informação, demonstrou abertura ou fez pergunta, preparar resposta curta.
7. DM só entra quando há sinal claro: resposta positiva, pergunta, follow-back ou inbound.

## Regras De Follow-up

Quando curtir nosso comentário:

- Não mandar DM imediatamente por padrão.
- Marcar como `liked-us`.
- Aguardar outro sinal ou próximo bloco de monitoramento.
- Se também seguir de volta ou responder, considerar DM.

Quando responder publicamente:

- Responder no mesmo post se a resposta for leve e pública.
- Se a resposta pedir detalhe, convidar para conversa com permissão.

Exemplo público:

```text
Verdade. Quando a base já gosta da casa, uma ação simples de retorno costuma fazer diferença. Posso te mandar uma ideia rápida por direct?
```

Quando houver permissão para DM:

```text
Oi! Vi seu retorno no comentário e achei que fazia sentido mandar uma ideia bem rápida. O Conecta ajuda lojas locais a trazer cliente antigo de volta com pontos, recompensas e campanhas simples. Quer que eu te mande um exemplo prático para o seu segmento?
```

## Critérios Para Não Enviar DM

Não enviar DM se:

- só houve uma curtida isolada;
- o perfil parece pessoal/privado;
- a resposta foi apenas emoji neutro sem abertura;
- houve crítica, incômodo ou pedido para parar;
- já houve contato no mesmo dia por outro canal;
- WhatsApp/Instagram teve aviso ou risco de bloqueio.

## Registro No ERP

Atualizar `instagramLeads`:

- `status`: `liked-us`, `replied`, `followed-back`, `dm-ready`, `warm`, `negative`.
- `lastSignalAt`.
- `lastSignalType`.
- `nextStep`.
- `notes` com resumo factual.

Criar `instagramInteractions`:

- `type`: `comment-liked`, `reply`, `followed-back`, `dm-inbound`, `dm-sent`, `negative`.
- `company`, `instagramHandle`, `postUrl`, `createdAt`, `commentText` ou `notes`.

Atualizar `prospects`:

- `status`: `qualified` se houve pergunta/abertura clara; `contacted` se apenas curtida/resposta leve.
- `temperature`: `morno-organico` ou `quente-organico`.
- `nextStep`: próxima ação segura.

## Notificação Ao Bruno

Avisar Bruno quando:

- houver resposta com intenção real;
- houver DM inbound;
- houver sinal negativo;
- houver bloqueio/captcha/risco de conta;
- uma empresa virar `dm-ready`.

Resumo ideal:

```text
Instagram: @perfil respondeu/curtiu nosso comentário. Sinal: X. Sugestão: responder público / aguardar / pedir permissão para DM. Texto sugerido: ...
```

## Aprendizado

Ao final de cada checagem, registrar:

- quais sinais apareceram;
- quais respostas funcionaram;
- quais segmentos engajaram;
- o que evitar na próxima abordagem;
- ajustes necessários na skill de prospecção orgânica.
