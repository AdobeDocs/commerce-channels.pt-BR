---
title: Fluxos de trabalho de preenchimento do Amazon
description: O preenchimento de uma ordem de uma lista Amazon segue uma sequência específica, desde a submissão até a entrega.
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Fluxos de trabalho de preenchimento do Amazon

## Exemplo: preenchido pelo comerciante

| Etapa | Descrição |
|----|----|
| 1 | **Um pedido preenchido pelo comerciante é feito no Amazon.** O Amazon atribui um status de `Pending` até que as informações de cartão de crédito do cliente sejam verificadas. Pedidos em `Pending` status automaticamente importar para o canal de vendas do Amazon, mas não exibir no _[!UICONTROL Orders]_guia. |
| 2 | **O pedido é verificado pela Amazon.** Quando verificado, o Amazon altera o status para `Unshipped`. Com essa alteração de status, o pedido é atualizado no canal de vendas da Amazon e aparece na _[!UICONTROL Orders]_guia. |
| 3 | **Os detalhes do pedido são atualizados.** O canal de vendas da Amazon atualiza os detalhes do pedido com o preço, email do cliente e nome do cliente. Durante essa atualização, o pedido do Amazon cria a solicitação [!DNL Commerce] pedido na página de gerenciamento de pedidos. A variável [!DNL Commerce] o número do pedido é exibido com as informações sobre o pedido no _[!UICONTROL Orders]_guia. |
| 4 | **Uma nova conta de cliente é criada.** Se estiver configurado nas configurações do pedido e o cliente não existir no [!DNL Commerce] banco de dados, um novo cliente será criado em seu [!DNL Commerce] usando as informações correspondentes do cliente no pedido do Amazon. Se você escolher `No Customer Creation (guest)` nas configurações do seu pedido, o pedido segue o [!DNL Commerce] processo de convidado e não criar um cliente no banco de dados. Neste ponto, se o seu [!DNL Commerce] for integrado a um ERP/OMS/WMS, o pedido será recebido de acordo com a integração de um novo pedido que estiver sendo feito e criado dentro [!DNL Commerce]. |
| 5 | **A ordem é remetida.** No [!DNL Commerce] processamento de pedidos, você envia o pedido e adiciona um número de rastreamento. Quando todos os itens estiverem marcados em uma `Shipped` Status:<ul><li>O status do [!DNL Commerce] alterações do pedido em `Complete`.</li><li>O status da ordem do canal de vendas do Amazon muda para `Shipped`.</li><li>O número de rastreamento é sincronizado com o Amazon e o status do pedido no Amazon muda para `Shipped`.</li><li>As notificações de envio são enviadas ao cliente por meio do Amazon, não do [!DNL Commerce] (de acordo com as políticas da Amazon). |

## Exemplo: preenchido pelo Amazon (FBA)

| Etapa | Descrição |
|---|---|
| 1 | **Um pedido preenchido pela Amazon é feito no Amazon.** |
| 2 | **A ordem é importada.** O pedido não é importado para o canal de vendas do Amazon até que o pedido seja atribuído ao `Shipped` Status por Amazon. Como a Amazon tem o inventário para este produto, isso evita a interferência com o gerenciamento de depósito/inventário. |
| 3 | **Os detalhes do pedido são atualizados.** Se configurado no seu [configurações do pedido](./order-settings.md), o pedido do Amazon cria o correspondente [!DNL Commerce] pedido e ser criado como um pedido com um status de `Complete`. |
