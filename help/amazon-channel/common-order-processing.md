---
title: Tarefas comuns de processamento de pedidos do Amazon
description: Use os  [!DNL Commerce] pedidos correspondentes criados para pedidos do Amazon para gerenciar a atividade e o processamento de pedidos no Administrador [!UICONTROL Commerce].
feature: Sales Channels, Orders
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Tarefas comuns de processamento de pedidos do Amazon

[o processamento de pedidos da Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) pode gerenciar seus pedidos da Amazon, inclusive enviar um email ao comprador, atender ao pedido (envio), emitir créditos/reembolsos, adicionar comentários e muito mais. Para gerenciar seus pedidos do Amazon, a configuração [**Importar Pedidos do Amazon**](./order-settings.md) deve ser definida como `Enabled` para que os pedidos [!DNL Commerce] correspondentes sejam criados quando os pedidos do Amazon forem recebidos. As informações do pedido do Amazon são exibidas na seção *[!UICONTROL Recent Orders]* do painel de armazenamento.

Quando habilitados, os pedidos [!DNL Commerce] correspondentes são criados para pedidos Amazon, e o número do pedido Amazon é exibido na coluna _[!UICONTROL Order Number]_. Se um pedido [!DNL Commerce] correspondente for criado, clique no número do pedido para abrir o pedido na página [processamento de pedido do Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order). Você pode gerenciar o pedido como faz com seu outro [[!DNL Commerce] processamento de pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

O número de pedido [!DNL Commerce] não é exibido com as informações _[!UICONTROL Recent Orders]_. O número do pedido do Commerce só é exibido quando você clica no número do pedido no painel da loja e abre o pedido em [processamento de pedido do Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order). Ao exibir o pedido [!DNL Commerce], o número do Pedido Amazon aparece na seção *[!UICONTROL Payment & Shipping Method]*. Também inclui opções para *[!UICONTROL View or Cancel Amazon Order]*e *[!UICONTROL View all Amazon Orders]*, dependendo do status de remessa do pedido.

Consulte [cancelar uma ordem não remetida](./cancel-unshipped-order.md).

![Informações do pedido Amazon no pedido Commerce](assets/amazon-order-number-payment-info.png){width="500"}

Ao processar um pedido do Amazon, o canal de vendas do Amazon atualiza e sincroniza as informações do pedido com a conta do [!DNL Amazon Seller Central]. Suas configurações de cron determinam com que frequência as informações de pedido são sincronizadas entre o canal de vendas do Amazon e do Amazon.

As tarefas comuns de [processamento de pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) do Commerce incluem:

- [Solicitar ações](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#actions)
- [Pesquisa de Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#order-search)
- [Processar um pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order)
   - [Exibir um pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#view-an-order)
   - [Processar um pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#process-an-order)
   - [Informações sobre pedidos e contas](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-and-account-information)
   - [Informações de Endereço](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#address-information)
   - [Método de pagamento e envio](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#payment--shipping-method)
   - [Revisar itens solicitados](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#review-items-ordered)
- [Emitindo um crédito/reembolso](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memo-create.html)
- [Preenchendo/enviando um pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/shipments.html#create-a-shipment)
- [Criar uma fatura](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html#create-an-invoice)
- [Cancelar uma ordem não remetida](./cancel-unshipped-order.md)

>[!NOTE]
>
>Se um pedido estiver com o status `Unshipped`, você poderá [cancelar um pedido de Amazon](./cancel-unshipped-order.md) na página [[!UICONTROL Amazon Order Details]](./amazon-order-details.md). Se uma ordem tiver sido entregue, ela não poderá ser cancelada.

Consulte [Commerce Order Management](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/introduction.html#order-management-and-operations).
