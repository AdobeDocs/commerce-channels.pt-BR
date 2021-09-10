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
| 1 | **Um pedido realizado pelo comerciante é feito no Amazon.** A Amazon atribui um status de  `Pending` até que as informações do cartão de crédito do cliente sejam verificadas. Os pedidos no status `Pending` são importados automaticamente para o canal de vendas do Amazon, mas não são exibidos na guia _[!UICONTROL Orders]_. |
| 2 | **O pedido é verificado pela Amazon.** Quando verificado, o Amazon altera o status para  `Unshipped`. Com essa alteração de status, o pedido é atualizado no canal de vendas da Amazon e exibido na guia _[!UICONTROL Orders]_. |
| 1 | **Os detalhes do pedido são atualizados.** O canal de vendas da Amazon atualiza os detalhes do pedido com o preço, o email do cliente e o nome do cliente. Durante essa atualização, a ordem do Amazon cria a ordem [!DNL Commerce] correspondente na página de gerenciamento de pedidos. O número do pedido [!DNL Commerce] é exibido com as informações do pedido na guia _[!UICONTROL Orders]_. |
| 4 | **Uma nova conta de cliente é criada.** Se configurado nas configurações do pedido e o cliente não existir no  [!DNL Commerce] banco de dados, um novo cliente será criado no  [!DNL Commerce] banco de dados usando as informações correspondentes do cliente do pedido da Amazon. Se você escolher `No Customer Creation (guest)` nas configurações do pedido, a ordem seguirá o processo de convidado [!DNL Commerce] e não criará um cliente no banco de dados. Neste ponto, se o sistema [!DNL Commerce] estiver integrado a um ERP/OMS/WMS, o pedido será recebido de acordo com a integração de um novo pedido que está sendo colocado e criado dentro de [!DNL Commerce]. |
| 5 | **O pedido é enviado.** Na página de processamento do  [!DNL Commerce] pedido, é possível enviar o pedido e adicionar um número de rastreamento. Quando todos os itens estão marcados em um status `Shipped` :<ul><li>O status da ordem [!DNL Commerce] muda para `Complete`.</li><li>O status da ordem do canal de vendas da Amazon muda para `Shipped`.</li><li>O número de rastreamento é sincronizado com o Amazon, e o status do pedido no Amazon muda para `Shipped`.</li><li>As notificações de remessa são enviadas ao cliente por meio da Amazon, não de [!DNL Commerce] (de acordo com as políticas da Amazon). |

## Exemplo: realizado pela Amazon (FBA)

| Etapa | Descrição |
|---|---|
| 1 | **Um pedido preenchido pela Amazon é feito no Amazon.** |
| 2 | **O pedido é importado.** O pedido não é importado para o canal de vendas da Amazon até que o  `Shipped` status do pedido seja atribuído pelo Amazon. Como a Amazon tem o inventário para este produto, ele evita interferência com o gerenciamento de depósito/inventário. |
| 1 | **Os detalhes do pedido são atualizados.** Se configurado nas configurações [ do ](./order-settings.md)pedido, o pedido da Amazon cria o  [!DNL Commerce] pedido correspondente e é criado como um pedido com status de  `Complete`. |
