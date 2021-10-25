---
title: Detalhes do pedido Amazon
description: Veja os detalhes dos pedidos do Amazon Marketplace no Adobe Commerce ou no Magento Open Source Admin.
exl-id: a85bb6b3-817d-4859-a815-41777f4b8667
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Detalhes do pedido Amazon

![Detalhes do pedido Amazon](assets/amazon-order-details-header.png)

## Exibir detalhes do pedido da Amazon

1. Clique em **[!UICONTROL View Store]** no cartão da loja.

1. No _[!UICONTROL Recent Orders]_clique em um número de pedido.

   O _[!UICONTROL Amazon Order Details]_será aberta.

>[!NOTE]
>
>Se a importação de pedidos estiver ativada na [Configurações da ordem](./order-settings.md) e a ordem é [realizado pela Amazon (FBA)](./fulfilled-by.md), você pode ver dados de teste para alguns campos nos detalhes do pedido. A Amazon não envia os seguintes dados para pedidos FBA.
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

O _[!UICONTROL Order and Shipping Details]_mostra informações detalhadas do pedido, conforme recebido da Amazon.

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
>Não se esqueça de clicar em **Salvar pedido** após fazer edições.

![Detalhes da Ordem e Entrega](assets/amazon-order-details.png)

### Guia Itens da Ordem

O _[!UICONTROL Order Items]_mostra todos os itens associados ao pedido da Amazon, conforme recebido da Amazon.

![Detalhes do Item da Ordem](assets/amazon-order-item-details.png)

### Guia Tracking

O _[!UICONTROL Tracking]_mostra as informações de rastreamento associadas ao pedido do Amazon.

![Detalhes do rastreamento](assets/amazon-order-tracking-details.png)
