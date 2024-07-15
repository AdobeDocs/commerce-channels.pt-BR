---
title: Fluxos de trabalho de preenchimento do Amazon
description: O preenchimento de uma ordem de uma lista Amazon segue uma sequência específica, desde a submissão até a entrega.
feature: Sales Channels, Orders, Shipping/Delivery
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Fluxos de trabalho de preenchimento do Amazon

## Exemplo: preenchido pelo comerciante

| Etapa | Descrição |
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 | **Um pedido preenchido pelo comerciante é feito no Amazon.O** Amazon atribuirá um status de `Pending` até que as informações de cartão de crédito do cliente sejam verificadas. Os pedidos no status `Pending` são importados automaticamente para o canal de vendas do Amazon, mas não são exibidos na guia _[!UICONTROL Orders]_. |
| 2 | **A ordem foi verificada pela Amazon.** Quando verificado, o Amazon altera o status para `Unshipped`. Com essa alteração de status, o pedido é atualizado no canal de vendas da Amazon e aparece na guia _[!UICONTROL Orders]_. |
| 3 | **Os detalhes do pedido são atualizados.O canal de vendas do Amazon** atualiza os detalhes do pedido com o preço, email do cliente e nome do cliente. Durante essa atualização, o pedido do Amazon cria o pedido [!DNL Commerce] correspondente na página de gerenciamento de pedidos. O número do pedido [!DNL Commerce] é exibido com as informações do pedido na guia _[!UICONTROL Orders]_. |
| 4 | **Uma nova conta de cliente é criada.** Se definido nas configurações do seu pedido e o cliente não existir no banco de dados [!DNL Commerce], um novo cliente será criado no banco de dados [!DNL Commerce] usando as informações correspondentes do cliente no pedido Amazon. Se você escolheu `No Customer Creation (guest)` nas configurações do pedido, o pedido segue o processo de convidado de [!DNL Commerce] e não cria um cliente no banco de dados. Neste ponto, se o seu sistema [!DNL Commerce] estiver integrado a um ERP/OMS/WMS, o pedido será recebido de acordo com a integração de um novo pedido que está sendo feito e criado dentro de [!DNL Commerce]. |
| 5 | **A ordem foi remetida.** Na página de processamento de pedidos [!DNL Commerce], você envia o pedido e adiciona um número de rastreamento. Quando todos os itens estiverem marcados em um status `Shipped`:<ul><li>O status da ordem [!DNL Commerce] muda para `Complete`.</li><li>O status da ordem do canal de vendas da Amazon muda para `Shipped`.</li><li>O número de rastreamento é sincronizado com o Amazon, e o status do pedido no Amazon muda para `Shipped`.</li><li>As notificações de remessa são enviadas ao cliente por meio do Amazon, não de [!DNL Commerce] (de acordo com as políticas da Amazon). |

## Exemplo: preenchido pelo Amazon (FBA)

| Etapa | Descrição |
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 | **Um pedido preenchido pela Amazon é feito no Amazon.** |
| 2 | **A ordem foi importada.** O pedido não é importado para o canal de vendas da Amazon até que o pedido receba o status `Shipped` pela Amazon. Como a Amazon tem o inventário para este produto, isso evita a interferência com o gerenciamento de depósito/inventário. |
| 3 | **Os detalhes do pedido são atualizados.** Se configurado nas [configurações do pedido](./order-settings.md), o pedido do Amazon cria o pedido [!DNL Commerce] correspondente e é criado como um pedido com o status `Complete`. |
