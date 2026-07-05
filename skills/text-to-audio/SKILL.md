---
name: "text-to-audio"
description: "Transforma roteiros em narracao por IA, com audio final, legenda sincronizada, marcacao de tempo e revisao de portugues brasileiro."
---

# Text To Audio

Use para transformar roteiros escritos do Conecta Clube em narração, áudio final, legenda sincronizada, marcação de tempo e pacote de revisão para vídeos comerciais, institucionais, tutoriais, treinamentos e apresentações.

## Entradas esperadas

- Roteiro bruto.
- Objetivo do vídeo.
- Público-alvo.
- Tom desejado.
- Duração estimada.
- Estilo de fala.
- Divisão por cenas.
- Nome do produto, funcionalidade ou área do SaaS.
- Observações de pronúncia.
- Termos que devem manter grafia específica.

## Saídas obrigatórias

- `narracao-final.mp3`
- `roteiro-narracao-final.md`
- `legenda-final.srt`
- `marcacao-tempo-cenas.md`
- `checklist-audio-legenda.md`
- `checklist-portugues-legenda.md`
- `relatorio-text-to-audio.md`

Gerar também `narracao-final.wav` e `legenda-final.vtt` quando forem úteis para edição, arquivamento ou compatibilidade.

## Fluxo obrigatório

1. Receber o roteiro bruto e confirmar objetivo, público, tom e duração.
2. Revisar português brasileiro, acentuação, pontuação, concordância e naturalidade.
3. Ajustar o texto para fala com frases curtas e ritmo de tutorial guiado.
4. Remover termos confusos, ambíguos ou técnicos sem necessidade.
5. Padronizar nomes, especialmente “Conecta Clube”.
6. Validar UTF-8 e ausência de caracteres corrompidos.
7. Gerar narração com ferramenta segura, oficial, reconhecida ou já autorizada.
8. Validar pronúncia, ritmo, clareza e naturalidade.
9. Ajustar o roteiro e gerar nova versão se a narração ficar artificial.
10. Gerar legenda SRT a partir da narração final.
11. Gerar VTT quando útil.
12. Validar acentuação, gramática, timestamps e ordem dos blocos.
13. Salvar todos os arquivos em pasta organizada.
14. Documentar ferramenta usada, origem, configuração, riscos, limitações e ganho de ROI.

## Padrão de voz

- Idioma: português brasileiro.
- Tom: claro, profissional, confiante, didático e acessível.
- Ritmo: moderado.
- Estilo: tutorial guiado.
- Energia: comercial, sem exagero publicitário.
- Objetivo: facilitar compreensão da navegação.
- Evitar fala robótica.
- Evitar frases longas.
- Evitar excesso de termos técnicos.

## Ferramentas

Priorizar ferramentas locais, oficiais, gratuitas ou já autorizadas. Pedir aprovação humana antes de usar ferramenta com custo novo, contratação paga, cartão de crédito, login pessoal, acesso amplo a arquivos, envio de dados reais de clientes, publicação automática, alteração em produção, executável de origem não oficial ou permissão administrativa elevada.

Registrar sempre:

- Nome da ferramenta.
- Tipo.
- Fonte oficial ou origem.
- Motivo de uso.
- Ganho esperado de ROI.
- Arquivos gerados.
- Riscos identificados.
- Medidas de segurança.
- Observações para reutilização.

## Validação de português e legenda

Antes de gerar áudio ou legenda:

- Corrigir acentuação, concordância, regência, pontuação, crase, plural e singular.
- Preservar caracteres como á, é, í, ó, ú, â, ê, ô, ã, õ e ç.
- Corrigir qualquer sinal de encoding quebrado, como `Ã§`, `Ã£`, `Ã©` ou símbolo de substituição Unicode.
- Garantir que a legenda reflita a narração final.
- Validar SRT no formato `00:00:00,000 --> 00:00:00,000`.
- Manter blocos curtos e legíveis.

## Padrão de arquivos

- `narracao-final.mp3`
- `narracao-final.wav`
- `roteiro-narracao-final.md`
- `legenda-final.srt`
- `legenda-final.vtt`
- `marcacao-tempo-cenas.md`
- `checklist-audio-legenda.md`
- `checklist-portugues-legenda.md`
- `relatorio-text-to-audio.md`

## Teste mínimo

Para validar a skill, gerar um teste curto com:

“Bem-vindo ao Conecta Clube. Neste tour rápido, você vai conhecer as principais áreas da plataforma e entender como ela facilita a rotina dos usuários.”

Salvar:

- `teste-narracao-conecta-clube.mp3`
- `teste-narracao-conecta-clube.wav`, se útil
- `teste-narracao-conecta-clube.srt`
- `teste-narracao-conecta-clube.vtt`, se útil
- `relatorio-teste-text-to-audio.md`
