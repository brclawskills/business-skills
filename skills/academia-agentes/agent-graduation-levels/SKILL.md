---
name: "agent-graduation-levels"
description: "Graduacao de agentes por niveis de autonomia: assistente, operador interno, semi-autonomo, supervisor e executivo."
---

# Agent Graduation Levels

Use esta skill para classificar, promover ou rebaixar agentes conforme evidencia real de confiabilidade. A graduacao evita liberar um agente imaturo para enviar mensagens, alterar CRM, criar cron ou tomar decisoes sensiveis.

## Regra central

Autonomia e conquistada por evidencia, nao por vontade. Um agente so sobe de nivel quando executa bem o nivel atual com logs, criterio de pronto, baixa taxa de erro e escalonamento correto.

## Niveis

### Nivel 1 - Assistente

Pode:

- ler contexto autorizado;
- resumir;
- responder perguntas internas;
- sugerir plano;
- criar rascunhos.

Nao pode:

- alterar sistemas;
- enviar mensagens externas;
- criar cron;
- decidir por conta propria.

Criterio de promocao: 5 saidas uteis em dry-run, sem inventar dado e com proximo passo claro.

### Nivel 2 - Operador interno

Pode:

- atualizar CRM/ERP/board com campos permitidos;
- criar tarefas;
- organizar arquivos;
- registrar evidencias;
- preparar rascunhos para aprovacao.

Nao pode:

- enviar para cliente;
- publicar conteudo;
- mexer em preco, contrato, financeiro ou producao.

Criterio de promocao: 10 execucoes internas corretas, com rollback simples ou correcao auditavel.

### Nivel 3 - Semi-autonomo

Pode:

- rodar rotina recorrente;
- criar cron de leitura/report;
- tomar decisoes de baixo risco;
- executar follow-up interno;
- preparar fila operacional.

Nao pode:

- disparar alto volume;
- contatar cliente sem regra;
- aprovar oferta, desconto, contrato ou campanha sensivel.

Criterio de promocao: 2 semanas de rotina com report consistente, falhas registradas e nenhuma acao fora de limite.

### Nivel 4 - Supervisor

Pode:

- coordenar agentes de niveis menores;
- cobrar reports;
- reconciliar ERP/CRM/board;
- abrir tarefas;
- detectar gargalos;
- escalar decisoes humanas.

Nao pode:

- substituir responsavel legal, financeiro, tecnico ou comercial em decisoes sensiveis.

Criterio de promocao: fechar ciclos completos com decisao, evidencia, responsavel e melhoria operacional.

### Nivel 5 - Executivo

Pode:

- priorizar o dia;
- decidir realocacao de capacidade;
- propor mudanca de estrategia;
- consolidar report executivo;
- recomendar parar, escalar ou corrigir operacao.

Nao pode:

- assumir risco juridico, financeiro, reputacional ou contratual sem aprovacao humana.

Criterio de manutencao: gerar decisao util, nao apenas resumo.

## Processo de promocao

1. Identificar nivel atual e nivel desejado.
2. Reunir evidencias do nivel atual.
3. Medir erros, retrabalho, omissoes e escalonamentos.
4. Rodar teste do proximo nivel em ambiente controlado.
5. Definir novas permissoes, limites e criterio de rollback.
6. Registrar aprovador humano.
7. Promover por tempo limitado.
8. Revisar depois de 3, 7 ou 14 dias conforme risco.

## Rebaixamento

Rebaixar o agente imediatamente quando houver:

- dado inventado;
- acao externa indevida;
- registro falso ou incompleto;
- perda de controle de cron;
- falha repetida sem aprendizado;
- risco juridico, financeiro ou reputacional;
- descumprimento de opt-out, consentimento ou limite de canal.

## Quando ler referencias

- Leia `references/graduation-matrix.md` quando precisar montar uma matriz de permissao por nivel.

## Guardrails

- Promocao sem evidencias cria risco operacional.
- Cron aumenta impacto de erro; tratar como promocao de autonomia.
- Acesso de escrita deve ser menor que acesso de leitura.
- Acoes externas exigem nivel, canal, limite, aprovacao e log.
- Rebaixar nao e punicao; e controle de qualidade.
