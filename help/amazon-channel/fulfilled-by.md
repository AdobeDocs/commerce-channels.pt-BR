---
title: Preenchido por
description: Use as configurações Preenchido por para determinar como os pedidos das listagens da Amazon são cumpridos (entregues).
redirect_from: /sales-channels/asc/ob-fulfilled-by.html
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# Preenchido por

_[!UICONTROL Fulfilled By]_As configurações fazem parte das configurações da listagem de loja. As configurações de listagem são acessadas do [painel de loja](./amazon-store-dashboard.md).

Essas configurações definem a parte que atende (ou envia) as ordens. Se todos os seus pedidos forem realizados usando um método, escolha entre um comerciante (você) ou a Amazon. Se você planeja cumprir pedidos de suas localizações e usar o Amazon, é uma prática recomendada usar a terceira opção e configurar um [!DNL Commerce] atributo do produto.

- **[!UICONTROL Fulfilled by Merchant]** - Escolha se você, o comerciante, atende a todos os pedidos. Quando um pedido é feito, o inventário é deduzido de seu [!DNL Commerce] catálogo.

- **[!UICONTROL Fulfilled by Amazon]** - Escolha se a Amazon atende a todos os pedidos. Com essa opção, o inventário de produtos não é deduzido de sua [!DNL Commerce] catálogo quando um pedido é feito. O estoque de estoque para pedidos atendidos do Amazon é armazenado e deduzido de seus depósitos. Antes de atribuir essa opção, você deve verificar em [!DNL Amazon Seller Central] considera que seus produtos estão qualificados para _Cumprido Pela Amazon_ (FBA) execução. O inventário FBA é gerenciado diretamente por meio de seu [!DNL Amazon Seller Central] Conta. Com esse método de preenchimento, o canal de vendas da Amazon não compartilha atualizações de quantidade entre [!DNL Commerce] e Amazon. Portanto, nem todas as ferramentas de marketing descritas nas Configurações de quantidade estão disponíveis no canal de vendas da Amazon.

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Se os seus produtos puderem ser cumpridos por você e pela Amazon, talvez você queira criar um [!DNL Commerce] atributo do produto com valores para Fulfillment by Merchant e Fulfillment by Amazon. Definir esse valor por produto indica quem atende aos pedidos.

O método de cumprimento é um atributo regional e com base no **[!UICONTROL Amazon Marketplace Country]** definição durante [integração de loja](./store-integration.md). Quando uma alteração é feita, a alteração afeta todas as listagens do Amazon que compartilham esse compartilhamento [!DNL Amazon Seller SKU] em suas lojas Amazon que vendem na mesma região (conforme definido em _[!UICONTROL Amazon Marketplace Country]_during [integração de loja](./store-integration.md)). Uma alteração em um compartilhado [!DNL Amazon Seller SKU] nos Estados Unidos não afeta suas lojas do Amazon definidas para uma região diferente (conforme definido durante a integração da loja).

>[!NOTE]
>
>Quando um pedido é realizado pela Amazon (FBA) e o pedido é importado, você pode ver dados fictícios para alguns campos nos detalhes do pedido. Consulte [Detalhes do pedido Amazon](./amazon-order-details.md).

## Configure o [!UICONTROL Fulfilled By] configurações {#configure-fulfilled-by-settings}

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda o _[!UICONTROL Fulfilled By]_seção.

1. Para **[!UICONTROL Product Fulfilled By]**, escolha quem preenche (envia) a ordem:

   - `Fulfilled by Merchant` - O comerciante cumpre a ordem.

   - `Fulfilled by Amazon` - Amazon warehouse cumpre a ordem.

   - `Assign Fulfilled By Using Magento Product Attribute` - A [!DNL Commerce] indica quem atende ao pedido por produto.

      Se escolhido, escolha a variável [!DNL Commerce] atributo no qual você deseja mapear **[!UICONTROL Fulfilled by Attribute]**.

1. Ao concluir, clique em **[!UICONTROL Save listing settings]**.

![Preenchido por configurações](assets/amazon-fulfilled-by.png)

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Product Fulfilled By] | Opções:<ul><li>**[!UICONTROL Fulfilled by Merchant]** - (FBM) Escolha se você atende às ordens. Quando um pedido é feito, o inventário é deduzido de seu [!DNL Commerce] catálogo. Quando um novo produto é criado, o método de preenchimento de Merchant Fulfill é atribuído.</li><li>**[!UICONTROL Fulfilled by Amazon]** - (FBA) Escolha se a Amazon atende aos pedidos. Com esse método de cumprimento, o inventário de produtos não é deduzido de seu [!DNL Commerce] catálogo quando um pedido é feito. Quando um produto é criado, ele é criado com _[!UICONTROL Fulfilled by Amazon (FBA)]_como o tipo de cumprimento. Certifique-se de que seus produtos estejam qualificados para o cumprimento do FBA em seu [!DNL Amazon Seller Central] conta. O inventário FBA também é gerenciado diretamente por meio de seu [!DNL Amazon Seller Central] conta. Com esse método de cumprimento, as atualizações de quantidade não são enviadas em relação ao seu [!DNL Commerce] , portanto, não é possível usar algumas das ferramentas de marketing descritas em [Configurações de estoque/quantidade](./stock-quantity.md).</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Escolha se você tem um [!DNL Commerce] que determina se é preenchido pelo comerciante ou pela Amazon. Quando escolhido, **[!UICONTROL Fulfilled by Attribute]** ativa.</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | Escolha a [!DNL Commerce] atributo usado para determinar o método de preenchimento.<br><br>Por exemplo, se o atributo for _Preenchido por_ e você escolhe o valor do atributo como _[!UICONTROL Fulfilled By Merchant]_ou_[!UICONTROL Fulfilled By Amazon (FBA)]_, o sistema usa esse valor como o tipo de cumprimento para um novo produto. Como comerciante, você deve garantir que seus produtos estejam qualificados para o cumprimento do FBA em seu [!DNL Amazon Seller Central] conta. O inventário FBA também é gerenciado diretamente por meio de sua conta de vendedores da Amazon.<br><br>As opções dependem dos atributos configurados para os produtos Amazon. |

**Acesso rápido** - [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
