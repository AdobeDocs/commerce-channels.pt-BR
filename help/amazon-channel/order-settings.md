---
title: Configurações da ordem
description: Use as configurações de Pedido para determinar como os pedidos Amazon são importados e processados na loja do Commerce.
redirect_from: /sales-channels/asc/ob-order-settings.html: 
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 1462
ht-degree: 0%

---

# Configurações da ordem

As configurações de pedido definem se e como os pedidos Amazon são importados e processados em [!DNL Commerce] e podem ser acessados no [painel de loja](./amazon-store-dashboard.md).

As configurações de importação de pedido são definidas como `Enabled` por padrão, o que significa que seus pedidos do Amazon aparecem no painel de loja e criam pedidos [!DNL Commerce] correspondentes. Os pedidos importados podem ser gerenciados no workflow [!DNL Commerce] [Orders](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}.

>[!NOTE]
>
>Independentemente das configurações de seu pedido, os pedidos da Amazon que existiam antes da integração de loja não são importados.

Depois que [armazenar integração](./store-integration.md) for concluída, você poderá alterar as configurações do pedido. Se você definir as configurações de pedido como `Disabled`, os pedidos do Amazon serão exibidos no painel da loja, mas deverão ser gerenciados em sua conta [!DNL Amazon Seller Central].

Quando um pedido é criado no Amazon, ele não é importado imediatamente para [!DNL Commerce]. A Amazon atribui um status `Pending` a pedidos recém-criados. Depois que a Amazon verificar o pedido e o método de pagamento, o status do pedido é alterado para `Unshipped`. Essa alteração de status aciona a importação da ordem e [!DNL Commerce] cria uma ordem correspondente.

Os pedidos importados do Amazon podem ser gerenciados no [!DNL Commerce] [fluxo de trabalho de pedidos](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}. Consulte também [Gerenciar pedidos](./managing-orders.md).

## Definir configurações de ordem {#configure-order-settings}

1. Clique em **[!UICONTROL Order Settings]** no painel da loja.

1. Para **[!UICONTROL Import Amazon Orders]** (obrigatório), escolha uma opção:

   - `Disabled` - Escolha quando você não deseja criar ordens correspondentes em  [!DNL Commerce] quando novos pedidos forem recebidos da Amazon. Quando escolhidos, todos os outros campos nesta página serão desativados.

   - `Enabled` - (Padrão) Escolha quando deseja criar  [!DNL Commerce] ordens correspondentes quando novos pedidos forem recebidos da Amazon. [!DNL Commerce] os pedidos são criados com base no status da Amazon e nos níveis de estoque.

      >[!NOTE]
      >
      >Importar pedidos da Amazon deve ser definido como `Enabled` para gerenciar pedidos da Amazon no fluxo de trabalho [!DNL Commerce] [orders](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}. Quando definido como `Disabled`, seus pedidos Amazon não têm um número de ordem [!DNL Commerce] correspondente e não podem ser gerenciados em [!DNL Commerce]. Você gerencia esses pedidos em sua conta [!DNL Amazon Seller Central].

1. Para **[!UICONTROL Import Amazon Orders Into Magento Store]**, escolha a qual [!DNL Commerce] armazenar os pedidos do Amazon estão associados quando a ordem correspondente é criada em [!DNL Commerce].

   Essa configuração assume como padrão a Exibição de armazenamento do site selecionado quando você [adiciona o Amazon store](./store-integration.md). Se você quiser alterar essa configuração, a lista de opções dependerá dos armazenamentos [!DNL Commerce] que você configurou em sua configuração. Consulte [Lojas](https://docs.magento.com/user-guide/stores/stores-all-create-view.html#create-a-new-store-view){:target=&quot;_blank&quot;}.

1. Para **[!UICONTROL Customer Creation]**, escolha uma opção:

   - `No Customer Creation (guest)` - (Padrão) Escolha quando não deseja criar uma conta de cliente no  [!DNL Commerce] uso dos dados de cliente importados do pedido da Amazon. Quando escolhido, [!DNL Commerce] processa um pedido Amazon importado da mesma forma que processa um check-out de convidado em [!DNL Commerce].

   - `Build New Customer Account` - Escolha quando deseja criar uma Nova Conta de Cliente ao  [!DNL Commerce] usar os dados de cliente importados com o pedido da Amazon. Essa opção ajuda a criar o banco de dados do cliente a partir de seus pedidos da Amazon.

1. Para **[!UICONTROL Order Number Source]**, escolha uma opção:

   - `Build Using Magento Order Number` - (Padrão) Escolha quando deseja criar um número de  [!DNL Commerce] pedido exclusivo para o pedido Amazon correspondente usando a ID de pedido atribuída de  [!DNL Commerce] forma incremental.

   - `Build Using Amazon Order Number` - Escolha quando deseja criar o número do  [!DNL Commerce] pedido usando o número do pedido atribuído pela Amazon correspondente.
   >[!NOTE]
   >
   >Depois que um pedido é importado, o número do pedido Amazon é exibido na lista _[!UICONTROL Recent Orders]_no painel da loja. O número do pedido [!DNL Commerce] é exibido ao visualizar os detalhes do pedido no espaço de trabalho [!DNL Commerce] [Orders](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}.

1. Para **[!UICONTROL Order Status]** (obrigatório), escolha uma opção:

   - `Default Order Status` - (Padrão) Escolha quando deseja que os pedidos recém-criados importados da Amazon sejam atribuídos ao status de ordem padrão definido para novos pedidos. O status padrão para novos pedidos (a menos que você tenha criado um status de pedido personalizado para novos pedidos) é `Pending`. Consulte [Processando Pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){:target=&quot;_blank&quot;}.

   - `Custom Order Status` - Escolha quando deseja que pedidos recém-criados importados da Amazon recebam um status diferente do padrão.

   - `Processing Order Status` - Ativado quando  **[!UICONTROL Order Status]** está definido como  `Custom Order Status`. Escolha o status que deseja usar para pedidos recém-criados importados do Amazon. As opções neste campo são baseadas nas opções de status padrão em [!DNL Commerce]. Consulte [Status do Pedido](https://docs.magento.com/user-guide/sales/order-status.html). Você também pode criar um status de pedido personalizado para mostrar aqui para seleção. Para criar um status de pedido personalizado, consulte [Status do Pedido Personalizado](https://docs.magento.com/user-guide/sales/order-status-custom.html){:target=&quot;_blank&quot;}.

1. Quando terminar, clique em **[!UICONTROL Save order settings]**.

![Configurações da ordem](assets/amazon-order-settings.png)

| Campo | Descrição |
|---|---|
| [!UICONTROL Import Amazon Orders] | Opções:<ul><li>**[!UICONTROL Disabled]** - Escolha quando você não deseja criar ordens correspondentes em  [!DNL Commerce] quando novos pedidos forem recebidos da Amazon. Quando escolhidos, todos os outros campos nesta página serão desativados.</li><li>**[!UICONTROL Enabled]** - (Padrão) Escolha quando deseja criar  [!DNL Commerce] ordens correspondentes quando novos pedidos forem recebidos da Amazon. [!DNL Commerce] os pedidos são criados com base no status da Amazon e nos níveis de estoque.</li></ul><br><br>`Enabled` deve ser escolhido para gerenciar pedidos da Amazon no  [!DNL Commerce]. Quando `Disabled` é escolhido, seus pedidos do Amazon são exibidos no painel de loja, mas os pedidos devem ser gerenciados em sua conta [!DNL Amazon Seller Central]. |
| [!UICONTROL Import Amazon Orders Into Magento Store] | Escolha a qual [!DNL Commerce] armazenar os pedidos do Amazon estão associados quando são criados no espaço de trabalho [!DNL Commerce] [Orders](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}. Essa configuração assume como padrão a Visualização de loja do [!DNL Commerce] site selecionado quando você [adiciona o Amazon store](./store-integration.md). Se você quiser alterar essa configuração, a lista de opções dependerá dos armazenamentos [!DNL Commerce] que você configurou em sua configuração. Consulte [Lojas](https://docs.magento.com/user-guide/stores/stores-all-stores.html){:target=&quot;_blank&quot;}. |
| [!UICONTROL Customer Creation] | Opções:<ul><li>**[!UICONTROL No Customer Creation (guest)]** - (Padrão) Escolha quando não deseja criar uma conta de cliente no  [!DNL Commerce] uso dos dados de cliente importados do pedido da Amazon. Quando escolhida, essa opção informa [!DNL Commerce] para processar um pedido Amazon importado da mesma forma que processa um check-out de convidado.</li><li>**[!UICONTROL Build New Customer Account]** - Escolha quando deseja criar uma Nova Conta de Cliente no banco de dados de seu  [!DNL Commerce] cliente usando os dados do cliente importados com o pedido da Amazon. Essa opção ajuda a criar o banco de dados [!DNL Commerce] do cliente a partir de seus pedidos do Amazon.</li></ul> |
| Origem do Número da Ordem | Opções:<ul><li>**[!UICONTROL Build Using Magento Order Number]** - (Padrão) Escolha quando deseja criar um número de  [!DNL Commerce] pedido exclusivo para o pedido Amazon correspondente usando a ID de pedido atribuída de  [!DNL Commerce] forma incremental. </li><li>**Criar usando o número do pedido da Amazon**  - Escolha quando deseja criar o número do  [!DNL Commerce] pedido usando o número do pedido atribuído pela Amazon correspondente.</li></ul> |
| Pedidos pendentes | Opções:<ul><li>**[!UICONTROL Do Not Reserve Quantity]** - Escolha quando você não deseja que sua quantidade  [!DNL Commerce] de estoque seja afetada por seus pedidos Amazon. Escolha se você usa o Amazon para o seu processo de atendimento (FBA). Quando escolhida e você receber um pedido Amazon, a quantidade solicitada não afetará sua quantidade [!DNL Commerce] de estoque.</li><li>**[!UICONTROL Reserve Quantity]** - Escolha quando deseja que a quantidade da ordem no Amazon seja &quot;reservada&quot; na quantidade  [!DNL Commerce] de estoque. Quando escolhida e você receber um pedido da Amazon, a quantidade solicitada será &quot;reservada&quot; em sua [!DNL Commerce] quantidade de estoque para evitar que seu [!DNL Commerce] estoque seja &quot;vendido em excesso&quot;. A quantidade &quot;reservada&quot; não está disponível para compra por meio da loja [!DNL Commerce].</li></ul> |
| [!UICONTROL Order Status] | Opções:<ul><li>**[!UICONTROL Default Order Status]** - (Padrão) Escolha quando deseja que os pedidos recém-criados importados da Amazon sejam atribuídos ao status de pedido padrão para novos pedidos. O status padrão para novos pedidos (a menos que você tenha criado um status de pedido personalizado para novos pedidos) é `Pending`. Consulte [Processando Pedidos](https://docs.magento.com/user-guide/sales/order-processing.html).</li><li>>**[!UICONTROL Custom Order Status]** - Escolha quando deseja que os pedidos recém-criados importados do Amazon recebam um status diferente do padrão. Quando escolhido, **[!UICONTROL Processing Order Status]** permite que você escolha o status que deseja usar para pedidos recém-criados importados do Amazon.</li></ul> |
| [!UICONTROL Processing Orders Status] | Ativado quando _[!UICONTROL Order Status]_está definido como `Custom Order Status`. Escolha o status da ordem que deseja atribuir a novas ordens. As opções neste campo dependem das opções de status padrão em [!DNL Commerce]. Consulte [Status do Pedido](https://docs.magento.com/user-guide/sales/order-status.html){:target=&quot;_blank&quot;}. Você também pode criar um status de pedido personalizado para mostrar aqui. Para criar um status de pedido personalizado, consulte [Status do Pedido Personalizado](https://docs.magento.com/user-guide/sales/order-status-custom.html){:target=&quot;_blank&quot;}. |

## [!DNL Commerce] criação de pedidos

[!DNL Commerce] os pedidos são criados para pedidos da Amazon com base no status e nas condições de inventário a seguir.

### Criação de Ordens com Gerenciamento de Inventário

>[!NOTE]
>
>Suportado somente nas integrações do Adobe Commerce e Magento Open Source 2.3.x.

| Canal de Cumprimento | [!DNL Commerce] Status do inventário | Status do pedido Amazon | [!UICONTROL Create Magento Order] Configuração | Inventário Reservado |
|---|---|---|---|---|
| FBA | Em estoque<br>Não disponível para estoque<br>Não gerenciar | Pending | Não | Não |
| FBA | Em estoque<br>Não disponível para estoque<br>Não gerenciar | PendingAvailability | Não | Não |
| FBA | Em estoque<br>Não disponível para estoque<br>Não gerenciar | Cancelado | Não | Não |
| FBA | Em estoque<br>Não disponível para estoque<br>Não gerenciar | Erro | Não | Não |
| FBA | Em estoque<br>Não disponível para estoque<br>Não gerenciar | Não Entregue | Não | Não |
| FBA | Em estoque<br>Não disponível para estoque<br>Não gerenciar | ParcialmenteEnviado | Não | Não |
| FBA | Em estoque<br>Não Gerenciar | Entregue | Sim | Não |
| FBA | Produto esgotado | Entregue | Não | Não |
| FBM | Em estoque<br>Não disponível para estoque<br>Não gerenciar | Pending | Não | Não |
| FBM | Em estoque<br>Não disponível para estoque<br>Não gerenciar | PendingAvailability | Não | Não |
| FBM | Em estoque<br>Não disponível para estoque<br>Não gerenciar | Cancelado | Não | Não |
| FBM | Em estoque<br>Não disponível para estoque<br>Não gerenciar | Erro | Não | Não |
| FBM | Em estoque<br>Não Gerenciar | Não Entregue | Sim | Sim |
| FBM | Produto esgotado | Não Entregue | Não | Não |
| FBM | Em estoque<br>Não Gerenciar | ParcialmenteEnviado | Sim | Sim |
| FBM | Produto esgotado | ParcialmenteEnviado | Não | Não |
| FBM | Em estoque<br>Não Gerenciar | Entregue | Sim | Sim |
| FBM | Produto esgotado | Entregue | Não | Não |

>[!NOTE]
>Se um pedido Amazon for importado em um status `Partially Shipped` ou `Shipped`, a reserva de inventário criada será para todos os itens na ordem. O canal de vendas da Amazon não compensa itens que foram enviados anteriormente.
>
>Se um pedido for preenchido pelo Amazon (FBA), mas um item estiver no status `out of stock` , [!DNL Commerce] não poderá criar um pedido correspondente. Essa é uma limitação das integrações de Gerenciamento de inventário.
