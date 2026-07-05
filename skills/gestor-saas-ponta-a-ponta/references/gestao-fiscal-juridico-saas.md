# Referencia Operacional: Fiscal, Juridico, 5S, RH, Financeiro e PO para SaaS BR

## Tributario/Fiscal

Fontes verificadas em 2026-06-18:

- Portal do Simples Nacional/gov.br: regras, anexos, fator R e resolucoes vigentes devem ser consultados antes de definir regime/anexo.
- CONCLA/IBGE: usar para confirmar descricoes oficiais de CNAE, incluindo 6203-1/00, 6202-3/00, 6201-5/01, 6204-0/00, 6209-1/00 e 6311-9/00.
- Prefeitura do municipio emissor: confirmar codigo de servico, ISS, exigibilidade e descricao da NFS-e.

Matriz inicial:

- 6203-1/00: software nao-customizavel/licenciamento/produto padronizado. Candidato comum para SaaS, validar municipio e contador.
- 6202-3/00: software customizavel/licenciamento com customizacao.
- 6201-5/01: desenvolvimento sob encomenda.
- 6204-0/00: consultoria TI.
- 6209-1/00: suporte tecnico/manutencao/outros servicos TI.
- 6311-9/00: tratamento de dados, aplicacao hospedada, hospedagem. Usar com cautela conforme entrega real.

Fator R:

- Fator R = folha/pro-labore/encargos dos ultimos 12 meses / receita bruta dos ultimos 12 meses.
- Referencia operacional: se >= 28%, simular Anexo III quando atividade permitir; se < 28%, simular Anexo V para atividades sujeitas ao fator R.
- Sempre calcular aliquota efetiva pela receita bruta acumulada e tabela vigente.

## Juridico e LGPD

Fontes: Lei 13.709/2018 no Planalto, ANPD/gov.br.

Checklist SaaS:

- Termos de uso/contrato.
- Politica de privacidade.
- DPA/controlador-operador quando aplicavel.
- Registro de bases legais.
- Processo para direitos de titulares.
- Plano de resposta a incidente.
- Contratos com fornecedores e prestadores.

## RH

Fontes: eSocial/gov.br para obrigacoes trabalhistas; boas praticas de gestao por scorecard, onboarding e RACI.

Rotina:

- Scorecard de vaga.
- Onboarding 30/60/90.
- 1:1.
- Avaliacao por output.
- RACI.
- Checklist de desligamento e acessos.

## 5S

Fonte: Sebrae e literatura de qualidade/lean.

Aplicar 5S em CRM, financeiro, documentos, acessos, repositorios, backlog, suporte e criativos:

- Seiri: remover excessos.
- Seiton: ordenar e nomear.
- Seiso: limpar dados e processos.
- Seiketsu: padronizar.
- Shitsuke: disciplinar e auditar.

## Product Owner

Usar roadmap por outcome, RICE adaptado, criterios de aceite, tracking e validacao por evidencias reais: entrevistas, uso, tickets, churn e vendas perdidas.
