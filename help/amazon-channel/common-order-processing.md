---
title: Tarefas de Processamento de Pedido Comum
description: Use o correspondente [!DNL Commerce] pedidos criados para pedidos Amazon para gerenciar a atividade e o processamento de pedidos na [!UICONTROL Commerce] Admin.
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Tarefas de Processamento de Pedido Comum

[[!DNL Commerce] processamento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"} O pode gerenciar seus pedidos do Amazon, incluindo enviar um email ao comprador, atender à ordem (envio), emitir créditos/reembolsos, adicionar comentários e muito mais. Para gerenciar seus pedidos da Amazon, [**Importar Ordens do Amazon**](./order-settings.md) A configuração deve ser definida como `Enabled` de modo que as [!DNL Commerce] os pedidos são criados quando os pedidos do Amazon são recebidos. As informações do pedido do Amazon são exibidas na *[!UICONTROL Recent Orders]* seção do painel de armazenamento.

Quando ativado, o correspondente [!DNL Commerce] são criados para pedidos Amazon e o número do pedido Amazon é exibido na _[!UICONTROL Order Number]_coluna. Se um correspondente [!DNL Commerce] pedido for criado, clique no número do pedido para abrir o pedido na caixa [!DNL Commerce] [processamento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"} page. You can manage the order as you do your other [[!DNL Commerce] order processing](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"}.

A variável [!DNL Commerce] o número do pedido não é exibido com o _[!UICONTROL Recent Orders]_informações. A variável [!DNL Commerce] o número do pedido só é exibido quando você clica no número do pedido no painel da loja e abre o pedido em [[!DNL Commerce] processamento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"}. Ao visualizar a variável [!DNL Commerce] pedido, o número do pedido Amazon aparece na caixa *[!UICONTROL Payment & Shipping Method]*seção. Também inclui opções para *[!UICONTROL View or Cancel Amazon Order]*e *[!UICONTROL View all Amazon Orders]*, dependendo do status de envio do pedido.

Consulte [cancelar uma ordem não remetida](./cancel-unshipped-order.md).

![Informações do pedido Amazon na ordem do Commerce](assets/amazon-order-number-payment-info.png)

Ao processar um pedido do Amazon, o canal de vendas do Amazon atualiza e sincroniza as informações do pedido com o seu [!DNL Amazon Seller Central] conta. Suas configurações de cron determinam com que frequência as informações de pedido são sincronizadas entre o canal de vendas do Amazon e do Amazon.

Comum [!DNL Commerce] [processamento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"} as tarefas incluem:

- [Ações do pedido](https://docs.magento.com/user-guide/sales/order-actions.html){target="_blank"}
- [Pesquisa de pedidos](https://docs.magento.com/user-guide/sales/orders-search.html){target="_blank"}
- [Processar um pedido](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"}
   - [Exibir um pedido](https://docs.magento.com/user-guide/sales/order-processing.html#view-an-order){target="_blank"}
   - [Processar um pedido](https://docs.magento.com/user-guide/sales/order-processing.html#process-an-order){target="_blank"}
   - [Informações sobre pedidos e contas](https://docs.magento.com/user-guide/sales/order-processing.html#order-and-account-information){target="_blank"}
   - [Informações de Endereço](https://docs.magento.com/user-guide/sales/order-processing.html#address-information){target="_blank"}
   - [Método de pagamento e envio](https://docs.magento.com/user-guide/sales/order-processing.html#payment--shipping-method){target="_blank"}
   - [Revisar itens solicitados](https://docs.magento.com/user-guide/sales/order-processing.html#review-items-ordered){target="_blank"}
- [Emitir um crédito/reembolso](https://docs.magento.com/user-guide/sales/credit-memo-create.html){target="_blank"}
- [Atendimento/entrega de uma ordem](https://docs.magento.com/user-guide/sales/shipments-create.html){target="_blank"}
- [Criar uma fatura](https://docs.magento.com/user-guide/sales/invoice-create.html){target="_blank"}
- [Cancelar uma ordem não remetida](./cancel-unshipped-order.md)

>[!NOTE]
>
>Se um pedido estiver em `Unshipped` status, você pode [cancelar um pedido do Amazon](./cancel-unshipped-order.md) no [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) página. Se uma ordem tiver sido entregue, ela não poderá ser cancelada.

Consulte [Gerenciamento de pedidos de comércio](https://docs.magento.com/user-guide/sales/order-management.html){target="_blank"}.
