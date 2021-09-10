---
title: Cancelar um pedido não entregue
description: Cancele um pedido pendente ou parcialmente enviado (não enviado) por meio da conta Amazon [!DNL Seller Central] .
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# Cancelar uma ordem não entregue

Os pedidos Amazon só podem ser cancelados se estiverem em um status `Unshipped`. Se o pedido estiver pendente ou parcialmente enviado (não enviado), o pedido só poderá ser cancelado por meio da sua conta [!DNL Amazon Seller Central]. Se o item tiver sido enviado, os retornos e trocas também deverão ser manipulados em sua Conta [!DNL Amazon Seller Central].

>[!NOTE]
>
>Para tarefas diferentes do cancelamento de um pedido:
>
>- Se você tiver [importação de ordem](./order-settings.md) ativada, os pedidos serão gerenciados no [[!DNL Commerce] fluxo de trabalho de pedidos](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}.
>- Se [order import](./order-settings.md) estiver desativado, você deverá gerenciar seus pedidos em [!DNL Amazon Seller Central].


## Cancelar um pedido no status `Unshipped`

1. Clique em **[!UICONTROL View Store]** no cartão de armazenamento.

1. Na seção _[!UICONTROL Recent Orders]_do painel de loja, clique em um número de pedido.

   A página _[!UICONTROL Amazon Order Details]_é exibida.

1. Clique em **[!UICONTROL Cancel Order]** na barra de cabeçalho.

   Essa opção só aparece para pedidos no status `Unshipped`.

1. Para **[!UICONTROL Reason for cancellation]**, escolha uma opção.

1. Clique em **[!UICONTROL Confirm]**.

   O pedido é cancelado e o status é atualizado para `Canceled` nos detalhes do pedido.

A notificação de cancelamento é enviada para sua conta [!DNL Amazon Seller Central] e o cliente associado ao pedido também é notificado. O status da ordem [!DNL Commerce] correspondente, se houver, muda para `Complete`.
