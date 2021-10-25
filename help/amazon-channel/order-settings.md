---
title: Configurações da ordem
description: Use as configurações de Pedido para determinar como os pedidos Amazon são importados e processados na loja do Commerce.
redirect_from: /sales-channels/asc/ob-order-settings.html
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '1462'
ht-degree: 0%

---

# Configurações da ordem

As configurações de pedido definem se e como os pedidos Amazon são importados e processados em [!DNL Commerce] e podem ser acessadas na [painel de loja](./amazon-store-dashboard.md).

As configurações de importação de ordem estão definidas como `Enabled` por padrão, o que significa que os pedidos da Amazon são exibidos no painel da loja e criam os [!DNL Commerce] ordens. Os pedidos importados podem ser gerenciados no [!DNL Commerce] [Pedidos](https://docs.magento.com/user-guide/sales/orders.html)Fluxo de trabalho {target=&quot;_blank&quot;}.

>[!NOTE]
>
>Independentemente das configurações de seu pedido, os pedidos da Amazon que existiam antes da integração de loja não são importados.

Depois [integração de loja](./store-integration.md) estiver concluído, você poderá alterar as configurações do pedido. Se você definir as configurações de pedido como `Disabled`, os pedidos da Amazon são exibidos no painel da loja, mas devem ser gerenciados em [!DNL Amazon Seller Central] conta.

Quando um pedido é criado no Amazon, ele não é imediatamente importado para o [!DNL Commerce]. A Amazon atribui um `Pending` status para ordens recém-criadas. Depois que a Amazon verificar o pedido e o método de pagamento, o status do pedido é alterado para `Unshipped`. Essa alteração de status aciona a importação de pedidos e [!DNL Commerce] cria uma ordem correspondente.

Os pedidos importados da Amazon podem ser gerenciados na variável [!DNL Commerce] [fluxo de trabalho de pedidos](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}. Consulte também [Gerenciar pedidos](./managing-orders.md).

## Definir configurações de ordem {#configure-order-settings}

1. Clique em **[!UICONTROL Order Settings]** no painel da loja.

1. Para **[!UICONTROL Import Amazon Orders]** (obrigatório), escolha uma opção:

   - `Disabled` - Escolha quando você não deseja criar ordens correspondentes em [!DNL Commerce] quando novos pedidos são recebidos da Amazon. Quando escolhidos, todos os outros campos nesta página serão desativados.

   - `Enabled` - (Padrão) Escolha quando deseja criar um [!DNL Commerce] pedidos quando novos pedidos são recebidos da Amazon. [!DNL Commerce] os pedidos são criados com base no status da Amazon e nos níveis de estoque.

      >[!NOTE]
      >
      >Importar pedidos da Amazon deve ser definido como `Enabled` para gerenciar pedidos da Amazon na [!DNL Commerce] [ordens](https://docs.magento.com/user-guide/sales/orders.html)Fluxo de trabalho {target=&quot;_blank&quot;}. Quando definido como `Disabled`, seus pedidos do Amazon não têm um [!DNL Commerce] número do pedido e não pode ser gerenciado em [!DNL Commerce]. Você gerencia esses pedidos em seu [!DNL Amazon Seller Central] conta.

1. Para **[!UICONTROL Import Amazon Orders Into Magento Store]**, escolha qual [!DNL Commerce] armazene os pedidos da Amazon associados quando o pedido correspondente é criado em [!DNL Commerce].

   Esta configuração assume como padrão a Visualização de armazenamento do site selecionado ao [adição da loja Amazon](./store-integration.md). Se você quiser alterar essa configuração, a lista de opções dependerá do [!DNL Commerce] armazenamentos que você configurou em sua configuração. Consulte [Lojas](https://docs.magento.com/user-guide/stores/stores-all-create-view.html#create-a-new-store-view){target=&quot;_blank&quot;}.

1. Para **[!UICONTROL Customer Creation]**, escolha uma opção:

   - `No Customer Creation (guest)` - (Padrão) Escolha quando você não deseja criar uma conta de cliente em [!DNL Commerce] usando os dados do cliente importados do pedido da Amazon. Quando escolhido, [!DNL Commerce] processa um pedido Amazon importado da mesma forma que processa um check-out de convidado em [!DNL Commerce].

   - `Build New Customer Account` - Escolha quando deseja criar uma Nova Conta de Cliente em [!DNL Commerce] usando os dados do cliente importados com o pedido da Amazon. Essa opção ajuda a criar o banco de dados do cliente a partir de seus pedidos da Amazon.

1. Para **[!UICONTROL Order Number Source]**, escolha uma opção:

   - `Build Using Magento Order Number` - (Padrão) Escolha quando deseja criar um [!DNL Commerce] número do pedido do pedido Amazon correspondente usando o [!DNL Commerce] ID de ordem atribuída de forma incremental.

   - `Build Using Amazon Order Number` - Escolha quando deseja criar o [!DNL Commerce] número do pedido usando o número do pedido atribuído pela Amazon correspondente.
   >[!NOTE]
   >
   >Depois que um pedido é importado, o número de pedido da Amazon é exibido na variável _[!UICONTROL Recent Orders]_no painel de loja. O [!DNL Commerce] o número do pedido é exibido ao exibir os detalhes do pedido na [!DNL Commerce] [Pedidos](https://docs.magento.com/user-guide/sales/orders.html)Espaço de trabalho {target=&quot;_blank&quot;}.

1. Para **[!UICONTROL Order Status]** (obrigatório), escolha uma opção:

   - `Default Order Status` - (Padrão) Escolha quando deseja que os pedidos recém-criados importados da Amazon sejam atribuídos ao status de ordem padrão definido para novos pedidos. O status padrão para novos pedidos (a menos que tenha criado um status de pedido personalizado para novos pedidos) é `Pending`. Consulte [Processamento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}.

   - `Custom Order Status` - Escolha quando deseja que pedidos recém-criados importados da Amazon recebam um status diferente do padrão.

   - `Processing Order Status` - Ativado quando **[!UICONTROL Order Status]** está definida como `Custom Order Status`. Escolha o status que deseja usar para pedidos recém-criados importados do Amazon. As opções neste campo são baseadas nas opções de status padrão em [!DNL Commerce]. Consulte [Status do pedido](https://docs.magento.com/user-guide/sales/order-status.html). Você também pode criar um status de pedido personalizado para mostrar aqui para seleção. Para criar um status de pedido personalizado, consulte [Status do pedido personalizado](https://docs.magento.com/user-guide/sales/order-status-custom.html){target=&quot;_blank&quot;}.

1. Ao concluir, clique em **[!UICONTROL Save order settings]**.

![Configurações da ordem](assets/amazon-order-settings.png)

| Campo | Descrição |
|---|---|
| [!UICONTROL Import Amazon Orders] | Opções:<ul><li>**[!UICONTROL Disabled]** - Escolha quando você não deseja criar ordens correspondentes em [!DNL Commerce] quando novos pedidos são recebidos da Amazon. Quando escolhidos, todos os outros campos nesta página serão desativados.</li><li>**[!UICONTROL Enabled]** - (Padrão) Escolha quando deseja criar um [!DNL Commerce] pedidos quando novos pedidos são recebidos da Amazon. [!DNL Commerce] os pedidos são criados com base no status da Amazon e nos níveis de estoque.</li></ul><br><br>`Enabled` deve ser escolhido para gerenciar os pedidos da Amazon em [!DNL Commerce]. When `Disabled` for escolhida, seus pedidos do Amazon serão exibidos no painel da loja, mas os pedidos deverão ser gerenciados em [!DNL Amazon Seller Central] conta. |
| [!UICONTROL Import Amazon Orders Into Magento Store] | Escolha qual [!DNL Commerce] armazene os pedidos da Amazon associados ao quando eles são criados na [!DNL Commerce] [Pedidos](https://docs.magento.com/user-guide/sales/orders.html)Espaço de trabalho {target=&quot;_blank&quot;}. Essa configuração assume como padrão a Exibição de armazenamento da variável [!DNL Commerce] site selecionado ao [adição da loja Amazon](./store-integration.md). Se você quiser alterar essa configuração, a lista de opções dependerá do [!DNL Commerce] armazenamentos que você configurou em sua configuração. Consulte [Lojas](https://docs.magento.com/user-guide/stores/stores-all-stores.html){target=&quot;_blank&quot;}. |
| [!UICONTROL Customer Creation] | Opções:<ul><li>**[!UICONTROL No Customer Creation (guest)]** - (Padrão) Escolha quando você não deseja criar uma conta de cliente em [!DNL Commerce] usando os dados do cliente importados do pedido da Amazon. Quando escolhida, essa opção informa [!DNL Commerce] para processar um pedido importado do Amazon da mesma forma que processa um check-out de convidado.</li><li>**[!UICONTROL Build New Customer Account]** - Escolha quando deseja criar uma Nova Conta de Cliente em seu [!DNL Commerce] banco de dados do cliente usando os dados do cliente importados com o pedido da Amazon. Essa opção ajuda a criar [!DNL Commerce] banco de dados de clientes de seus pedidos da Amazon.</li></ul> |
| Origem do Número da Ordem | Opções:<ul><li>**[!UICONTROL Build Using Magento Order Number]** - (Padrão) Escolha quando deseja criar um [!DNL Commerce] número do pedido do pedido Amazon correspondente usando o [!DNL Commerce] ID de ordem atribuída de forma incremental. </li><li>**Criar usando o número do pedido do Amazon** - Escolha quando deseja criar o [!DNL Commerce] número do pedido usando o número do pedido atribuído pela Amazon correspondente.</li></ul> |
| Pedidos pendentes | Opções:<ul><li>**[!UICONTROL Do Not Reserve Quantity]** - Escolha quando você não deseja que sua [!DNL Commerce] quantidade de estoque afetada por seus pedidos da Amazon. Escolha se você usa o Amazon para o seu processo de atendimento (FBA). Quando escolhido e você recebe um pedido da Amazon, a quantidade solicitada não afeta a [!DNL Commerce] quantidade de estoque.</li><li>**[!UICONTROL Reserve Quantity]** - Escolha quando deseja que a quantidade do pedido na Amazon seja &quot;reservada&quot; em seu [!DNL Commerce] quantidade de estoque. Quando escolhido e você recebe um pedido Amazon, a quantidade solicitada &quot;reserva&quot; em seu [!DNL Commerce] quantidade de estoque para evitar [!DNL Commerce] ações de &quot;venda em excesso&quot;. A quantidade &quot;reservada&quot; não está disponível para compra por meio de [!DNL Commerce] loja.</li></ul> |
| [!UICONTROL Order Status] | Opções:<ul><li>**[!UICONTROL Default Order Status]** - (Padrão) Escolha quando deseja que os pedidos recém-criados importados da Amazon sejam atribuídos ao status de pedido padrão para novos pedidos. O status padrão para novos pedidos (a menos que tenha criado um status de pedido personalizado para novos pedidos) é `Pending`. Consulte [Processamento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html).</li><li>>**[!UICONTROL Custom Order Status]** - Escolha quando deseja que pedidos recém-criados importados da Amazon recebam um status diferente do padrão. Quando escolhido, **[!UICONTROL Processing Order Status]** permite que você escolha o status que deseja usar para pedidos recém-criados importados do Amazon.</li></ul> |
| [!UICONTROL Processing Orders Status] | Ativado quando _[!UICONTROL Order Status]_está definida como `Custom Order Status`. Escolha o status da ordem que deseja atribuir a novas ordens. As opções nesse campo dependem das opções de status padrão em [!DNL Commerce]. Consulte [Status do pedido](https://docs.magento.com/user-guide/sales/order-status.html){target=&quot;_blank&quot;}. Você também pode criar um status de pedido personalizado para mostrar aqui. Para criar um status de pedido personalizado, consulte [Status do pedido personalizado](https://docs.magento.com/user-guide/sales/order-status-custom.html){target=&quot;_blank&quot;}. |

## [!DNL Commerce] criação de pedidos

[!DNL Commerce] os pedidos são criados para pedidos da Amazon com base no status e nas condições de inventário a seguir.

### Criação de Ordens com Gerenciamento de Inventário

>[!NOTE]
>
>Suportado somente nas integrações Adobe Commerce e Magento Open Source 2.3.x.

| Canal de Cumprimento | [!DNL Commerce] Status do inventário | Status do pedido Amazon | [!UICONTROL Create Magento Order] Configuração | Inventário Reservado |
|---|---|---|---|---|
| FBA | Em estoque<br>Produto esgotado<br>Não Gerenciar | Pending | Não | Não |
| FBA | Em estoque<br>Produto esgotado<br>Não Gerenciar | PendingAvailability | Não | Não |
| FBA | Em estoque<br>Produto esgotado<br>Não Gerenciar | Cancelado | Não | Não |
| FBA | Em estoque<br>Produto esgotado<br>Não Gerenciar | Erro | Não | Não |
| FBA | Em estoque<br>Produto esgotado<br>Não Gerenciar | Não Entregue | Não | Não |
| FBA | Em estoque<br>Produto esgotado<br>Não Gerenciar | ParcialmenteEnviado | Não | Não |
| FBA | Em estoque<br>Não Gerenciar | Entregue | Sim | Não |
| FBA | Produto esgotado | Entregue | Não | Não |
| FBM | Em estoque<br>Produto esgotado<br>Não Gerenciar | Pending | Não | Não |
| FBM | Em estoque<br>Produto esgotado<br>Não Gerenciar | PendingAvailability | Não | Não |
| FBM | Em estoque<br>Produto esgotado<br>Não Gerenciar | Cancelado | Não | Não |
| FBM | Em estoque<br>Produto esgotado<br>Não Gerenciar | Erro | Não | Não |
| FBM | Em estoque<br>Não Gerenciar | Não Entregue | Sim | Sim |
| FBM | Produto esgotado | Não Entregue | Não | Não |
| FBM | Em estoque<br>Não Gerenciar | ParcialmenteEnviado | Sim | Sim |
| FBM | Produto esgotado | ParcialmenteEnviado | Não | Não |
| FBM | Em estoque<br>Não Gerenciar | Entregue | Sim | Sim |
| FBM | Produto esgotado | Entregue | Não | Não |

>[!NOTE]
>Se um pedido da Amazon for importado em um `Partially Shipped` ou `Shipped` , a reserva de inventário criada é para todos os itens na ordem. O canal de vendas da Amazon não compensa itens que foram enviados anteriormente.
>
>Se um pedido for preenchido pela Amazon (FBA), mas um item estiver em `out of stock` status, [!DNL Commerce] O não pode criar um pedido correspondente. Essa é uma limitação das integrações de Gerenciamento de inventário.
