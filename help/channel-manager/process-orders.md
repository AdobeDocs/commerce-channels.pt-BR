---
title: Processar ordens
description: Instruções de expedição e cancelamento [!DNL Walmart Marketplace] pedidos do Adobe Commerce e do Magento Open Source.
source-git-commit: 5670639697550b2d7fee67dd29be9c6278d5782b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Processar ordens

Se você usar o Adobe Commerce e o Magento Open Source Order Management para gerenciar seu [!DNL Commerce] armazenar vendas, você processa [!DNL Walmart Marketplace] pedidos do Commerce usando um fluxo de trabalho semelhante.

Ao processar um pedido no Commerce, o Gerenciador de Canais sincroniza atualizações no [!DNL Walmart Marketplace]. Essa atualização garante que o inventário de produtos e o status do pedido do Commerce correspondam aos dados rastreados no [!DNL Walmart Marketplace] e notifica a Walmart para enviar o status do pedido e as informações de envio para os clientes.

>[!NOTE]
>
> Pode demorar até cinco minutos para que o pedido seja sincronizado com [!DNL Walmart Marketplace]. Para verificar o status do pedido, retorne para [!DNL Channel Manager] Pedidos.

## Enviar uma ordem

Quando você envia um pedido do Commerce, usa a variável [[!DNL Commerce Order Management] fluxo de trabalho de envio](https://docs.magento.com/user-guide/sales/order-ship.html). Após enviar o pedido, as atualizações são sincronizadas com o [!DNL Walmart Marketplace]. Em seguida, o Walmart notifica os clientes sobre o status do pedido e os detalhes de envio.

**Pré-requisito**

Antes de enviar as ordens, verifique se a variável [configurações de envio de canal e configuração de operadora](map-shipping-carriers.md) conheça [!DNL Walmart Marketplace requirements].

### Criar e enviar a remessa

Quando você envia um [!DNL Walmart Marketplace] ordenar de [!DNL Commerce], é necessário adicionar um número de rastreamento. Os clientes recebem o número de rastreamento na notificação de remessa da qual recebem [!DNL Walmart].

1. Em Admin, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** para abrir o [!UICONTROL Channel Manager Marketplace Stores] página.

1. Abra a visualização da loja selecionando o ícone de olho de uma loja de canais de vendas.

1. Para exibir [!DNL Walmart Marketplace] pedidos, selecione *[!UICONTROL *Orders]**.

1. Na tabela Pedidos , abra o pedido a ser enviado selecionando o **Número do pedido de comércio**.

1. Criar e enviar uma remessa para toda ou parte de uma ordem selecionando **[!UICONTROL Ship]**.

   - Para escolher uma transportadora e adicionar um número de rastreamento, selecione **[!UICONTROL Add tracking number]**.

   - Preencha o restante do formulário de envio, conforme necessário. Consulte [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) para obter instruções detalhadas.

1. Depois de enviar a entrega, rastreie o [status do pedido](manage-orders.md#about-order-status) em [!DNL Channel Manager] para verificar se as atualizações foram enviadas para [!DNL Walmart Marketplace].

## Cancelar um pedido

Ao cancelar um [!DNL Walmart Marketplace] O Walmart requer um motivo de cancelamento. Quando o cancelamento do pedido é atualizado para o Walmart, o motivo do cancelamento é incluído no aviso de cancelamento enviado ao cliente.

O motivo do cancelamento também é exibido na variável [!DNL Commerce] informações sobre pagamentos de pedidos.

1. Em Admin, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** para abrir o [!UICONTROL Channel Manager Marketplace Stores] página.

1. Abra a visualização da loja selecionando o ícone de olho de uma loja de canais de venda.

1. Para exibir [!DNL Walmart Marketplace] pedidos, selecione *[!UICONTROL *Orders]**.

1. Na tabela Pedidos , abra a página de detalhes do pedido selecionando o **Número do pedido de comércio** para o cancelamento do pedido.

   ![Exibição detalhada de Pedido de comércio para um pedido do Walmart](assets/order-detail-with-external-order-id.png)

1. Cancele o pedido.

   - Selecionar **Cancelar** no menu Detalhes do pedido.

   - No formulário Cancelar pedido , selecione o **Motivo do cancelamento**.

      ![Exibição detalhada de Pedido de comércio para um pedido do Walmart](assets/order-detail-with-external-order-id.png)

   - Selecionar **Cancelar pedido**.

1. Verifique se as atualizações foram enviadas para o [!DNL Walmart Marketplace] verificando a [status do pedido](manage-orders.md#about-order-status) em [!DNL Channel Manager].
