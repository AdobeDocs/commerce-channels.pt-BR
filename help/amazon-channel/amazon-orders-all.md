---
title: Exibir pedidos do Amazon
description: Veja seus pedidos do Amazon Marketplace no Adobe Commerce ou no Magento Open Source Admin.
feature: Sales Channels, Orders
exl-id: d7811604-8e15-4d1a-a0e7-9fa61c61ef5d
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Exibir pedidos do Amazon

Há duas maneiras de exibir seus pedidos da Amazon: _[!UICONTROL Recent Orders]_e_[!UICONTROL All Orders]_.

Ambas as opções mostram informações básicas sobre pedidos, conforme recebidas do Amazon, incluindo:

- Data de compra
- Número do pedido
- Status
- Nome do Comprador
- Total geral
- Notas do pedido

O modo de exibição _[!UICONTROL All Orders]_adiciona opções de filtragem para pesquisas de pedidos.

>[!NOTE]
>
>Exceto pela coluna _[!UICONTROL Order Notes]_, a tabela_[!UICONTROL Amazon orders]_ é preenchida com informações de pedido conforme recebidas da Amazon. A coluna _Notas de Pedido_ é atualizada por [!DNL Commerce] como o processo de pedido.

## Pedidos recentes

Você pode exibir seus pedidos mais recentes na seção _[!UICONTROL Recent Orders]_do [painel de armazenamento](./amazon-store-dashboard.md).

![Pedidos recentes](assets/amazon-recent-orders-imported.png){width="600" zoomable="yes"}

### Exibir pedidos recentes do Amazon

1. Clique em **[!UICONTROL View Store]** em um cartão de loja.

1. Exiba seus pedidos na seção _[!UICONTROL Recent Orders]_.

1. Para exibir detalhes do pedido, clique no número do pedido Amazon na coluna _[!UICONTROL Order Number]_.

   A página _[!UICONTROL Amazon Order Details]_do pedido é aberta.

## Exibir todas as ordens

Você pode exibir todos os seus pedidos do Amazon na página _[!UICONTROL Amazon orders]_(também conhecida como exibição_[!UICONTROL All Orders]_). A tabela Pedidos da Amazon é semelhante à seção _[!UICONTROL Recent Orders]_do painel de armazenamento, mas permite visualizar todos os pedidos da Amazon e restringir sua lista de pedidos com as seguintes opções de filtro:

- [!UICONTROL Purchase Date (range)]
- [!UICONTROL Order Number]
- [!UICONTROL Buyer's Name]
- [!UICONTROL Total (range)]
- [!UICONTROL Status]

![Pedidos da Amazon](assets/amazon-orders-list-all.png){width="600" zoomable="yes"}

### Exibir todos os pedidos do Amazon

1. Clique em **[!UICONTROL View Store]** em um cartão de loja.

1. Clique em **[!UICONTROL All Orders]** na seção _[!UICONTROL Recent Orders]_.

1. Para restringir a lista ou procurar um número de pedido específico, complete os parâmetros **[!UICONTROL Filter by]** e clique em **[!UICONTROL Apply filters]**.

1. Para exibir detalhes do pedido, clique no número do pedido Amazon na coluna _[!UICONTROL Order Number]_.

   A página _[!UICONTROL Amazon Order Details]_do pedido é aberta.

## Utilização de filtros

Você pode aplicar filtros à sua lista de pedidos na seção _[!UICONTROL Filter by]_. Faça suas seleções e clique em **[!UICONTROL Apply filters]**. Os filtros aplicados são exibidos acima da grade de pedidos.

![Filtros para exibir pedidos do Amazon](assets/amazon-orders-filter-view.png){width="600" zoomable="yes"}

### Alteração de filtros aplicados

- Você pode adicionar ou alterar seus filtros na seção _[!UICONTROL Filter by]_. Clique em **[!UICONTROL Apply filters]**para atualizar a lista de pedidos e as opções de filtro que aparecem acima da grade de pedidos.

- Você pode remover filtros, um de cada vez, clicando no `x` do filtro, ou todos de uma vez, clicando em **[!UICONTROL Clear all filters]**. A remoção de um filtro atualiza a lista de pedidos e as opções de filtro que aparecem acima da grade de pedidos.

- Se a lista de pedidos for longa, você poderá usar os controles de paginação abaixo da grade para exibir mais pedidos.

>[!TIP]
>
>Algumas dicas sobre a visualização de pedidos:
>
>- Se você tiver várias integrações de loja da Amazon, uma atualização da visualização de página ao alternar entre visualizações de loja pode ser necessária para atualizar a lista de pedidos e as visualizações de paginação da loja atual.
>- Ao classificar por coluna, a classificação se aplica somente à exibição em lista atual. Filtrar sua lista e classificar a página que você está visualizando é uma prática recomendada.
>- Dependendo da largura da janela de exibição, você pode ver textos sobrepostos nas colunas. Para expandir as colunas do texto a ser quebrado, amplie a visualização da janela.
>- Ao filtrar por _[!UICONTROL Total]_, filtre por números inteiros. Inserir um valor decimal pode causar erros nos resultados.

### Colunas padrão

| Coluna | Descrição |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Filter by] | Disponível somente na exibição _[!UICONTROL All Orders]_.<br>Restringir a lista de pedidos com base em:<ul><li>`Purchase Date (range)`</li><li>`Order Number`</li><li>`Buyer's Name`</li><li>`Total (range)`</li><li>`Status`</li></ul> |
| [!UICONTROL Purchase Date] | A data da compra, conforme recebida do Amazon. |
| [!UICONTROL Order Number] | O número do pedido gerado e recebido do Amazon. Para exibir a tela Detalhes do pedido Amazon, clique no link. |
| [!UICONTROL Status] | O status do pedido, conforme recebido pela Amazon. Opções: `Error` / `Pending` / `Shipped` / `Canceled` / `Completed` / `Unshipped` / `PartiallyShipped` / `PendingAvailability` |
| [!UICONTROL Buyer's Name] | O nome da pessoa que fez o pedido, conforme recebido do Amazon. |
| [!UICONTROL Grand Total] | O valor monetário total do pedido, conforme recebido do Amazon. |
| [!UICONTROL Order Notes] | Ação mais recente registrada para o pedido enquanto ele é processado em [!DNL Commerce]. As informações incluem, entre outros, erros de importação de pedidos e atualizações de processamento de pedidos.<br>**Observação**: este campo é atualizado por [!DNL Commerce] conforme o pedido é processado. |
