---
title: Listagens de terceiros
description: Atualize as configurações de listagem de terceiros para determinar se seu catálogo de Comércio importa produtos de suas listagens existentes da Central de Vendas da Amazon.
redirect_from: /sales-channels/asc/ob-third-party-listings.html
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Listagens de terceiros

As configurações de listagem de terceiros fazem parte das configurações da listagem de loja. As configurações de listagem são acessadas do [painel de loja](./amazon-store-dashboard.md).

Essas configurações determinam se a [!DNL Commerce] o catálogo importa produtos de seu [!DNL Amazon Seller Central] listagens. É uma prática recomendada importar listas do Amazon para garantir que todas as listas tenham correspondência [!DNL Commerce] produtos. Quando as listagens fazem parte de [!DNL Commerce] você pode gerenciar todos os seus produtos de um único catálogo e usar os recursos do canal de vendas da Amazon. Esses recursos incluem atendimento e gerenciamento de pedidos com o Amazon, reprecificação inteligente e gerenciamento de quantidade.

Quando configurado para importar suas listagens do Amazon, o canal de vendas do Amazon importa suas listagens do Amazon para o [!DNL Commerce] catálogo, tentando associá-los a produtos existentes. Se uma correspondência não for encontrada automaticamente, você pode importar a listagem do Amazon como uma nova [!DNL Commerce] ou corresponder manualmente a listagem a um produto.

Se você optar por importar as listagens do Amazon, escolha a variável [!DNL Commerce] atributos com valores para o SKU do vendedor de Amazon e o Amazon ASIN. Se você não tiver [!DNL Commerce] [atributos do produto](./ob-creating-magento-attributes.md), considere criá-los e atribuí-los. O mapeamento desses atributos ajuda a corresponder corretamente as listagens do Amazon importadas ao seu [!DNL Commerce] produtos.

A importação da listagem inicial é iniciada quando [integração de loja](./store-integration.md) for concluído. Depois e com base nas configurações do cron, [!DNL Commerce] verifica continuamente se há listas do Amazon recém-adicionadas (não criadas no Amazon Sales Channel) e atualiza seu [!DNL Commerce] de acordo com suas configurações de listagens de terceiros.

## Definir configurações de listagem de terceiros

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda o _[!UICONTROL Third Party Listings]_seção.

1. Para **[!UICONTROL Import Third Party Listings]** (obrigatório), escolha uma opção:

   - `Import Listing` - (Padrão) Escolha quando deseja que as informações do produto das listagens do Amazon sejam importadas para o seu [!DNL Commerce] catálogo de produtos. Essa opção é o padrão e é recomendada.

   - `Do Not Import Listing` - Escolha quando deseja manualmente [criar e atribuir novos produtos](https://docs.magento.com/user-guide/catalog/products.html){target=&quot;_blank&quot;} para sua [!DNL Commerce] catálogo para suas listagens do Amazon.
   >[!NOTE]
   >Os campos de opções a seguir só estão ativos quando definidos como `Import Listing`.

1. Para **[!UICONTROL Attribute That Contains Amazon Seller SKU]**, escolha o [!DNL Commerce] que corresponde ao valor do SKU do vendedor de Amazon.

1. Para **[!UICONTROL Attribute That Contains Amazon ASIN]**, escolha o [!DNL Commerce] atributo que você criou e corresponda ao Amazon ASIN.

   >[!NOTE]
   >Caso não tenha criado [!DNL Commerce] atributos para suas listagens do Amazon, consulte [Criar atributos para correspondência do Amazon](./ob-creating-magento-attributes.md).

1. Ao concluir, clique em **[!UICONTROL Save listing settings]**.

![Listagens de terceiros](assets/amazon-third-party-listings.png)

| Campo | Descrição |
|---|---|
| [!UICONTROL Import Third Party Listings] | Obrigatório. Opções:<ul><li>**[!UICONTROL Import Listing]** - (Padrão) Escolha quando deseja que as informações do produto das listagens do Amazon sejam importadas para o seu [!DNL Commerce] catálogo de produtos. </li><li>**[!UICONTROL Do Not Import Listing]** - Escolha quando deseja manualmente [criar e atribuir novos produtos](https://docs.magento.com/user-guide/catalog/products.html){target=&quot;_blank&quot;} para sua [!DNL Commerce] catálogo para suas listagens do Amazon.</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | Somente ativo quando definido como `Import Listing`.<br>Escolha a [!DNL Commerce] como uma correspondência ao atributo Amazon para o SKU do vendedor do Amazon. Se esse atributo não existir, consulte [Criação de atributos de produto do Amazon para correspondência do Amazon](./ob-creating-magento-attributes.md). Se necessário, revise [!DNL Commerce] [atributos](./managing-attributes.md) e crie ou edite um atributo para corresponder a esses dados do Amazon. |
| [!UICONTROL Attribute That Contains Amazon ASIN] | Somente ativo quando definido como `Import Listing`.<br>Escolha a [!DNL Commerce] que corresponde ao atributo Amazon para o ASIN do Amazon. Se esse atributo não existir, consulte [Criação de atributos de produto do Amazon para correspondência do Amazon](./ob-creating-magento-attributes.md). Se necessário, revise [!DNL Commerce] [atributos](./managing-attributes.md) e crie ou edite um atributo para corresponder a esses dados do Amazon. |

**Acesso rápido** - [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
