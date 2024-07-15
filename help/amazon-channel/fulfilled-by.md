---
title: Configurações de Preenchido por para listagens do Amazon
description: Use as configurações Atendido por para determinar como as ordens das listagens do Amazon são atendidas (entregues).
feature: Sales Channels, Products
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Configurações de Preenchido por para listagens do Amazon

As configurações de _[!UICONTROL Fulfilled By]_fazem parte das configurações da lista de lojas. As configurações de listagem são acessadas no [painel de armazenamento](./amazon-store-dashboard.md).

Essas configurações definem a parte que atende (ou envia) as ordens. Se todos os seus pedidos forem atendidos usando um método, escolha entre comerciante (você) ou Amazon. Se você planeja atender pedidos de seus locais e usar o Amazon, é uma prática recomendada usar a terceira opção e configurar um atributo de produto [!DNL Commerce].

- **[!UICONTROL Fulfilled by Merchant]** - Escolha se você, o comerciante, atende a todos os pedidos. Quando um pedido é feito, o estoque é deduzido do catálogo [!DNL Commerce].

- **[!UICONTROL Fulfilled by Amazon]** - Escolha se a Amazon atende a todos os pedidos. Com esta opção, o estoque de produtos não é deduzido do catálogo [!DNL Commerce] quando um pedido é feito. O estoque de estoque para ordens preenchidas Amazon é armazenado e deduzido de seus depósitos. Antes de atribuir esta opção, você deve verificar em sua conta do [!DNL Amazon Seller Central] se seus produtos estão qualificados para o preenchimento do _Fulfilled By Amazon_ (FBA). O inventário FBA é gerenciado diretamente por meio da conta [!DNL Amazon Seller Central]. Com esse método de preenchimento, o canal de vendas da Amazon não compartilha atualizações de quantidade entre [!DNL Commerce] e a Amazon. Portanto, nem todas as ferramentas de marketing descritas em Configurações de quantidade estão disponíveis no canal de vendas do Amazon.

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Se os produtos podem ser preenchidos por você e pela Amazon, é possível criar um atributo de produto [!DNL Commerce] com valores para Preenchido pelo comerciante e Preenchido pela Amazon. Definir esse valor por produto indica quem atende aos pedidos.

O método de preenchimento é um atributo regional e se baseia na configuração **[!UICONTROL Amazon Marketplace Country]** definida durante a [integração de armazenamento](./store-integration.md). Quando uma alteração é feita, ela afeta todas as listagens do Amazon que compartilham esse [!DNL Amazon Seller SKU] nas lojas Amazon que vendem na mesma região (como definido em _[!UICONTROL Amazon Marketplace Country]_durante a [integração de lojas](./store-integration.md)). Uma alteração em um [!DNL Amazon Seller SKU] compartilhado nos Estados Unidos não afeta suas lojas Amazon definidas para uma região diferente (conforme definido durante a integração da loja).

>[!NOTE]
>
>Quando um pedido é preenchido pelo Amazon (FBA) e é importado, você pode ver dados fictícios de alguns campos nos detalhes do pedido. Consulte [Detalhes do Pedido Amazon](./amazon-order-details.md).

## Definir as configurações de [!UICONTROL Fulfilled By] {#configure-fulfilled-by-settings}

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda a seção _[!UICONTROL Fulfilled By]_.

1. Para **[!UICONTROL Product Fulfilled By]**, escolha quem preenche (envia) o pedido:

   - `Fulfilled by Merchant` - O comerciante atende ao pedido.

   - `Fulfilled by Amazon` - O depósito do Amazon atende à ordem.

   - `Assign Fulfilled By Using Magento Product Attribute` - Um atributo [!DNL Commerce] indica quem atende ao pedido por produto.

     Se for escolhido, escolha o atributo [!DNL Commerce] que deseja mapear em **[!UICONTROL Fulfilled by Attribute]**.

1. Quando terminar, clique em **[!UICONTROL Save listing settings]**.

![Configurações de Preenchido por](assets/amazon-fulfilled-by.png){width="500" zoomable="yes"}

| Campo | Descrição |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product Fulfilled By] | Opções:<ul><li>**[!UICONTROL Fulfilled by Merchant]** - (FBM) Escolha se você atende aos pedidos. Quando um pedido é feito, o estoque é deduzido do catálogo [!DNL Commerce]. Quando um novo produto é criado, o método de preenchimento do Comerciante Atendido é atribuído.</li><li>**[!UICONTROL Fulfilled by Amazon]** - (FBA) Escolha se a Amazon atende aos pedidos. Com esse método de preenchimento, o estoque de produtos não é deduzido do catálogo [!DNL Commerce] quando um pedido é feito. Quando um produto é criado, ele é criado com _[!UICONTROL Fulfilled by Amazon (FBA)]_como o tipo de preenchimento. Verifique se seus produtos estão qualificados para o preenchimento FBA na conta do [!DNL Amazon Seller Central]. O inventário FBA também é gerenciado diretamente por meio da conta [!DNL Amazon Seller Central]. Com esse método de preenchimento, as atualizações de quantidade não são enviadas em relação ao catálogo [!DNL Commerce], portanto, você não pode usar algumas das ferramentas de marketing descritas em [Configurações de estoque/quantidade](./stock-quantity.md).</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Escolha se você tem um atributo [!DNL Commerce] existente que determina se ele é preenchido pelo comerciante ou preenchido pela Amazon. Quando escolhido, **[!UICONTROL Fulfilled by Attribute]** habilita.</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | Escolha o atributo [!DNL Commerce] usado para determinar o método de preenchimento.<br><br>Por exemplo, se o atributo for _Atendido por_ e você escolher o valor do atributo como `Fulfilled By Merchant` ou `Fulfilled By Amazon (FBA)`, o sistema usará esse valor como o tipo de preenchimento para um novo produto. Como comerciante, você deve garantir que seus produtos sejam qualificados para o preenchimento do FBA na conta do [!DNL Amazon Seller Central]. O inventário FBA também é gerenciado diretamente por meio de sua conta de vendedor da Amazon.<br><br>As opções dependem dos atributos configurados para seus produtos Amazon. |

**Acesso rápido** - [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
