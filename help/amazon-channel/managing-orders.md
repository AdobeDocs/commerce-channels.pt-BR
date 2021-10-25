---
title: Gerenciar pedidos
description: Você pode habilitar a importação de pedidos nas Configurações do pedido para gerenciar mais facilmente seus pedidos do Amazon com o Administrador do Commerce.
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: 1d1b888db4de4f6e3658af768cd6f5cf30828788
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Gerenciar pedidos

Você pode exibir suas informações de pedido da Amazon, conforme recebidas da Amazon, no _[!UICONTROL Recent Orders]_da seção [painel de loja](./amazon-store-dashboard.md) ou na_[!UICONTROL Amazon orders]_ (também chamada de _[!UICONTROL All Orders]_).

A forma como você gerencia seus pedidos do Amazon depende se a importação de pedidos está ativada ou desativada em seu [Configurações da ordem](./order-settings.md#configure-order-settings).

## Com importação de pedido ativada

Depois [integração de loja](./store-integration.md), o [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) é `Enabled` por padrão. Com essa configuração, [!DNL Commerce] os pedidos são criados para seus pedidos da Amazon e podem ser gerenciados na variável [[!DNL Commerce] Pedidos](https://docs.magento.com/user-guide/sales/orders.html)Fluxo de trabalho {target=&quot;_blank&quot;}.

>[!NOTE]
>
>Independentemente das configurações de importação de seu pedido, os pedidos Amazon que existiam em seu [!DNL Amazon Seller Central] antes da [integração de loja](./store-integration.md) não são importados.

Os pedidos importados do Amazon são gerenciados na [[!DNL Commerce] Pedidos](https://docs.magento.com/user-guide/sales/orders.html)Fluxo de trabalho {target=&quot;_blank&quot;}, exatamente como o outro [!DNL Commerce] lojas. Clique no número do pedido da Amazon na *[!UICONTROL Order Number]* para abrir a ordem na coluna [[!DNL Commerce] processo de pedido](https://docs.magento.com/user-guide/sales/order-processing.html#order-view-descriptions){target=&quot;_blank&quot;}. Consulte [Exibir pedidos da Amazon](./amazon-orders-all.md).

### Processo de importação de pedidos

Quando um pedido é feito no Amazon e [importação de pedidos](./order-settings.md) estiver habilitado, o seguinte processo será iniciado.

| Alterar | Ações |
|---|---|
| Um pedido é feito no Amazon. | <ul><li>O Amazon define o status do pedido como `Pending`.</li><li>As informações do pedido são enviadas para [!DNL Commerce].</li><li>A ordem é adicionada a [_Pedidos Amazon_ tabela](./amazon-orders-all.md) com um `Pending` status.</li></ul> |
| O Amazon altera o status do pedido para `Unshipped`. | <ul><li>A alteração de status é enviada para [!DNL Commerce].</li><li>No [_Pedidos Amazon_ tabela](./amazon-orders-all.md), o status do pedido muda para `Unshipped`.</li><li>No [[!DNL Commerce] fluxo de trabalho de pedidos](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}, um [!DNL Commerce] a ordem é criada com um `Processing` status.</li></ul> |
| Em [[!DNL Commerce] fluxo de trabalho de pedidos](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}, a variável [!DNL Commerce] a ordem é processada e o status muda para `Shipped`. | <ul><li>No [_Pedidos Amazon_ tabela](./amazon-orders-all.md), o status do pedido muda para `Shipped`.</li><li>No próximo trabalho de cron, o status do pedido muda para `Complete` no [[!DNL Commerce] fluxo de trabalho de pedidos](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}.</li></ul> |

### Bloqueadores de criação de pedidos

Há alguns cenários que impedem a criação do [!DNL Commerce] ordem. [!DNL Commerce] os pedidos não são criados para pedidos recebidos quando qualquer um dos seguintes problemas ocorrer.

| Cenário | Solução |
|---|---|
| O item não existe no [!DNL Commerce] catálogo. | [Criar o produto](./creating-assigning-catalog-products.md) em seu [!DNL Commerce] catálogo e [correspondência manual](./creating-assigning-catalog-products.md) ao produto. |
| O item no catálogo está desativado. | Certifique-se de que a variável [status do produto](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){target=&quot;_blank&quot;} está habilitado. |
| O item solicitado está indisponível. | Atualize ou configure o [opções do produto](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){target=&quot;_blank&quot;} para quantidade e origem. |

Quando os pedidos não podem ser importados, uma mensagem do sistema semelhante à seguinte aparece na parte superior da tela:

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

Quando o problema for resolvido, a variável [!DNL Commerce] A ordem é criada na próxima sincronização.

## Com importação de pedido desativada

Se você não quiser importar e gerenciar seus pedidos da Amazon em [!DNL Commerce], é possível alterar a variável [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) configurar para `Disabled`. Essa configuração significa que, quando novos pedidos são recebidos da Amazon, o [!DNL Commerce] os pedidos não são criados.

Quando desativado, as informações de pedido recebidas da Amazon serão exibidas na variável _[!UICONTROL Recent Orders]_no painel da loja e na_[!UICONTROL All Orders]_ exibir. Essas informações do pedido são somente visualização e você deve gerenciar esses pedidos em [!DNL Amazon Seller Central]. Para abrir os detalhes do pedido em [!DNL Amazon Seller Central], clique no número do pedido da Amazon na _[!UICONTROL Order Number]_coluna.

Consulte também [Exibir pedidos da Amazon](./amazon-orders-all.md), [Exibir detalhes do pedido da Amazon](./amazon-order-details.md)e [Tarefas comuns de processamento de pedidos](./common-order-processing.md).
