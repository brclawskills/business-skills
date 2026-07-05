# Playbook de captacao, qualificacao e CRM

Use este playbook quando o agente precisar descobrir empresas, enriquecer dados publicos, qualificar fit e registrar leads no CRM/ERP antes de qualquer abordagem.

## Objetivo

Transformar pesquisa solta em uma fila comercial auditavel:

1. descobrir empresas com fit;
2. confirmar que o negocio existe e esta ativo;
3. encontrar dados publicos suficientes;
4. enriquecer CNPJ quando possivel;
5. pontuar fit e risco;
6. deduplicar;
7. salvar no CRM;
8. sugerir proximo passo seguro.

## Entradas

- Segmento alvo: exemplo `restaurantes`, `clinicas de estetica`, `pet shops`, `moda feminina`.
- Praca: cidade, bairro, regiao ou raio.
- Oferta ou tese: qual dor o produto resolve para esse segmento.
- Limite de volume: quantidade maxima por rodada.
- Canais permitidos: Google Search, Google Maps/Places, Instagram, site publico, diretorios publicos.
- CRM/ERP de destino e campos obrigatorios.

## Descoberta via Google Search no navegador

Use quando nao houver chave de API do Google Places ou quando o agente precisar validar contexto manualmente.

Consultas uteis:

```text
<segmento> <cidade> Instagram
<segmento> <bairro> <cidade> WhatsApp
site:instagram.com <segmento> <cidade>
site:google.com/maps <segmento> <cidade>
"<nome do negocio>" "<cidade>" CNPJ
"<nome do negocio>" "CNPJ"
"<nome do negocio>" "telefone"
```

Procedimento:

1. Abrir busca normal no navegador.
2. Coletar apenas resultados publicos.
3. Priorizar resultados com site oficial, Google Maps, Instagram ativo ou telefone publico.
4. Registrar a URL usada como evidencia.
5. Nao inferir CNPJ apenas por nome parecido; marcar como `cnpj_unconfirmed` quando houver duvida.

## Descoberta via Google Places API

Use quando o negocio tiver chave de API, billing e permissao para Places API.

Endpoint sugerido da Places API nova:

```http
POST https://places.googleapis.com/v1/places:searchText
X-Goog-Api-Key: <GOOGLE_API_KEY>
X-Goog-FieldMask: places.id,places.displayName,places.formattedAddress,places.nationalPhoneNumber,places.websiteUri,places.googleMapsUri,places.businessStatus,places.rating,places.userRatingCount,places.primaryType,places.types,places.location
Content-Type: application/json
```

Body exemplo:

```json
{
  "textQuery": "restaurantes em Curitiba PR",
  "languageCode": "pt-BR",
  "regionCode": "BR"
}
```

Campos a salvar:

- `googlePlaceId`
- `businessName`
- `address`
- `city`
- `state`
- `phone`
- `website`
- `googleMapsUrl`
- `businessStatus`
- `rating`
- `reviewCount`
- `types`
- `source = google_places`

Boas praticas:

- Usar field mask enxuto para reduzir custo.
- Respeitar termos da API e politica de armazenamento.
- Nao chamar API em loop sem limite.
- Cachear resultado por `googlePlaceId`.
- Revalidar dados antigos antes de contato.

## Enriquecimento com CNPJ.ws

Use CNPJ.ws apenas com CNPJ em digitos, sem pontuacao.

Endpoint publico:

```http
GET https://publica.cnpj.ws/cnpj/<CNPJ_DIGITOS>
```

Exemplo:

```http
GET https://publica.cnpj.ws/cnpj/00000000000100
```

Fluxo:

1. Remover pontuacao do CNPJ.
2. Validar que tem 14 digitos.
3. Consultar CNPJ.ws.
4. Se retornar erro, registrar `cnpj_enrichment_status = failed` e motivo.
5. Se retornar dados, salvar somente campos uteis para qualificacao.

Campos uteis:

- `cnpj`
- `razaoSocial`
- `nomeFantasia`
- `situacaoCadastral`
- `dataInicioAtividade`
- `cnaePrincipal`
- `cnaesSecundarios`
- `porte`
- `naturezaJuridica`
- `simplesNacional`, quando disponivel
- `endereco`
- `municipio`
- `uf`
- `telefone`
- `email`, quando publico no retorno

Regras:

- Nao usar CNPJ.ws como fonte de opt-in.
- Nao abordar pessoa fisica a partir de quadro societario.
- Nao publicar dados enriquecidos em canais publicos.
- Nao descartar automaticamente por CNAE divergente; usar como sinal, nao como verdade absoluta.
- Registrar URL/fonte e timestamp da consulta.

## Como encontrar CNPJ com seguranca

Ordem recomendada:

1. Site oficial do negocio, rodape, politica de privacidade, termos ou nota fiscal.
2. Google Search com nome exato + cidade + `CNPJ`.
3. Diretorios publicos confiaveis.
4. Receita/dados publicos equivalentes, quando disponiveis.

Nunca confirmar CNPJ quando:

- o nome fantasia e comum e ha varias empresas na mesma cidade;
- o endereco diverge;
- o segmento diverge;
- a fonte nao mostra relacao clara com o negocio;
- o dado vem de pagina duvidosa ou desatualizada.

Se houver duvida, salvar:

```json
{
  "cnpj": null,
  "cnpjStatus": "unconfirmed",
  "cnpjEvidence": "Busca encontrou candidatos divergentes; precisa revisao humana."
}
```

## Deduplicacao

Antes de criar lead novo, procurar duplicados por:

- CNPJ;
- Google Place ID;
- telefone/WhatsApp normalizado;
- dominio do site;
- Instagram handle;
- nome + cidade + endereco.

Se encontrar duplicado:

1. Atualizar evidencias e campos faltantes.
2. Nao resetar status comercial sem motivo.
3. Nao criar nova oportunidade se ja existe deal aberto.
4. Registrar a nova fonte em `sources[]`.

## Score de fit

Pontuar de 0 a 100.

Sinais positivos:

- segmento aderente a dor resolvida pelo produto;
- negocio local com recorrencia;
- base de clientes ou fluxo repetido;
- Instagram ativo;
- WhatsApp/site publico;
- avaliacoes recentes;
- campanhas, cardapio, agenda, delivery, clube, recorrencia ou pos-venda;
- decisor ou canal comercial identificavel.

Sinais negativos:

- negocio fechado/inativo;
- sem canal publico de contato;
- baixa aderencia a recorrencia;
- perfil pessoal sem relacao clara com empresa;
- CNPJ baixado/inapto;
- fonte contraditoria;
- risco juridico/reputacional;
- opt-out anterior.

Faixas:

- `80-100`: qualificado e pronto para proximo passo.
- `60-79`: bom lead, precisa validar canal ou decisor.
- `40-59`: manter em pesquisa ou nutricao.
- `<40`: descartar ou arquivar com motivo.

## Status de CRM

Use status simples:

- `discovered`: encontrado, ainda sem enriquecimento.
- `enriched`: dados publicos coletados.
- `qualified`: fit suficiente para proximo passo.
- `contact-ready`: canal e abordagem definidos.
- `contacted`: primeira interacao registrada.
- `responded`: houve resposta.
- `opportunity`: virou conversa comercial real.
- `discarded`: sem fit, duplicado, fechado, opt-out ou risco.
- `blocked`: precisa aprovacao, revisao humana, captcha, limite ou dado ausente.

## Payload minimo para CRM/ERP

```json
{
  "businessName": "Nome publico do negocio",
  "legalName": "Razao social, se confirmada",
  "cnpj": "00000000000100",
  "cnpjStatus": "confirmed|unconfirmed|not_found|failed",
  "segment": "restaurante",
  "city": "Cidade",
  "state": "UF",
  "source": "google_places|google_search|instagram|site|directory",
  "sources": [
    {
      "type": "google_maps",
      "url": "https://maps.google.com/...",
      "checkedAt": "2026-01-01T12:00:00-03:00"
    }
  ],
  "googlePlaceId": "place_id",
  "instagramHandle": "@perfil",
  "website": "https://site.example",
  "phone": "+55...",
  "whatsapp": "+55...",
  "fitScore": 82,
  "fitReason": "Restaurante ativo, recorrencia clara, Instagram ativo e WhatsApp publico.",
  "status": "qualified",
  "nextStep": "Preparar comentario contextual no Instagram ou validar decisor.",
  "risk": "none",
  "owner": "agente ou area",
  "notes": "Resumo curto com evidencias e criterio."
}
```

## Cron sugerido

Use crons separados por etapa, com limite e saida auditavel.

### Descoberta

- Frequencia: diario ou 2 a 3 vezes por semana.
- Volume: 20 a 100 candidatos por rodada, conforme maturidade.
- Saida: leads `discovered` com fontes.
- Nao executar abordagem nesta etapa.

### Enriquecimento

- Frequencia: a cada 1 a 6 horas enquanto houver fila.
- Volume: pequeno e com rate limit.
- Saida: leads `enriched`, `qualified`, `discarded` ou `blocked`.
- Registrar falhas de API sem quebrar a rotina.

### Qualificacao

- Frequencia: diaria.
- Saida: score, motivo, proximo passo e status.
- Revisar manualmente leads de alto valor com dados divergentes.

### Higiene do CRM

- Frequencia: semanal.
- Saida: duplicados, leads sem proximo passo, bloqueios antigos e dados vencidos.

### Interacao

- Frequencia: blocos curtos, nao um cron agressivo.
- Saida: interacoes registradas.
- Exigir limites por canal, aprovacao e criterio de parada.

## Critérios de pronto

Uma rodada so esta pronta quando:

- todos os leads possuem fonte;
- duplicados foram tratados;
- CNPJ confirmado, ausente ou marcado como incerto;
- status e score foram definidos;
- proximo passo e guardrail estao claros;
- CRM/ERP foi atualizado;
- erros e bloqueios foram registrados.
