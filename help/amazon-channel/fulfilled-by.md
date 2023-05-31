---
title: Configurações de Preenchido por para listagens do Amazon
description: Use as configurações Atendido por para determinar como as ordens das listagens do Amazon são atendidas (entregues).
redirect_from: /sales-channels/asc/ob-fulfilled-by.html
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 077d680da3c98ef9a48958eb548a9d5c1612f74e
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Configurações de Preenchido por para listagens do Amazon

_[!UICONTROL Fulfilled By]_as configurações fazem parte das configurações da lista de lojas. As configurações de listagem são acessadas no [painel de armazenamento](./amazon-store-dashboard.md).

Essas configurações definem a parte que atende (ou envia) as ordens. Se todos os seus pedidos forem atendidos usando um método, escolha entre comerciante (você) ou Amazon. Se você planeja atender pedidos de seus locais e usar o Amazon, é uma prática recomendada usar a terceira opção e configurar uma [!DNL Commerce] atributo de produto.

- **[!UICONTROL Fulfilled by Merchant]** - Escolha se você, o comerciante, cumpre todas as ordens. Quando um pedido é feito, o inventário é deduzido do [!DNL Commerce] catálogo.

- **[!UICONTROL Fulfilled by Amazon]** - Escolha se a Amazon atende a todos os pedidos. Com essa opção, o inventário de produtos não é deduzido do seu [!DNL Commerce] catálogo quando um pedido é feito. O estoque de estoque para ordens preenchidas Amazon é armazenado e deduzido de seus depósitos. Antes de atribuir essa opção, você deve verificar em [!DNL Amazon Seller Central] conta para a qual seus produtos estão qualificados _Preenchido pela Amazon_ (FBA). O inventário FBA é gerenciado diretamente por meio de [!DNL Amazon Seller Central] Conta. Com esse método de preenchimento, o canal de vendas da Amazon não compartilha atualizações de quantidade entre [!DNL Commerce] e Amazon. Portanto, nem todas as ferramentas de marketing descritas em Configurações de quantidade estão disponíveis no canal de vendas do Amazon.

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Se os seus produtos podem ser preenchidos por você e pela Amazon, talvez você queira criar uma [!DNL Commerce] atributo de produto com valores para Atendido pelo Comerciante e Atendido pela Amazon. Definir esse valor por produto indica quem atende aos pedidos.

O método de preenchimento é um atributo regional e tem como base **[!UICONTROL Amazon Marketplace Country]** configuração definida durante [integração de loja](./store-integration.md). Quando uma alteração é feita, ela afeta todas as listagens do Amazon que a compartilham [!DNL Amazon Seller SKU] em suas lojas Amazon que vendem na mesma região (conforme definido em _[!UICONTROL Amazon Marketplace Country]_durante [integração de loja](./store-integration.md)). Uma alteração em um compartilhamento [!DNL Amazon Seller SKU] nos Estados Unidos não afeta suas lojas Amazon definidas para uma região diferente (conforme definido durante a integração da loja).

>[!NOTE]
>
>Quando um pedido é preenchido pelo Amazon (FBA) e é importado, você pode ver dados fictícios de alguns campos nos detalhes do pedido. Consulte [Detalhes do pedido Amazon](./amazon-order-details.md).

## Configure o [!UICONTROL Fulfilled By] configurações {#configure-fulfilled-by-settings}

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda a _[!UICONTROL Fulfilled By]_seção.

1. Para **[!UICONTROL Product Fulfilled By]**, escolha quem preenche (envia) a ordem:

   - `Fulfilled by Merchant` - O comerciante cumpre a ordem.

   - `Fulfilled by Amazon` - O depósito da Amazon atende à ordem.

   - `Assign Fulfilled By Using Magento Product Attribute` - A [!DNL Commerce] O atributo indica quem atende ao pedido por produto.

      Se escolhido, escolha o [!DNL Commerce] atributo que você deseja mapear em **[!UICONTROL Fulfilled by Attribute]**.

1. Quando terminar, clique em **[!UICONTROL Save listing settings]**.

![Configurações de Preenchido por](assets/amazon-fulfilled-by.png){width="500" zoomable="yes"}

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Product Fulfilled By] | Opções:<ul><li>**[!UICONTROL Fulfilled by Merchant]** - (FBM) Escolha se você atende aos pedidos. Quando um pedido é feito, o inventário é deduzido do [!DNL Commerce] catálogo. Quando um novo produto é criado, o método de preenchimento do Comerciante Atendido é atribuído.</li><li>**[!UICONTROL Fulfilled by Amazon]** - (FBA) Escolha se a Amazon atende aos pedidos. Com esse método de preenchimento, o inventário de produtos não é deduzido do seu [!DNL Commerce] catálogo quando um pedido é feito. Quando um produto é criado, ele é criado com _[!UICONTROL Fulfilled by Amazon (FBA)]_como o tipo de preenchimento. Certifique-se de que seus produtos estejam qualificados para o cumprimento do FBA em seu [!DNL Amazon Seller Central] conta. O inventário FBA também é gerenciado diretamente por meio de [!DNL Amazon Seller Central] conta. Com esse método de atendimento, as atualizações de quantidade não são enviadas em relação às [!DNL Commerce] catálogo, portanto, não é possível usar algumas das ferramentas de marketing descritas em [Configurações de estoque/quantidade](./stock-quantity.md).</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Escolha se você tem um existente [!DNL Commerce] atributo que determina se é preenchido pelo comerciante ou preenchido pela Amazon. Quando escolhido, **[!UICONTROL Fulfilled by Attribute]** habilita.</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | Escolha o [!DNL Commerce] atributo usado para determinar o método de preenchimento.<br><br>Por exemplo, se o atributo for _Preenchido por_ e você escolher o valor do atributo como `Fulfilled By Merchant` ou `Fulfilled By Amazon (FBA)`, o sistema usa esse valor como o tipo de preenchimento para um novo produto. Como comerciante, você deve garantir que seus produtos sejam qualificados para o preenchimento do FBA em seu [!DNL Amazon Seller Central] conta. O inventário FBA também é gerenciado diretamente por meio de sua conta de vendedor da Amazon.<br><br>As opções dependem dos atributos configurados para seus produtos Amazon. |

**Acesso rápido** - [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
