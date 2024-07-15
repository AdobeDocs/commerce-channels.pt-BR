---
title: Gerenciar pedidos do Amazon
description: Você pode ativar a importação de pedidos nas Configurações de pedido para gerenciar com mais facilidade seus pedidos do Amazon com o administrador do Commerce.
feature: Sales Channels, Orders
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Gerenciar pedidos do Amazon

Você pode exibir suas informações de pedido do Amazon, conforme recebidas do Amazon, na seção _[!UICONTROL Recent Orders]_do [painel de armazenamento](./amazon-store-dashboard.md) ou na página_[!UICONTROL Amazon orders]_ (também chamada de exibição _[!UICONTROL All Orders]_).

A forma como você gerencia os pedidos da Amazon depende de a importação do pedido estar habilitada ou desabilitada nas [Configurações do Pedido](./order-settings.md#configure-order-settings).

## Com a importação da ordem ativada

Após a [integração de armazenamento](./store-integration.md), a configuração [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) é `Enabled` por padrão. Com essa configuração, os pedidos [!DNL Commerce] correspondentes são criados para seus pedidos da Amazon e podem ser gerenciados no fluxo de trabalho [[!DNL Commerce] Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).

>[!NOTE]
>
>Independentemente das configurações de importação do pedido, os pedidos do Amazon existentes na conta do [!DNL Amazon Seller Central] antes da [integração de loja](./store-integration.md) não são importados.

Os pedidos Amazon importados são gerenciados no fluxo de trabalho [[!DNL Commerce] Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html), da mesma forma que os outros armazenamentos [!DNL Commerce]. Clique no número do pedido Amazon na coluna *[!UICONTROL Order Number]* para abrir o pedido no [[!DNL Commerce] processo de pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-view-descriptions). Consulte [Exibir Pedidos Do Amazon](./amazon-orders-all.md).

### Processo de importação de ordem

Quando um pedido é feito no Amazon e a [importação de pedido](./order-settings.md) é habilitada, o processo a seguir é iniciado.

| Alterar | Ações |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Um pedido é feito no Amazon. | <ul><li>O Amazon define o status do pedido como `Pending`.</li><li>As informações do pedido são enviadas para [!DNL Commerce].</li><li>O pedido foi adicionado à tabela [_Pedidos da Amazon_](./amazon-orders-all.md) com status `Pending`.</li></ul> |
| O Amazon altera o status do pedido para `Unshipped`. | <ul><li>A alteração de status é enviada para [!DNL Commerce].</li><li>Na tabela [_Pedidos da Amazon_](./amazon-orders-all.md), o status do pedido muda para `Unshipped`.</li><li>No [[!DNL Commerce] fluxo de trabalho de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html), uma ordem [!DNL Commerce] correspondente é criada com um status `Processing`.</li></ul> |
| No [[!DNL Commerce] fluxo de trabalho de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html), a ordem [!DNL Commerce] é processada e o status muda para `Shipped`. | <ul><li>Na tabela [_Pedidos da Amazon_](./amazon-orders-all.md), o status do pedido muda para `Shipped`.</li><li>No próximo trabalho cron, o status do pedido muda para `Complete` no [[!DNL Commerce] fluxo de trabalho de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).</li></ul> |

### Bloqueadores de criação de pedidos

Há alguns cenários que impedem a criação da ordem [!DNL Commerce] correspondente. [!DNL Commerce] pedidos não são criados para pedidos que são recebidos quando qualquer um dos seguintes problemas ocorrer.

| Cenário | Solução |
|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O item não existe no catálogo [!DNL Commerce]. | [Crie o produto](./creating-assigning-catalog-products.md) no catálogo [!DNL Commerce] e [corresponda-o manualmente](./creating-assigning-catalog-products.md) ao produto. |
| O item no catálogo está desabilitado. | Verifique se o [status do produto](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) está habilitado. |
| O item solicitado está esgotado. | Atualize ou configure as [opções do produto](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) para quantidade e origem. |

Quando os pedidos não puderem ser importados, uma mensagem do sistema semelhante à seguinte será exibida na parte superior da tela:

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

Quando o problema for resolvido, a ordem [!DNL Commerce] será criada na próxima sincronização.

## Com a importação do pedido desativada

Se não quiser importar e gerenciar seus pedidos da Amazon no [!DNL Commerce], você pode alterar a configuração do [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) para `Disabled`. Esta configuração significa que quando novos pedidos são recebidos da Amazon, os pedidos [!DNL Commerce] correspondentes não são criados.

Quando desabilitadas, as informações de pedido recebidas do Amazon aparecem na seção _[!UICONTROL Recent Orders]_do painel de armazenamento e na exibição_[!UICONTROL All Orders]_. Estas informações do pedido são somente para visualização, e você deve gerenciar esses pedidos em [!DNL Amazon Seller Central]. Para abrir os detalhes do pedido em [!DNL Amazon Seller Central], clique no número do pedido do Amazon na coluna _[!UICONTROL Order Number]_.

Consulte também [Exibir Pedidos do Amazon](./amazon-orders-all.md), [Exibir Detalhes do Pedido do Amazon](./amazon-order-details.md) e [Tarefas Comuns de Processamento de Pedidos](./common-order-processing.md).
