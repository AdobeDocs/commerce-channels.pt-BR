---
title: Configurações de loja padrão para listagens do Amazon
description: Modifique as configurações padrão do Commerce para personalizar o Sales Channel do Amazon para sua loja.
role: Admin
feature: Sales Channels, Integration, Configuration
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Configurações de loja padrão para listagens do Amazon

Depois que o armazenamento for conectado e você configurar sua primeira regra de listagem, a sincronização de dados entre o Amazon e o [!DNL Commerce] será iniciada. Há vários tipos de configurações de loja que permitem personalizar a loja de acordo com suas necessidades. As configurações de armazenamento são acessadas no [painel](./amazon-store-dashboard.md) do armazenamento.

As configurações de armazenamento incluem:

- [**[!UICONTROL Listing settings]**](./listing-settings.md) - Controlar como o catálogo de produtos interage com o [!DNL Amazon Marketplace].

- [**[!UICONTROL Order settings]**](./order-settings.md) - Controlar como os pedidos da Amazon são gerenciados.

- [**[!UICONTROL Listing rules]**](./listing-rules.md) - Defina quais produtos de catálogo estão qualificados para serem listados no Amazon.

- [**[!UICONTROL Pricing rules]**](./pricing-products.md) - Defina como o preço de lista do Amazon é alterado para as listagens qualificadas.

- **[!UICONTROL Store reports]** - [Análise de preço competitiva](./competitive-price-analysis.md) e [melhorias na listagem](./listing-improvements.md).

- **[!UICONTROL Logs]** - [Listando alterações](./listing-changes-log.md) e [erros de comunicação](./communication-errors-log.md).

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md) - Revise as configurações de email e nome do armazenamento do canal de vendas da Amazon no Administrador [!DNL Commerce].

## Algumas configurações padrão importantes

| Configuração | Padrão | Descrição | Localização |
|----------------------------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [!UICONTROL Import Amazon Orders] | `Enabled` | Cria pedidos [!DNL Commerce] correspondentes quando novos pedidos são recebidos da Amazon, permitindo que os pedidos sejam gerenciados no fluxo de trabalho [[!DNL Commerce] Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html). Quando `Disabled`, a Amazon solicita a importação de informações de pedidos para revisão, mas os pedidos devem ser gerenciados na sua conta [!DNL Amazon Seller Central]. | [Configurações do pedido](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | Os dados do cliente de pedidos da Amazon não são importados para o banco de dados do [!DNL Commerce]. Os pedidos Amazon importados são processados como check-out de convidado. Se você quiser criar o banco de dados de cliente do [!DNL Commerce], altere esta configuração para `Build New Customer Account`. | [Configurações do pedido](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] produtos de catálogo (que atendem aos requisitos de qualificação da Amazon) para publicar automaticamente no Amazon e criar Listagens do Amazon. Se quiser revisar e publicar manualmente seus produtos, altere essa configuração para `Do Not Automatically List Eligible Products`. Os produtos aguardando publicação manual aparecem na guia [_Pronto para Listar_](./ready-to-list.md). | [Ações de Listagem de Produtos](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | Define o atributo de origem de preço usado como a base para suas listagens do Amazon. Se você não quiser usar o atributo [!DNL Commerce] `Price` como o preço base no qual suas regras de preço se baseiam, deverá alterar essa configuração para um atributo diferente. | [Preço de Listagem](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | O comerciante atende a todas as ordens. Se você usar Abastecimento por Amazon ou uma combinação de métodos de preenchimento, deverá alterar essa configuração. | [Atendido por](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | Se todos os seus produtos estiverem na mesma condição, você poderá selecionar uma das opções de condição do Amazon para representar todos os seus produtos. Se o catálogo contiver produtos em condições diferentes (como Novo, Usado e Recondicionado), você deverá alterar essa configuração para `Assign Condition Using Product Attribute` e mapear seus atributos de condição do [!DNL Commerce] para as condições da sua lista de Amazon. | [Condição de listagem de produtos](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | nenhum | Defina as regras usadas para determinar quais produtos o canal de vendas do Amazon publica para o Amazon. Essas regras fornecem muitas opções para criar regras simples a complexas para incluir ou excluir produtos como listas. | [Regras de Listagem](./listing-rules.md) |
| Regras de preços | nenhum | Defina seu atributo de preço de lista do Amazon diferente do _[!UICONTROL Magento Price Source]_definido em seu [Preço de lista](./listing-price.md). Para ajustar o preço de sua lista (para cima ou para baixo) em relação à sua configuração do_[!UICONTROL Magento Price Source]_, crie regras. | [Regras de preços](./pricing-products.md) |

Para obter mais informações, consulte [Configurações da loja](./ob-store-review.md).
