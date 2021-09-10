---
title: Detalhes do pedido Amazon
description: Veja os detalhes dos seus pedidos do Amazon Marketplace no Adobe Commerce ou no Magento Open Source Admin.
exl-id: a85bb6b3-817d-4859-a815-41777f4b8667
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Detalhes do pedido Amazon

![Detalhes do pedido Amazon](assets/amazon-order-details-header.png)

## Exibir detalhes do pedido da Amazon

1. Clique em **[!UICONTROL View Store]** no cartão de armazenamento.

1. Na seção _[!UICONTROL Recent Orders]_, clique em um número de pedido.

   A página _[!UICONTROL Amazon Order Details]_é aberta.

>[!NOTE]
>
>Se a importação de pedidos estiver ativada em [Order Settings](./order-settings.md) e o pedido for [realizado pelo Amazon (FBA)](./fulfilled-by.md), você poderá ver dados fictícios para alguns campos nos detalhes do pedido. A Amazon não envia os seguintes dados para pedidos FBA.
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


### Guia Detalhes da Ordem e Entrega

A guia _[!UICONTROL Order and Shipping Details]_mostra as informações detalhadas do pedido, conforme recebidas do Amazon.

>[!IMPORTANT]
>
>A Amazon aceita informações de endereço não padrão que não podem ser importadas para o canal de vendas da Amazon, impedindo assim que os códigos de estado/país sejam atualizados corretamente para alguns pedidos. Para corrigir erros de endereço, os seguintes campos são editáveis nos detalhes do pedido:
>
>- `Shipping address 1`
>- `Shipping address 2`
>- `Shipping address 3`
>- `Shipping city`
>- `Shipping region`
>- `Shipping postal code`
>- `Shipping country`

>
>Não se esqueça de clicar em **Salvar pedido** depois de fazer edições.

![Detalhes da Ordem e Entrega](assets/amazon-order-details.png)

### Guia Itens da Ordem

A guia _[!UICONTROL Order Items]_mostra todos os itens associados ao pedido do Amazon, conforme recebido do Amazon.

![Detalhes do Item da Ordem](assets/amazon-order-item-details.png)

### Guia Tracking

A guia _[!UICONTROL Tracking]_mostra as informações de rastreamento associadas ao pedido do Amazon.

![Detalhes do rastreamento](assets/amazon-order-tracking-details.png)
