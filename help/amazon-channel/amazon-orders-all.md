---
title: Exibir pedidos da Amazon
description: Veja seus pedidos do Amazon Marketplace no Adobe Commerce ou no Magento Open Source Admin.
exl-id: d7811604-8e15-4d1a-a0e7-9fa61c61ef5d
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Exibir pedidos do Amazon

Há duas maneiras de visualizar seus pedidos do Amazon: _[!UICONTROL Recent Orders]_e_[!UICONTROL All Orders]_.

Ambas as opções mostram informações básicas de pedido, conforme recebidas da Amazon, incluindo:

- Data de compra
- Número do pedido
- Status
- Nome do comprador
- Total geral
- Notas de pedido

_[!UICONTROL All Orders]_view adiciona opções de filtragem para pesquisas de ordem.

>[!NOTE]
>
>Exceto pelo _[!UICONTROL Order Notes]_coluna, a_[!UICONTROL Amazon orders]_ é preenchida com informações de pedido, conforme recebidas da Amazon. O _Notas de pedido_ é atualizada por [!DNL Commerce] conforme o pedido é processado.

## Pedidos recentes

Você pode visualizar seus pedidos mais recentes na _[!UICONTROL Recent Orders]_da seção [painel de loja](./amazon-store-dashboard.md).

![Pedidos recentes](assets/amazon-recent-orders-imported.png)

### Exibir pedidos recentes do Amazon

1. Clique em **[!UICONTROL View Store]** em um cartão de loja.

1. Veja seus pedidos na _[!UICONTROL Recent Orders]_seção.

1. Para exibir detalhes do pedido, clique no número do pedido Amazon na _[!UICONTROL Order Number]_coluna.

   O _[!UICONTROL Amazon Order Details]_será aberta uma página para a ordem.

## Exibir todos os pedidos

Você pode visualizar todos os seus pedidos da Amazon no _[!UICONTROL Amazon orders]_(também chamada de_[!UICONTROL All Orders]_ ). A tabela Pedidos da Amazon é semelhante à _[!UICONTROL Recent Orders]_seção do painel da loja, mas permite visualizar todos os pedidos da Amazon e limitar a lista de pedidos com as seguintes opções de filtro:

- [!UICONTROL Purchase Date (range)]
- [!UICONTROL Order Number]
- [!UICONTROL Buyer's Name]
- [!UICONTROL Total (range)]
- [!UICONTROL Status]

![Pedidos Amazon](assets/amazon-orders-list-all.png)

### Exibir todos os pedidos da Amazon

1. Clique em **[!UICONTROL View Store]** em um cartão de loja.

1. Clique em **[!UICONTROL All Orders]** no _[!UICONTROL Recent Orders]_seção.

1. Para restringir a lista ou procurar um número de ordem específico, preencha o **[!UICONTROL Filter by]** e clique em **[!UICONTROL Apply filters]**.

1. Para exibir detalhes do pedido, clique no número do pedido Amazon na _[!UICONTROL Order Number]_coluna.

   O _[!UICONTROL Amazon Order Details]_será aberta uma página para a ordem.

## Uso de filtros

Você pode aplicar filtros à sua lista de pedidos na _[!UICONTROL Filter by]_seção. Faça suas seleções e clique em **[!UICONTROL Apply filters]**. Os filtros aplicados aparecem acima da grade de pedidos.

![Filtros para exibir pedidos do Amazon](assets/amazon-orders-filter-view.png)

### Alteração dos filtros aplicados

- Você pode adicionar ou alterar seus filtros na _[!UICONTROL Filter by]_seção. Clique em **[!UICONTROL Apply filters]**para atualizar a lista de pedidos e as opções de filtro que aparecem acima da grade de ordens.

- Você pode remover filtros, um de cada vez, clicando no botão `x` para o filtro ou tudo ao mesmo tempo clicando em **[!UICONTROL Clear all filters]**. Remover um filtro atualiza a lista de pedidos e as opções de filtro que aparecem acima da grade de pedidos.

- Se a lista de pedidos for longa, você poderá usar os controles de paginação abaixo da grade para exibir mais pedidos.

>[!TIP]
>
>Algumas dicas sobre a exibição de pedidos:
>
>- Se você tiver várias integrações de loja da Amazon, pode ser necessário atualizar a visualização de página ao alternar entre exibições de loja para atualizar a lista de pedidos e as exibições de paginação da loja atual.
>- Ao classificar por coluna, a classificação se aplica somente à exibição de lista atual. Filtrar sua lista e classificar a página que você está visualizando é uma prática recomendada.
>- Dependendo da largura da janela de exibição, você pode ver o texto sobreposto nas colunas. Para expandir as colunas para o texto a ser quebrado, amplie a exibição de janela.
>- Ao filtrar por _[!UICONTROL Total]_, filtrar por números inteiros. Inserir uma quantidade decimal pode causar erros nos resultados.


### Colunas padrão

| Coluna | Descrição |
|---|---|
| [!UICONTROL Filter by] | Disponível somente no _[!UICONTROL All Orders]_exibir.<br>Restrinja a lista de ordens com base em:<ul><li>`Purchase Date (range)`</li><li>`Order Number`</li><li>`Buyer's Name`</li><li>`Total (range)`</li><li>`Status`</li></ul> |
| [!UICONTROL Purchase Date] | A data da compra, conforme recebida da Amazon. |
| [!UICONTROL Order Number] | O número do pedido gerado e recebido da Amazon. Para exibir a tela Detalhes do pedido da Amazon, clique no link . |
| [!UICONTROL Status] | O status do pedido, conforme recebido pela Amazon. Opções: `Error` / `Pending` / `Shipped` / `Canceled` / `Completed` / `Unshipped` / `PartiallyShipped` / `PendingAvailability` |
| [!UICONTROL Buyer's Name] | O nome da pessoa que fez o pedido, conforme recebido da Amazon. |
| [!UICONTROL Grand Total] | O valor monetário total do pedido, conforme recebido da Amazon. |
| [!UICONTROL Order Notes] | Ação mais recente registrada para a ordem em que é processada em [!DNL Commerce]. As informações incluem, entre outros, erros de importação de pedidos e atualizações de processamento de pedidos.<br>**Observação**: Este campo é atualizado por [!DNL Commerce] conforme o pedido é processado. |
