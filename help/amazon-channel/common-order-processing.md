---
title: Tarefas comuns de processamento de pedidos
description: Use o [!DNL Commerce] orders created for Amazon orders to manage order activity and processing in the [!UICONTROL Commerce] Administrador
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# Tarefas comuns de processamento de pedidos

[[!DNL Commerce] processamento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html)O {target=&quot;_blank&quot;} pode gerenciar seus pedidos da Amazon, incluindo enviar emails para o comprador, atender ao pedido (envio), emitir créditos/reembolsos, adicionar comentários e muito mais. Para gerenciar seus pedidos da Amazon, [**Importar pedidos da Amazon**](./order-settings.md) deve ser definida como `Enabled` de forma que [!DNL Commerce] os pedidos são criados quando os pedidos Amazon são recebidos. As informações do pedido da Amazon são exibidas na *[!UICONTROL Recent Orders]* do painel de loja.

Quando ativado, correspondente [!DNL Commerce] os pedidos são criados para pedidos da Amazon, e o número do pedido da Amazon é exibido na _[!UICONTROL Order Number]_coluna. Se uma [!DNL Commerce] o pedido é criado, clique no número do pedido para abrir o pedido na [!DNL Commerce] [processamento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html)página {target=&quot;_blank&quot;}. Você pode gerenciar a ordem como faz com os outros [[!DNL Commerce] processamento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}.

O [!DNL Commerce] o número do pedido não é exibido com o _[!UICONTROL Recent Orders]_informações. O [!DNL Commerce] o número do pedido só é exibido quando você clica no número do pedido no painel da loja e abre o pedido em [[!DNL Commerce] processamento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}. Ao visualizar o [!DNL Commerce] O número do pedido do Amazon é exibido na *[!UICONTROL Payment & Shipping Method]*seção. Também inclui opções para *[!UICONTROL View or Cancel Amazon Order]*e *[!UICONTROL View all Amazon Orders]*, dependendo do status do envio do pedido.

Consulte [cancelar uma ordem não entregue](./cancel-unshipped-order.md).

![Informações do pedido do Amazon no pedido de comércio](assets/amazon-order-number-payment-info.png)

Ao processar um pedido da Amazon, o canal de vendas da Amazon atualiza e sincroniza as informações do pedido com seu [!DNL Amazon Seller Central] conta. As configurações da cron determinam a frequência com que as informações de pedido são sincronizadas entre o canal de vendas da Amazon e da Amazon.

Frequentes [!DNL Commerce] [processamento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html)As tarefas {target=&quot;_blank&quot;} incluem:

- [Ações de pedido](https://docs.magento.com/user-guide/sales/order-actions.html){target=&quot;_blank&quot;}
- [Pesquisa de pedido](https://docs.magento.com/user-guide/sales/orders-search.html){target=&quot;_blank&quot;}
- [Processar um pedido](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}
   - [Exibir um pedido](https://docs.magento.com/user-guide/sales/order-processing.html#view-an-order){target=&quot;_blank&quot;}
   - [Processar um pedido](https://docs.magento.com/user-guide/sales/order-processing.html#process-an-order){target=&quot;_blank&quot;}
   - [Informações de pedido e conta](https://docs.magento.com/user-guide/sales/order-processing.html#order-and-account-information){target=&quot;_blank&quot;}
   - [Informações de endereço](https://docs.magento.com/user-guide/sales/order-processing.html#address-information){target=&quot;_blank&quot;}
   - [Método de Pagamento e Entrega](https://docs.magento.com/user-guide/sales/order-processing.html#payment--shipping-method){target=&quot;_blank&quot;}
   - [Rever itens ordenados](https://docs.magento.com/user-guide/sales/order-processing.html#review-items-ordered){target=&quot;_blank&quot;}
- [Emissão de um crédito/reembolso](https://docs.magento.com/user-guide/sales/credit-memo-create.html){target=&quot;_blank&quot;}
- [Cumprimento/envio de um pedido](https://docs.magento.com/user-guide/sales/shipments-create.html){target=&quot;_blank&quot;}
- [Criar uma fatura](https://docs.magento.com/user-guide/sales/invoice-create.html){target=&quot;_blank&quot;}
- [Cancelar uma ordem não entregue](./cancel-unshipped-order.md)

>[!NOTE]
>
>Se um pedido estiver em `Unshipped` , você pode [cancelar um pedido da Amazon](./cancel-unshipped-order.md) no [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) página. Se um pedido tiver sido enviado, ele não poderá ser cancelado.

Consulte [Gerenciamento de pedidos de comércio](https://docs.magento.com/user-guide/sales/order-management.html){target=&quot;_blank&quot;}.
