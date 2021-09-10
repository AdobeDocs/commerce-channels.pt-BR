---
title: Gerenciar pedidos
description: Você pode habilitar a importação de pedidos nas Configurações do pedido para gerenciar mais facilmente seus pedidos do Amazon com o Administrador do Commerce.
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Gerenciar pedidos

Você pode exibir suas informações de pedido do Amazon, conforme recebidas do Amazon, na seção _[!UICONTROL Recent Orders]_do [painel de armazenamento](./amazon-store-dashboard.md) ou na página_[!UICONTROL Amazon orders]_ (também chamada de _[!UICONTROL All Orders]_exibição).

A forma como você gerencia seus pedidos do Amazon depende se a importação de pedido está ativada ou desativada em suas [Configurações do pedido](./order-settings.md#configure-order-settings).

## Com importação de pedido ativada

Depois de [armazenar integração](./store-integration.md), a configuração [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) é `Enabled` por padrão. Com essa configuração, os pedidos [!DNL Commerce] correspondentes são criados para seus pedidos Amazon e podem ser gerenciados no fluxo de trabalho [[!DNL Commerce] Orders](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;} .

>[!NOTE]
>
>Independentemente das configurações de importação de seus pedidos, os pedidos Amazon que existiam em sua conta [!DNL Amazon Seller Central] antes de sua [integração de loja](./store-integration.md) não são importados.

Os pedidos Amazon importados são gerenciados no fluxo de trabalho [[!DNL Commerce] Orders](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}, exatamente como seus outros [!DNL Commerce] armazenamentos. Clique no número do pedido Amazon na coluna *[!UICONTROL Order Number]* para abrir o pedido no [[!DNL Commerce] processo do pedido](https://docs.magento.com/user-guide/sales/order-processing.html#order-view-descriptions){target=&quot;_blank&quot;}. Consulte [Exibir pedidos da Amazon](./amazon-orders-all.md).

### Processo de importação de pedidos

Quando um pedido é colocado no Amazon e [order import](./order-settings.md) está ativado, o seguinte processo é iniciado.

| Alterar | Ações |
|---|---|
| Um pedido é feito no Amazon. | <ul><li>O Amazon define o status do pedido como `Pending`.</li><li>As informações do pedido são enviadas para [!DNL Commerce].</li><li>A ordem é adicionada à tabela [_Amazon orders_](./amazon-orders-all.md) com um status `Pending`.</li></ul> |
| O Amazon altera o status do pedido para `Unshipped`. | <ul><li>A alteração de status é enviada para [!DNL Commerce].</li><li>Na tabela [_Amazon orders_](./amazon-orders-all.md), o status do pedido muda para `Unshipped`.</li><li>No workflow [[!DNL Commerce] orders](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}, uma ordem [!DNL Commerce] correspondente é criada com um status `Processing`.</li></ul> |
| Em [[!DNL Commerce] orders workflow](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}, a ordem [!DNL Commerce] é processada e o status muda para `Shipped`. | <ul><li>Na tabela [_Amazon orders_](./amazon-orders-all.md), o status do pedido muda para `Shipped`.</li><li>No próximo trabalho cron, o status do pedido muda para `Complete` no [[!DNL Commerce] workflow de pedidos](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}.</li></ul> |

### Bloqueadores de criação de pedidos

Há alguns cenários que impedem a criação da ordem [!DNL Commerce] correspondente. [!DNL Commerce] os pedidos não são criados para pedidos recebidos quando qualquer um dos seguintes problemas ocorrer.

| Cenário | Solução |
|---|---|
| O item não existe no catálogo [!DNL Commerce]. | [Crie a ](./creating-assigning-catalog-products.md) produção em seu  [!DNL Commerce] catálogo e  [faça a correspondência ](./creating-assigning-catalog-products.md) manual ao produto. |
| O item no catálogo está desativado. | Certifique-se de que o [status do produto](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){:target=&quot;_blank&quot;} esteja ativado. |
| O item solicitado está indisponível. | Atualize ou configure as [opções do produto](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){:target=&quot;_blank&quot;} para quantidade e origem. |

Quando os pedidos não podem ser importados, uma mensagem do sistema semelhante à seguinte aparece na parte superior da tela:

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

Quando o problema é resolvido, a ordem [!DNL Commerce] é criada na próxima sincronização.

## Com importação de pedido desativada

Se não quiser importar e gerenciar seus pedidos do Amazon em [!DNL Commerce], é possível alterar a configuração [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) para `Disabled`. Essa configuração significa que, quando novos pedidos são recebidos da Amazon, os pedidos [!DNL Commerce] correspondentes não são criados.

Quando desativado, as informações de pedido recebidas do Amazon são exibidas na seção _[!UICONTROL Recent Orders]_do painel da loja e na visualização_[!UICONTROL All Orders]_. Essas informações de pedido são somente visualização e você deve gerenciar esses pedidos em [!DNL Amazon Seller Central]. Para abrir os detalhes do pedido em [!DNL Amazon Seller Central], clique no número do pedido Amazon na coluna _[!UICONTROL Order Number]_.

Consulte também [Exibir pedidos da Amazon](./amazon-orders-all.md), [Exibir detalhes do pedido da Amazon](./amazon-order-details.md) e [Tarefas de processamento de pedidos comuns](./common-order-processing.md).
