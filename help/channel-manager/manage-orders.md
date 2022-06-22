---
title: '"Exibir e rastrear pedidos de [!DNL Channel Manager]'''
description: '"Exibir e gerenciar [!DNL Walmart Marketplace] ordens com [!DNL Channel Manager] para Adobe Commerce e Magento Open Source."'
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: 8146be1c94ffb1c8abd0d28e53d3476fd78f2c62
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 0%

---

# Exibir e rastrear pedidos de [!DNL Channel Manager]

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
| **Controle**                    | **Descrição**                                                                                                                                                                                                                                                                  | |—|—| | [!UICONTROL Filter orders]     | Classifique a exibição selecionando uma das [!UICONTROL Order Status] cartões.                                                                                                                                                                                                           | | Descrição do erro | Fornece informações mais detalhadas sobre pedidos com um status de Erro.                                                                                                                                                                                                            | | [!UICONTROL View order detail] | Para exibir os detalhes do pedido, selecione o [!DNL Commerce] número do pedido na [!UICONTROL Order] tabela. Em seguida, use [!DNL Commerce] opções de pedido para processar o pedido.                                                                                                                    | | [!UICONTROL Channel Settings]  | Para modificar a configuração do canal, selecione as credenciais do canal Walmart Connection, os atributos mapeados ou os identificadores de envio, as configurações selecionam a variável [!DNL Commerce] número do pedido na [!UICONTROL Order] tabela. Em seguida, use [!DNL Commerce] opções de pedido para processar o pedido. |


**Descrições das colunas**

| Campo | Descrição |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Walmart Order Number] | O número da ordem de compra atribuído ao pedido na [!DNL Walmart Marketplace]. Quando um pedido é importado inicialmente para [!DNL Channel Manager], somente o [!DNL Walmart] número do pedido é exibido. Quando a variável [!DNL Commerce] a ordem é criada, a variável [!DNL Walmart] o número do pedido é armazenado na variável [!UICONTROL External ID] atributo do produto. |
| [!DNL Commerce] Número do pedido | O número atribuído ao [!DNL Commerce] pedido criado a partir do [!DNL Walmart Marketplace] ordem. |
| Itens | Número de itens pedidos em [!DNL Walmart Marketplace]. |
| [!UICONTROL Order Value] | Custo total dos itens solicitados. |
| [!UICONTROL Date Ordered] | A data em que o pedido foi enviado no [!DNL Walmart Marketplace]. |
| [!UICONTROL Ship By Date] | Data em que o pedido deve ser enviado por para atender [!DNL Walmart Marketplace] requisitos. |
| [!UICONTROL Deliver By Date] | Data em que o pedido deve ser entregue ao cliente para atender [!DNL Walmart Marketplace] requisitos no formato UTC. |
| [!UICONTROL Ship Method] | O [[!DNL Walmart Marketplace] Método de Entrega](https://sellerhelp.walmart.com/s/guide?article=000007893) selecionado para o pedido. |
| [!UICONTROL Last Update At] | Carimbo de data e hora que indica a última vez que os dados do pedido foram atualizados em [!DNL Channel Manager] no formato UTC. |
| [!UICONTROL Status] | Indica o status atual do pedido na [!DNL Commerce] fluxo de trabalho do pedido. O status inicial de um pedido importado de [!DNL Walmart Marketplace] é _Abrir_. Atualizações adicionais de status ocorrem quando [!DNL Commerce] os pedidos são processados e [!DNL Channel Manager] sincroniza com êxito atualizações de entrega, entrega parcial e cancelamento para a [!DNL Walmart Marketplace]. |
| [!UICONTROL Error Description] | Fornece informações mais detalhadas sobre pedidos com um _[!UICONTROL Error]_status. |

## Status do pedido


[!UICONTROL Order Status] fornece informações sobre o estado atual de [!DNL Walmart Marketplace] pedidos gerenciados do Adobe Commerce ou Magento Open Source. Atualizações do status do pedido ocorrem quando [!DNL Channel Manager] recebe informações atualizadas do pedido da [!DNL Walmart Marketplace] ou [!DNL Commerce] sistema de pedido. Os pedidos podem ter os seguintes status:

- **[!UICONTROL Shipped]**-Pedidos enviados do [!DNL Commerce] armazenar. Quando a ordem for enviada, [!DNL Channel Manager] envia uma atualização para [!DNL Walmart Marketplace] para atualizar o status de entrega no Walmart e fornecer o número de rastreamento de pedido para a remessa.

- **[!UICONTROL Partially Shipped]**—Pedidos que têm alguns itens marcados como enviados e outros aguardando para serem enviados. Quando os itens na ordem são enviados, [!DNL Channel Manager] envia uma atualização para [!DNL Walmart Marketplace] para atualizar o status de envio para _[!DNL Partially Shipped]_no Walmart e forneça o número de rastreamento do pedido para a remessa.

- **[!UICONTROL Canceled]**- Pedidos que foram cancelados do [!DNL Commerce] armazenar.

   Depois que o cancelamento do pedido for concluído, a variável [!DNL Commerce] atualizações de quantidade de estoque para refletir os itens retornados. Então, [!DNL Channel Manager] sincroniza a atualização com o [!DNL Walmart Marketplace].

- **[!UICONTROL Error]**- Pedidos com erros. Erros podem ocorrer quando uma operação de atualização de pedido falha. Por exemplo, erros ocorrem se [!DNL Channel Manager] O não pode receber um novo pedido do Walmart. Eles também podem ocorrer se [!DNL Channel Manager] não é possível enviar uma entrega da ordem ou atualização do cancelamento para a [!DNL Walmart Marketplace]. Se uma operação falhar, a página Pedidos mostrará um _Erro_ status do pedido. Para obter detalhes, consulte [Corrigir erros de ordem](process-orders.md#fix-Shipping-and-cancelation-errors).

- **[!UICONTROL Error description]**-Fornece informações detalhadas sobre erros de pedido que ocorrem devido a problemas como informações ausentes ou valores inválidos, detalhes de remessa incorretos ou cancelamento de pedido com falha. A descrição ajuda a determinar se ocorreu um erro no [!DNL Commerce] ou na [!DNL Walmart Marketplace].

>[!NOTE]
>
>Se os itens da ordem forem enviados em várias entregas, o status da ordem em [!DNL Channel Manager] reflete o último status de pedido disponível. Por exemplo, se o primeiro item é enviado e nenhum erro é retornado quando as atualizações de pedido são sincronizadas com o [!DNL Channel Manager] e [!DNL Walmart Marketplace], o [!DNL Channel Manager] status do pedido _[!UICONTROL Partially Shipped]_. Se um segundo item for enviado e [!DNL Channel Manager] retorna um erro, o status do pedido é atualizado para_[!UICONTROL Error]_.

## Revisar pedidos

1. Em Admin, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** para abrir o [!UICONTROL Channel Manager Marketplace Stores] página.

1. Abra a visualização da loja selecionando o ícone de olho na linha de entrada da loja.

1. Para exibir informações do pedido, selecione *[!UICONTROL *Orders]**.

1. Obtenha informações sobre o pedido e determine as próximas etapas verificando o **[Status](#about-order-status)** coluna.

## Exibir detalhes da ordem

Depois que um pedido for recebido do marketplace e importado para a Adobe Commerce ou o Magento Open Source, use a [!DNL Commerce] ID do pedido para exibir o pedido no Adobe Commerce.

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

