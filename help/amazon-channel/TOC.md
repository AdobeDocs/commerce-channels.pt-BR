---
user-guide-title: Guia do usuário do Amazon Sales Channel
user-guide-description: Gere vendas por meio da Amazon, integrando o Adobe Commerce ou o Magento Open Source com seu [!DNL Amazon Seller Central] conta.
breadcrumb-title: Canal de vendas da Amazon
source-git-commit: 193f7bfc0c2373f9a79f9cdb7d01877971f31083
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---


# Canal de vendas da Amazon - [!DNL channel manager] para Adobe Commerce {#amazon}

- [Visão geral do guia](guide-overview.md)
- [Introdução ao canal de vendas da Amazon](overview.md)
- [Notas de versão](release-notes.md)
- Introdução {#getting-started}
   - [Sobre o canal de vendas da Amazon](about-amazon-sales-channel.md)
   - [Sobre o Amazon Marketplace](about-amazon-marketplace.md)
   - [Sobre o Amazon e seu catálogo de comércio](about-listings-and-catalog.md)
   - [Práticas recomendadas e limitações](amazon-best-practices.md)
   - [Instalar a extensão](install.md)
- Integração {#onboarding}
   - [Canal de vendas integrado da Amazon](amazon-onboarding-home.md)
   - [Tarefas de pré-configuração](amazon-pre-setup-tasks.md)
   - [Criar [!DNL Commerce] atributos para Amazon](ob-creating-magento-attributes.md)
   - [Verificar a chave da API do Amazon](amazon-verify-api-key.md)
   - [Integração de loja](store-integration.md)
   - [Criar regra de listagem](ob-create-listing-rule.md)
   - [Configurações de armazenamento padrão](default-store-settings.md)
- Gerenciar o canal de vendas {#manage}
   - [Página inicial](amazon-sales-channel-home.md)
   - [Lojas Amazon](managing-stores.md)
   - [Controles do Workspace](workspace-controls.md)
   - [Aprendizagem e preparação](learning-preparation.md)
   - Atributos {#attributes}
      - [Exibir atributos](attributes-view.md)
      - [Gerenciar atributos](managing-attributes.md)
      - [Criar e editar atributos](creating-attributes.md)
      - [Exibir mapeamento de atributo](amazon-matching-attributes-values.md)
   - [Configurações de administrador do canal de vendas](sales-channel-settings.md)
   - [Painel da loja da Amazon](amazon-store-dashboard.md)
   - [Configurações de armazenamento](ob-store-review.md)
- Configurações de listagem {#listing-settings}
   - [Exibir configurações de listagem](listing-settings.md)
   - [Ações de listagem de produtos](product-listing-actions.md)
   - [Listagens de terceiros](third-party-listing-settings.md)
   - [Preço de cotação](listing-price.md)
   - [(B2B) fixação de preços para as empresas](business-pricing.md)
   - [Existências/quantidade](stock-quantity.md)
   - [Cumprido por](fulfilled-by.md)
   - [Pesquisa no catálogo](catalog-search.md)
   - [Condição de listagem do produto](product-listing-condition.md)
   - [Produtos renovados](renewed-products.md)
- [Configurações da ordem](order-settings.md)
- [Configurações de integração da loja](store-integration-settings.md)
- Regras de listagem e preços {#rules}
   - [Regras de listagem](listing-rules.md)
   - Regras de preços {#pricing-rules}
      - [Gerenciar preços](pricing-products.md)
      - [Adicionar nova regra de preços](add-pricing-rule.md)
      - [Configurações gerais da regra de preço](pricing-rule-general-settings.md)
      - [Condições das regras de preço](pricing-rule-conditions.md)
      - [Ações da regra de preço](pricing-rule-actions.md)
      - [Regra de preço padrão](standard-price-rules.md)
      - [Regra de reprecificação inteligente](intelligent-repricing-rules.md)
      - [Variações condicionais do concorrente](competitor-conditional-variances.md)
      - [Ajuste de preço](price-adjustment.md)
      - [Preço mínimo](floor-price.md)
      - [Preço limite máximo opcional](optional-ceiling-price.md)
      - [Âmbito do preço](price-scope.md)
      - [Lógica de prioridade de preço](price-priority-logic.md)
      - [Preços da concorrência Buy Box](buy-box-competitor-pricing.md)
      - [Preços mais baixos do concorrente](lowest-competitor-pricing.md)
   - Exemplos {#rules-examples}
      - [Definir uma condição](ob-define-condition-example.md)
      - [Exemplos de regras de preço](price-rule-examples.md)
- Relatórios e logs {#reports-logs}
   - [Registra e armazena relatórios](amazon-logs-reports.md)
   - Armazenar relatórios {#store-reports}
      - [Análise de preços competitiva](competitive-price-analysis.md)
      - [Melhorias na listagem](listing-improvements.md)
   - Logs {#logs}
      - [Log de alterações de listagem](listing-changes-log.md)
      - [Log de erros de comunicação](communication-errors-log.md)
- Gerenciar listas {#admin-listings}
   - [Gerenciar listas do Amazon](managing-product-listings.md)
   - Por status/guia {#status-tab}
      - [Gerenciar por status/guia](managing-listings-by-tab.md)
      - [Listas incompletas](incomplete-listings.md)
      - [Novas listagens de terceiros](new-third-party-listings.md)
      - [Pronto para listar](ready-to-list.md)
      - [Listas inativas](inactive-listings.md)
      - [Listas ativas](active-listings.md)
      - [Substituições](overrides.md)
      - [Listas não elegíveis](ineligible-listings.md)
      - [Listas adicionadas](ended-listings.md)
   - Por ações {#actions}
      - [Gerenciar por ações](managing-listings-by-action.md)
      - [Criar e atribuir produtos de catálogo](creating-assigning-catalog-products.md)
      - [Criar e editar substituições](creating-editing-overrides.md)
      - [Criar um SKU de vendedor de alias](create-alias-seller-sku.md)
      - [Editar uma ASIN atribuída](edit-assigned-asin.md)
      - [Encerrar uma listagem da Amazon](end-listings-manually.md)
      - [Publicar uma lista do Amazon](publish-listings-manually.md)
      - [Atualizar informações necessárias](amazon-manually-update-incomplete-listing.md)
      - [Exibir detalhes](product-listing-details.md)
- Gerenciar pedidos {#admin-orders}
   - [Gerenciar pedidos](managing-orders.md)
   - [Exibir pedidos do Amazon](amazon-orders-all.md)
   - [Exibir detalhes do pedido da Amazon](amazon-order-details.md)
   - [Tarefas comuns de processamento de pedidos](common-order-processing.md)
   - [Fluxos de trabalho de preenchimento](fulfillment-workflows.md)
   - [Cancelar ordens não entregues](cancel-unshipped-order.md)
