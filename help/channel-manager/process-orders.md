---
title: Processar ordens
description: Instruções de expedição e cancelamento [!DNL Walmart Marketplace] pedidos do Adobe Commerce e do Magento Open Source.
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: fac4bbd3985e07b919f986c877b8584da797e6fe
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Processar ordens

Se você usar o Adobe Commerce e o Magento Open Source Order Management para gerenciar seu [!DNL Commerce] armazenar vendas, você pode processar [!DNL Walmart Marketplace] pedidos do Commerce usando o mesmo fluxo de trabalho.

Ao processar um pedido no Commerce, o Gerenciador de Canais sincroniza atualizações no [!DNL Walmart Marketplace]. Essa atualização garante que o status do pedido e as informações de envio do Commerce correspondam aos dados rastreados no [!DNL Walmart Marketplace].

* **Encomendar entregas**-Walmart requer um número de rastreamento para todas as remessas. Você pode criar entregas parciais se não tiver estoque para todos os itens na ordem. Após submeter a entrega, as atualizações de pedido serão sincronizadas com o [!DNL Walmart Marketplace]. Em seguida, o Walmart notifica os clientes sobre o status do pedido e os detalhes de envio.

* **Cancelamentos de pedido**-Ao cancelar um [!DNL Walmart Marketplace] pedido, o Walmart requer um motivo de cancelamento que é incluído no aviso de cancelamento do pedido enviado ao cliente. O motivo do cancelamento também é exibido na variável [!DNL Commerce] informações sobre pagamentos de pedidos.

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

   * Escolha uma transportadora e adicione um número de rastreamento selecionando **[!UICONTROL Add tracking number]**.

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


1. Depois de enviar o cancelamento, rastreie o [status do pedido](manage-orders.md#about-order-status) em [!DNL Channel Manager] para verificar se as atualizações foram enviadas para [!DNL Walmart Marketplace].
