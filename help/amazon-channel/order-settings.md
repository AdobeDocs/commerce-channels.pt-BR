---
title: Configurações de pedido do Amazon
description: Use as configurações de Pedido para determinar como os pedidos do Amazon são importados e processados na sua loja de Commerce.
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '1542'
ht-degree: 0%

---

# Configurações de pedido do Amazon

As configurações de pedido definem se e como os pedidos do Amazon são importados e processados no [!DNL Commerce] e pode ser acessado no [painel de armazenamento](./amazon-store-dashboard.md).

As configurações de importação de ordem estão definidas como `Enabled` por padrão, o que significa que seus pedidos do Amazon aparecem no painel de armazenamento e criam relatórios correspondentes [!DNL Commerce] pedidos. Os pedidos importados podem ser gerenciados no [!DNL Commerce] [Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) fluxo de trabalho.

>[!NOTE]
>
>Independentemente das configurações do pedido, os pedidos do Amazon existentes antes da integração da loja não são importados.

Depois [integração de loja](./store-integration.md) estiver concluído, você poderá alterar as configurações do pedido. Se você definir as configurações de pedido como `Disabled`, os pedidos do Amazon são exibidos no painel da loja, mas devem ser gerenciados no [!DNL Amazon Seller Central] conta.

Quando um pedido é criado no Amazon, ele não é importado imediatamente para o [!DNL Commerce]. O Amazon atribui um `Pending` status para pedidos recém-criados. Depois que o Amazon verifica o pedido e o método de pagamento, o status do pedido é alterado para `Unshipped`. Essa alteração de status aciona a importação da ordem e [!DNL Commerce] cria uma ordem correspondente.

Os pedidos importados da Amazon podem ser gerenciados na [!DNL Commerce] [fluxo de trabalho de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html). Consulte também [Gerenciar Pedidos](./managing-orders.md).

## Definir configurações de pedido {#configure-order-settings}

1. Clique em **[!UICONTROL Order Settings]** no painel da loja.

1. Para **[!UICONTROL Import Amazon Orders]** (obrigatório), escolha uma opção:

   - `Disabled` - Escolha quando você não deseja criar pedidos correspondentes no [!DNL Commerce] quando novos pedidos são recebidos da Amazon. Quando selecionados, todos os outros campos desta página são desativados.

   - `Enabled` - (Padrão) Escolha quando deseja criar a correspondência [!DNL Commerce] pedidos quando novos pedidos são recebidos da Amazon. [!DNL Commerce] os pedidos são criados com base no status do Amazon e nos níveis de estoque.

      >[!NOTE]
      >
      >Importar Ordens do Amazon deve ser definido como `Enabled` para gerenciar pedidos da Amazon no [!DNL Commerce] [pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) fluxo de trabalho. Quando definido como `Disabled`, seus pedidos do Amazon não têm um correspondente [!DNL Commerce] número do pedido e não pode ser gerenciado no [!DNL Commerce]. Você gerencia esses pedidos na sua [!DNL Amazon Seller Central] conta.

1. Para **[!UICONTROL Import Amazon Orders Into Magento Store]**, escolha qual [!DNL Commerce] armazenar as ordens do Amazon associadas a quando a ordem correspondente é criada no [!DNL Commerce].

   Essa configuração assume o padrão da Exibição de loja para o site selecionado quando você [adicionou a loja da Amazon](./store-integration.md). Se quiser alterar essa configuração, a lista de opções dependerá do [!DNL Commerce] lojas que você configurou em sua configuração. Consulte [Lojas](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html).

1. Para **[!UICONTROL Customer Creation]**, escolha uma opção:

   - `No Customer Creation (guest)` - (Padrão) Escolha quando você não deseja criar uma conta de cliente no [!DNL Commerce] usando os dados do cliente importados do pedido do Amazon. Quando escolhido, [!DNL Commerce] processa um pedido Amazon importado da mesma maneira que processa um check-out de convidado em [!DNL Commerce].

   - `Build New Customer Account` - Escolha quando deseja criar uma Nova Conta de Cliente no [!DNL Commerce] usando os dados do cliente importados com o pedido do Amazon. Essa opção ajuda a criar o banco de dados do cliente a partir dos pedidos da Amazon.

1. Para **[!UICONTROL Order Number Source]**, escolha uma opção:

   - `Build Using Magento Order Number` - (Padrão) Escolha quando deseja criar uma [!DNL Commerce] número do pedido do pedido Amazon correspondente usando o [!DNL Commerce] ID da ordem atribuída de forma incremental.

   - `Build Using Amazon Order Number` - Escolha quando deseja criar a variável [!DNL Commerce] número do pedido usando o número do pedido atribuído pela Amazon correspondente.
   >[!NOTE]
   >
   >Depois que um pedido é importado, o número do pedido do Amazon é exibido no _[!UICONTROL Recent Orders]_no painel de armazenamento. A variável [!DNL Commerce] o número do pedido é exibido ao exibir os detalhes do pedido no [!DNL Commerce] [Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) espaço de trabalho.

1. Para **[!UICONTROL Order Status]** (obrigatório), escolha uma opção:

   - `Default Order Status` - (Padrão) Escolha quando deseja que as ordens recém-criadas importadas do Amazon sejam atribuídas ao status de ordem padrão definido para novas ordens. O status padrão para novos pedidos (a menos que você tenha criado um status de pedido personalizado para novos pedidos) é `Pending`. Consulte [Processamento de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

   - `Custom Order Status` - Escolha quando deseja que as ordens recém-criadas importadas do Amazon recebam um status diferente do padrão.

   - `Processing Order Status` - Ativado quando **[!UICONTROL Order Status]** está definida como `Custom Order Status`. Escolha o status que deseja usar para pedidos recém-criados importados do Amazon. As opções neste campo são baseadas nas opções de status padrão em [!DNL Commerce]. Consulte [Status do pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html). Você também pode criar um status de pedido personalizado para mostrar aqui para seleção. Para criar um status de pedido personalizado, consulte [Status do pedido personalizado](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html#custom-order-status).

1. Quando terminar, clique em **[!UICONTROL Save order settings]**.

![Configurações do pedido](assets/amazon-order-settings.png){width="600" zoomable="yes"}

| Campo | Descrição |
|---|---|
| [!UICONTROL Import Amazon Orders] | Opções:<ul><li>**[!UICONTROL Disabled]** - Escolha quando você não deseja criar pedidos correspondentes no [!DNL Commerce] quando novos pedidos são recebidos da Amazon. Quando selecionados, todos os outros campos desta página são desativados.</li><li>**[!UICONTROL Enabled]** - (Padrão) Escolha quando deseja criar a correspondência [!DNL Commerce] pedidos quando novos pedidos são recebidos da Amazon. [!DNL Commerce] os pedidos são criados com base no status do Amazon e nos níveis de estoque.</li></ul><br><br>`Enabled` deve ser escolhido para gerenciar pedidos da Amazon no [!DNL Commerce]. Quando `Disabled` for escolhida, seus pedidos do Amazon serão exibidos no painel da loja, mas os pedidos deverão ser gerenciados no [!DNL Amazon Seller Central] conta. |
| [!UICONTROL Import Amazon Orders Into Magento Store] | Escolha qual [!DNL Commerce] armazenar os pedidos do Amazon que são associados quando são criados na [!DNL Commerce] [Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) espaço de trabalho. Essa configuração assume o padrão da Exibição de loja para [!DNL Commerce] site selecionado quando você [adicionou a loja da Amazon](./store-integration.md). Se quiser alterar essa configuração, a lista de opções dependerá do [!DNL Commerce] lojas que você configurou em sua configuração. Consulte [Lojas](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html). |
| [!UICONTROL Customer Creation] | Opções:<ul><li>**[!UICONTROL No Customer Creation (guest)]** - (Padrão) Escolha quando você não deseja criar uma conta de cliente no [!DNL Commerce] usando os dados do cliente importados do pedido do Amazon. Quando escolhida, essa opção informa ao [!DNL Commerce] para processar um pedido Amazon importado da mesma maneira que processa um check-out de convidado.</li><li>**[!UICONTROL Build New Customer Account]** - Escolha quando deseja criar uma Nova Conta de Cliente em sua [!DNL Commerce] banco de dados do cliente usando os dados do cliente importados com o pedido do Amazon. Essa opção ajuda a criar [!DNL Commerce] banco de dados do cliente dos seus pedidos da Amazon.</li></ul> |
| Origem do Número da Ordem | Opções:<ul><li>**[!UICONTROL Build Using Magento Order Number]** - (Padrão) Escolha quando deseja criar uma [!DNL Commerce] número do pedido do pedido Amazon correspondente usando o [!DNL Commerce] ID da ordem atribuída de forma incremental. </li><li>**Criar usando o número do pedido do Amazon** - Escolha quando deseja criar a variável [!DNL Commerce] número do pedido usando o número do pedido atribuído pela Amazon correspondente.</li></ul> |
| Pedidos pendentes | Opções:<ul><li>**[!UICONTROL Do Not Reserve Quantity]** - Escolha quando você não quer o seu [!DNL Commerce] quantidade em estoque afetada por seus pedidos do Amazon. Escolha se você usa o Amazon para o seu processo de preenchimento (FBA). Quando for escolhida e você receber um pedido Amazon, a quantidade solicitada não afetará o [!DNL Commerce] quantidade em estoque.</li><li>**[!UICONTROL Reserve Quantity]** - Escolha quando deseja que a quantidade do pedido na ordem do Amazon seja &quot;reservada&quot; na [!DNL Commerce] quantidade em estoque. Quando for escolhida e você receber um pedido Amazon, a quantidade solicitada será &quot;reservada&quot; em seu [!DNL Commerce] quantidade em estoque para evitar que seu [!DNL Commerce] ações de &quot;venda excessiva&quot;. A quantidade &quot;reservada&quot; não está disponível para compra por meio do [!DNL Commerce] vitrine eletrônica.</li></ul> |
| [!UICONTROL Order Status] | Opções:<ul><li>**[!UICONTROL Default Order Status]** - (Padrão) Escolha quando deseja que as ordens recém-criadas importadas do Amazon recebam o status de ordem padrão para novas ordens. O status padrão para novos pedidos (a menos que você tenha criado um status de pedido personalizado para novos pedidos) é `Pending`. Consulte [Processamento de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).</li><li>>**[!UICONTROL Custom Order Status]** - Escolha quando deseja que as ordens recém-criadas importadas do Amazon recebam um status diferente do padrão. Quando escolhido, **[!UICONTROL Processing Order Status]** permite que você escolha o status que deseja usar para ordens recém-criadas importadas do Amazon.</li></ul> |
| [!UICONTROL Processing Orders Status] | Ativado quando _[!UICONTROL Order Status]_está definida como `Custom Order Status`. Escolha o status da ordem que deseja atribuir às novas ordens. As opções nesse campo dependem das opções de status padrão no [!DNL Commerce]. Consulte [Status do pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html). Você também pode criar um status de pedido personalizado para mostrar aqui. Para criar um status de pedido personalizado, consulte [Status do pedido personalizado]( | [!UICONTROL Processing Orders Status] | Ativado quando _[!UICONTROL Order Status]_está definida como `Custom Order Status`. Escolha o status da ordem que deseja atribuir às novas ordens. As opções nesse campo dependem das opções de status padrão no [!DNL Commerce]. Consulte [Status do pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html). Você também pode criar um status de pedido personalizado para mostrar aqui. Para criar um status de pedido personalizado, consulte [Status do pedido personalizado](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html#custom-order-status). |
| ). |

## [!DNL Commerce] criação de pedido

[!DNL Commerce] as ordens são criadas para ordens do Amazon com base no status e nas condições de inventário a seguir.

### Criação de pedidos com o Inventory management

>[!NOTE]
>
>Suportado somente em integrações Adobe Commerce e Magento Open Source 2.3.x.

| Canal de Abastecimento | [!DNL Commerce] Status do inventário | Status do pedido Amazon | [!UICONTROL Create Magento Order] Configuração | Estoque Reservado |
|---|---|---|---|---|
| FBA | Em estoque<br>Sem estoque<br>Não Gerenciar | Pending | Não | Não |
| FBA | Em estoque<br>Sem estoque<br>Não Gerenciar | PendingAvailability | Não | Não |
| FBA | Em estoque<br>Sem estoque<br>Não Gerenciar | Cancelado | Não | Não |
| FBA | Em estoque<br>Sem estoque<br>Não Gerenciar | Erro | Não | Não |
| FBA | Em estoque<br>Sem estoque<br>Não Gerenciar | Não remetido | Não | Não |
| FBA | Em estoque<br>Sem estoque<br>Não Gerenciar | ParcialmenteEnviado | Não | Não |
| FBA | Em estoque<br>Não Gerenciar | Enviado | Sim | Não |
| FBA | Sem estoque | Enviado | Não | Não |
| FBM | Em estoque<br>Sem estoque<br>Não Gerenciar | Pending | Não | Não |
| FBM | Em estoque<br>Sem estoque<br>Não Gerenciar | PendingAvailability | Não | Não |
| FBM | Em estoque<br>Sem estoque<br>Não Gerenciar | Cancelado | Não | Não |
| FBM | Em estoque<br>Sem estoque<br>Não Gerenciar | Erro | Não | Não |
| FBM | Em estoque<br>Não Gerenciar | Não remetido | Sim | Sim |
| FBM | Sem estoque | Não remetido | Não | Não |
| FBM | Em estoque<br>Não Gerenciar | ParcialmenteEnviado | Sim | Sim |
| FBM | Sem estoque | ParcialmenteEnviado | Não | Não |
| FBM | Em estoque<br>Não Gerenciar | Enviado | Sim | Sim |
| FBM | Sem estoque | Enviado | Não | Não |

>[!NOTE]
>Se um pedido do Amazon for importado em um `Partially Shipped` ou `Shipped` status, a reserva de estoque criada é para todos os itens na ordem. O canal de vendas da Amazon não compensa itens que foram enviados anteriormente.
>
>Se um pedido for Atendido pela Amazon (FBA), mas um item estiver em `out of stock` status, [!DNL Commerce] O não pode criar uma ordem correspondente. Essa é uma limitação das integrações do Inventory management.
