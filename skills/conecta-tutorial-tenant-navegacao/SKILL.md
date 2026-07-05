---
name: "conecta-tutorial-tenant-navegacao"
description: "Tutorial painel tenant Conecta."
---

# Conecta Tutorial Tenant Navegacao

Use quando precisar demonstrar, gravar, revisar ou explicar o fluxo de empresa tenant cliente assinante do Conecta Clube: cadastro no checkout, onboarding modular, dashboard, configuracao inicial, catalogo, cliente, produto, recompensa, pontos e integracoes.

## Guardrails

- Usar dados ficticios/teste quando criar tenant, cliente, produto ou recompensa.
- Nao autenticar ERP, gateway, WhatsApp, Instagram, Facebook ou marketplace real durante tutorial basico.
- Nao mostrar senhas em video ou resposta.
- Se precisar reutilizar um tenant de teste, ler a credencial em arquivo de secrets fora da memoria comum e nunca publicar esse caminho ou conteudo.
- Para pagamento, deixar claro que o checkout abre no Asaas; em simulacao, voltar ao Conecta sem pagar.
- Nao prometer conectores externos que nao aparecem no painel. No fluxo observado, "e-commerce" pratico e o Catalogo digital; gateway ativo e Asaas; ERP ativo e Bling.

## Fluxo De Cadastro E Onboarding

1. Acessar `https://www.conectaclube.app.br`; confirmar redirecionamento para `https://conectaclube.app.br`.
2. Ir em Planos e escolher Performance, ou abrir `/checkout?plan=performance&interval=monthly`.
3. Preencher cadastro publico:
   - Responsavel
   - Empresa
   - Nome fantasia
   - Email
   - Senha
   - WhatsApp
   - CPF/CNPJ opcional
4. Criar conta e ir ao checkout.
5. Ao cair no Asaas, nao pagar em simulacao; voltar para `https://conectaclube.app.br/login`.
6. Entrar com a conta criada se necessario.
7. Concluir onboarding modular:
   - Etapa 1 ERP: selecionar Bling.
   - Etapa 2 Pagamentos: selecionar Asaas.
   - Etapa 3 Mensageria/redes: selecionar WhatsApp API Oficial.
   - Etapa 4 Recursos: selecionar Catalogo digital.
   - Etapa 5 Preparar ambiente: revisar e clicar `Instalar e iniciar operacao`.

## Dashboard Apos Onboarding

No dashboard, mostrar:

- Atalhos operacionais: Novo cliente, Dar pontos, Registrar beneficio usado, Catalogo, Campanha, Relatorios.
- Cadastro publico com link e QR Code.
- Checklist `Comece em 4 passos`.
- Cards: clientes cadastrados, clientes que voltaram, pontos em circulacao, risco em beneficios.
- Mini visao operacional.

## Menu Lateral

Operacao essencial:

- Dashboard da loja
- Clientes
- Dar pontos ao cliente
- Trocas de beneficios
- Atendimento WhatsApp
- Relatorios simples

Marketing:

- Catalogo
- Cupons
- WhatsApp / Campanhas
- Recompensas

Vendas e beneficios:

- Gestao de pedidos
- Produtos
- Ranking de clientes
- Controle de clientes e vendas
- Indicadores avancados

Loja de integracoes:

- Explorar integracoes

Configuracoes:

- Usuarios
- Assinatura
- Formas de Pagamento
- Paginas de Politica
- Programa de pontos
- Capacitacao
- Integracoes ERP
- API e Webhooks
- Ajuda

## Setup Minimo Para Tutorial

Programa de pontos:

1. Caminho: Configuracoes > Programa de pontos.
2. Configurar regra simples:
   - 1 ponto por R$ 1 gasto.
   - 1 ponto vale R$ 0,03.
   - Bonus de cadastro: 10 pontos.
3. Salvar configuracoes.
4. Explicar como isso equivale a cashback/recompra com controle de margem.

Recompensa:

1. Caminho: Marketing > Recompensas.
2. Criar uma recompensa simples:
   - Titulo: R$ 10 de desconto no proximo pedido.
   - Criterio: Presenca.
   - Meta: 1 visita.
   - Pontos necessarios: 300.
   - Custo: R$ 10,00.
   - Valor de referencia: R$ 10,00.
   - Status: ativo.
3. Confirmar que aparece na tabela.

Catalogo:

1. Caminho: Marketing > Catalogo.
2. Ativar `Catalogo online ativo`.
3. Preencher slug, titulo, descricao, email central e WhatsApp.
4. Salvar.
5. Confirmar URL publica gerada.
6. Evitar dominio personalizado no tutorial basico.

Produto:

1. Caminho: Vendas e beneficios > Produtos, ou Catalogo > Revisar produtos.
2. Criar produto teste:
   - SKU: COMBO-SMASH-TUT.
   - Titulo: Combo Smash Burger Tutorial.
   - Descricao: produto teste para tutorial.
   - Custo: R$ 18,00.
   - Preco: R$ 39,90.
   - Pontos: 500.
   - Catalogo: ativo.
   - Resgate: permitido.
   - Estoque: nao controlado.
3. Confirmar que aparece na tabela.

Cliente:

1. Caminho: Operacao essencial > Clientes ou Dashboard > Cadastrar cliente agora.
2. Criar cliente ficticio com nome, CPF valido de teste, telefone e email.
3. Manter opt-in de campanhas se o objetivo for demonstrar CRM/campanhas.
4. Confirmar que o cliente aparece na lista e recebeu bonus de cadastro.

Pontos:

1. Caminho: Operacao essencial > Dar pontos ao cliente.
2. Buscar cliente por CPF.
3. Selecionar tipo de pontuacao.
4. Emitir pontos.
5. Voltar ao dashboard e confirmar pontos em circulacao/risco em beneficios.

## Loja De Integracoes

Caminho: Loja de integracoes > Explorar integracoes.

Durante tutorial basico, mostrar sem autenticar:

- Ativos: Catalogo digital, Asaas, WhatsApp API Oficial, Bling ERP.
- Inclusos/visiveis: Entregas, SMTP, Indique e Ganhe, Palpite Certo, SLA Atendimento, Instagram, Facebook, Tiny ERP.
- Contratacao/upgrade: Midia Indoor, Sorteios, Mercado Pago, Pagar.me, InfinitePay, Getnet.

## Roteiro De Gravacao Recomendado

Sessao 1: Cadastro e onboarding.
Sessao 2: Dashboard e setup minimo.
Sessao 3: Loja de integracoes e links publicos.

Para video curto, gravar por sessoes do menu em vez de um take unico longo.

## Observacoes Aprendidas

- Recompensas ficam em Marketing, nao em Vendas e beneficios.
- Produtos ficam em Vendas e beneficios.
- Catalogo fica em Marketing.
- Programa de pontos fica em Configuracoes.
- O dashboard e os atalhos sao o melhor caminho narrativo para lojista novo.
- Algumas rotas diretas podem voltar ao dashboard dependendo do estado; preferir menu lateral/atalhos durante gravacao.
