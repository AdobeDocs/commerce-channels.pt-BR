---
title: Listagens incompletas do Amazon
description: O canal de vendas da Amazon fornece a guia [!UICONTROL Incomplete] para ajudar você a identificar e atender aos requisitos de qualificação para suas listas incompletas do Amazon.
feature: Sales Channels, Products
exl-id: f943c9cc-fa1d-4f3e-a3de-3a8d00f87890
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---

# Listagens incompletas do Amazon

A guia _[!UICONTROL Incomplete]_lista os produtos do catálogo [!DNL Commerce] que atendem aos requisitos de qualificação da Amazon (definidos nas [regras de listagem](./listing-rules.md)), mas faltam informações exigidas pela Amazon (como a Amazon ASIN ou uma condição de produto definida).

Há quatro causas possíveis para uma listagem incompleta, cada uma identificada por seu status.

| Status | Motivo | Ação |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Condição ausente | A Amazon aceita listagens em várias condições (como _Nova_, _Recondicionada_, _Usada: Como Nova_). A listagem requer uma condição definida. | Atualize as informações necessárias e [atribua manualmente uma condição](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) a uma lista. |
| Não é possível atribuir à listagem do Amazon | A correspondência automática desta listagem ao seu catálogo falhou. Se nenhuma correspondência for encontrada, a lista não poderá ser gerenciada pelo Amazon Sales Channel | Atualize as informações necessárias e [atribua manualmente um ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) ao produto de catálogo para corresponder à lista. |
| Várias Correspondências Encontradas | A correspondência automática desta listagem ao seu catálogo falhou. Se várias correspondências possíveis forem encontradas, você deverá selecionar a correspondência correta para seu produto. | Atualize as informações necessárias e [escolha manualmente uma correspondência de produto](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) para o produto e a lista. |
| Têm variantes | Se seu produto tiver variantes, como uma camiseta disponível em diferentes tamanhos ou cores, escolha a variante no catálogo para ser atribuída corretamente e correspondida à lista | Atualize as informações necessárias e [escolha manualmente a variante correta](./amazon-manually-update-incomplete-listing.md#update-required-info-has-variants) para atribuir e corresponder a esta lista. |

>[!NOTE]
>Quando listas incompletas são correspondidas corretamente aos seus produtos de catálogo, a lista é movida da guia _[!UICONTROL Incomplete]_e é publicada no Amazon com base nas suas configurações de [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md).

As ações disponíveis na guia _[!UICONTROL Incomplete]_incluem:

Em _[!UICONTROL Actions]_:

- **[!UICONTROL Re-attempt to auto match to Amazon listings]**: escolha iniciar o processo automático para correspondência dos dados das listagens do Amazon com o catálogo [!DNL Commerce]. Se os produtos não corresponderem automaticamente, revise suas opções do [_[!UICONTROL Catalog Search]_](./catalog-search.md) nas suas permissões de listagem. Se as listagens não corresponderem automaticamente depois de atualizar suas opções do _[!UICONTROL Catalog Search]_, você poderá corresponder produtos manualmente na ação [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found).

Em **[!UICONTROL Select]**, na coluna _[!UICONTROL Action]_:

- **[!UICONTROL Update Required Info]**: escolha quando as listagens não corresponderem automaticamente ao seu catálogo. Você pode [corresponder manualmente produtos de catálogo a listagens](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found), [atribuir manualmente uma ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) a uma correspondência de catálogo ou [atribuir uma condição ausente](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) para listagem.

- **[!UICONTROL View Details]**: Opte por exibir os detalhes da listagem, incluindo o [Log de Atividades da Listagem](./product-listing-details.md#listing-activity-log), [Preços de Concorrentes de Buy Box](./product-listing-details.md#buy-box-competitor-pricing) e [Preços de Concorrentes Mais Baixos](./product-listing-details.md#lowest-competitor-pricing). Esta ação é somente para exibição. Nenhuma alteração pode ser feita nos detalhes da lista. Consulte [Exibir Detalhes](./product-listing-details.md).

>[!NOTE]
>
>Se você tiver listagens em andamento, o número de listagens aparecerá em uma mensagem acima das guias.

![Listagens incompletas do Amazon](assets/amazon-incomplete-listings.png){width="600" zoomable="yes"}

As home pages dos canais de vendas do Amazon compartilham alguns [controles de espaço de trabalho](./workspace-controls.md) comuns que permitem personalizar os dados exibidos.

| Coluna | Descrição |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | A SKU (Unidade de manutenção de estoque) atribuída pela Amazon a um produto para identificar o produto, as opções, o preço e o fabricante. |
| [!UICONTROL ASIN] | Um bloco exclusivo de 10 letras e/ou números que identificam itens.<br><br>ASIN significa [!DNL Amazon Standard Identification Number]. Um ASIN é um bloco exclusivo de 10 letras e/ou números que identificam itens. Para livros, o ASIN é o mesmo que o número ISBN, mas para todos os outros produtos, um novo ASIN é criado quando o item é carregado para o seu catálogo. Você pode encontrar um ASIN de itens na página de detalhes do produto no Amazon, juntamente com mais detalhes relacionados ao item. |
| [!UICONTROL Product Listing Name] | O nome do produto. |
| [!UICONTROL Condition] | A [condição](./product-listing-condition.md) do produto. |
| [!UICONTROL Landed Price] | O preço de listagem do produto mais seu preço de envio. |
| [!UICONTROL Amazon Quantity] | A quantidade disponível quando o produto está ativamente listado no Amazon. |
| [!UICONTROL Status] | O status da lista, definido pelo Amazon. Consulte a tabela Status acima. |
| [!UICONTROL Action] | Lista de ações disponíveis que podem ser aplicadas a uma lista específica. Para aplicar uma ação, clique em **[!UICONTROL Select]** na coluna _[!UICONTROL Action]_e selecione uma opção:<ul><li>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
