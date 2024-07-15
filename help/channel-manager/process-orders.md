---
title: Processar Pedidos
description: 'Instruções para envio e cancelamento [!DNL Walmart Marketplace] de pedidos da Adobe Commerce e do Magento Open Source.'
feature: Sales Channels, Orders, Shipping/Delivery, Customer Service
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Processar Pedidos

Depois que [!DNL Walmart Marketplace] pedidos forem confirmados e enviados com êxito para [!DNL Channel Manager], você usará [Commerce Order Management](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#orders-workspace) para processar o pedido.

O Gerenciador de Canais sincroniza atualizações para [!DNL Walmart Marketplace] para garantir que o status do pedido e as informações de envio de [!DNL Commerce] correspondam aos dados rastreados em [!DNL Walmart Marketplace].

* **Remessas de pedidos**-O Walmart requer um número de rastreamento para todas as remessas. Se alguns itens estiverem esgotados, você poderá criar entregas parciais para enviar itens que estão disponíveis no momento. Depois de enviar a remessa, as atualizações da ordem serão sincronizadas com [!DNL Walmart Marketplace]. Em seguida, o Walmart notifica os clientes sobre o status do pedido e os detalhes de envio.

* **Cancelamentos de pedidos**-Quando você cancela um pedido de [!DNL Walmart Marketplace], o Walmart exige um motivo de cancelamento que está incluído no aviso de cancelamento do pedido enviado ao cliente. O motivo do cancelamento também é exibido nas informações de pagamentos da ordem [!DNL Commerce]. Após enviar o cancelamento, as atualizações de estoque serão sincronizadas com [!DNL Walmart Marketplace]. Em seguida, o Walmart notifica os clientes sobre o status do pedido e os detalhes de envio.

  Na vitrine, você deve cancelar todo o pedido. [!DNL Commerce] não permite cancelamentos parciais.

* **Solicitação de reembolso**-Se uma devolução do Walmart Marketplace for solicitada para uma ordem remetida, a [!UICONTROL Status details] incluirá um link para a devolução. As devoluções e os reembolsos são gerenciados no painel [Devoluções](return-refund-orders.md).

Quando os pedidos do Commerce são processados e o [!DNL Channel Manager] sincroniza com êxito as atualizações de remessa, remessa parcial e cancelamento para o [!DNL Walmart Marketplace], o processamento do pedido é concluído. As solicitações de devolução e os reembolsos de pedidos enviados são gerenciados no painel [Devoluções](return-refund-orders.md).

>[!NOTE]
>
> Pode levar até cinco minutos para que as atualizações de pedidos sejam sincronizadas com o [!DNL Walmart Marketplace]. Para verificar o status do pedido, volte para a página [!DNL Channel Manager] Pedidos.

## Enviar um pedido

1. No Administrador, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Abra a exibição de loja selecionando o ícone de olho de uma loja de canal de vendas.

1. Para exibir [!DNL Walmart Marketplace] pedidos, selecione **[!UICONTROL Orders]**.

1. Na tabela Pedidos, abra o pedido a ser enviado selecionando o **[!UICONTROL Commerce Order Number]**.

1. Crie e envie uma remessa para todo ou parte de um pedido selecionando **[!UICONTROL Ship]**.

   ![Exibição detalhada de Pedido Commerce para um pedido [!DNL Walmart Marketplace]](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

   * Escolha uma transportadora e adicione um número de rastreamento selecionando **[!UICONTROL Add tracking number]**.

     ![Exibição detalhada de Pedido Commerce para um pedido [!DNL Walmart Marketplace]](assets/order-shipment-add-tracking-number.png){width="600" zoomable="yes"}

   * Preencha o restante do formulário de remessa conforme necessário. Consulte [[!DNL Shipping an Order]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-ship.html) para obter instruções detalhadas.

1. Após enviar a remessa, rastreie o [status do pedido](manage-orders.md#about-order-status) em [!DNL Channel Manager] para verificar se as atualizações foram enviadas para [!DNL Walmart Marketplace].

Depois que um pedido for enviado, você poderá processar reembolsos totais ou parciais de [!DNL Channel Manager] para os itens incluídos no pedido com base nas solicitações de devolução recebidas de [!DNL Walmart Marketplace]. Consulte [Ordens de devolução e reembolso](return-refund-orders.md).

## Cancelar um pedido

1. No Administrador, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Abra a exibição de loja selecionando o ícone de olho de uma loja de canais de vendas.

1. Para exibir [!DNL Walmart Marketplace] pedidos, selecione *[!UICONTROL Orders]**.

1. Na tabela Pedidos, abra a [página de detalhes do pedido](manage-orders.md#view-order-detail) selecionando a **[!UICONTROL Commerce Order Number]** para o pedido ser cancelado.

   ![Exibição detalhada do Pedido Commerce para um[!DNL Walmart Marketplace]pedido](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

1. Cancelar o pedido.

   * Selecione **Cancelar** no menu Detalhes do pedido.

   * No formulário [!UICONTROL Cancel Order], selecione o **[!UICONTROL Cancellation reason]**.

   ![Exibição detalhada de Pedido Commerce para um pedido [!DNL Walmart Marketplace]](assets/cancel-order-reason-selector.png){width="600" zoomable="yes"}

   * Selecione **[!UICONTROL Cancel Order]**.

1. Após enviar o cancelamento, rastreie o [status do pedido](manage-orders.md#about-order-status) em [!DNL Channel Manager] para verificar se as atualizações foram enviadas para [!DNL Walmart Marketplace].

## Corrigir erros de pedido

Podem ocorrer erros durante o processo de sincronização de ordens de [!DNL Walmart Marketplace] ou durante o processo de atualização de ordens para remessas, remessas parciais e cancelamentos.

Se a operação de sincronização de uma remessa, remessa parcial ou atualização de cancelamento falhar, a página Pedidos [!DNL Channel Manager] mostrará um status _Erro_ para o pedido. Para garantir que as informações de remessa e as informações de cancelamento de pedido sejam refletidas com precisão na conta do Walmart Marketplace, atualize manualmente o pedido em sua loja [!DNL Walmart Marketplace].


