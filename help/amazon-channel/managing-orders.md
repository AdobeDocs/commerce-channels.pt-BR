---
title: Gerenciar pedidos do Amazon
description: Você pode ativar a importação de pedidos nas Configurações de pedidos para gerenciar mais facilmente os pedidos do Amazon com o administrador do Commerce.
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Gerenciar pedidos do Amazon

Você pode visualizar as informações do pedido do Amazon, conforme recebidas da Amazon, no _[!UICONTROL Recent Orders]_seção do [painel de armazenamento](./amazon-store-dashboard.md) ou no_[!UICONTROL Amazon orders]_ página (também chamada de _[!UICONTROL All Orders]_exibir).

A forma como você gerencia os pedidos do Amazon depende de a importação do pedido estar ativada ou desativada no [Configurações do pedido](./order-settings.md#configure-order-settings).

## Com a importação da ordem ativada

Depois [integração de loja](./store-integration.md), o [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) a configuração é `Enabled` por padrão. Com essa configuração, o correspondente a [!DNL Commerce] são criados para seus pedidos da Amazon e podem ser gerenciados no [[!DNL Commerce] Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) fluxo de trabalho.

>[!NOTE]
>
>Independentemente das configurações de importação do seu pedido, os pedidos do Amazon que existiam em seu [!DNL Amazon Seller Central] antes da sua [integração de loja](./store-integration.md) não são importados.

Os pedidos Amazon importados são gerenciados na [[!DNL Commerce] Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) fluxo de trabalho, exatamente como o seu outro [!DNL Commerce] lojas. Clique no número do pedido Amazon na caixa *[!UICONTROL Order Number]* coluna para abrir a ordem na [[!DNL Commerce] processo de pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-view-descriptions). Consulte [Exibir Pedidos do Amazon](./amazon-orders-all.md).

### Processo de importação de ordem

Quando um pedido é feito no Amazon e [importação de ordem](./order-settings.md) estiver ativado, o processo a seguir será iniciado.

| Alterar | Ações |
|---|---|
| Um pedido é feito no Amazon. | <ul><li>O Amazon define o status do pedido como `Pending`.</li><li>As informações do pedido são enviadas para [!DNL Commerce].</li><li>O pedido é adicionado a [_Pedidos do Amazon_ tabela](./amazon-orders-all.md) com um `Pending` status.</li></ul> |
| O Amazon altera o status do pedido para `Unshipped`. | <ul><li>A alteração de status é enviada para [!DNL Commerce].</li><li>No [_Pedidos do Amazon_ tabela](./amazon-orders-all.md), o status do pedido muda para `Unshipped`.</li><li>No [[!DNL Commerce] fluxo de trabalho de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html), um correspondente [!DNL Commerce] o pedido é criado com um `Processing` status.</li></ul> |
| Entrada [[!DNL Commerce] fluxo de trabalho de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html), o [!DNL Commerce] pedido for processado e o status for alterado para `Shipped`. | <ul><li>No [_Pedidos do Amazon_ tabela](./amazon-orders-all.md), o status do pedido muda para `Shipped`.</li><li>No próximo trabalho cron, o status do pedido muda para `Complete` no [[!DNL Commerce] fluxo de trabalho de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).</li></ul> |

### Bloqueadores de criação de pedidos

Existem alguns cenários que impedem a criação dos correspondentes [!DNL Commerce] pedido. [!DNL Commerce] os pedidos não são criados para pedidos que são recebidos quando qualquer um dos seguintes problemas ocorrer.

| Cenário | Solução |
|---|---|
| O item não existe no [!DNL Commerce] catálogo. | [Criar o produto](./creating-assigning-catalog-products.md) no seu [!DNL Commerce] catálogo e [correspondência manual](./creating-assigning-catalog-products.md) ao produto. |
| O item no catálogo está desabilitado. | Certifique-se de que a variável [status do produto](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) está ativado. |
| O item solicitado está esgotado. | Atualize ou configure o [opções de produto](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) para quantidade e origem. |

Quando os pedidos não puderem ser importados, uma mensagem do sistema semelhante à seguinte será exibida na parte superior da tela:

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

Quando o problema for resolvido, a variável [!DNL Commerce] pedido é criado na próxima sincronização.

## Com a importação do pedido desativada

Se não quiser importar e gerenciar seus pedidos do Amazon no [!DNL Commerce], você pode alterar a [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) configuração para `Disabled`. Essa configuração significa que, quando novos pedidos forem recebidos da Amazon, as solicitações [!DNL Commerce] os pedidos não são criados.

Quando desativadas, as informações do pedido recebidas do Amazon são exibidas na _[!UICONTROL Recent Orders]_do painel de armazenamento e na guia_[!UICONTROL All Orders]_ exibição. Estas informações do pedido são somente para visualização e você deve gerenciar esses pedidos em [!DNL Amazon Seller Central]. Para abrir os detalhes do pedido em [!DNL Amazon Seller Central], clique no número do pedido Amazon na caixa _[!UICONTROL Order Number]_coluna.

Consulte também [Exibir Pedidos do Amazon](./amazon-orders-all.md), [Exibir detalhes do pedido Amazon](./amazon-order-details.md), e [Tarefas de Processamento de Pedido Comum](./common-order-processing.md).
