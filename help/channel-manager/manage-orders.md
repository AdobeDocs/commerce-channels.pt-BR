---
title: '"Exibir e gerenciar pedidos a partir de [!DNL Channel Manager]'''
description: "Exibir e gerenciar [!DNL Walmart Marketplace] ordens com [!DNL Channel Manager] para Adobe Commerce e Magento Open Source."
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# Exibir e rastrear pedidos a partir de [!DNL Channel Manager]

[!DNL Walmart Marketplace] dados de pedido para [!DNL Commerce] os produtos sincronizam automaticamente com [!DNL Channel Manager] after [!DNL Walmart] processa o pedido.

No [!DNL Commerce] além disso, uma sincronização bem-sucedida inicia as seguintes ações:

- [!DNL Channel Manager] envia uma confirmação de pedido para o Walmart.

- Um [!DNL Commerce] A ordem é criada a partir da ordem Walmart.

- As informações atualizadas do pedido são exibidas na [!DNL Channel Manager] Painel de pedidos.

No Administrador da loja, é possível visualizar os dados do pedido de [!DNL Channel Manager] abrindo o armazenamento de canal de vendas e selecionando **[!UICONTROL Orders]**.

![Exibição Pedidos do gerenciador de canais para gerenciar [!DNL Walmart Marketplace] ordens](assets/orders-dashboard-view.png)

>[!NOTE]
>
>Pode levar até 35 minutos para um [!DNL Walmart Marketplace] para exibir no [!DNL Channel Manager] lista de pedidos. [!DNL Walmart] requer aproximadamente 30 minutos para processar pedidos recebidos e enviá-los para [!DNL Channel Manager]. Depois que o Gerente de canal recebe o pedido, leva aproximadamente mais cinco minutos para criar e exibir o pedido no Adobe Commerce ou no Magento Open Source.

## Controles de pedidos e descrições de colunas

As tabelas a seguir descrevem os controles e colunas disponíveis para Pedidos.

**Controles para[!UICONTROL Orders]**

<table>
<tr>
<td><strong>Controle</strong></td>
<td><strong>Descrição</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter orders]</td>
<td>Classifique a exibição ao selecionar uma das [!UICONTROL Order Status] cartões.</td>
</tr>
<tr>
<td>Detalhes do status</td>
<td>Fornece informações sobre erros de pedido e solicitações de retorno. Para exibir informações de devolução e o status de reembolso de um pedido, selecione o <strong>[!UICONTROL Return requested]</strong> texto para abrir o [!UICONTROL Returns] painel.</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>Para exibir detalhes do pedido, selecione a [!DNL Commerce] número do pedido na [!UICONTROL Order] tabela. Em seguida, use [!DNL Commerce] opções de pedido para processar o pedido.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>Para modificar a configuração do canal, selecione as credenciais do canal Walmart Connection, os atributos mapeados ou os identificadores de envio, as configurações selecionam a variável [!DNL Commerce] número do pedido na [!UICONTROL Order] tabela. Em seguida, use [!DNL Commerce] opções de pedido para processar o pedido.</td>
</tr>
</table>


**Descrições das colunas**

<table>
<tr>
<td>Campo</td>
<td>Descrição</td>
</tr>
<tr>
<td>[!UICONTROL Walmart Order #]</td>
<td>O número da ordem de compra atribuído ao pedido na [!DNL Walmart Marketplace]. Quando um pedido é importado inicialmente para [!DNL Channel Manager], somente o [!DNL Walmart] número do pedido é exibido. Quando a variável [!DNL Commerce] a ordem é criada, a variável [!DNL Walmart] o número do pedido é armazenado na variável [!UICONTROL External ID] atributo do produto.</td>
</tr>
<tr>
<td>[!DNL Commerce] Nº do pedido</td>
<td>O número atribuído ao [!DNL Commerce] pedido criado a partir do [!DNL Walmart Marketplace] ordem.</td>
</tr>
<tr>
<td>Itens</td>
<td>Número de itens pedidos em [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Order Value]</td>
<td>Custo total dos itens solicitados.</td>
</tr>
<tr>
<td>[!UICONTROL Ordered]</td>
<td>A data em que o pedido foi enviado ao [!DNL Walmart Marketplace] convertido para o fuso horário local.</td>
</tr>
<tr>
<td>[!UICONTROL Ship By (timezone)]</td>
<td>A data em que o pedido deve ser enviado para atender [!DNL Walmart Marketplace] requisitos convertidos para o fuso horário local.
</td>
</tr>
<tr>
<td>[!UICONTROL Deliver By (timezone)]</td>
<td>A data em que o pedido deve ser entregue ao cliente para atender [!DNL Walmart Marketplace] requisitos convertidos para o fuso horário local.</td>
</tr>
<tr>
<td>[!UICONTROL Ship Method]</td>
<td>O [[!DNL Walmart Marketplace] Método de Entrega](https://sellerhelp.walmart.com/s/guide?language=en_US&amp;article=000007893%29 selecionado para o pedido.</td>
</tr>
<tr>
<td>[!UICONTROL Last Update]</td>
<td>Carimbo de data e hora que indica a última vez que os dados do pedido foram atualizados em [!DNL Channel Manager] convertido em fuso horário local.</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>Indica o status atual do pedido na [!DNL Commerce] fluxo de trabalho do pedido. O status inicial de um pedido importado de [!DNL Walmart Marketplace] é _Open_. Atualizações adicionais de status ocorrem quando [!DNL Commerce] os pedidos são processados e [!DNL Channel Manager] sincroniza com êxito atualizações de entrega, entrega parcial e cancelamento para a [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>Fornece informações mais detalhadas sobre pedidos com erros ou solicitações de reembolso.</td>
</tr>
</table>

## Status do pedido

[!UICONTROL Order Status] fornece informações sobre o estado atual de [!DNL Walmart Marketplace] pedidos gerenciados do Adobe Commerce ou Magento Open Source. Atualizações do status do pedido ocorrem quando [!DNL Channel Manager] recebe informações atualizadas do pedido da [!DNL Walmart Marketplace] ou [!DNL Commerce] sistema de pedido. Os pedidos podem ter os seguintes status:

- **[!UICONTROL Shipped]**—Pedidos enviados a partir do [!DNL Commerce] armazenar. Quando a ordem for enviada, [!DNL Channel Manager] envia uma atualização para [!DNL Walmart Marketplace] para atualizar o status de entrega no Walmart e fornecer o número de rastreamento de pedido para a remessa. Depois que um pedido é enviado, os itens de pedido podem ser total ou parcialmente reembolsados se o Walmart emitir um formulário de Autorização de Devolução de Produto. Consulte [Devoluções e reembolsos](return-refund-orders.md).

- **[!UICONTROL Partially Shipped]**—Pedidos que têm alguns itens marcados como enviados e outros aguardando para serem enviados. Quando os itens na ordem são enviados, [!DNL Channel Manager] envia uma atualização para [!DNL Walmart Marketplace] para atualizar o status de envio para _[!DNL Partially Shipped]_no Walmart e forneça o número de rastreamento do pedido para a remessa.

- **[!UICONTROL Canceled]**—Pedidos anulados do [!DNL Commerce] armazenar.

   Depois que o cancelamento do pedido for concluído, a variável [!DNL Commerce] atualizações de quantidade de estoque para refletir os itens retornados. Então, [!DNL Channel Manager] sincroniza a atualização com o [!DNL Walmart Marketplace].

- **[!UICONTROL Return requested]**—Se o Walmart Marketplace solicitar uma devolução para itens de pedido que foram enviados, uma `Return requested` é exibido na [!UICONTROL Status details] coluna. Selecionar o link abre o [!UICONTROL Returns] painel para visualizar o retorno e gerenciar o processo de reembolso.

- **[!UICONTROL Error]**—Pedidos com erros. Erros podem ocorrer quando uma operação de atualização de pedido falha. Por exemplo, erros ocorrem se [!DNL Channel Manager] O não pode receber um novo pedido do Walmart. Eles também podem ocorrer se [!DNL Channel Manager] não é possível enviar uma entrega da ordem ou atualização do cancelamento para a [!DNL Walmart Marketplace]. Se uma operação falhar, a página Pedidos mostrará um _Erro_ status do pedido. Para obter detalhes, consulte [Corrigir erros de ordem](process-orders.md#fix-Shipping-and-cancelation-errors).

- **[!UICONTROL Status details]**-Fornece mais informações sobre erros de pedido que ocorrem devido a problemas como informações ausentes ou valores inválidos, detalhes de remessa incorretos ou cancelamento de pedido com falha. A descrição ajuda a determinar se ocorreu um erro no [!DNL Commerce] ou na [!DNL Walmart Marketplace].

>[!NOTE]
>
>Se os itens da ordem forem enviados em várias entregas, o status da ordem em [!DNL Channel Manager] reflete o último status de pedido disponível. Por exemplo, se o primeiro item é enviado e nenhum erro é retornado quando as atualizações de pedido são sincronizadas com o [!DNL Channel Manager] e [!DNL Walmart Marketplace], o [!DNL Channel Manager] status do pedido _[!UICONTROL Partially Shipped]_. Se um segundo item for enviado e [!DNL Channel Manager] retorna um erro, o status do pedido é atualizado para_[!UICONTROL Error]_.

## Revisar pedidos

1. Em Admin, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** para abrir o [!UICONTROL Channel Manager Marketplace Stores] página.

1. Abra a visualização da loja selecionando o ícone de olho na linha de entrada da loja.

1. Para exibir informações do pedido, selecione *[!UICONTROL *Orders]**.

1. Obtenha informações sobre o pedido e determine as próximas etapas verificando o **[Status](#order-status)** coluna.

## Revisar Detalhes do Pedido

Depois que um pedido é recebido do marketplace e importado para a loja de canais de vendas, use o [!DNL Commerce] ID do pedido para exibir os detalhes do pedido no Adobe Commerce.

De **[!UICONTROL Orders]**, selecione o **[!UICONTROL Commerce Order Number]** para abrir o [!DNL Commerce] detalhes do pedido.

![Exibição detalhada do pedido de comércio para um [!DNL Walmart Marketplace] pedido](assets/order-detail-with-external-order-id.png)

Na loja do Commerce, pedidos importados de [!DNL Walmart Marketplace] ter as seguintes informações adicionais incluídas nos dados do pedido:

- **Informações sobre Pagamento e Método de Entrega**-Pedidos importados do Walmart incluem os seguintes valores para campos de pagamento e remessa:

   - **[!UICONTROL Offline Channel Payment]**—Indica que o pagamento da ordem é processado offline por [!DNL Walmart Marketplace].

   - **[!UICONTROL External Order Number]**—Exibe a [!DNL Walmart Marketplace] número do pedido.

   - **[!UICONTROL Channel Shipping - Value]**-Indica que as taxas de frete são tratadas por [!DNL Walmart Marketplace].

   - **[!UICONTROL Cancellation Reason]**-Este campo é exibido somente se um pedido importado de [!DNL Walmart Marketplace] é cancelado. Os motivos de cancelamento incluem:

      - [!UICONTROL Price or other listing errors.]
      - [!UICONTROL The item is out of stock.]
      - [!UICONTROL Unavailable carrier or shipping information.]
      - [!UICONTROL Additional information is required by our Credit or Fraud Avoidance department.]

- **Itens pedidos**—Esta seção lista os itens do pedido em todos os pedidos do Commerce. O [!UICONTROL Qty] fornece o histórico de status dos itens da ordem. Por exemplo, se um pedido foi faturado, enviado e reembolsado, você pode ver as transições de status.

   ![Histórico de status do item de ordem Detalhado da Ordem [!DNL Walmart Marketplace] ordens](assets/order-detail-status-history.png)

Exibir a fatura do item e os detalhes da restituição selecionando o [!UICONTROL Invoice] e [!UICONTROL Credit Memo] no menu de navegação. Você também pode acessar o Aviso de crédito diretamente da [[!UICONTROL Returns]](return-refund-orders.md) painel na loja de canais de vendas.
