---
name: "conecta-video-ia-campanhas"
description: "QA obrigatorio antes de entregar video"
---

# Atualizacao proposta - QA obrigatorio para videos e criativos Conecta

## Objetivo

Adicionar um portao de qualidade obrigatorio ao workflow de videos IA, Reels, Shorts, criativos animados, imagens, carrosseis e edicoes do Conecta. A entrega so pode ser marcada como pronta depois de pesquisa/referencia adequada e revisao visual real do arquivo final.

## Nova regra operacional obrigatoria

Antes de entregar qualquer video, imagem, carrossel, story, criativo de ads ou asset visual ao Bruno:

1. Quando a qualidade do resultado anterior for criticada ou houver duvida de nivel profissional, buscar referencias e tutoriais validados na internet antes de refazer.
2. Usar referencias para aprender padroes de ritmo, legenda, cortes, movimento, audio, CTA, composicao e acabamento, sem copiar conteudo, roteiro, identidade visual, marca, template proprietario ou frase de concorrente.
3. Visualizar todas as imagens geradas ou editadas antes de dizer que estao prontas.
4. Revisar videos gerados ou editados apos renderizacao, no minimo com:
   - duracao, resolucao, formato e audio via `ffprobe`/ferramenta equivalente;
   - contact sheet ou frames distribuidos ao longo do video;
   - frames especificos de inicio, meio e fim;
   - conferencia de logo oficial, legibilidade mobile, sobreposicao, cortes estranhos e CTA;
   - checagem objetiva de volume/normalizacao quando houver audio.
5. Se a ferramenta nao permitir assistir/ouvir como humano, dizer isso claramente e usar as melhores validacoes possiveis; nao fingir que assistiu.
6. Se a revisao propria reprovar o asset, corrigir antes de enviar ao Bruno.
7. Nunca responder "pronto", "feito" ou equivalente apenas porque o arquivo foi renderizado. Renderizacao nao e aprovacao.
8. Ao entregar, informar de forma curta quais verificacoes foram feitas e qualquer limitacao real, por exemplo: voz TTS fallback, video sem movimento real, provedor bloqueado, audio nao ouvido humanamente.

## Criterios minimos de aprovacao de video/Reels

Um video so pode ser entregue como pronto quando passar pelos criterios abaixo:

- Gancho compreensivel nos primeiros 1-2 segundos.
- Visual com movimento perceptivel: corte, pan, zoom, troca de plano, animacao ou acao real. Nao entregar cena estatica com apenas legenda se o pedido for video profissional.
- Legenda com hierarquia: poucas palavras por tela, contraste forte, sem texto encostando em linha/rodape/logo, sem quebra feia, sem aspecto pobre.
- Audio com ritmo natural e sem pausas exageradas; para TTS fallback, testar velocidade entre 1.2x e 1.3x quando a voz soar lenta.
- Logo oficial aplicada sem duplicidade, deformacao, recorte, sombra suja ou tentativa de recriacao por IA.
- Promessas seguras: sem ROI garantido, sem numeros inventados, sem copiar concorrente.
- Arquivo final conferido visualmente apos a renderizacao final, nao apenas nos arquivos intermediarios.

## Quando usar referencias externas

Pesquisar referencias/tutoriais sempre que:

- Bruno disser que algo parece robotico, pobre, amador, estatico, lento ou sem nivel profissional.
- O criativo for para Reels/Ads e precisar competir com mercado real.
- Houver mudanca de formato, ferramenta, legenda, locucao, motion design ou estilo visual.
- A propria revisao mostrar problemas de ritmo, legibilidade, movimento, acabamento ou conversao.

Fontes aceitaveis: tutoriais de CapCut/Canva/After Effects/DaVinci, guias de criativos Meta Ads/Reels, canais de motion/captions reconhecidos, paginas publicas de concorrentes para benchmarking de padrao, bibliotecas de ads quando disponiveis e perfis de mercado observados como referencia visual.

## Registro de QA

Para entregas importantes, criar ou atualizar um pequeno arquivo de QA no pacote do asset com:

- referencias/tutoriais consultados;
- decisoes incorporadas;
- arquivos finais gerados;
- validacoes feitas;
- problemas conhecidos ou limitacoes;
- veredito: aprovado, aprovado com ressalva ou reprovado/corrigido.

## Frase de disciplina

A regra e: assistir/visualizar primeiro, entregar depois. Se eu nao revisei o arquivo final, eu nao digo que esta pronto.
