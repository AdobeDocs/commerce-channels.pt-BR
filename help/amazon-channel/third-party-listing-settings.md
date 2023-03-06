---
title: Listagens de terceiros
description: Atualize as configurações da lista de terceiros para determinar se o catálogo do Commerce importa produtos das listas existentes da Central de vendas da Amazon.
redirect_from: /sales-channels/asc/ob-third-party-listings.html
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# Listagens de terceiros

As configurações de listagem de terceiros fazem parte das configurações de listagem de lojas. As configurações de listagem são acessadas no [painel de armazenamento](./amazon-store-dashboard.md).

Essas configurações determinam se o [!DNL Commerce] o catálogo importa produtos do seu existente [!DNL Amazon Seller Central] listagens. É uma prática recomendada importar listas do Amazon para garantir que todas as listas tenham listas correspondentes [!DNL Commerce] produtos. Quando as listagens fazem parte do seu [!DNL Commerce] catálogo, você pode gerenciar todos os seus produtos em um único catálogo e usar os recursos do canal de vendas da Amazon. Esses recursos incluem gerenciamento de atendimento e pedido com o Amazon, reavaliação inteligente de preços e gerenciamento de quantidade.

Quando configurado para importar suas listas do Amazon, o canal de vendas do Amazon importa suas listas do Amazon para o [!DNL Commerce] catálogo, tentando correspondê-los aos produtos existentes. Se uma correspondência não for encontrada automaticamente, você poderá importar a lista do Amazon como uma nova [!DNL Commerce] produto ou corresponder manualmente a lista a um produto.

Se você optar por importar suas listagens do Amazon, escolha a [!DNL Commerce] atributos com valores para o Amazon Seller SKU e o Amazon ASIN. Se você não tiver [!DNL Commerce] [atributos do produto](./ob-creating-magento-attributes.md), considere criá-los e atribuí-los. O mapeamento desses atributos ajuda a corresponder corretamente as listagens do Amazon importadas ao seu [!DNL Commerce] produtos.

A importação de listagem inicial começa quando [integração de loja](./store-integration.md) está concluído. Depois, e com base nas configurações de cron, [!DNL Commerce] O verifica continuamente se há listagens do Amazon adicionadas recentemente (não criadas no Amazon Sales Channel) e atualiza o [!DNL Commerce] catálogo de acordo com suas configurações de listagens de terceiros.

## Definir configurações da lista de terceiros

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda a _[!UICONTROL Third Party Listings]_seção.

1. Para **[!UICONTROL Import Third Party Listings]** (obrigatório), escolha uma opção:

   - `Import Listing` - (Padrão) Escolha quando deseja que as informações do produto das suas listas do Amazon sejam importadas para o [!DNL Commerce] catálogo de produtos. Essa opção é a padrão e é recomendada.

   - `Do Not Import Listing` - Escolha quando deseja fazer isso manualmente [criar e atribuir novos produtos](https://docs.magento.com/user-guide/catalog/products.html){target="_blank"} ao seu [!DNL Commerce] catálogo para suas listagens do Amazon.
   >[!NOTE]
   >Os campos de opções a seguir só estarão ativos quando definidos como `Import Listing`.

1. Para **[!UICONTROL Attribute That Contains Amazon Seller SKU]**, escolha o [!DNL Commerce] atributo que corresponde ao valor da SKU do vendedor da Amazon.

1. Para **[!UICONTROL Attribute That Contains Amazon ASIN]**, escolha o [!DNL Commerce] que você criou e faça a correspondência dele com o Amazon ASIN.

   >[!NOTE]
   >Se você não criou esses [!DNL Commerce] atributos para suas listagens do Amazon, consulte [Criação de atributos para correspondência do Amazon](./ob-creating-magento-attributes.md).

1. Quando terminar, clique em **[!UICONTROL Save listing settings]**.

![Listagens de terceiros](assets/amazon-third-party-listings.png)

| Campo | Descrição |
|---|---|
| [!UICONTROL Import Third Party Listings] | Obrigatório. Opções:<ul><li>**[!UICONTROL Import Listing]** - (Padrão) Escolha quando deseja que as informações do produto das suas listas do Amazon sejam importadas para o [!DNL Commerce] catálogo de produtos. </li><li>**[!UICONTROL Do Not Import Listing]** - Escolha quando deseja fazer isso manualmente [criar e atribuir novos produtos](https://docs.magento.com/user-guide/catalog/products.html){target="_blank"} ao seu [!DNL Commerce] catálogo para suas listagens do Amazon.</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | Ativo somente quando definido como `Import Listing`.<br>Escolha o [!DNL Commerce] como uma correspondência ao atributo Amazon do SKU do vendedor da Amazon. Se este atributo não existir, consulte [Criação de atributos de produto do Amazon para correspondência do Amazon](./ob-creating-magento-attributes.md). Se necessário, revise [!DNL Commerce] [atributos](./managing-attributes.md) e criar ou editar um atributo para corresponder a esses dados do Amazon. |
| [!UICONTROL Attribute That Contains Amazon ASIN] | Ativo somente quando definido como `Import Listing`.<br>Escolha o [!DNL Commerce] que corresponde ao atributo Amazon para o Amazon ASIN. Se este atributo não existir, consulte [Criação de atributos de produto do Amazon para correspondência do Amazon](./ob-creating-magento-attributes.md). Se necessário, revise [!DNL Commerce] [atributos](./managing-attributes.md) e criar ou editar um atributo para corresponder a esses dados do Amazon. |

**Acesso rápido** - [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
