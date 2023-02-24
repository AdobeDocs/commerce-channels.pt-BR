---
title: Processar Ordens
description: "Instruções de expedição e cancelamento [!DNL Walmart Marketplace] pedidos da Adobe Commerce e do Magento Open Source."
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# Processar Ordens

Depois [!DNL Walmart Marketplace] os pedidos foram confirmados e enviados com êxito para [!DNL Channel Manager], você usa [Gerenciamento de pedidos de comércio](https://docs.magento.com/user-guide/sales/orders-workspace.html) para processar o pedido.

O Gerenciador de canais sincroniza atualizações para [!DNL Walmart Marketplace] para garantir que o status do pedido e as informações de envio sejam da [!DNL Commerce] corresponde aos dados rastreados no [!DNL Walmart Marketplace].

* **Encomendar entregas**-Walmart requer um número de rastreamento para todas as remessas. Se alguns itens estiverem em falta, é possível criar entregas parciais para enviar itens que estão disponíveis no momento. Após submeter a entrega, as atualizações de pedido serão sincronizadas com o [!DNL Walmart Marketplace]. Em seguida, o Walmart notifica os clientes sobre o status do pedido e os detalhes de envio.

* **Cancelamentos de pedido**-Ao cancelar um [!DNL Walmart Marketplace] pedido, o Walmart requer um motivo de cancelamento que é incluído no aviso de cancelamento do pedido enviado ao cliente. O motivo do cancelamento também é exibido na variável [!DNL Commerce] informações sobre pagamentos de pedidos. Após enviar o cancelamento, as atualizações de inventário são sincronizadas com [!DNL Walmart Marketplace]. Em seguida, o Walmart notifica os clientes sobre o status do pedido e os detalhes de envio.

   Na loja, você deve cancelar o pedido inteiro. [!DNL Commerce] não permite cancelamentos parciais.

* **Pedido de reembolso**-Se um retorno do Walmart for solicitado para um pedido enviado, a variável [!UICONTROL Status details] inclui um link para o retorno. As devoluções e os reembolsos são gerenciados no [Devoluções](return-refund-orders.md) painel.

Quando os pedidos de comércio são processados e [!DNL Channel Manager] sincroniza com êxito atualizações de entrega, entrega parcial e cancelamento para a [!DNL Walmart Marketplace], o processamento do pedido é concluído. As solicitações e os reembolsos de devolução para pedidos enviados são gerenciados a partir do [Devoluções](return-refund-orders.md) painel.

>[!NOTE]
>
> Pode levar até cinco minutos para que as atualizações de pedido sejam sincronizadas com o [!DNL Walmart Marketplace]. Para verificar o status do pedido, retorne para o [!DNL Channel Manager] Página Pedidos .

## Enviar uma ordem

1. Em Admin, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Abra a visualização da loja selecionando o ícone de olho de uma loja de canais de vendas.

1. Para exibir [!DNL Walmart Marketplace] pedidos, selecione **[!UICONTROL Orders]**.

1. Na tabela Pedidos , abra o pedido a ser enviado selecionando o **Número do pedido de comércio**.

1. Criar e enviar uma remessa para toda ou parte de uma ordem selecionando **[!UICONTROL Ship]**.

   ![Exibição detalhada do pedido de comércio para um [!DNL Walmart Marketplace] pedido](assets/order-detail-with-external-order-id.png)

   * Escolha uma transportadora e adicione um número de rastreamento selecionando **[!UICONTROL Add tracking number]**.

      ![Exibição detalhada do pedido de comércio para um [!DNL Walmart Marketplace] pedido](assets/order-shipment-add-tracking-number.png)


   * Preencha o restante do formulário de envio, conforme necessário. Consulte [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) para obter instruções detalhadas.

1. Depois de enviar a entrega, rastreie o [status do pedido](manage-orders.md#about-order-status) em [!DNL Channel Manager] para verificar se as atualizações foram enviadas para [!DNL Walmart Marketplace].

Depois que um pedido for enviado, você poderá processar reembolsos totais ou parciais do [!DNL Channel Manager] para itens incluídos na ordem com base em solicitações de retorno recebidas de [!DNL Walmart Marketplace]. Consulte [pedidos de devolução e reembolso](return-refund-orders.md).

## Cancelar um pedido

1. Em Admin, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Abra a visualização da loja selecionando o ícone de olho de uma loja de canais de venda.

1. Para exibir [!DNL Walmart Marketplace] pedidos, selecione *[!UICONTROL *Orders]**.

1. Na tabela Pedidos , abra o [página de detalhes do pedido](manage-orders.md#view-order-detail) selecionando o **Número do pedido de comércio** para o cancelamento do pedido.

   ![Exibição detalhada do pedido de comércio para um[!DNL Walmart Marketplace]pedido](assets/order-detail-with-external-order-id.png)

1. Cancele o pedido.

   * Selecionar **Cancelar** no menu Detalhes do pedido.

   * No [!UICONTROL Cancel Order] , selecione o **Motivo do cancelamento**.
   ![Exibição detalhada do pedido de comércio para um [!DNL Walmart Marketplace] pedido](assets/cancel-order-reason-selector.png)

   * Selecionar **Cancelar pedido**.


1. Depois de enviar o cancelamento, rastreie o [status do pedido](manage-orders.md#about-order-status) em [!DNL Channel Manager] para verificar se as atualizações foram enviadas para [!DNL Walmart Marketplace].

## Corrigir erros de ordem

Erros podem ocorrer durante o processo de sincronização de pedidos a partir de [!DNL Walmart Marketplace]ou durante o processo de atualização de ordem de entregas, entregas parciais e cancelamentos.

Se a operação de sincronização de uma entrega, entrega parcial ou atualização de cancelamento falhar, a [!DNL Channel Manager] A página Pedidos mostra um _Erro_ status do pedido. Para garantir que as informações de entrega e cancelamento de pedido sejam refletidas com precisão na conta do Walmart Marketplace, atualize manualmente a ordem em seu [!DNL Walmart Marketplace] armazenar.


