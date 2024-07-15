---
title: 'Exibir e Gerenciar Pedidos de [!DNL Channel Manager]'
description: 'Exibir e gerenciar [!DNL Walmart Marketplace] pedidos com [!DNL Channel Manager] para Adobe Commerce e Magento Open Source.'
feature: Sales Channels, Orders
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---

# Exibir e Acompanhar Pedidos de [!DNL Channel Manager]

Os dados de pedido de [!DNL Walmart Marketplace] para produtos [!DNL Commerce] sincronizam automaticamente com [!DNL Channel Manager] depois que [!DNL Walmart] processa o pedido.

No lado do [!DNL Commerce], uma sincronização bem-sucedida aciona as seguintes ações:

- [!DNL Channel Manager] envia uma confirmação de pedido ao Walmart.

- Um pedido [!DNL Commerce] correspondente é criado a partir do pedido do Walmart.

- As informações atualizadas do pedido são exibidas no painel Pedidos [!DNL Channel Manager].

No Administrador da loja, é possível exibir dados de pedidos de [!DNL Channel Manager] abrindo a loja de canais de vendas e selecionando **[!UICONTROL Orders]**.

![Exibição de Pedidos do gerente de canal para gerenciar [!DNL Walmart Marketplace] pedidos](assets/orders-dashboard-view.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Pode levar até 35 minutos para um pedido [!DNL Walmart Marketplace] ser exibido na lista de pedidos [!DNL Channel Manager]. O [!DNL Walmart] leva aproximadamente 30 minutos para processar pedidos recebidos e enviá-los para [!DNL Channel Manager]. Depois que o Gerenciador de canais receber o pedido, ele levará aproximadamente mais cinco minutos para criar e exibir o pedido no Adobe Commerce ou no Magento Open Source.

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
<td>Classifique a exibição selecionando um dos cartões [!UICONTROL Order Status].</td>
</tr>
<tr>
<td>Detalhes do status</td>
<td>Fornece informações sobre erros de pedido e solicitações de devolução. Para exibir as informações de devolução e o status do reembolso de um pedido, selecione o texto <strong>[!UICONTROL Return requested]</strong> para abrir o painel [!UICONTROL Returns].</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>Para exibir detalhes do pedido, selecione o número do pedido [!DNL Commerce] na tabela [!UICONTROL Order]. Em seguida, use as opções de pedido [!DNL Commerce] para processar o pedido.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>Para modificar a configuração do canal, selecione credenciais de conexão Walmart do canal, atributos mapeados ou identificadores de envio. As configurações selecionam o número de pedido [!DNL Commerce] na tabela [!UICONTROL Order]. Em seguida, use as opções de pedido [!DNL Commerce] para processar o pedido.</td>
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
<td>O número da ordem de compra atribuído à ordem no [!DNL Walmart Marketplace]. Quando um pedido é importado inicialmente para [!DNL Channel Manager], somente o número do pedido [!DNL Walmart] é exibido. Quando o pedido [!DNL Commerce] é criado, o número do pedido [!DNL Walmart] é armazenado no atributo de produto [!UICONTROL External ID].</td>
</tr>
<tr>
<td>[!DNL Commerce] Nº do pedido</td>
<td>O número atribuído à ordem [!DNL Commerce] criado a partir da ordem [!DNL Walmart Marketplace].</td>
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
<td>A data em que o pedido foi enviado para o [!DNL Walmart Marketplace] convertido no fuso horário local.</td>
</tr>
<tr>
<td>[!UICONTROL Ship By (timezone)]</td>
<td>A data em que o pedido deve ser enviado para atender aos requisitos de [!DNL Walmart Marketplace] convertidos para o fuso horário local.
</td>
</tr>
<tr>
<td>[!UICONTROL Deliver By (timezone)]</td>
<td>A data em que o pedido deve ser entregue ao cliente para atender aos requisitos de [!DNL Walmart Marketplace] convertidos para o fuso horário local.</td>
</tr>
<tr>
<td>[!UICONTROL Ship Method]</td>
<td>O [[!DNL Walmart Marketplace] Método de Remessa](https://sellerhelp.walmart.com/s/guide?language=en_US&amp;article=000007893%29 selecionado para o pedido.</td>
</tr>
<tr>
<td>[!UICONTROL Last Update]</td>
<td>Carimbo de data/hora indicando a última vez que os dados do pedido foram atualizados em [!DNL Channel Manager] convertidos para o fuso horário local.</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>Indica o status atual do pedido no fluxo de trabalho do pedido [!DNL Commerce]. O status inicial de um pedido importado de [!DNL Walmart Marketplace] é _Open_. Atualizações adicionais de status ocorrem quando [!DNL Commerce] pedidos são processados e [!DNL Channel Manager] sincroniza com êxito as atualizações de remessa, remessa parcial e cancelamento para [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>Fornece informações mais detalhadas sobre pedidos com erros ou solicitações de reembolso.</td>
</tr>
</table>

## Status do pedido

[!UICONTROL Order Status] fornece informações sobre o estado atual de [!DNL Walmart Marketplace] pedidos gerenciados por Adobe Commerce ou Magento Open Source. As atualizações do status do pedido ocorrem quando [!DNL Channel Manager] recebe informações atualizadas do pedido do sistema de pedidos [!DNL Walmart Marketplace] ou [!DNL Commerce]. Os pedidos podem ter os seguintes status:

- **[!UICONTROL Shipped]** — Pedidos que foram enviados do armazenamento [!DNL Commerce]. Quando o pedido é enviado, [!DNL Channel Manager] envia uma atualização para [!DNL Walmart Marketplace] a fim de atualizar o status da remessa no Walmart e fornecer o número de rastreamento do pedido para a remessa. Depois que um pedido for enviado, os itens do pedido poderão ser parcial ou totalmente reembolsados se o Walmart emitir um formulário de Autorização de devolução de mercadoria. Consulte [Devoluções e Reembolsos](return-refund-orders.md).

- **[!UICONTROL Partially Shipped]** — Pedidos que têm alguns itens marcados como remetidos e outros aguardando para serem remetidos. Quando os itens no pedido são enviados, [!DNL Channel Manager] envia uma atualização para [!DNL Walmart Marketplace] a fim de atualizar o status do envio para _[!DNL Partially Shipped]_no Walmart e fornecer o número de rastreamento do pedido para o envio.

- **[!UICONTROL Canceled]** — Pedidos que foram cancelados no armazenamento [!DNL Commerce].

  Após a conclusão do cancelamento do pedido, a quantidade em estoque de [!DNL Commerce] é atualizada para refletir os itens devolvidos. Em seguida, [!DNL Channel Manager] sincroniza a atualização para o [!DNL Walmart Marketplace].

- **[!UICONTROL Return requested]** — Se o Walmart Marketplace solicitar uma devolução para itens de pedido enviados, um link `Return requested` será exibido na coluna [!UICONTROL Status details]. Selecionar o link abre o painel [!UICONTROL Returns] para exibir o retorno e gerenciar o processo de reembolso.

- **[!UICONTROL Error]** — Pedidos com erros. Podem ocorrer erros quando uma operação de atualização de ordem falhar. Por exemplo, ocorrerão erros se [!DNL Channel Manager] não puder receber um novo pedido do Walmart. Eles também podem ocorrer se [!DNL Channel Manager] não puder enviar uma remessa de pedido ou atualização de cancelamento para o [!DNL Walmart Marketplace]. Se uma operação falhar, a página Pedidos mostrará o status _Erro_ para o pedido. Para obter detalhes, consulte [Corrigir erros de pedido](process-orders.md#fix-shipping-and-cancel-errors).

- **[!UICONTROL Status details]**-Fornece mais informações sobre erros de pedido que ocorrem devido a problemas como informações ausentes ou valores inválidos, detalhes de envio incorretos ou um cancelamento de pedido com falha. A descrição ajuda a determinar se ocorreu um erro na instância [!DNL Commerce] ou no [!DNL Walmart Marketplace].

>[!NOTE]
>
>Se os itens do pedido forem enviados em várias remessas, o status do pedido em [!DNL Channel Manager] refletirá o último status de pedido disponível. Por exemplo, se o primeiro item for enviado e nenhum erro for retornado quando as atualizações de pedido forem sincronizadas com [!DNL Channel Manager] e [!DNL Walmart Marketplace], o status do pedido [!DNL Channel Manager] será _[!UICONTROL Partially Shipped]_. Se um segundo item for enviado e [!DNL Channel Manager] retornar um erro, o status do pedido será atualizado para_[!UICONTROL Error]_.

## Revisar Pedidos

1. No Admin, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** para abrir a página [!UICONTROL Channel Manager Marketplace Stores].

1. Abra a visualização de loja selecionando o ícone de olho em uma linha de entrada de loja.

1. Para exibir informações do pedido, selecione *[!UICONTROL *Orders]**.

1. Obtenha informações sobre o pedido e determine as próximas etapas, verificando a coluna **[Status](#order-status)**.

## Revisar detalhes do pedido

Depois que um pedido for recebido do marketplace e importado em sua loja de canal de vendas, use a ID do Pedido [!DNL Commerce] para exibir os detalhes do pedido no Adobe Commerce.

Em **[!UICONTROL Orders]**, selecione **[!UICONTROL Commerce Order Number]** para abrir os detalhes do pedido [!DNL Commerce].

![Exibição detalhada de Pedido Commerce para um pedido [!DNL Walmart Marketplace]](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

Na loja da Commerce, os pedidos importados de [!DNL Walmart Marketplace] têm as seguintes informações adicionais incluídas nos dados do pedido:

- **Informações de Pagamento e Método de Envio**-Os pedidos importados do Walmart incluem os seguintes valores para campos de pagamento e envio:

   - **[!UICONTROL Offline Channel Payment]** — Indica que o pagamento da ordem é processado offline por [!DNL Walmart Marketplace].

   - **[!UICONTROL External Order Number]** — Exibe o número do pedido [!DNL Walmart Marketplace].

   - **[!UICONTROL Channel Shipping - Value]** - Indica que os encargos de remessa são tratados por [!DNL Walmart Marketplace].

   - **[!UICONTROL Cancellation Reason]** - Este campo é exibido somente se uma ordem importada de [!DNL Walmart Marketplace] for cancelada. Os motivos do cancelamento incluem:

      - [!UICONTROL Price or other listing errors.]
      - [!UICONTROL The item is out of stock.]
      - [!UICONTROL Unavailable carrier or shipping information.]
      - [!UICONTROL Additional information is required by our Credit or Fraud Avoidance department.]

- **Itens Solicitados** — Esta seção lista os itens do pedido em todos os pedidos do Commerce. A coluna [!UICONTROL Qty] fornece o histórico de status dos itens de pedido. Por exemplo, se uma ordem tiver sido faturada, remetida e reembolsada, você poderá ver as transições de status.

  ![Histórico de status do item solicitado de Detalhes do Pedido [!DNL Walmart Marketplace] pedidos](assets/order-detail-status-history.png){width="600" zoomable="yes"}

Exiba os detalhes da fatura e do reembolso do item selecionando as opções [!UICONTROL Invoice] e [!UICONTROL Credit Memo] no menu de navegação. Você também pode acessar o Memorando de Crédito diretamente do painel [[!UICONTROL Returns]](return-refund-orders.md) em sua loja de canal de vendas.
