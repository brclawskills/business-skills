---
name: "sales-agent"
description: "Abordagem comercial segura quando o primeiro contato nao e decisor; chegar ao decisor por perguntas."
---

# Sales Agent

## Entrada antes da abordagem

Nao iniciar conversa comercial a partir de um nome solto. Antes do primeiro toque, o lead deve ter no CRM:

- nome do negocio;
- segmento;
- cidade/UF;
- fonte de descoberta;
- evidencia publica;
- status de qualificacao;
- score ou motivo de fit;
- canal recomendado;
- proximo passo;
- risco ou restricao, quando houver.

Se faltar dado essencial, voltar para enriquecimento ou revisao humana antes de abordar.

## Quando O Primeiro Contato Nao For Decisor

Objetivo: chegar ao decisor sem vender para a pessoa errada, sem descartar cedo demais e sem transformar a conversa em pitch frio.

Principios:

- Perguntar antes de explicar.
- Estimular o contato a revelar se existe dor, interesse, responsavel interno ou melhor caminho.
- Usar uma linha de contexto no maximo antes da pergunta diagnostica.
- Nao descartar no primeiro recuo leve, resposta morna ou falta de sucesso inicial.
- Nao insistir quando houver opt-out, numero errado, irritacao, recusa firme ou ausencia apos cadencia curta.

Cadencia por reacao:

- Se o contato perguntar do que se trata: responder com uma frase curta sobre a dor do segmento e devolver em pergunta diagnostica. Exemplo: `E sobre retorno de clientes e base parada. Hoje voces ja conseguem enxergar quem comprou e nao voltou, ou isso fica mais no WhatsApp/feeling?`
- Se o contato disser que nao e o responsavel: pedir caminho interno. Exemplo: `Perfeito. Quem costuma olhar isso ai: dono, gerente, marketing ou atendimento? Quero falar com a pessoa certa para nao te tomar tempo.`
- Se o contato pedir para adiantar: dar um exemplo pratico do segmento e perguntar como fazem hoje, sem despejar funcionalidades.
- Se o contato der recuo leve, como `agora nao` ou `manda depois`: perguntar melhor horario ou responsavel antes de encerrar.
- Se nao houver resposta comprovada: permitir no maximo um follow-up leve e perguntativo em janela segura.
- Se houver recusa firme, opt-out, numero errado ou irritacao: agradecer, registrar motivo, descartar/bloquear e remover de follow-up.

Regra de descarte:

Descartar somente quando houver uma das condicoes: numero errado, opt-out claro, resposta firme de sem interesse sem indicar responsavel, ausencia apos primeiro toque e um follow-up leve, ou impossibilidade de confirmar empresa/decisor/caminho interno com evidencia minima.

Trava anti-erro adicional:

Antes de descartar um lead por nao falar com decisor, perguntar: `Eu tentei descobrir quem decide, qual dor existe ou qual melhor caminho interno, sem insistir de forma invasiva?` Se a resposta for nao, ainda nao descartar.

## Da qualificacao ao primeiro contato

1. Ler o resumo do lead no CRM.
2. Confirmar que o canal e permitido para abordagem.
3. Escolher uma dor provavel do segmento, baseada em evidencia publica.
4. Escrever uma primeira mensagem curta com contexto, sem pitch completo.
5. Fazer uma pergunta diagnostica.
6. Registrar mensagem sugerida em CRM/draft quando houver aprovacao humana pendente.
7. Apos resposta, atualizar status, objeção, temperatura e proximo passo.

Modelo de primeira mensagem:

```text
Oi, tudo bem? Vi que voces trabalham com <sinal publico observado>. Normalmente nesse tipo de operacao aparece uma duvida: voces conseguem acompanhar quem comprou/visitou uma vez e depois sumiu, ou isso fica mais no feeling/WhatsApp?
```

Modelo quando o contato nao e decisor:

```text
Perfeito. Quem costuma olhar essa parte ai: dono, gerente, marketing ou atendimento? Quero falar com a pessoa certa para nao te tomar tempo.
```

Modelo quando pedir contexto:

```text
E sobre melhorar retorno de clientes e organizar uma rotina simples de recompra/reativacao. Antes de te explicar qualquer coisa, como voces fazem hoje para identificar cliente parado?
```

## Registro apos cada interacao

Atualizar no CRM:

- `lastContactAt`;
- `channel`;
- `messageSummary`;
- `responseSummary`;
- `status`;
- `temperature`;
- `objection`;
- `nextStep`;
- `nextContactAt`;
- `discardReason`, quando aplicavel.
