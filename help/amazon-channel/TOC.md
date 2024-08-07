---
user-guide-title: Guia do usuário do Amazon Sales Channel
user-guide-description: Gere vendas por meio do Amazon integrando o Adobe Commerce ou o Magento Open Source à sua conta  [!DNL Amazon Seller Central] .
breadcrumb-title: Canal de vendas da Amazon
role: Admin, User
feature: Sales Channels
recommendations: noDisplay
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 4%

---


# Canal de vendas da Amazon - [!DNL channel manager] para Adobe Commerce {#amazon}

- [Guia do usuário do Amazon Sales Channel](guide-overview.md)
- [Introdução ao canal de vendas do Amazon](overview.md)
- Introdução {#getting-started}
   - [Sobre o Amazon Marketplace](about-amazon-marketplace.md)
   - [Amazon e o catálogo do Commerce](about-listings-and-catalog.md)
   - [Práticas recomendadas e limitações](amazon-best-practices.md)
   - [Instalar a extensão](install.md)
- Integração de {#onboarding}
   - [Canal de vendas integrado do Amazon](amazon-onboarding-home.md)
   - [Tarefas de pré-configuração](amazon-pre-setup-tasks.md)
   - [Criar  [!DNL Commerce] atributos para o Amazon](ob-creating-magento-attributes.md)
   - [Verifique a chave da API do Amazon](amazon-verify-api-key.md)
   - [Integração da loja](store-integration.md)
   - [Criar regra de listagem](ob-create-listing-rule.md)
   - [Configurações de loja padrão](default-store-settings.md)
- Gerenciar o canal de vendas {#manage}
   - [Home page](amazon-sales-channel-home.md)
   - [lojas Amazon](managing-stores.md)
   - [Controles do Workspace](workspace-controls.md)
   - [Aprendizagem e preparação](learning-preparation.md)
   - Atributos {#attributes}
      - [Exibir atributos](attributes-view.md)
      - [Gerenciar atributos](managing-attributes.md)
      - [Criar e editar atributos](creating-attributes.md)
      - [Exibir mapeamento de atributo](amazon-matching-attributes-values.md)
   - [Configurações do administrador do canal de vendas](sales-channel-settings.md)
   - [painel de loja da Amazon](amazon-store-dashboard.md)
   - [Configurações da loja](ob-store-review.md)
- Configurações de listagem {#listing-settings}
   - [Exibir configurações de listagem](listing-settings.md)
   - [Ações de lista de produtos](product-listing-actions.md)
   - [Listagens de terceiros](third-party-listing-settings.md)
   - [Preço de tabela](listing-price.md)
   - [Preços comerciais (B2B)](business-pricing.md)
   - [Estoque/quantidade](stock-quantity.md)
   - [Preenchido por](fulfilled-by.md)
   - [Pesquisa no catálogo](catalog-search.md)
   - [Condição de lista de produtos](product-listing-condition.md)
   - [Produtos renovados](renewed-products.md)
- [Configurações do pedido](order-settings.md)
- [Configurações de integração de loja](store-integration-settings.md)
- Listagem e regras de preço {#rules}
   - [Regras de listagem](listing-rules.md)
   - Regras de preços {#pricing-rules}
      - [Gerenciar preços](pricing-products.md)
      - [Adicionar nova regra de preços](add-pricing-rule.md)
      - [Configurações gerais da regra de preço](pricing-rule-general-settings.md)
      - [Condições da regra de preço](pricing-rule-conditions.md)
      - [Ações de regra de preço](pricing-rule-actions.md)
      - [Regra de preço padrão](standard-price-rules.md)
      - [Regra inteligente de reavaliação de preços](intelligent-repricing-rules.md)
      - [Variações condicionais do concorrente](competitor-conditional-variances.md)
      - [Ajuste de preço](price-adjustment.md)
      - [Preço mínimo](floor-price.md)
      - [Preço máximo opcional](optional-ceiling-price.md)
      - [Escopo de preço](price-scope.md)
      - [Lógica de prioridade de preço](price-priority-logic.md)
      - [Preços do concorrente Buy Box](buy-box-competitor-pricing.md)
      - [Menor preço para concorrentes](lowest-competitor-pricing.md)
   - Exemplos {#rules-examples}
      - [Definir uma condição](ob-define-condition-example.md)
      - [Exemplos de regras de preço](price-rule-examples.md)
- Relatórios e logs {#reports-logs}
   - [Registra e armazena relatórios](amazon-logs-reports.md)
   - Armazenar relatórios {#store-reports}
      - [Análise de preço competitiva](competitive-price-analysis.md)
      - [Melhorias na listagem](listing-improvements.md)
   - Logs {#logs}
      - [Log de alterações de listagem](listing-changes-log.md)
      - [Log de erros de comunicação](communication-errors-log.md)
- Gerenciar listas {#admin-listings}
   - [Gerenciar listagens do Amazon](managing-product-listings.md)
   - Por status/guia {#status-tab}
      - [Gerenciar por status/guia](managing-listings-by-tab.md)
      - [Listagens incompletas](incomplete-listings.md)
      - [Novas listagens de terceiros](new-third-party-listings.md)
      - [Pronto para listar](ready-to-list.md)
      - [Listagens inativas](inactive-listings.md)
      - [Listagens ativas](active-listings.md)
      - [Substituições](overrides.md)
      - [Listagens inelegíveis](ineligible-listings.md)
      - [Listagens encerradas](ended-listings.md)
   - Por ações {#actions}
      - [Gerenciar por ações](managing-listings-by-action.md)
      - [Criar e atribuir produtos de catálogo](creating-assigning-catalog-products.md)
      - [Criar e editar sobreposições](creating-editing-overrides.md)
      - [Criar um SKU de Vendedor Alias](create-alias-seller-sku.md)
      - [Editar uma ASIN atribuída](edit-assigned-asin.md)
      - [Encerrar uma lista do Amazon](end-listings-manually.md)
      - [PUBLISH e AMAZON](publish-listings-manually.md)
      - [Atualização das informações necessárias](amazon-manually-update-incomplete-listing.md)
      - [Exibir detalhes](product-listing-details.md)
- Gerenciar pedidos {#admin-orders}
   - [Gerenciar pedidos](managing-orders.md)
   - [Exibir pedidos do Amazon](amazon-orders-all.md)
   - [Exibir detalhes do pedido Amazon](amazon-order-details.md)
   - [Tarefas comuns de processamento de ordens](common-order-processing.md)
   - [Fluxos de trabalho de preenchimento](fulfillment-workflows.md)
   - [Cancelar ordens não entregues](cancel-unshipped-order.md)
- [Notas de versão](release-notes.md)
