---
title: Cancelar uma Ordem Não Entregue
description: Cancelar um pedido pendente ou parcialmente remetido (não remetido) por meio da Amazon [!DNL Seller Central] conta.
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# Cancelar uma Ordem Não Entregue

Os pedidos do Amazon só podem ser cancelados se estiverem em uma `Unshipped` status. Se a ordem estiver pendente ou parcialmente entregue (não entregue), a ordem só poderá ser cancelada por meio de [!DNL Amazon Seller Central] conta. Se o item tiver sido enviado, as devoluções e as trocas também deverão ser tratadas em seu [!DNL Amazon Seller Central] Conta.

>[!NOTE]
>
>Para tarefas diferentes do cancelamento de um pedido:
>
>- Se você tiver [importação de ordem](./order-settings.md) ativado, os pedidos são gerenciados na variável [[!DNL Commerce] fluxo de trabalho de pedidos](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"}.
>- Se [importação de ordem](./order-settings.md) estiver desativado, você deverá gerenciar seus pedidos no [!DNL Amazon Seller Central].


## Cancelar um pedido no `Unshipped` status

1. Clique em **[!UICONTROL View Store]** no cartão de loja.

1. No _[!UICONTROL Recent Orders]_do painel de armazenamento, clique em um número de pedido.

   A variável _[!UICONTROL Amazon Order Details]_é exibida.

1. Clique em **[!UICONTROL Cancel Order]** na barra de cabeçalho.

   Essa opção só aparece para pedidos no `Unshipped` status.

1. Para **[!UICONTROL Reason for cancellation]**, escolha uma opção.

1. Clique em **[!UICONTROL Confirm]**.

   A ordem é cancelada e o status é atualizado para `Canceled` nos detalhes do pedido.

A notificação de cancelamento é enviada ao seu [!DNL Amazon Seller Central] e o cliente associado ao pedido também é notificado. O status do correspondente [!DNL Commerce] pedido, se houver, alterações no `Complete`.
