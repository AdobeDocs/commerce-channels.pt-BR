---
title: Cancelar um pedido não entregue
description: Cancelar um pedido pendente ou parcialmente entregue (não enviado) através da Amazon [!DNL Seller Central] conta.
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# Cancelar uma ordem não entregue

Os pedidos Amazon só podem ser cancelados se estiverem em um `Unshipped` status. Se o pedido estiver pendente ou parcialmente entregue (não entregue), o pedido só poderá ser cancelado por meio de sua [!DNL Amazon Seller Central] conta. Se o item tiver sido enviado, os retornos e as trocas também deverão ser manipulados em seu [!DNL Amazon Seller Central] Conta.

>[!NOTE]
>
>Para tarefas diferentes do cancelamento de um pedido:
>
>- Se tiver [importação de pedidos](./order-settings.md) ativados, os pedidos são gerenciados na [[!DNL Commerce] fluxo de trabalho de pedidos](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}.
>- If [importação de pedidos](./order-settings.md) estiver desativado, você deverá gerenciar seus pedidos no [!DNL Amazon Seller Central].


## Cancelar um pedido em `Unshipped` status

1. Clique em **[!UICONTROL View Store]** no cartão da loja.

1. No _[!UICONTROL Recent Orders]_no painel da loja, clique em um número de pedido.

   O _[!UICONTROL Amazon Order Details]_será exibida.

1. Clique em **[!UICONTROL Cancel Order]** na barra de cabeçalho.

   Essa opção só aparece para pedidos em `Unshipped` status.

1. Para **[!UICONTROL Reason for cancellation]**, escolha uma opção.

1. Clique em **[!UICONTROL Confirm]**.

   O pedido é cancelado e o status é atualizado para `Canceled` nos detalhes do pedido.

A notificação de cancelamento é enviada para o [!DNL Amazon Seller Central] e o cliente associado ao pedido também é notificado. O status do [!DNL Commerce] alterar para `Complete`.
