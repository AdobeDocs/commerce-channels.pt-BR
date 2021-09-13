---
title: Tarefas comuns de processamento de pedidos
description: Use o  [!DNL Commerce] orders created for Amazon orders to manage order activity and processing in the [!UICONTROL Commerce] Admin correspondente.
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Tarefas comuns de processamento de pedidos

[[!DNL Commerce] o processamento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;} pode gerenciar seus pedidos da Amazon, incluindo enviar emails ao comprador, atender ao pedido (envio), emitir créditos/reembolsos, adicionar comentários e muito mais. Para gerenciar seus pedidos do Amazon, sua configuração [**Importar pedidos do Amazon**](./order-settings.md) deve ser definida como `Enabled` para que os pedidos [!DNL Commerce] correspondentes sejam criados quando os pedidos do Amazon são recebidos. As informações do pedido Amazon são exibidas na seção *[!UICONTROL Recent Orders]* do painel da loja.

Quando ativados, os pedidos [!DNL Commerce] correspondentes são criados para pedidos Amazon e o número de pedido Amazon é exibido na coluna _[!UICONTROL Order Number]_. Se uma ordem [!DNL Commerce] correspondente for criada, clique no número do pedido para abrir o pedido na página [!DNL Commerce] [processamento do pedido](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}. Você pode gerenciar a ordem como faz com seus outros [[!DNL Commerce] processamento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}.

O número do pedido [!DNL Commerce] não é exibido com as informações _[!UICONTROL Recent Orders]_. O número do pedido [!DNL Commerce] só é exibido quando você clica no número do pedido no painel da loja e abre o pedido em [[!DNL Commerce] processamento do pedido](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}. Ao visualizar a ordem [!DNL Commerce], o número do pedido do Amazon aparece na seção *[!UICONTROL Payment & Shipping Method]*. Também inclui opções para *[!UICONTROL View or Cancel Amazon Order]*e *[!UICONTROL View all Amazon Orders]*, dependendo do status do envio do pedido.

Consulte [cancelar um pedido não entregue](./cancel-unshipped-order.md).

![Informações do pedido do Amazon no pedido de comércio](assets/amazon-order-number-payment-info.png)

Ao processar um pedido da Amazon, o canal de vendas da Amazon atualiza e sincroniza as informações do pedido com sua conta [!DNL Amazon Seller Central]. As configurações da cron determinam a frequência com que as informações de pedido são sincronizadas entre o canal de vendas da Amazon e da Amazon.

As tarefas comuns [!DNL Commerce] [de processamento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;} incluem:

- [Ações de Pedido](https://docs.magento.com/user-guide/sales/order-actions.html){target=&quot;_blank&quot;}
- [Pesquisa de pedidos](https://docs.magento.com/user-guide/sales/orders-search.html){target=&quot;_blank&quot;}
- [Processar um pedido](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}
   - [Exibir um pedido](https://docs.magento.com/user-guide/sales/order-processing.html#view-an-order){target=&quot;_blank&quot;}
   - [Processar um pedido](https://docs.magento.com/user-guide/sales/order-processing.html#process-an-order){target=&quot;_blank&quot;}
   - [Informações da ordem e da conta](https://docs.magento.com/user-guide/sales/order-processing.html#order-and-account-information){target=&quot;_blank&quot;}
   - [Informações de endereço](https://docs.magento.com/user-guide/sales/order-processing.html#address-information){target=&quot;_blank&quot;}
   - [Método de Pagamento e Entrega](https://docs.magento.com/user-guide/sales/order-processing.html#payment--shipping-method){target=&quot;_blank&quot;}
   - [Revisar itens pedidos](https://docs.magento.com/user-guide/sales/order-processing.html#review-items-ordered){target=&quot;_blank&quot;}
- [Emitir um crédito/reembolso](https://docs.magento.com/user-guide/sales/credit-memo-create.html){target=&quot;_blank&quot;}
- [Preenchendo/enviando um pedido](https://docs.magento.com/user-guide/sales/shipments-create.html){target=&quot;_blank&quot;}
- [Criar uma fatura](https://docs.magento.com/user-guide/sales/invoice-create.html){target=&quot;_blank&quot;}
- [Cancelar uma ordem não entregue](./cancel-unshipped-order.md)

>[!NOTE]
>
>Se um pedido estiver no status `Unshipped` , você poderá [cancelar um pedido Amazon](./cancel-unshipped-order.md) na página [[!UICONTROL Amazon Order Details]](./amazon-order-details.md). Se um pedido tiver sido enviado, ele não poderá ser cancelado.

Consulte [Gerenciamento de Ordem de Comércio](https://docs.magento.com/user-guide/sales/order-management.html){target=&quot;_blank&quot;}.
