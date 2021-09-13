---
title: Preenchido por
description: Use as configurações Preenchido por para determinar como os pedidos das listagens da Amazon são cumpridos (entregues).
redirect_from: /sales-channels/asc/ob-fulfilled-by.html: 
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 0
ht-degree: 0%

---

# Preenchido por

_[!UICONTROL Fulfilled By]_As configurações fazem parte das configurações da listagem de loja. As configurações de listagem são acessadas no [painel de armazenamento](./amazon-store-dashboard.md).

Essas configurações definem a parte que atende (ou envia) as ordens. Se todos os seus pedidos forem realizados usando um método, escolha entre um comerciante (você) ou a Amazon. Se você planeja atender pedidos de suas localizações e usar o Amazon, é uma prática recomendada usar a terceira opção e configurar um atributo de produto [!DNL Commerce].

- **[!UICONTROL Fulfilled by Merchant]** - Escolha se você, o comerciante, atende a todos os pedidos. Quando um pedido é feito, o inventário é deduzido de seu catálogo [!DNL Commerce].

- **[!UICONTROL Fulfilled by Amazon]** - Escolha se a Amazon atende a todos os pedidos. Com essa opção, o inventário de produtos não é deduzido de seu catálogo [!DNL Commerce] quando um pedido é feito. O estoque de estoque para pedidos atendidos do Amazon é armazenado e deduzido de seus depósitos. Antes de atribuir essa opção, você deve verificar em sua conta [!DNL Amazon Seller Central] se os produtos estão qualificados para _Cumprido pelo Amazon_ (FBA) cumprimento. O inventário FBA é gerenciado diretamente por meio da sua conta [!DNL Amazon Seller Central]. Com esse método de cumprimento, o canal de vendas da Amazon não compartilha atualizações de quantidade entre [!DNL Commerce] e a Amazon. Portanto, nem todas as ferramentas de marketing descritas nas Configurações de quantidade estão disponíveis no canal de vendas da Amazon.

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Se os seus produtos podem ser cumpridos por você e pela Amazon, você pode criar um atributo de  [!DNL Commerce] produto com valores para Fulfillment by Merchant e Fulfillment by Amazon. Definir esse valor por produto indica quem atende aos pedidos.

O método de cumprimento é um atributo regional e baseia-se na configuração **[!UICONTROL Amazon Marketplace Country]** definida durante [integração de armazenamento](./store-integration.md). Quando uma alteração é feita, a alteração afeta todas as listagens do Amazon que compartilham esse [!DNL Amazon Seller SKU] em suas lojas do Amazon que vendem na mesma região (conforme definido em _[!UICONTROL Amazon Marketplace Country]_durante [integração de loja](./store-integration.md)). Uma alteração em um [!DNL Amazon Seller SKU] compartilhado nos Estados Unidos não afeta suas lojas do Amazon definidas para uma região diferente (conforme definido durante a integração da loja).

>[!NOTE]
>
>Quando um pedido é realizado pela Amazon (FBA) e o pedido é importado, você pode ver dados fictícios para alguns campos nos detalhes do pedido. Consulte [Detalhes do pedido do Amazon](./amazon-order-details.md).

## Defina as configurações de [!UICONTROL Fulfilled By] {#configure-fulfilled-by-settings}

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda a seção _[!UICONTROL Fulfilled By]_.

1. Para **[!UICONTROL Product Fulfilled By]**, escolha quem atende (envia) a ordem:

   - `Fulfilled by Merchant` - O comerciante cumpre a ordem.

   - `Fulfilled by Amazon` - Amazon warehouse cumpre a ordem.

   - `Assign Fulfilled By Using Magento Product Attribute` - Um  [!DNL Commerce] atributo indica quem atende à ordem por produto.

      Se escolhido, escolha o atributo [!DNL Commerce] que deseja mapear em **[!UICONTROL Fulfilled by Attribute]**.

1. Quando terminar, clique em **[!UICONTROL Save listing settings]**.

![Preenchido por configurações](assets/amazon-fulfilled-by.png)

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Product Fulfilled By] | Opções:<ul><li>**[!UICONTROL Fulfilled by Merchant]** - (FBM) Escolha se você atende às ordens. Quando um pedido é feito, o inventário é deduzido de seu catálogo [!DNL Commerce]. Quando um novo produto é criado, o método de preenchimento de Merchant Fulfill é atribuído.</li><li>**[!UICONTROL Fulfilled by Amazon]** - (FBA) Escolha se a Amazon atende aos pedidos. Com esse método de cumprimento, o inventário de produtos não é deduzido de seu catálogo [!DNL Commerce] quando um pedido é feito. Quando um produto é criado, ele é criado com _[!UICONTROL Fulfilled by Amazon (FBA)]_como o tipo de cumprimento. Certifique-se de que seus produtos estejam qualificados para o cumprimento do FBA em sua conta [!DNL Amazon Seller Central]. O inventário FBA também é gerenciado diretamente por meio de sua conta [!DNL Amazon Seller Central]. Com esse método de cumprimento, as atualizações de quantidade não são enviadas em relação ao catálogo [!DNL Commerce], portanto, você não pode usar algumas das ferramentas de marketing descritas em [Configurações de estoque / Quantidade](./stock-quantity.md).</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Escolha se você tem um  [!DNL Commerce] atributo existente que determina se ele é preenchido pelo comerciante ou realizado pela Amazon. Quando escolhido, **[!UICONTROL Fulfilled by Attribute]** ativa.</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | Escolha o atributo [!DNL Commerce] usado para determinar o método de preenchimento.<br><br>Por exemplo, se o atributo for  _preenchido_ por e você escolher o valor do atributo como  _[!UICONTROL Fulfilled By Merchant]_ou_[!UICONTROL Fulfilled By Amazon (FBA)]_, o sistema usará esse valor como o tipo de preenchimento para um novo produto. Como comerciante, você deve garantir que seus produtos estejam qualificados para o cumprimento do FBA em sua conta [!DNL Amazon Seller Central]. O inventário FBA também é gerenciado diretamente por meio de sua conta de vendedores da Amazon.<br><br>As opções dependem dos atributos configurados para os produtos Amazon. |

**Acesso rápido**  -  [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
