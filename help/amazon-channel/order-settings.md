---
title: Configurações de pedido do Amazon
description: Use as configurações de Pedido para determinar como os pedidos do Amazon são importados e processados na loja da Commerce.
feature: Sales Channels, Orders, Inventory, Configuration
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: a93ba31a95f32cc6ea285aed2399255021985693
workflow-type: tm+mt
source-wordcount: '1388'
ht-degree: 0%

---

# Configurações de pedido do Amazon

As configurações de pedido definem se e como os pedidos do Amazon são importados e processados em [!DNL Commerce] e podem ser acessados no [painel de armazenamento](./amazon-store-dashboard.md).

As configurações de importação de pedido estão definidas como `Enabled` por padrão, o que significa que seus pedidos do Amazon aparecem no painel de armazenamento e criam pedidos [!DNL Commerce] correspondentes. Os pedidos importados podem ser gerenciados no fluxo de trabalho [!DNL Commerce] [Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).

>[!NOTE]
>
>Independentemente das configurações do pedido, os pedidos do Amazon existentes antes da integração da loja não são importados.

Depois que a [integração de loja](./store-integration.md) for concluída, você poderá alterar as configurações de pedido. Se você definir as configurações do pedido como `Disabled`, os pedidos do Amazon serão exibidos no painel da loja, mas deverão ser gerenciados na sua conta [!DNL Amazon Seller Central].

Quando um pedido é criado no Amazon, ele não é importado imediatamente para o [!DNL Commerce]. O Amazon atribui um status `Pending` a pedidos recém-criados. Depois que a Amazon verificar o pedido e a forma de pagamento, o status do pedido é alterado para `Unshipped`. Esta alteração de status dispara a importação da ordem e [!DNL Commerce] cria uma ordem correspondente.

Os pedidos importados da Amazon podem ser gerenciados no [!DNL Commerce] [fluxo de trabalho de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html). Consulte também [Gerenciar pedidos](./managing-orders.md).

## Definir configurações de pedido {#configure-order-settings}

1. Clique em **[!UICONTROL Order Settings]** no painel da loja.

1. Para **[!UICONTROL Import Amazon Orders]** (obrigatório), escolha uma opção:

   - `Disabled` - Escolha quando você não deseja criar pedidos correspondentes em [!DNL Commerce] quando novos pedidos forem recebidos da Amazon. Quando selecionados, todos os outros campos desta página são desativados.

   - `Enabled` - (Padrão) Escolha quando deseja criar [!DNL Commerce] pedidos correspondentes quando novos pedidos forem recebidos da Amazon. [!DNL Commerce] pedidos são criados com base no status do Amazon e nos níveis de estoque.

     >[!NOTE]
     >
     >Importar Pedidos Amazon deve ser definido como `Enabled` para gerenciar pedidos Amazon no fluxo de trabalho [!DNL Commerce] [pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html). Quando definido como `Disabled`, seus pedidos do Amazon não têm um número de pedido [!DNL Commerce] correspondente e não podem ser gerenciados em [!DNL Commerce]. Você gerencia esses pedidos na sua conta [!DNL Amazon Seller Central].

1. Para **[!UICONTROL Import Amazon Orders Into Magento Store]**, escolha a qual [!DNL Commerce] armazenará os pedidos do Amazon associados quando o pedido correspondente for criado em [!DNL Commerce].

   Esta configuração é padronizada para o Modo de Exibição de Loja do site selecionado quando você [adicionou a loja da Amazon](./store-integration.md). Se você quiser alterar essa configuração, a lista de opções dependerá dos [!DNL Commerce] armazenamentos configurados na sua configuração. Consulte [Lojas](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html).

1. Para **[!UICONTROL Customer Creation]**, escolha uma opção:

   - `No Customer Creation (guest)` - (Padrão) Escolha quando você não deseja criar uma conta de cliente em [!DNL Commerce] usando os dados de cliente importados da ordem do Amazon. Quando escolhido, o [!DNL Commerce] processa um pedido de Amazon importado da mesma forma que processa um check-out de convidado no [!DNL Commerce].

   - `Build New Customer Account` - Escolha quando deseja criar uma Nova Conta de Cliente em [!DNL Commerce] usando os dados do cliente importados com o pedido do Amazon. Essa opção ajuda a criar o banco de dados do cliente a partir dos pedidos da Amazon.

1. Para **[!UICONTROL Order Number Source]**, escolha uma opção:

   - `Build Using Magento Order Number` - (Padrão) Escolha quando deseja criar um número de pedido [!DNL Commerce] exclusivo para o pedido Amazon correspondente usando a ID de pedido atribuída de forma incremental [!DNL Commerce].

   - `Build Using Amazon Order Number` - Escolha quando deseja criar o número de pedido [!DNL Commerce] usando o número de pedido atribuído pela Amazon correspondente.

   >[!NOTE]
   >
   >Depois que um pedido é importado, o número do pedido do Amazon é exibido na lista _[!UICONTROL Recent Orders]_no painel da loja. O número do pedido [!DNL Commerce] é exibido ao visualizar os detalhes do pedido no espaço de trabalho [!DNL Commerce] [Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).

1. Para **[!UICONTROL Order Status]** (obrigatório), escolha uma opção:

   - `Default Order Status` - (Padrão) Escolha quando deseja que os pedidos recém-criados importados da Amazon recebam o status de pedido padrão definido para os novos pedidos. O status padrão para novos pedidos (a menos que você tenha criado um status de pedido personalizado para novos pedidos) é `Pending`. Consulte [Processando Ordens](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

   - `Custom Order Status` - Escolha quando deseja que as ordens recém-criadas importadas do Amazon recebam um status diferente do padrão.

   - `Processing Order Status` - Habilitado quando **[!UICONTROL Order Status]** está definido como `Custom Order Status`. Escolha o status que deseja usar para pedidos recém-criados importados do Amazon. As opções neste campo são baseadas nas opções de status padrão em [!DNL Commerce]. Consulte [Status do pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html). Você também pode criar um status de pedido personalizado para mostrar aqui para seleção. Para criar um status de pedido personalizado, consulte [Status de Pedido Personalizado](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html#custom-order-status).

1. Quando terminar, clique em **[!UICONTROL Save order settings]**.

![Configurações do pedido](assets/amazon-order-settings.png){width="600" zoomable="yes"}

| Campo | Descrição |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Import Amazon Orders] | Opções:<ul><li>**[!UICONTROL Disabled]** - Escolha quando você não deseja criar pedidos correspondentes em [!DNL Commerce] quando novos pedidos forem recebidos da Amazon. Quando selecionados, todos os outros campos desta página são desativados.</li><li>**[!UICONTROL Enabled]** - (Padrão) Escolha quando deseja criar [!DNL Commerce] pedidos correspondentes quando novos pedidos forem recebidos da Amazon. [!DNL Commerce] pedidos são criados com base no status do Amazon e nos níveis de estoque.</li></ul><br><br>`Enabled` deve ser escolhido para gerenciar pedidos da Amazon em [!DNL Commerce]. Quando `Disabled` é escolhido, seus pedidos do Amazon são exibidos no painel da loja, mas os pedidos devem ser gerenciados na sua conta [!DNL Amazon Seller Central]. |
| [!UICONTROL Import Amazon Orders Into Magento Store] | Escolha a qual [!DNL Commerce] armazenam os pedidos do Amazon associados quando eles são criados no espaço de trabalho [!DNL Commerce] [Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html). Esta configuração é padronizada para o Modo de Exibição de Loja do site [!DNL Commerce] selecionado quando você [adicionou a loja da Amazon](./store-integration.md). Se você quiser alterar essa configuração, a lista de opções dependerá dos [!DNL Commerce] armazenamentos configurados na sua configuração. Consulte [Lojas](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html). |
| [!UICONTROL Customer Creation] | Opções:<ul><li>**[!UICONTROL No Customer Creation (guest)]** - (Padrão) Escolha quando você não deseja criar uma conta de cliente em [!DNL Commerce] usando os dados de cliente importados da ordem do Amazon. Quando escolhida, essa opção informa ao [!DNL Commerce] para processar um pedido Amazon importado da mesma maneira que processa um check-out de convidado.</li><li>**[!UICONTROL Build New Customer Account]** - Escolha quando deseja criar uma Nova Conta de Cliente no banco de dados de clientes [!DNL Commerce] usando os dados do cliente importados com o pedido do Amazon. Esta opção ajuda a criar o banco de dados do cliente do [!DNL Commerce] a partir dos seus pedidos da Amazon.</li></ul> |
| Número do pedido Source | Opções:<ul><li>**[!UICONTROL Build Using Magento Order Number]** - (Padrão) Escolha quando deseja criar um número de pedido [!DNL Commerce] exclusivo para o pedido Amazon correspondente usando a ID de pedido atribuída de forma incremental [!DNL Commerce]. </li><li>**Criar Usando o Número do Pedido da Amazon** - Escolha quando deseja criar o número do pedido [!DNL Commerce] usando o número do pedido atribuído pela Amazon correspondente.</li></ul> |
| Pedidos pendentes | Opções:<ul><li>**[!UICONTROL Do Not Reserve Quantity]** - Escolha quando não deseja que a quantidade em estoque de [!DNL Commerce] seja afetada por seus pedidos da Amazon. Escolha se você usa o Amazon para o seu processo de preenchimento (FBA). Quando escolhido e você recebe um pedido Amazon, a quantidade solicitada não afeta sua quantidade em estoque [!DNL Commerce].</li><li>**[!UICONTROL Reserve Quantity]** - Escolha quando deseja que a quantidade da ordem na Amazon seja &quot;reservada&quot; na quantidade em estoque de [!DNL Commerce]. Quando for escolhida e você receber um pedido Amazon, a quantidade solicitada será &quot;reservada&quot; na quantidade em estoque do seu [!DNL Commerce] para evitar que seu estoque do [!DNL Commerce] seja &quot;vendido em excesso&quot;. A quantidade &quot;reservada&quot; não está disponível para compra em sua loja [!DNL Commerce].</li></ul> |
| [!UICONTROL Order Status] | Opções:<ul><li>**[!UICONTROL Default Order Status]** - (Padrão) Escolha quando deseja que os pedidos recém-criados importados da Amazon recebam o status de pedido padrão para novos pedidos. O status padrão para novos pedidos (a menos que você tenha criado um status de pedido personalizado para novos pedidos) é `Pending`. Consulte [Processando Ordens](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).</li><li>**[!UICONTROL Custom Order Status]** - Escolha quando deseja que as ordens recém-criadas importadas do Amazon recebam um status diferente do padrão. Quando escolhido, o **[!UICONTROL Processing Order Status]** permite que você escolha o status que deseja usar para pedidos recém-criados importados da Amazon.</li></ul> |
| [!UICONTROL Processing Orders Status] | Habilitado quando _[!UICONTROL Order Status]_está definido como `Custom Order Status`. Escolha o status da ordem que deseja atribuir às novas ordens. As opções neste campo dependem das opções de status padrão em [!DNL Commerce]. Consulte [Status do pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html). Você também pode criar um status de pedido personalizado para mostrar aqui. Para criar um status de pedido personalizado, consulte [Status de Pedido Personalizado] |

## Criação de pedido [!DNL Commerce]

[!DNL Commerce] ordens são criadas para ordens do Amazon com base no status e nas condições de estoque a seguir.

### Criação de pedidos com o Inventory management

>[!NOTE]
>
>Suportado somente em integrações Adobe Commerce e Magento Open Source 2.3.x.

| Canal de Abastecimento | Status do inventário de [!DNL Commerce] | Status do pedido Amazon | Configuração de [!UICONTROL Create Magento Order] | Estoque Reservado |
|---------------------|-------------------------------------------|---------------------|-------------------------------------------|--------------------|
| FBA | Em estoque<br>Fora de estoque<br>Não Gerenciar | Pending | Não | Não |
| FBA | Em estoque<br>Fora de estoque<br>Não Gerenciar | PendingAvailability | Não | Não |
| FBA | Em estoque<br>Fora de estoque<br>Não Gerenciar | Cancelado | Não | Não |
| FBA | Em estoque<br>Fora de estoque<br>Não Gerenciar | Erro | Não | Não |
| FBA | Em estoque<br>Fora de estoque<br>Não Gerenciar | Não remetido | Não | Não |
| FBA | Em estoque<br>Fora de estoque<br>Não Gerenciar | ParcialmenteEnviado | Não | Não |
| FBA | Em estoque<br>Não Gerenciar | Enviado | Sim | Não |
| FBA | Sem estoque | Enviado | Não | Não |
| FBM | Em estoque<br>Fora de estoque<br>Não Gerenciar | Pending | Não | Não |
| FBM | Em estoque<br>Fora de estoque<br>Não Gerenciar | PendingAvailability | Não | Não |
| FBM | Em estoque<br>Fora de estoque<br>Não Gerenciar | Cancelado | Não | Não |
| FBM | Em estoque<br>Fora de estoque<br>Não Gerenciar | Erro | Não | Não |
| FBM | Em estoque<br>Não Gerenciar | Não remetido | Sim | Sim |
| FBM | Sem estoque | Não remetido | Não | Não |
| FBM | Em estoque<br>Não Gerenciar | ParcialmenteEnviado | Sim | Sim |
| FBM | Sem estoque | ParcialmenteEnviado | Não | Não |
| FBM | Em estoque<br>Não Gerenciar | Enviado | Sim | Sim |
| FBM | Sem estoque | Enviado | Não | Não |

>[!NOTE]
>Se um pedido Amazon for importado com um status `Partially Shipped` ou `Shipped`, a reserva de estoque criada é para todos os itens no pedido. O canal de vendas da Amazon não compensa itens que foram enviados anteriormente.
>
>Se um pedido for Atendido pela Amazon (FBA), mas um item estiver no status `out of stock`, [!DNL Commerce] não poderá criar um pedido correspondente. Essa é uma limitação das integrações do Inventory management.
