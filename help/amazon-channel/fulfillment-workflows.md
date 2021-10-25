---
title: Fluxos de trabalho de preenchimento do Amazon
description: O atendimento de um pedido de uma listagem da Amazon segue uma sequência específica desde o envio do pedido até o envio.
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Workflows de cumprimento do Amazon

## Exemplo: realizado pelo comerciante

| Etapa | Descrição |
|----|----|
| 1 | **Um pedido realizado pelo comerciante é feito no Amazon.** A Amazon atribui um status de `Pending` até que as informações do cartão de crédito do cliente sejam verificadas. Pedidos em `Pending` O status é importado automaticamente para o canal de vendas do Amazon, mas não é exibido no _[!UICONTROL Orders]_guia . |
| 2 | **O pedido é verificado pela Amazon.** Quando verificado, o Amazon altera o status para `Unshipped`. Com essa alteração de status, o pedido é atualizado no canal de vendas da Amazon e exibido na variável _[!UICONTROL Orders]_guia . |
| 3 | **Os detalhes do pedido são atualizados.** O canal de vendas da Amazon atualiza os detalhes do pedido com o preço, o email do cliente e o nome do cliente. Durante essa atualização, o pedido do Amazon cria o [!DNL Commerce] pedido na página de gerenciamento de pedidos. O [!DNL Commerce] o número do pedido é exibido com as informações do pedido no _[!UICONTROL Orders]_guia . |
| 4 | **Uma nova conta de cliente é criada.** Se configurado nas configurações do pedido, o cliente não existe em seu [!DNL Commerce] , um novo cliente é criado em seu [!DNL Commerce] banco de dados usando as informações correspondentes do cliente do pedido da Amazon. Se você escolher `No Customer Creation (guest)` nas configurações do seu pedido, a ordem segue o [!DNL Commerce] processo de convidado e não criar um cliente no banco de dados. Nesse momento, se o [!DNL Commerce] O sistema é integrado a um ERP/OMS/WMS, o pedido é recebido de acordo com a integração de um novo pedido que está sendo colocado e criado dentro de [!DNL Commerce]. |
| 5 | **O pedido é enviado.** No [!DNL Commerce] na página de processamento do pedido, envie o pedido e adicione um número de rastreamento. Quando todos os itens estão marcados em um `Shipped` status:<ul><li>O status da variável [!DNL Commerce] alterar a ordem para `Complete`.</li><li>O status da ordem do canal de vendas da Amazon muda para `Shipped`.</li><li>O número de rastreamento é sincronizado com o Amazon, e o status do pedido no Amazon muda para `Shipped`.</li><li>As notificações de remessa são enviadas ao cliente via Amazon, não de [!DNL Commerce] (de acordo com as políticas da Amazon). |

## Exemplo: realizado pela Amazon (FBA)

| Etapa | Descrição |
|---|---|
| 1 | **Um pedido preenchido pela Amazon é feito no Amazon.** |
| 2 | **O pedido é importado.** O pedido não é importado para o canal de vendas da Amazon até que o pedido seja atribuído `Shipped` status pela Amazon. Como a Amazon tem o inventário para este produto, ele evita interferência com o gerenciamento de depósito/inventário. |
| 3 | **Os detalhes do pedido são atualizados.** Se configurado em [configurações de ordem](./order-settings.md), a ordem do Amazon cria o [!DNL Commerce] pedido e ser criado como um pedido com status de `Complete`. |
