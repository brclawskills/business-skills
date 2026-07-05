# Matriz de graduacao de agentes

## Matriz resumida

| Nivel | Nome | Pode fazer | Nao pode fazer | Evidencia minima |
| --- | --- | --- | --- | --- |
| 1 | Assistente | Ler, resumir, rascunhar | Escrever em sistema, enviar, criar cron | 5 dry-runs corretos |
| 2 | Operador interno | Atualizar CRM/ERP/board permitido | Enviar externo, publicar, mudar preco | 10 execucoes internas corretas |
| 3 | Semi-autonomo | Rodar rotina e cron de baixo risco | Alto volume, promessa, contrato, producao | 2 semanas sem desvio |
| 4 | Supervisor | Coordenar agentes e conciliar reports | Assumir decisao sensivel humana | Ciclos fechados com evidencia |
| 5 | Executivo | Priorizar, decidir internamente e recomendar estrategia | Risco legal, financeiro ou reputacional sem aprovacao | Decisoes uteis e auditaveis |

## Campos recomendados por agente

```json
{
  "agentName": "nome-do-agente",
  "department": "comercial",
  "currentLevel": 2,
  "targetLevel": 3,
  "owner": "responsavel humano",
  "allowedTools": ["crm_read", "crm_write_limited"],
  "blockedTools": ["external_send", "billing_change"],
  "cronAllowed": false,
  "externalActionsAllowed": false,
  "lastReviewAt": "2026-01-01",
  "evidence": ["link ou registro"],
  "risks": ["sem aprovacao para WhatsApp"],
  "nextStep": "rodar 5 dry-runs de follow-up"
}
```

## Sinais de promocao

- Saidas consistentes.
- Pouca correcao humana.
- Registro claro no sistema oficial.
- Reconhecimento de lacunas.
- Escalonamento correto.
- Sem extrapolar permissao.

## Sinais de rebaixamento

- Inventa fonte.
- Omite risco.
- Envia sem aprovacao.
- Cria duplicidade no CRM.
- Usa cron para repetir erro.
- Ignora opt-out ou limite de canal.
- Gera report bonito sem acao ou evidencia.
