---
name: "text-to-audio"
description: "Transforma roteiros em narracao por IA, com audio final, legenda sincronizada, marcacao de tempo e revisao de portugues brasileiro."
---

# Text To Audio

Use para transformar roteiros escritos de qualquer produto, servico ou area de negocio em narracao, audio final, legenda sincronizada, marcacao de tempo e pacote de revisao para videos comerciais, institucionais, tutoriais, treinamentos e apresentacoes.

## Entradas esperadas

- Roteiro bruto.
- Objetivo do video.
- Publico-alvo.
- Tom desejado.
- Duracao estimada.
- Estilo de fala.
- Divisao por cenas.
- Nome do produto, funcionalidade ou area do SaaS.
- Observacoes de pronuncia.
- Termos que devem manter grafia especifica.

## Saidas obrigatorias

- `narracao-final.mp3`
- `roteiro-narracao-final.md`
- `legenda-final.srt`
- `marcacao-tempo-cenas.md`
- `checklist-audio-legenda.md`
- `checklist-portugues-legenda.md`
- `relatorio-text-to-audio.md`

Gerar tambem `narracao-final.wav` e `legenda-final.vtt` quando forem uteis para edicao, arquivamento ou compatibilidade.

## Fluxo obrigatorio

1. Receber o roteiro bruto e confirmar objetivo, publico, tom e duracao.
2. Revisar portugues brasileiro, acentuacao, pontuacao, concordancia e naturalidade.
3. Ajustar o texto para fala com frases curtas e ritmo de tutorial guiado.
4. Remover termos confusos, ambiguos ou tecnicos sem necessidade.
5. Padronizar nomes do produto, marca, area e funcionalidades.
6. Validar UTF-8 e ausencia de caracteres corrompidos.
7. Gerar narracao com ferramenta segura, oficial, reconhecida ou ja autorizada.
8. Validar pronuncia, ritmo, clareza e naturalidade.
9. Ajustar o roteiro e gerar nova versao se a narracao ficar artificial.
10. Gerar legenda SRT a partir da narracao final.
11. Gerar VTT quando util.
12. Validar acentuacao, gramatica, timestamps e ordem dos blocos.
13. Salvar todos os arquivos em pasta organizada.
14. Documentar ferramenta usada, origem, configuracao, riscos, limitacoes e ganho de ROI.

## Padrao de voz

- Idioma: portugues brasileiro.
- Tom: claro, profissional, confiante, didatico e acessivel.
- Ritmo: moderado.
- Estilo: tutorial guiado.
- Energia: comercial, sem exagero publicitario.
- Objetivo: facilitar compreensao da navegacao, do processo ou da oferta.
- Evitar fala robotica.
- Evitar frases longas.
- Evitar excesso de termos tecnicos.

## Ferramentas

Priorizar ferramentas locais, oficiais, gratuitas ou ja autorizadas. Pedir aprovacao humana antes de usar ferramenta com custo novo, contratacao paga, cartao de credito, login pessoal, acesso amplo a arquivos, envio de dados reais de clientes, publicacao automatica, alteracao em producao, executavel de origem nao oficial ou permissao administrativa elevada.

Registrar sempre:

- Nome da ferramenta.
- Tipo.
- Fonte oficial ou origem.
- Motivo de uso.
- Ganho esperado de ROI.
- Arquivos gerados.
- Riscos identificados.
- Medidas de seguranca.
- Observacoes para reutilizacao.

## Validacao de portugues e legenda

Antes de gerar audio ou legenda:

- Corrigir acentuacao, concordancia, regencia, pontuacao, crase, plural e singular.
- Preservar caracteres corretos quando o arquivo final exigir acentos.
- Corrigir qualquer sinal de encoding quebrado, caracteres duplicados ou simbolo de substituicao Unicode.
- Garantir que a legenda reflita a narracao final.
- Validar SRT no formato `00:00:00,000 --> 00:00:00,000`.
- Manter blocos curtos e legiveis.

## Padrao de arquivos

- `narracao-final.mp3`
- `narracao-final.wav`
- `roteiro-narracao-final.md`
- `legenda-final.srt`
- `legenda-final.vtt`
- `marcacao-tempo-cenas.md`
- `checklist-audio-legenda.md`
- `checklist-portugues-legenda.md`
- `relatorio-text-to-audio.md`

## Teste minimo

Para validar a skill, gerar um teste curto com:

"Bem-vindo ao produto. Neste tour rapido, voce vai conhecer as principais areas da plataforma e entender como ela facilita a rotina dos usuarios."

Salvar:

- `teste-narracao-produto.mp3`
- `teste-narracao-produto.wav`, se util
- `teste-narracao-produto.srt`
- `teste-narracao-produto.vtt`, se util
- `relatorio-teste-text-to-audio.md`
