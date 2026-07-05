# Business Skills

Repositorio publico de skills para empresarios, operadores e desenvolvedores que usam OpenClaw/Claw para automacoes de negocio.

## Objetivo

Reunir skills reutilizaveis para operar SaaS, marketing, vendas, customer success, suporte, conteudo, BI, integracoes e rotinas executivas com agentes.

As skills deste repositorio nasceram em operacao real e foram generalizadas para uso em qualquer negocio. Adapte nomes, canais, ferramentas, politicas, limites e aprovacoes antes de usar.

## Estrutura

As skills ficam agrupadas por departamento:

```text
skills/
  <departamento>/
    <skill>/
      SKILL.md
      instrucoes-de-uso.md
      references/          # opcional
```

Departamentos atuais:

- `comercial-vendas`
- `customer-success-suporte`
- `dados-erp-bi`
- `executivo-operacao`
- `instagram-meta-prospeccao`
- `integracoes-tecnologia`
- `juridico-financeiro-revops`
- `marketing-conteudo-growth`
- `produto-demo-video`

## Como usar

1. Escolha o departamento em `skills/<departamento>/`.
2. Abra `skills/<departamento>/<skill>/SKILL.md` para entender o procedimento principal.
3. Leia `skills/<departamento>/<skill>/instrucoes-de-uso.md` antes de ativar automacoes.
4. Substitua referencias genericas por sistemas, canais, politicas, credenciais e limites do negocio.
5. Teste em ambiente controlado ou dry-run antes de publicar, enviar mensagens, alterar dados ou criar crons.

## Cuidados

- Nao publique credenciais, tokens, cookies, arquivos de secrets, dados pessoais, bases de clientes ou prints internos.
- Skills comerciais e juridicas nao substituem decisores, contador, advogado, DPO ou responsavel tecnico.
- Acoes externas como posts, DMs, WhatsApp, emails, disparos, deploys e alteracoes financeiras devem exigir aprovacao humana quando houver risco.
- Para repositorios publicos, prefira exemplos genericos, caminhos configuraveis e instrucoes de uso separadas do procedimento principal.

## Contribuicao

Novas skills devem incluir:

- nome claro;
- departamento;
- `SKILL.md` com descricao curta, quando usar, procedimento e guardrails;
- `instrucoes-de-uso.md` com requisitos, ferramentas/acessos, sugestao de cron e atividades indicadas;
- criterio de pronto ou evidencia.
