# Playbook Inicial - Videos IA Conecta - 2026-06-21

## Objetivo

Padronizar uso de geracao de videos com IA para campanhas pagas, conteudo organico e materiais gratuitos do Conecta, minimizando retrabalho.

## Estado atual da ferramenta

Em 2026-06-21, a ferramenta local indicou OpenAI video com `sora-2` e `sora-2-pro`, mas nao configurado; OpenAI imagem estava configurado. Varios provedores de video existiam como fallback, mas nao configurados.

Docs oficiais consultadas: `developers.openai.com/api/docs/guides/video-generation`, `developers.openai.com/cookbook/examples/sora/sora2_prompting_guide`, help sobre descontinuacao do Sora.

Ponto critico: docs atuais informavam Sora web/app descontinuado em 2026-04-26 e API Sora/Videos com desligamento em 2026-09-24. Usar o metodo, mas nao depender de Sora sem fallback.

## Capacidades oficiais relevantes

Criar video por prompt, guiar com imagem/primeiro frame, reutilizar personagens/assets, estender video, editar video, baixar MP4/thumbnail/spritesheet e rodar filas via Batch API. Processo assincrono: criar job, aguardar/pollar/webhook, baixar MP4.

`sora-2`: mais rapido para exploracao. `sora-2-pro`: maior qualidade para final, 1080p vertical/horizontal. Duracoes documentadas: 4, 8, 12, 16 e 20 segundos.

## Guardrails Conecta

Nao usar rostos reais, pessoas publicas, personagens famosos, musicas protegidas, marcas de terceiros ou interface falsa como produto real. Nao recriar a logo do Conecta por IA; aplicar logo oficial depois. Nao prometer ROI/faturamento/percentuais garantidos.

## Ferramentas

- Video IA/OpenAI/Sora ou fallback: gerar movimento/cena bruta, preferindo sem texto e sem logo.
- GPT Image: criar first frame, cena base, assets, mascote/elementos e imagens derivadas.
- Canva: aplicar Brand Kit, logo oficial, texto/CTA, formatos, templates e variacoes estaticas/video simples.
- CapCut: ritmo, cortes, captions, locucao/TTS, trilha, efeitos leves, sound design e exportacao social.

## Pipeline

1. Escolher objetivo.
2. Escrever roteiro 8-12s.
3. Definir destino.
4. Criar imagem/base com GPT Image quando precisar consistencia.
5. Gerar video curto ou montar motion em Canva/CapCut.
6. Revisar sem texto/logo.
7. Finalizar em Canva/CapCut com legenda, logo oficial, CTA e audio.
8. Exportar 9:16.
9. Registrar no ERP.

## Canva

Usar para acabamento, padronizacao, logo oficial, Brand Kit, legendas limpas, CTA, redimensionamento e versoes estaticas. Evitar templates genericos, texto demais, animacoes exageradas e logo deformada.

## CapCut

Usar para cortes, ritmo, captions, locucao/TTS, trilha segura, zooms leves, transicoes simples, scan de QR e exportacao social. Revisar legendas automaticas e evitar efeitos virais que infantilizam B2B.

## Conceitos iniciais

1. Cliente sumiu - food/delivery.
2. WhatsApp cheio, CRM vazio - lojista local.
3. Cashback com regra - varejo.
4. Dia fraco - restaurante/bar.
5. Cliente voltou pelo QR/cupom - prova visual.
6. Raio-X de Recompra - convite consultivo.
