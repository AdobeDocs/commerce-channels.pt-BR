---
title: Gerenciar pedidos do Walmart Marketplace
description: Exibir e gerenciar [!DNL Walmart Marketplace] ordens com [!DNL Channel Manager] para Adobe Commerce e Magento Open Source.
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: ec85dc2496c22cd8173c550ca35f2bd207501c19
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Gerenciar pedidos do Walmart Marketplace

[!DNL Walmart Marketplace] ordens para [!DNL Commerce] as listas de produtos sincronizam automaticamente com [!DNL Channel Manager] depois que o Walmart processa o pedido. Quando a sincronização estiver concluída, você poderá exibir as informações do pedido selecionando **[!UICONTROL Orders]** na exibição de armazenamento de canais conectados em [!DNL Channel Manager].

![Exibição de Pedidos do Gerenciador de Canais para gerenciar pedidos do Walmart Marketplace](assets/orders-dashboard-view.png)

>[!NOTE]
>
>Pode levar até 35 minutos para um [!DNL Walmart Marketplace] para exibir no [!DNL Channel Manager] lista de pedidos. [!DNL Walmart] requer aproximadamente 30 minutos para processar pedidos recebidos e enviá-los para [!DNL Channel Manager]. Depois que o Gerente de canal recebe o pedido, leva aproximadamente mais cinco minutos para criar e exibir o pedido no Adobe Commerce ou no Magento Open Source.

## Revisar pedidos

1. Em Admin, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** para abrir o [!UICONTROL Channel Manager Marketplace Stores] página.

1. Abra a visualização da loja selecionando o ícone de lápis na linha de entrada da loja.

1. Para exibir informações do pedido, selecione *[!UICONTROL *Orders]**.

1. Obtenha informações sobre o pedido e determine as próximas etapas verificando o **[Status](#about-order-status)** para obter informações sobre os pedidos.

## Exibir detalhes da ordem

Depois que um pedido for recebido do marketplace e importado para a Adobe Commerce ou o Magento Open Source, use a [!DNL Commerce] ID do pedido para exibir o pedido no Adobe Commerce.

De **[!UICONTROL Orders]**, selecione o **[!UICONTROL Commerce Order Number]** para abrir o [!DNL Commerce] detalhes do pedido.

![Exibição detalhada de Pedido de comércio para um pedido do Walmart](assets/order-detail-with-external-order-id.png)

### Controles de pedidos e descrições de colunas

As tabelas a seguir descrevem os controles e colunas disponíveis para Pedidos.

**Controles para[!UICONTROL Orders]**
| **Controle**                    | **Descrição**                                                                                                                                               | |—|—| | [!UICONTROL Filter orders]     | Classifique a exibição selecionando uma das [!UICONTROL Order Status] cartões.                                                                                        | | Detalhes da mensagem de erro | Passe o mouse sobre [!UICONTROL Error Status] para ver a mensagem de erro detalhada.                                                                      | | [!UICONTROL View order detail] | Para exibir os detalhes do pedido, selecione o [!DNL Commerce] número do pedido na [!UICONTROL Order] tabela. Em seguida, use [!DNL Commerce] opções de pedido para processar o pedido. |

**Descrições das colunas**

| Campo | Descrição |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL  Walmart Order Number] | O número da ordem de compra atribuído ao pedido na [!DNL Walmart Marketplace]. Quando um pedido é importado inicialmente para [!DNL Channel Manager], somente o número de pedido do Walmart é exibido. Quando a variável [!DNL Commerce] a ordem é criada, a variável [!DNL Walmart] o número do pedido é armazenado na variável [!UICONTROL External ID] atributo do produto. |
| [!DNL Commerce]  Número do pedido | O número atribuído ao [!DNL Commerce]  pedido criado a partir do [!DNL Walmart Marketplace] ordem. |
| Itens | Número de itens pedidos em [!DNL Walmart Marketplace]. |
| [!UICONTROL Order Value] | Custo total dos itens solicitados. |
| [!UICONTROL Date Created] | A data em que o pedido foi criado na [!DNL Walmart Marketplace]. |
| [!UICONTROL Ship By Date] | Data em que o pedido deve ser enviado por para atender [!DNL Walmart Marketplace] requisitos. |
| [!UICONTROL Order Status] | Indica o status atual do pedido na [!DNL Commerce] fluxo de trabalho do pedido. O status é atualizado quando você adiciona produtos ao [!DNL Channel Manager] e quando você combinar produtos na [!DNL Walmart Marketplace]. Se uma operação falhar, a listagem mostra um status de Erro. Depois de corrigir o erro, [!DNL Channel Manager] tenta novamente a operação e atualiza o status. |

| [!UICONTROL Error description]    | Fornece informações mais detalhadas sobre pedidos com um *Erro* status.|

### Sobre o status do pedido

[!UICONTROL Order Status] fornece informações sobre o estado atual de [!DNL Walmart Marketplace] pedidos gerenciados do Adobe Commerce ou Magento Open Source. Atualizações do status do pedido ocorrem quando [!DNL Channel Manager] recebe informações atualizadas do pedido da [!DNL Walmart Marketplace] ou [!DNL Commerce] sistema de pedido. Os pedidos podem ter os seguintes status:

* **[!UICONTROL Open]**-Pedidos recebidos do [!DNL Walmart Marketplace] pronto para ser revisado e processado no Adobe Commerce ou no Magento Open Source.

   Depois que um cliente solicita um produto da [!DNL Walmart Marketplace], pode levar até 35 minutos para que a ordem de abertura seja exibida no espaço de trabalho da ordem do canal conectado. [!DNL Commerce] requer aproximadamente 30 minutos para processar pedidos recebidos e enviá-los para [!DNL Channel Manager]. Depois que o Gerenciador de canais recebe o pedido, leva mais 5 minutos para criar e exibir o relatório [!DNL Commerce] ordem.

* **[!UICONTROL Processed]**-Pedidos enviados, cancelados ou reembolsados pelo [!DNL Commerce] armazenar.

   Para mostrar todas as ordens enviadas, canceladas e reembolsadas, selecione a variável **Processado** cartão de status.

* **[!UICONTROL Canceled]**- Pedidos que foram cancelados do [!DNL Commerce] armazenar.

   Depois que o cancelamento do pedido for concluído, a variável [!DNL Commerce] atualizações de quantidade de estoque para refletir os itens retornados. Então, [!DNL Channel Manager] sincroniza a atualização com o [!DNL Walmart Marketplace].

* **[!UICONTROL Refunded]**-Pedidos reembolsados pela [!DNL Commerce] armazenar.

   Depois que a restituição for concluída, a [!DNL Commerce] atualizações de quantidade de estoque para refletir os itens reembolsados. Então, [!DNL Channel Manager] sincroniza a atualização com o [!DNL Walmart Marketplace].

* **[!UICONTROL Error]**- Pedidos com erros. Erros podem ocorrer quando uma operação de atualização de pedido falha. Por exemplo, erros ocorrem se [!DNL Channel Manager] O não pode receber um novo pedido do Walmart. Eles também podem ocorrer se [!DNL Channel Manager] não é possível enviar uma entrega da ordem ou atualização do cancelamento para a [!DNL Walmart Marketplace].

* **[!UICONTROL Error description]**-Fornece informações detalhadas sobre erros de pedido que ocorrem devido a problemas como informações ausentes ou valores inválidos, detalhes de remessa incorretos ou cancelamento de pedido com falha. A descrição ajuda a determinar se ocorreu um erro no [!DNL Commerce] ou na [!DNL Walmart Marketplace].
