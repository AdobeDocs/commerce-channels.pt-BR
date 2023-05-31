---
title: Processar Pedidos
description: "Instruções para envio e cancelamento [!DNL Walmart Marketplace] pedidos da Adobe Commerce e da Magento Open Source."
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# Processar Pedidos

Depois [!DNL Walmart Marketplace] os pedidos foram confirmados e enviados com êxito para [!DNL Channel Manager], você usa [Gerenciamento de pedidos de comércio](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#orders-workspace) para processar o pedido.

O Gerenciador de canais sincroniza as atualizações para [!DNL Walmart Marketplace] para garantir que o status do pedido e as informações de envio do [!DNL Commerce] corresponde aos dados rastreados no [!DNL Walmart Marketplace].

* **Entregas de ordem**-O Walmart exige um número de rastreamento para todas as remessas. Se alguns itens estiverem esgotados, você poderá criar entregas parciais para enviar itens que estão disponíveis no momento. Depois de submeter a entrega, as atualizações da ordem são sincronizadas com [!DNL Walmart Marketplace]. Em seguida, o Walmart notifica os clientes sobre o status do pedido e os detalhes de envio.

* **Cancelamentos de pedidos**-Quando você cancela um [!DNL Walmart Marketplace] pedido, o Walmart exige um motivo de cancelamento que está incluído no aviso de cancelamento do pedido enviado ao cliente. O motivo do cancelamento também é exibido na [!DNL Commerce] informações sobre pagamentos de pedidos. Depois de enviar o cancelamento, as atualizações de inventário são sincronizadas com o [!DNL Walmart Marketplace]. Em seguida, o Walmart notifica os clientes sobre o status do pedido e os detalhes de envio.

   Na vitrine, você deve cancelar todo o pedido. [!DNL Commerce] O não permite cancelamentos parciais.

* **Solicitação de reembolso**-Se for solicitada uma devolução do Walmart Marketplace para um pedido enviado, a [!UICONTROL Status details] inclui um link para o retorno. As devoluções e os reembolsos são gerenciados no [Devoluções](return-refund-orders.md) painel.

Quando os pedidos de comércio são processados e [!DNL Channel Manager] sincroniza com êxito as atualizações de remessa, remessa parcial e cancelamento à [!DNL Walmart Marketplace], o processamento do pedido está concluído. As solicitações de devolução e os reembolsos de pedidos enviados são gerenciados no [Devoluções](return-refund-orders.md) painel.

>[!NOTE]
>
> Pode levar até cinco minutos para que as atualizações de pedidos sejam sincronizadas com o [!DNL Walmart Marketplace]. Para verificar o status do pedido, volte para a [!DNL Channel Manager] Página Pedidos.

## Enviar um pedido

1. Em Admin, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Abra a exibição de loja selecionando o ícone de olho de uma loja de canal de vendas.

1. Para exibir [!DNL Walmart Marketplace] pedidos, selecione **[!UICONTROL Orders]**.

1. Na tabela Pedidos, abra o pedido para remessa selecionando o **[!UICONTROL Commerce Order Number]**.

1. Criar e submeter uma entrega para toda ou parte de uma ordem selecionando **[!UICONTROL Ship]**.

   ![Exibição detalhada da ordem de comércio para um [!DNL Walmart Marketplace] pedido](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

   * Escolha uma transportadora e adicione um número de rastreamento selecionando **[!UICONTROL Add tracking number]**.

      ![Exibição detalhada da ordem de comércio para um [!DNL Walmart Marketplace] pedido](assets/order-shipment-add-tracking-number.png){width="600" zoomable="yes"}

   * Preencha o restante do formulário de remessa conforme necessário. Consulte [[!DNL Shipping an Order]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-ship.html) para obter instruções detalhadas.

1. Após enviar a remessa, rastreie as [status do pedido](manage-orders.md#about-order-status) in [!DNL Channel Manager] para verificar se as atualizações foram enviadas para [!DNL Walmart Marketplace].

Depois que um pedido é enviado, você pode processar reembolsos totais ou parciais de [!DNL Channel Manager] para itens incluídos no pedido com base em solicitações de devolução recebidas de [!DNL Walmart Marketplace]. Consulte [Ordens de devolução e de reembolso](return-refund-orders.md).

## Cancelar um pedido

1. Em Admin, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Abra a exibição de loja selecionando o ícone de olho de uma loja de canais de vendas.

1. Para exibir [!DNL Walmart Marketplace] pedidos, selecione *[!UICONTROL Orders]**.

1. Na tabela Pedidos, abra o [página de detalhes do pedido](manage-orders.md#view-order-detail) selecionando o **[!UICONTROL Commerce Order Number]** para cancelar a ordem.

   ![Exibição detalhada da ordem de comércio para um[!DNL Walmart Marketplace]pedido](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

1. Cancelar o pedido.

   * Selecionar **Cancelar** no menu Detalhes do pedido.

   * No [!UICONTROL Cancel Order] , selecione o **[!UICONTROL Cancellation reason]**.
   ![Exibição detalhada da ordem de comércio para um [!DNL Walmart Marketplace] pedido](assets/cancel-order-reason-selector.png){width="600" zoomable="yes"}

   * Selecionar **[!UICONTROL Cancel Order]**.


1. Após enviar o cancelamento, rastreie as [status do pedido](manage-orders.md#about-order-status) in [!DNL Channel Manager] para verificar se as atualizações foram enviadas para [!DNL Walmart Marketplace].

## Corrigir erros de pedido

Podem ocorrer erros durante o processo de sincronização de pedidos de [!DNL Walmart Marketplace]ou durante o processo de atualização de ordens para entregas, entregas parciais e cancelamentos.

Se a operação de sincronização de uma entrega, entrega parcial ou atualização de cancelamento falhar, a [!DNL Channel Manager] A página Pedidos mostra uma _Erro_ status do pedido. Para garantir que as informações de remessa e as informações de cancelamento de pedido sejam refletidas com precisão na conta do Walmart Marketplace, atualize manualmente o pedido em seu [!DNL Walmart Marketplace] armazenamento.


