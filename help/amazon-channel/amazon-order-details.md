---
title: Detalhes do pedido Amazon
description: Veja os detalhes dos seus pedidos do Amazon Marketplace no Adobe Commerce ou no Magento Open Source Admin.
feature: Sales Channels, Orders
exl-id: a85bb6b3-817d-4859-a815-41777f4b8667
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Detalhes do pedido Amazon

![detalhes do pedido Amazon](assets/amazon-order-details-header.png){width="600" zoomable="yes"}

## Exibir detalhes do pedido Amazon

1. Clique em **[!UICONTROL View Store]** no cartão de armazenamento.

1. Na seção _[!UICONTROL Recent Orders]_, clique em um número de pedido.

   A página _[!UICONTROL Amazon Order Details]_é aberta.

>[!NOTE]
>
>Se a importação de pedidos estiver habilitada nas [Configurações do Pedido](./order-settings.md) e o pedido for [preenchido pelo Amazon (FBA)](./fulfilled-by.md), você poderá ver dados fictícios para alguns campos nos detalhes do pedido. A Amazon não envia os dados a seguir para pedidos FBA.
>
> - `AddressType`
> - `AddressLine1`
> - `AddressLine2`
> - `AddressLine3`
> - `BuyerName`
> - `Phone`
> - `PurchaseOrderNumber`
> - `RecipientName`
> - `CustomizedURL`
> - `GiftMessageText`

### Guia Detalhes da Ordem e da Entrega

A guia _[!UICONTROL Order and Shipping Details]_mostra informações detalhadas do pedido, conforme recebidas da Amazon.

>[!IMPORTANT]
>
>O Amazon aceita informações de endereço não padrão que não podem ser importadas para o canal de vendas do Amazon, impedindo assim que os códigos de estado/país sejam atualizados corretamente para alguns pedidos. Para corrigir erros de endereço, os seguintes campos são editáveis nos detalhes do pedido:
>
>- `Shipping address 1`
>- `Shipping address 2`
>- `Shipping address 3`
>- `Shipping city`
>- `Shipping region`
>- `Shipping postal code`
>- `Shipping country`
>
>Não se esqueça de clicar em **Salvar Pedido** depois de fazer edições.

![Detalhes do pedido e do envio](assets/amazon-order-details.png){width="600" zoomable="yes"}

### Guia Itens de pedido

A guia _[!UICONTROL Order Items]_mostra todos os itens associados ao pedido do Amazon, conforme recebidos do Amazon.

![Detalhes do item do pedido](assets/amazon-order-item-details.png){width="600" zoomable="yes"}

### Guia Tracking

A guia _[!UICONTROL Tracking]_mostra informações de rastreamento associadas à ordem do Amazon.

![Detalhes do rastreamento](assets/amazon-order-tracking-details.png){width="600" zoomable="yes"}
