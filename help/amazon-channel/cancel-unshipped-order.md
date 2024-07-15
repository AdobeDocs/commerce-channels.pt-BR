---
title: Cancelar um pedido Amazon não remetido
description: Cancelar um pedido pendente ou parcialmente remetido (não remetido) por meio da conta do Amazon [!DNL Seller Central] .
feature: Sales Channels, Orders, Shipping/Delivery
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---

# Cancelar um pedido Amazon não remetido

Pedidos Amazon só podem ser cancelados se estiverem com o status `Unshipped`. Se a ordem estiver pendente ou parcialmente remetida (não remetida), ela só poderá ser cancelada por meio da conta [!DNL Amazon Seller Central]. Se o item tiver sido enviado, as devoluções e trocas também deverão ser tratadas na sua Conta [!DNL Amazon Seller Central].

>[!NOTE]
>
>Para tarefas diferentes do cancelamento de um pedido:
>
>- Se você tiver a [importação de pedido](./order-settings.md) habilitada, os pedidos serão gerenciados no [[!DNL Commerce] fluxo de trabalho de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).
>- Se a [importação de pedido](./order-settings.md) estiver desabilitada, você deverá gerenciar seus pedidos em [!DNL Amazon Seller Central].

## Cancelar um pedido com status `Unshipped`

1. Clique em **[!UICONTROL View Store]** no cartão de armazenamento.

1. Na seção _[!UICONTROL Recent Orders]_do painel de armazenamento, clique em um número de pedido.

   A página _[!UICONTROL Amazon Order Details]_é exibida.

1. Clique em **[!UICONTROL Cancel Order]** na barra de cabeçalho.

   Esta opção só aparece para pedidos com status `Unshipped`.

1. Para **[!UICONTROL Reason for cancellation]**, escolha uma opção.

1. Clique em **[!UICONTROL Confirm]**.

   O pedido é cancelado e o status é atualizado para `Canceled` nos detalhes do pedido.

A notificação de cancelamento é enviada para sua conta [!DNL Amazon Seller Central], e o cliente associado ao pedido também é notificado. O status da ordem [!DNL Commerce] correspondente, se houver, muda para `Complete`.
