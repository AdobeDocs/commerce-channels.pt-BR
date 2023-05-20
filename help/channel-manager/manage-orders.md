---
title: 'Exibir e gerenciar pedidos de [!DNL Channel Manager]'
description: 'Exibir e gerenciar [!DNL Walmart Marketplace] pedidos com [!DNL Channel Manager] para Adobe Commerce e Magento Open Source.'
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# Exibir e rastrear pedidos a partir de [!DNL Channel Manager]

[!DNL Walmart Marketplace] dados do pedido para [!DNL Commerce] produtos sincroniza automaticamente com o [!DNL Channel Manager] após [!DNL Walmart] processa a ordem.

No [!DNL Commerce] além disso, uma sincronização bem-sucedida aciona as seguintes ações:

- [!DNL Channel Manager] envia uma confirmação de pedido ao Walmart.

- Um correspondente [!DNL Commerce] pedido é criado a partir do pedido do Walmart.

- As informações atualizadas do pedido são exibidas na [!DNL Channel Manager] Painel de pedidos.

No Administrador da loja, é possível visualizar os dados de pedidos em [!DNL Channel Manager] abrindo a loja do canal de vendas e selecionando **[!UICONTROL Orders]**.

![Gerenciador de canal - exibição de Pedidos para gerenciar [!DNL Walmart Marketplace] pedidos](assets/orders-dashboard-view.png)

>[!NOTE]
>
>Pode levar até 35 minutos para uma [!DNL Walmart Marketplace] para exibir no [!DNL Channel Manager] lista de pedidos. [!DNL Walmart] O requer aproximadamente 30 minutos para processar pedidos recebidos e enviá-los para o [!DNL Channel Manager]. Depois que o Gerenciador de canais receber o pedido, ele levará aproximadamente mais cinco minutos para criar e exibir o pedido no Adobe Commerce ou no Magento Open Source.

## Controles de Pedidos e Descrições de Coluna

As tabelas a seguir descrevem os controles e colunas disponíveis para Pedidos.

**Controles para[!UICONTROL Orders]**

<table>
<tr>
<td><strong>Controle</strong></td>
<td><strong>Descrição</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter orders]</td>
<td>Classifique a exibição selecionando uma das opções [!UICONTROL Order Status] cartões.</td>
</tr>
<tr>
<td>Detalhes do status</td>
<td>Fornece informações sobre erros de pedido e solicitações de devolução. Para exibir as informações de devolução e o status de reembolso de um pedido, selecione o <strong>[!UICONTROL Return requested]</strong> texto para abrir o [!UICONTROL Returns] painel.</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>Para exibir detalhes do pedido, selecione o [!DNL Commerce] número do pedido no [!UICONTROL Order] tabela. Em seguida, use [!DNL Commerce] opções de ordem para processar a ordem.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>Para modificar a configuração do canal, selecione as credenciais de conexão do canal Walmart, os atributos mapeados ou os identificadores de envio e as configurações selecionam o [!DNL Commerce] número do pedido no [!UICONTROL Order] tabela. Em seguida, use [!DNL Commerce] opções de ordem para processar a ordem.</td>
</tr>
</table>


**Descrições da coluna**

<table>
<tr>
<td>Campo</td>
<td>Descrição</td>
</tr>
<tr>
<td>[!UICONTROL Walmart Order #]</td>
<td>O número da ordem de compra atribuído à ordem na [!DNL Walmart Marketplace]. Quando um pedido é inicialmente importado para [!DNL Channel Manager], somente o [!DNL Walmart] o número do pedido é exibido. Quando a variável [!DNL Commerce] for criada, a variável [!DNL Walmart] o número do pedido é armazenado na variável [!UICONTROL External ID] atributo de produto.</td>
</tr>
<tr>
<td>[!DNL Commerce] Nº do pedido</td>
<td>O número atribuído à [!DNL Commerce] pedido criado a partir de [!DNL Walmart Marketplace] pedido.</td>
</tr>
<tr>
<td>Itens</td>
<td>Número de itens encomendados em [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Order Value]</td>
<td>Custo total dos itens solicitados.</td>
</tr>
<tr>
<td>[!UICONTROL Ordered]</td>
<td>A data em que o pedido foi enviado à [!DNL Walmart Marketplace] convertido para o fuso horário local.</td>
</tr>
<tr>
<td>[!UICONTROL Ship By (timezone)]</td>
<td>A data em que a ordem deve ser remetida para atender [!DNL Walmart Marketplace] requisitos convertidos para o fuso horário local.
</td>
</tr>
<tr>
<td>[!UICONTROL Deliver By (timezone)]</td>
<td>A data em que a ordem deve ser entregue ao cliente para atender [!DNL Walmart Marketplace] requisitos convertidos para o fuso horário local.</td>
</tr>
<tr>
<td>[!UICONTROL Ship Method]</td>
<td>O [[!DNL Walmart Marketplace] Método de envio](https://sellerhelp.walmart.com/s/guide?language=en_US&amp;article=000007893%29 selecionado para o pedido.</td>
</tr>
<tr>
<td>[!UICONTROL Last Update]</td>
<td>Carimbo de data e hora indicando a última vez que os dados do pedido foram atualizados em [!DNL Channel Manager] convertido para fuso horário local.</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>Indica o status atual do pedido na [!DNL Commerce] fluxo de trabalho do pedido. O status inicial de um pedido importado de [!DNL Walmart Marketplace] é _Open_. Atualizações adicionais de status ocorrem quando [!DNL Commerce] os pedidos são processados e [!DNL Channel Manager] sincroniza com êxito as atualizações de remessa, remessa parcial e cancelamento à [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>Fornece informações mais detalhadas sobre pedidos com erros ou solicitações de reembolso.</td>
</tr>
</table>

## Status do pedido

[!UICONTROL Order Status] fornece informações sobre o estado atual do [!DNL Walmart Marketplace] pedidos gerenciados da Adobe Commerce ou Magento Open Source. As atualizações de status do pedido ocorrem quando [!DNL Channel Manager] recebe informações atualizadas do pedido de qualquer uma das [!DNL Walmart Marketplace] ou o [!DNL Commerce] sistema de pedidos. Os pedidos podem ter os seguintes status:

- **[!UICONTROL Shipped]**—Pedidos que foram enviados do [!DNL Commerce] armazenamento. Quando a ordem for enviada, [!DNL Channel Manager] envia uma atualização para [!DNL Walmart Marketplace] para atualizar o status da entrega no Walmart e fornecer o número de rastreamento da ordem para a entrega. Depois que um pedido for enviado, os itens do pedido poderão ser parcial ou totalmente reembolsados se o Walmart emitir um formulário de Autorização de devolução de mercadoria. Consulte [Devoluções e Reembolsos](return-refund-orders.md).

- **[!UICONTROL Partially Shipped]**—Ordens que têm alguns itens marcados como entregues e outros aguardando para serem entregues. Quando os itens na entrega da ordem, [!DNL Channel Manager] envia uma atualização para [!DNL Walmart Marketplace] para atualizar o status da remessa para _[!DNL Partially Shipped]_no Walmart e forneça o número de rastreamento do pedido para a remessa.

- **[!UICONTROL Canceled]**—Pedidos que foram cancelados no [!DNL Commerce] armazenamento.

   Depois que o cancelamento do pedido for concluído, a [!DNL Commerce] atualizações de quantidade de estoque para refletir os itens devolvidos. Em seguida, [!DNL Channel Manager] sincroniza a atualização com o [!DNL Walmart Marketplace].

- **[!UICONTROL Return requested]**—Se o Walmart Marketplace solicitar uma devolução para itens de pedido que foram entregues, uma `Return requested` O link é exibido na [!UICONTROL Status details] coluna. Selecionar o link abre a variável [!UICONTROL Returns] painel para exibir a devolução e gerenciar o processo de reembolso.

- **[!UICONTROL Error]**—Pedidos com erros. Podem ocorrer erros quando uma operação de atualização de pedido falhar. Por exemplo, erros ocorrem se [!DNL Channel Manager] O não pode receber um novo pedido do Walmart. Elas também podem ocorrer se [!DNL Channel Manager] não é possível enviar uma atualização de remessa ou cancelamento de ordem para a [!DNL Walmart Marketplace]. Se uma operação falhar, a página Pedidos mostrará uma _Erro_ status do pedido. Para obter detalhes, consulte [Corrigir erros de pedido](process-orders.md#fix-shipping-and-cancel-errors).

- **[!UICONTROL Status details]**-Fornece mais informações sobre erros de pedido que ocorrem devido a problemas como informações ausentes ou valores inválidos, detalhes de envio incorretos ou um cancelamento de pedido com falha. A descrição ajuda a determinar se ocorreu um erro no [!DNL Commerce] instância ou no [!DNL Walmart Marketplace].

>[!NOTE]
>
>Se os itens da ordem forem enviados em várias entregas, o status da ordem em [!DNL Channel Manager] O reflete o último status de pedido disponível. Por exemplo, se o primeiro item for entregue e nenhum erro for retornado quando as atualizações de ordem forem sincronizadas com o [!DNL Channel Manager] e [!DNL Walmart Marketplace], o [!DNL Channel Manager] o status do pedido é _[!UICONTROL Partially Shipped]_. Se um segundo item for entregue e [!DNL Channel Manager] retorna um erro, o status do pedido é atualizado para_[!UICONTROL Error]_.

## Revisar Pedidos

1. Em Admin, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** para abrir o [!UICONTROL Channel Manager Marketplace Stores] página.

1. Abra a visualização de loja selecionando o ícone de olho em uma linha de entrada de loja.

1. Para exibir informações do pedido, selecione *[!UICONTROL *Orders]**.

1. Obtenha informações sobre o pedido e determine as próximas etapas, verificando o **[Status](#order-status)** coluna.

## Revisar detalhes do pedido

Depois que um pedido for recebido do marketplace e importado para sua loja de canal de vendas, use o [!DNL Commerce] ID do pedido para exibir os detalhes do pedido no Adobe Commerce.

De **[!UICONTROL Orders]**, selecione o **[!UICONTROL Commerce Order Number]** para abrir o [!DNL Commerce] detalhe do pedido.

![Exibição detalhada da ordem de comércio para um [!DNL Walmart Marketplace] pedido](assets/order-detail-with-external-order-id.png)

Na loja do Commerce, os pedidos importados da [!DNL Walmart Marketplace] tenha as seguintes informações adicionais incluídas nos dados do pedido:

- **Informações de pagamento e método de envio**-Os pedidos importados do Walmart incluem os seguintes valores para campos de pagamento e envio:

   - **[!UICONTROL Offline Channel Payment]**—Indica que o pagamento da ordem é processado offline por [!DNL Walmart Marketplace].

   - **[!UICONTROL External Order Number]**—Exibe o [!DNL Walmart Marketplace] número do pedido.

   - **[!UICONTROL Channel Shipping - Value]**-Indica que os encargos de remessa são tratados por meio de [!DNL Walmart Marketplace].

   - **[!UICONTROL Cancellation Reason]**-Este campo é exibido somente se um pedido for importado de [!DNL Walmart Marketplace] foi cancelado. Os motivos do cancelamento incluem:

      - [!UICONTROL Price or other listing errors.]
      - [!UICONTROL The item is out of stock.]
      - [!UICONTROL Unavailable carrier or shipping information.]
      - [!UICONTROL Additional information is required by our Credit or Fraud Avoidance department.]

- **Itens ordenados**—Esta seção lista os itens do pedido em todas as ordens do Commerce. A variável [!UICONTROL Qty] A coluna fornece o histórico de status dos itens de pedido. Por exemplo, se uma ordem tiver sido faturada, remetida e reembolsada, você poderá ver as transições de status.

   ![Detalhe do pedido histórico do status do item solicitado [!DNL Walmart Marketplace] pedidos](assets/order-detail-status-history.png)

Exibir detalhes de fatura de item e reembolso selecionando o [!UICONTROL Invoice] e [!UICONTROL Credit Memo] opções no menu de navegação. Você também pode acessar o Aviso de Crédito diretamente do [[!UICONTROL Returns]](return-refund-orders.md) painel em sua loja de canal de vendas.
