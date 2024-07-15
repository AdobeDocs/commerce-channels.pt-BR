---
title: Sales Channel Amazon - [!UICONTROL Third-party Listings]
description: Atualize as configurações da lista de terceiros para determinar se o catálogo do Commerce importa produtos das listas existentes da Central de vendas da Amazon.
feature: Sales Channels, Products
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# [!UICONTROL Third-party Listings]

As configurações de listagem de terceiros fazem parte das configurações de listagem de lojas. As configurações de listagem são acessadas no [painel de armazenamento](./amazon-store-dashboard.md).

Essas configurações determinam se o catálogo do [!DNL Commerce] importa produtos das listagens existentes do [!DNL Amazon Seller Central]. É uma prática recomendada importar listas do Amazon, para garantir que todas as listas tenham produtos [!DNL Commerce] correspondentes. Quando suas listas fazem parte do catálogo do [!DNL Commerce], você pode gerenciar todos os seus produtos de um único catálogo e usar os recursos do canal de vendas da Amazon. Esses recursos incluem gerenciamento de atendimento e pedido com o Amazon, reavaliação inteligente de preços e gerenciamento de quantidade.

Quando configurado para importar suas listagens do Amazon, o canal de vendas do Amazon importa suas listagens do Amazon para o catálogo do [!DNL Commerce], tentando correspondê-las aos produtos existentes. Se uma correspondência não for encontrada automaticamente, você poderá importar a lista do Amazon como um novo produto [!DNL Commerce] ou corresponder manualmente a lista a um produto.

Se você optar por importar suas listagens do Amazon, escolha os atributos [!DNL Commerce] com valores para o SKU do Vendedor da Amazon e o ASIN da Amazon. Se você não tiver [!DNL Commerce] [atributos de produto](./ob-creating-magento-attributes.md), considere criá-los e atribuí-los. O mapeamento desses atributos ajuda a corresponder corretamente as listagens de Amazon importadas aos seus produtos [!DNL Commerce].

A importação inicial da listagem é iniciada quando a [integração de armazenamento](./store-integration.md) é concluída. Depois, com base nas configurações de cron, o [!DNL Commerce] verifica continuamente se há listas do Amazon recém-adicionadas (não criadas no Sales Channel do Amazon) e atualiza o catálogo do [!DNL Commerce] de acordo com as configurações de listas de terceiros.

## Definir configurações da lista de terceiros

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda a seção _[!UICONTROL Third Party Listings]_.

1. Para **[!UICONTROL Import Third Party Listings]** (obrigatório), escolha uma opção:

   - `Import Listing` - (Padrão) Escolha quando deseja que as informações do produto das suas listas do Amazon sejam importadas para o catálogo de produtos [!DNL Commerce]. Essa opção é a padrão e é recomendada.

   - `Do Not Import Listing` - Escolha quando deseja [criar manualmente e atribuir novos produtos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html) ao catálogo [!DNL Commerce] para suas listagens do Amazon.

   >[!NOTE]
   >Os campos de opções a seguir só estão ativos quando definidos como `Import Listing`.

1. Para **[!UICONTROL Attribute That Contains Amazon Seller SKU]**, escolha o atributo [!DNL Commerce] que corresponda ao valor da SKU do Vendedor da Amazon.

1. Para **[!UICONTROL Attribute That Contains Amazon ASIN]**, escolha o atributo [!DNL Commerce] que você criou e faça a correspondência dele com o Amazon ASIN.

   >[!NOTE]
   >Se você não criou esses [!DNL Commerce] atributos para suas listagens do Amazon, consulte [Criação de Atributos para Correspondência do Amazon](./ob-creating-magento-attributes.md).

1. Quando terminar, clique em **[!UICONTROL Save listing settings]**.

![Listagens de terceiros](assets/amazon-third-party-listings.png){width="600" zoomable="yes"}

| Campo | Descrição |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Import Third Party Listings] | Obrigatório. Opções:<ul><li>**[!UICONTROL Import Listing]** - (Padrão) Escolha quando deseja que as informações do produto das suas listas do Amazon sejam importadas para o catálogo de produtos [!DNL Commerce]. </li><li>**[!UICONTROL Do Not Import Listing]** - Escolha quando deseja [criar manualmente e atribuir novos produtos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html) ao catálogo [!DNL Commerce] para suas listagens do Amazon.</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | Ativo somente quando definido como `Import Listing`.<br>Escolha o atributo [!DNL Commerce] como uma correspondência ao atributo Amazon para o SKU do Vendedor da Amazon. Se este atributo não existir, consulte [Criação de atributos de produto do Amazon para correspondência com o Amazon](./ob-creating-magento-attributes.md). Se necessário, revise seus [!DNL Commerce] [atributos](./managing-attributes.md) e crie ou edite um atributo para corresponder a esses dados do Amazon. |
| [!UICONTROL Attribute That Contains Amazon ASIN] | Ativo somente quando definido como `Import Listing`.<br>Escolha o atributo [!DNL Commerce] que corresponda ao atributo Amazon para o Amazon ASIN. Se este atributo não existir, consulte [Criação de atributos de produto do Amazon para correspondência com o Amazon](./ob-creating-magento-attributes.md). Se necessário, revise seus [!DNL Commerce] [atributos](./managing-attributes.md) e crie ou edite um atributo para corresponder a esses dados do Amazon. |

**Acesso rápido** - [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
