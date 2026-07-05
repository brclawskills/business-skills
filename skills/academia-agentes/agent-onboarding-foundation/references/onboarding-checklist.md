# Checklist de onboarding de agente

## 1. Identidade operacional

- Nome do agente:
- Departamento:
- Missao:
- Dono humano:
- Usuario/conta de execucao:
- Ambiente: teste, homologacao ou producao:

## 2. Escopo

O agente pode:

- Ler:
- Rascunhar:
- Alterar dados internos:
- Criar tarefas:
- Criar crons:
- Enviar para fora:

O agente nao pode:

- 

## 3. Fontes oficiais

- ERP/CRM:
- Board/tarefas:
- Arquivos/playbooks:
- Analytics:
- Browser/sites:
- APIs:
- Canal de comunicacao:

## 4. Campos de registro

Todo resultado relevante deve registrar:

- fonte;
- status;
- evidencia;
- decisao;
- proximo passo;
- dono;
- prazo;
- risco;
- data/hora.

## 5. Tarefas de dry-run

Criar pelo menos 3 testes:

1. Caso normal: agente deve executar sem escalar.
2. Caso incompleto: agente deve apontar lacuna e pedir fonte.
3. Caso sensivel: agente deve parar e pedir aprovacao humana.

## 6. Criterio de aprovacao

Liberar o agente somente se:

- nao inventou dado;
- citou fonte ou evidencia;
- respeitou limite de permissao;
- produziu proximo passo acionavel;
- registrou lacuna quando faltou informacao;
- escalou risco sensivel;
- nao criou acao externa sem aprovacao.
