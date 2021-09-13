---
title: Listagens de terceiros
description: Atualize as configurações de listagem de terceiros para determinar se seu catálogo de Comércio importa produtos de suas listagens existentes da Central de Vendas da Amazon.
redirect_from: /sales-channels/asc/ob-third-party-listings.html
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Listagens de terceiros

As configurações de listagem de terceiros fazem parte das configurações da listagem de loja. As configurações de listagem são acessadas no [painel de armazenamento](./amazon-store-dashboard.md).

Essas configurações determinam se seu catálogo [!DNL Commerce] importa produtos de suas listagens [!DNL Amazon Seller Central] existentes. É uma prática recomendada importar listas do Amazon para garantir que todas as listas tenham produtos [!DNL Commerce] correspondentes. Quando suas listagens fazem parte do seu catálogo [!DNL Commerce], você pode gerenciar todos os seus produtos de um único catálogo e usar os recursos do canal de vendas da Amazon. Esses recursos incluem atendimento e gerenciamento de pedidos com o Amazon, reprecificação inteligente e gerenciamento de quantidade.

Quando configurado para importar suas listagens do Amazon, o canal de vendas do Amazon importa suas listagens do Amazon para seu catálogo [!DNL Commerce], tentando vinculá-las aos produtos existentes. Se uma correspondência não for encontrada automaticamente, você pode importar a lista Amazon como um novo [!DNL Commerce] produto ou corresponder manualmente a lista a um produto.

Se você optar por importar suas listagens do Amazon, escolha os atributos [!DNL Commerce] com valores para o SKU do vendedor do Amazon e o Amazon ASIN. Se você não tiver [!DNL Commerce] [atributos do produto](./ob-creating-magento-attributes.md), considere criar e atribuí-los. Mapear esses atributos ajuda a corresponder corretamente as listagens do Amazon importadas aos seus produtos [!DNL Commerce].

A importação da listagem inicial é iniciada quando a [integração de loja](./store-integration.md) é concluída. Depois e com base nas configurações do cron, [!DNL Commerce] verifica continuamente se há listas do Amazon recém-adicionadas (não criadas no Amazon Sales Channel) e atualiza seu catálogo [!DNL Commerce] de acordo com as configurações de listagens de terceiros.

## Definir configurações de listagem de terceiros

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda a seção _[!UICONTROL Third Party Listings]_.

1. Para **[!UICONTROL Import Third Party Listings]** (obrigatório), escolha uma opção:

   - `Import Listing` - (Padrão) Escolha quando deseja que as informações do produto das listas do Amazon sejam importadas para o catálogo de  [!DNL Commerce] produtos. Essa opção é o padrão e é recomendada.

   - `Do Not Import Listing` - Escolha quando deseja  [criar e atribuir manualmente novos produtos](https://docs.magento.com/user-guide/catalog/products.html){:target=&quot;_blank&quot;} ao seu  [!DNL Commerce] catálogo para suas listagens do Amazon.
   >[!NOTE]
   >Os campos de opções a seguir só estão ativos quando definidos como `Import Listing`.

1. Para **[!UICONTROL Attribute That Contains Amazon Seller SKU]**, escolha o atributo [!DNL Commerce] que corresponda ao valor do SKU do vendedor de Amazon.

1. Para **[!UICONTROL Attribute That Contains Amazon ASIN]**, escolha o atributo [!DNL Commerce] que você criou e corresponda ao Amazon ASIN.

   >[!NOTE]
   >Se não tiver criado esses atributos [!DNL Commerce] para suas listagens do Amazon, consulte [Criação de atributos para o Amazon Matching](./ob-creating-magento-attributes.md).

1. Quando terminar, clique em **[!UICONTROL Save listing settings]**.

![Listagens de terceiros](assets/amazon-third-party-listings.png)

| Campo | Descrição |
|---|---|
| [!UICONTROL Import Third Party Listings] | Obrigatório. Opções:<ul><li>**[!UICONTROL Import Listing]** - (Padrão) Escolha quando deseja que as informações do produto das listas do Amazon sejam importadas para o catálogo de  [!DNL Commerce] produtos. </li><li>**[!UICONTROL Do Not Import Listing]** - Escolha quando deseja  [criar e atribuir manualmente novos produtos](https://docs.magento.com/user-guide/catalog/products.html){:target=&quot;_blank&quot;} ao seu  [!DNL Commerce] catálogo para suas listagens do Amazon.</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | Ativa somente quando definido como `Import Listing`.<br>Escolha o  [!DNL Commerce] atributo como uma correspondência com o atributo do Amazon para o SKU do vendedor de Amazon. Se esse atributo não existir, consulte [Criação de atributos de produto do Amazon para a Correspondência do Amazon](./ob-creating-magento-attributes.md). Se necessário, revise os [!DNL Commerce] [atributos](./managing-attributes.md) e crie ou edite um atributo para corresponder a esses dados do Amazon. |
| [!UICONTROL Attribute That Contains Amazon ASIN] | Ativa somente quando definido como `Import Listing`.<br>Escolha o  [!DNL Commerce] atributo que corresponde ao atributo do Amazon para o ASIN do Amazon. Se esse atributo não existir, consulte [Criação de atributos de produto do Amazon para a Correspondência do Amazon](./ob-creating-magento-attributes.md). Se necessário, revise os [!DNL Commerce] [atributos](./managing-attributes.md) e crie ou edite um atributo para corresponder a esses dados do Amazon. |

**Acesso rápido**  -  [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
