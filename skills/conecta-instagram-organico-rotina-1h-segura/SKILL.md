---
name: "conecta-instagram-organico-rotina-1h-segura"
description: "Rotacao de praca se bloco performar mal"
---

# Proposta de atualizacao - Rotacao de praca por baixa performance

## Objetivo

Fortalecer a skill `conecta-instagram-organico-rotina-1h-segura` com uma regra explicita de mudanca de municipio/regiao quando uma rodada de prospeccao ficar muito abaixo da meta ou quando a fila local estiver saturada.

## Adicao proposta

Inserir na secao `Regra de troca de municipio/regiao`:

### Gatilho de baixa performance

Trocar municipio/regiao imediatamente no proximo bloco quando ocorrer qualquer um destes sinais:

- O bloco entregar menos de 50% da meta de touchpoints qualificados, sem captcha/bloqueio que explique a queda.
- Um resultado for gritante baixo, por exemplo `2/40`, `5/40` ou outro numero claramente incompatível com a meta e com a disponibilidade de cidades boas.
- A fila atual estiver saturada por perfis ja seguidos, perfis qualificados sem acao nova segura, botoes ausentes/ambiguos ou repeticao dos mesmos handles.
- A automacao ou UI ficar insegura o suficiente para reduzir demais a execucao, mas ainda houver margem para tentar outra praca com acao manual/visual ou seletor mais escopado.

A troca de praca deve acontecer antes de afrouxar o ICP. Nao insistir em uma mesma cidade/fila so para tentar salvar volume.

## Pracas autorizadas/prioritarias

Quando Itabira, Joao Monlevade ou a fila atual saturarem, rotacionar entre:

- Uba
- Uberlandia
- Formiga
- Arcos
- Divinopolis
- Vale do Aco: Ipatinga, Coronel Fabriciano e Timoteo
- Sabara
- Santa Maria de Itabira
- Betim
- Contagem
- Nova Lima
- Itajai-SC
- Blumenau-SC
- Brusque-SC
- Balneario Camboriu-SC
- Florianopolis-SC
- Maringa-PR
- Outras cidades boas com comercio local recorrente, desde que o fit seja validado antes da interacao

## Procedimento ao trocar

1. Registrar no diario/ERP que a praca anterior performou mal e por quê.
2. Escolher uma nova praca antes de buscar novos leads.
3. Avaliar os primeiros 10 a 15 candidatos da nova praca.
4. Se a nova praca tambem vier fraca, trocar novamente ou encerrar com bloqueio honesto, sem inflar metrica.
5. No fechamento, informar regioes testadas, resultado por regiao, faltante e proxima praca recomendada.

## Regra de reporte

Quando a meta nao bater, o fechamento deve dizer claramente: meta, feito real, faltante, praca usada, motivo provavel e o que sera alterado na proxima tentativa. Nunca declarar meta batida por mapeamento, candidatos avaliados ou perfis sem acao externa confirmada.
