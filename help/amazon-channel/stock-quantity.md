---
title: Estoque/Quantidade
description: Para controlar a sincronização dos detalhes da quantidade do produto da loja do Commerce com a sua [!DNL Amazon Seller Central] , atualize as configurações de Estoque/Quantidade.
redirect_from: /sales-channels/asc/ob-stock-quantity.html
exl-id: a8b7ab6c-393c-43c6-b5ef-68845177edff
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# Estoque/Quantidade

*[!UICONTROL Stock/Quantity]* As configurações fazem parte das configurações da listagem de loja. As configurações de listagem são acessadas do [painel de loja](./amazon-store-dashboard.md).

Essas configurações são usadas para sincronizar os detalhes de quantidade do produto da sua [!DNL Commerce] vitrine para a quantidade em seu [!DNL Amazon Seller Central] conta. Essa ferramenta é poderosa e pode ser usada para anúncios adicionais, exibindo a urgência ao comprador e mantendo o inventário organizado. Por exemplo, alguns comerciantes podem ter 150 itens de um SKU específico em estoque em seu depósito e desejam garantir que os compradores da Amazon possam comprar todo o inventário. Outros comerciantes podem desejar listar apenas um item por vez para criar um sentimento de escassez para o usuário final. Nesse caso, defina a variável *[!UICONTROL Maximum Listed Quantity]* para `1`.

A quantidade é um atributo regional e tem como base **[!UICONTROL Amazon Marketplace Country]** definir durante [integração de loja](./store-integration.md). Quando uma alteração é feita na quantidade de um produto, a alteração afeta todas as listagens do Amazon que compartilham esse compartilhamento [!DNL Amazon Seller SKU] em suas lojas Amazon que vendem no mesmo país. Uma alteração em um compartilhado [!DNL Amazon Seller SKU] nos Estados Unidos não afeta suas lojas Amazon configuradas para um país diferente. Sua primeira loja Amazon integrada (com a data de criação mais antiga) controla a prioridade nas configurações de quantidade.

>[!NOTE]
>
>Para usuários do Adobe Commerce e Magento Open Source 2.3.x, o canal de vendas da Amazon oferece suporte ao uso da extensão Gerenciamento de inventário sem qualquer configuração adicional. Consulte [Gerenciamento de inventário](https://docs.magento.com/user-guide/v2.3/catalog/inventory-management.html){target=&quot;_blank&quot;}.

## Definir configurações de quantidade/estoque {#configure-stock--quantity-settings}

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda o **[!UICONTROL Stock / Quantity]** seção.

1. Para **[!UICONTROL Out-of-Stock Threshold]** (obrigatório), insira um valor numérico para a quantidade mais baixa de um produto, a fim de manter o produto qualificado para sua lista Amazon.

   O padrão é `0`. Se o seu [!DNL Commerce] o estoque do produto for menor que esse número, a respectiva listagem do Amazon não se qualificará para vendas por meio do Amazon.

1. Para **[!UICONTROL Maximum Listed Quantity]** (obrigatório), insira um valor numérico para a quantidade que você deseja exibir na sua lista do Amazon.

   Essa configuração lista todas as suas listagens Amazon qualificadas no valor inserido. Quando um item é vendido, a quantidade listada da Amazon não muda. A quantidade disponível na lista sempre usa esse valor, mesmo quando a quantidade real do produto é maior ou menor. Normalmente, essa configuração é usada quando você não gerencia o inventário de produtos. Por exemplo, você pode ter um produto com uma quantidade de 80 em seu [!DNL Commerce] catálogo. Com definição para `10`, a listagem do Amazon sempre exibe uma quantidade disponível de `10` e não se altera quando a venda do produto é feita.

1. Para **[!UICONTROL "Do Not Manage Stock" Quantity]** (obrigatório), insira um valor de quantidade a ser exibido nas listagens do Amazon.

   O Amazon exige que você publique uma quantidade disponível. Para [!DNL Commerce] produtos configurados para não gerenciar estoque, mas que você deseja listá-los no Amazon, a listagem é publicada com a quantidade disponível inserida aqui.

1. Ao concluir, clique em **[!UICONTROL Save listing settings]**.

![Configurações de estoque/quantidade](assets/amazon-stock-quantity.png)

| Campo | Descrição |
|---|---|
| [!UICONTROL Out-of-Stock Threshold] | Insira um valor numérico para a menor quantidade de um produto para manter o produto qualificado para sua listagem do Amazon (o padrão é `0`).<br><br>Se o seu [!DNL Commerce] o estoque do produto for menor que esse número, a respectiva listagem do Amazon não se qualificará para vendas por meio do Amazon. |
| [!UICONTROL Maximum Listed Quantity] | Insira um valor numérico para a quantidade que deseja mostrar na sua lista da Amazon.<br><br>Quando um item é vendido, a lista do Amazon é republicada com a quantidade inserida aqui. Normalmente, essa configuração é usada quando você não gerencia o inventário de produtos.<br><br>Por exemplo, você insere o valor Quantidade Listada Máxima como `10`. Sua quantidade real de um produto é `80`. Como você definiu esse valor como `10`, a listagem do Amazon sempre exibe uma quantidade disponível de `10`. A quantidade disponível é sempre exibida com o valor definido, mesmo quando a quantidade do estoque é menor. |
| [!UICONTROL "Do Not Manage Stock" Quantity] | Insira um valor para a quantidade de exibição das listagens do Amazon.<br><br>O Amazon exige que você publique uma quantidade disponível. Para [!DNL Commerce] produtos configurados para não gerenciar estoque, mas que você deseja listá-los no Amazon, a listagem é publicada com a quantidade disponível do valor inserido aqui. |

**Acesso rápido** - [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)

## Exemplo: Quantidade máxima indicada

Quando um item é vendido, a lista do Amazon o relista nessa quantidade.

Por exemplo, se você definir *[!UICONTROL Maximum Listed Quantity]* as `12`, a listagem do Amazon mostra uma quantidade de 12, mesmo que o produto tenha uma [!DNL Commerce] Quantidade de 80:

![Quantidade máxima listada exemplo 1](assets/amazon-max-listed-quantity.png)

Se você definir seu *[!UICONTROL Maximum Listed Quantity]* as `1`, todos os produtos elegíveis são indicados com uma quantidade de `1`. Quando um item é vendido, o sistema procura [!DNL Commerce] produto e, se houver estoque adicional, relista o item no Amazon com uma quantidade de `1`.

Essa opção pode ser valiosa para produtos que normalmente são solicitados em uma quantidade de 1. Também aumenta a urgência do comprador ao visualizar sua lista do Amazon.

![Quantidade máxima listada exemplo 2](assets/amazon-max-listed-quantity-1.png)
