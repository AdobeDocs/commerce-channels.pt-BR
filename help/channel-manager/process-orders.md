---
title: Processar ordens
description: Instruções de expedição e cancelamento [!DNL Walmart Marketplace] pedidos do Adobe Commerce e do Magento Open Source.
source-git-commit: 90ccbecd6d1433ae1312d79f7ae2d34c8f381b97
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---


# Processar ordens

Se você usar o Adobe Commerce e o Magento Open Source Order Management para gerenciar seu [!DNL Commerce] vendas de loja, processo [!DNL Walmart Marketplace] pedidos do Commerce usando um fluxo de trabalho semelhante.

Ao processar um pedido no Commerce, o Gerenciador de Canais sincroniza atualizações no [!DNL Walmart Marketplace]. Essa atualização garante que o status do pedido e as informações de envio do Commerce correspondam aos dados rastreados no [!DNL Walmart Marketplace].

* **Encomendar entregas**-Walmart requer um número de rastreamento para todas as remessas. Se a quantidade de estoque for insuficiente para preencher um pedido inteiro, crie uma entrega parcial. Após submeter a entrega, as atualizações de pedido serão sincronizadas com o [!DNL Walmart Marketplace]. Em seguida, o Walmart notifica os clientes sobre o status do pedido e os detalhes de envio.

* **Cancelamentos de pedido**-Ao cancelar um [!DNL Walmart Marketplace] O Walmart requer um motivo de cancelamento. O motivo do cancelamento é incluído no aviso de cancelamento do pedido enviado ao cliente. O motivo do cancelamento também é exibido na variável [!DNL Commerce] informações sobre pagamentos de pedidos.

>[!NOTE]
>
> Pode ser de até cinco minutos para que as atualizações de pedido sejam sincronizadas com o [!DNL Walmart Marketplace]. Para verificar o status do pedido, retorne para o [!DNL Channel Manager] Página Pedidos .

## Enviar uma ordem

1. Em Admin, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Abra a visualização da loja selecionando o ícone de olho de uma loja de canais de vendas.

1. Para exibir [!DNL Walmart Marketplace] pedidos, selecione *[!UICONTROL *Orders]**.

1. Na tabela Pedidos , abra o pedido a ser enviado selecionando o **Número do pedido de comércio**.

1. Criar e enviar uma remessa para toda ou parte de uma ordem selecionando **[!UICONTROL Ship]**.

   ![Exibição detalhada de Pedido de comércio para um pedido do Walmart](assets/order-detail-with-external-order-id.png)

   * Para escolher uma transportadora e adicionar um número de rastreamento, selecione **[!UICONTROL Add tracking number]**.

   * Preencha o restante do formulário de envio, conforme necessário. Consulte [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) para obter instruções detalhadas.

1. Depois de enviar a entrega, rastreie o [status do pedido](manage-orders.md#about-order-status) em [!DNL Channel Manager] para verificar se as atualizações foram enviadas para [!DNL Walmart Marketplace].

## Cancelar um pedido

1. Em Admin, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Abra a visualização da loja selecionando o ícone de olho de uma loja de canais de venda.

1. Para exibir [!DNL Walmart Marketplace] pedidos, selecione *[!UICONTROL *Orders]**.

1. Na tabela Pedidos , abra a página de detalhes do pedido selecionando o **Número do pedido de comércio** para o cancelamento do pedido.

![Exibição detalhada de Pedido de comércio para um pedido do Walmart](assets/order-detail-with-external-order-id.png)

1. Cancele o pedido.

   * Selecionar **Cancelar** no menu Detalhes do pedido.

   * No [!UICONTROL Cancel Order] , selecione o **Motivo do cancelamento**.

   ![Exibição detalhada de Pedido de comércio para um pedido do Walmart](assets/cancel-order-reason-selector.png)

   * Selecionar **Cancelar pedido**.


1. Verifique se as atualizações foram enviadas para o [!DNL Walmart Marketplace] verificando a [status do pedido](manage-orders.md#about-order-status) em [!DNL Channel Manager].
