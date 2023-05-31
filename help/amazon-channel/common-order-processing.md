---
title: Tarefas comuns de processamento de pedidos do Amazon
description: Use o correspondente [!DNL Commerce] pedidos criados para pedidos Amazon para gerenciar a atividade e o processamento de pedidos na [!UICONTROL Commerce] Admin.
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 6d221c2c2e9a37a42e9d660aceb3c525fedc511d
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# Tarefas comuns de processamento de pedidos do Amazon

[Processamento de pedido de comércio](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) O pode gerenciar seus pedidos do Amazon, incluindo enviar um email ao comprador, atender à ordem (envio), emitir créditos/reembolsos, adicionar comentários e muito mais. Para gerenciar seus pedidos da Amazon, [**Importar Ordens do Amazon**](./order-settings.md) A configuração deve ser definida como `Enabled` de modo que as [!DNL Commerce] os pedidos são criados quando os pedidos do Amazon são recebidos. As informações do pedido do Amazon são exibidas na *[!UICONTROL Recent Orders]* seção do painel de armazenamento.

Quando ativado, o correspondente [!DNL Commerce] são criados para pedidos Amazon e o número do pedido Amazon é exibido na _[!UICONTROL Order Number]_coluna. Se um correspondente [!DNL Commerce] pedido for criado, clique no número do pedido para abrir o pedido na caixa [Processamento de pedido de comércio](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) página. Você pode gerenciar a ordem da mesma maneira que faz com os outros [[!DNL Commerce] processamento de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

A variável [!DNL Commerce] o número do pedido não é exibido com o _[!UICONTROL Recent Orders]_informações. O número da ordem do Commerce é exibido somente quando você clica no número da ordem no painel da loja e abre a ordem em [Processamento de pedido de comércio](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order). Ao visualizar a variável [!DNL Commerce] pedido, o número do pedido Amazon aparece na caixa *[!UICONTROL Payment & Shipping Method]*seção. Também inclui opções para *[!UICONTROL View or Cancel Amazon Order]*e *[!UICONTROL View all Amazon Orders]*, dependendo do status de envio do pedido.

Consulte [cancelar uma ordem não remetida](./cancel-unshipped-order.md).

![Informações do pedido Amazon na ordem do Commerce](assets/amazon-order-number-payment-info.png){width="500"}

Ao processar um pedido do Amazon, o canal de vendas do Amazon atualiza e sincroniza as informações do pedido com o seu [!DNL Amazon Seller Central] conta. Suas configurações de cron determinam com que frequência as informações de pedido são sincronizadas entre o canal de vendas do Amazon e do Amazon.

Comércio comum [processamento de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) as tarefas incluem:

- [Ações do pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#actions)
- [Pesquisa de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#order-search)
- [Processar um pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order)
   - [Exibir um pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#view-an-order)
   - [Processar um pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#process-an-order)
   - [Informações sobre pedidos e contas](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-and-account-information)
   - [Informações de Endereço](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#address-information)
   - [Método de pagamento e envio](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#payment--shipping-method)
   - [Revisar itens solicitados](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#review-items-ordered)
- [Emitir um crédito/reembolso](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memo-create.html)
- [Atendimento/entrega de uma ordem](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/shipments.html#create-a-shipment)
- [Criar uma fatura](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html#create-an-invoice)
- [Cancelar uma ordem não remetida](./cancel-unshipped-order.md)

>[!NOTE]
>
>Se um pedido estiver em `Unshipped` status, você pode [cancelar um pedido do Amazon](./cancel-unshipped-order.md) no [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) página. Se uma ordem tiver sido entregue, ela não poderá ser cancelada.

Consulte [Gerenciamento de pedidos de comércio](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/introduction.html#order-management-and-operations).
