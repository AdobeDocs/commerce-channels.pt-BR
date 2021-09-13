---
title: Listagens incompletas
description: O canal de vendas do Amazon fornece a guia [!UICONTROL Incomplete] para ajudar a identificar e atender aos requisitos de qualificação para suas listagens incompletas do Amazon.
exl-id: f943c9cc-fa1d-4f3e-a3de-3a8d00f87890
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Listas incompletas

A guia _[!UICONTROL Incomplete]_lista os produtos do catálogo [!DNL Commerce] que atendem aos seus requisitos de elegibilidade do Amazon (definidos em suas [regras de listagem](./listing-rules.md)), mas não têm as informações necessárias para o Amazon (como o Amazon ASIN ou uma condição de produto definida).

Existem quatro causas possíveis para uma listagem incompleta, cada uma identificada pelo seu status.

| Status | Motivo | Ação |
|--- |--- |--- |
| Condição ausente | A Amazon aceita listas em várias condições (como _New_, _Refurbished_, _Usado: A listagem Como Novo_) requer uma condição definida. | Atualize as informações necessárias e atribua manualmente uma condição](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) a uma listagem.[ |
| Não é possível atribuir à listagem do Amazon | Falha na correspondência automática desta listagem ao catálogo. Se nenhuma correspondência for encontrada, a listagem não poderá ser gerenciada pelo Amazon Sales Channel | Atualize as informações necessárias e atribua manualmente um ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) ao produto do catálogo para que ele corresponda à lista.[ |
| Várias Correspondências Encontradas | Falha na correspondência automática desta listagem ao catálogo. Se várias correspondências possíveis forem encontradas, você deverá selecionar a correspondência correta para seu produto. | Atualize as informações necessárias e escolha manualmente [uma correspondência de produto](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) para o produto e a listagem. |
| Possui variantes | Se o seu produto tiver variantes, como uma camiseta disponível em diferentes tamanhos ou cores, você deverá escolher a variante no catálogo para ser atribuída corretamente e corresponder à listagem | Atualize as informações necessárias e escolha manualmente [a variante correta](./amazon-manually-update-incomplete-listing.md#update-required-info-has-variants) para atribuir e corresponder a esta listagem. |

>[!NOTE]
>Quando as listagens incompletas são correspondidas corretamente aos produtos do catálogo, a listagem é movida da guia _[!UICONTROL Incomplete]_e são publicadas no Amazon com base nas configurações [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md).

As ações disponíveis na guia _[!UICONTROL Incomplete]_incluem:

Em _[!UICONTROL Actions]_:

- **[!UICONTROL Re-attempt to auto match to Amazon listings]**: Escolha iniciar o processo automático para corresponder seus dados de listagens do Amazon ao seu  [!DNL Commerce] catálogo. Se os produtos não corresponderem automaticamente, revisite suas opções [_[!UICONTROL Catalog Search]_](./catalog-search.md) nas suas letras da listagem. Se as listagens não corresponderem automaticamente após a atualização das opções _[!UICONTROL Catalog Search]_, você poderá fazer a correspondência manual dos produtos na ação [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found).

Em **[!UICONTROL Select]** na coluna _[!UICONTROL Action]_:

- **[!UICONTROL Update Required Info]**: Escolha quando as listagens não correspondem automaticamente ao catálogo. Você pode [corresponder manualmente produtos de catálogo a listagens](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found), [atribuir manualmente um ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) a uma correspondência de catálogo ou [atribuir uma condição ausente](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) para listagem.

- **[!UICONTROL View Details]**: opte por exibir os detalhes da lista, incluindo o  [Registro](./product-listing-details.md#listing-activity-log) de atividades de listagem, o  [Preço do concorrente do Buy Box](./product-listing-details.md#buy-box-competitor-pricing) e o Preço do  [concorrente mais baixo](./product-listing-details.md#lowest-competitor-pricing). Esta ação é apenas para visualização. Não podem ser feitas alterações nos detalhes da lista. Consulte [Exibir Detalhes](./product-listing-details.md).

>[!NOTE]
>
>Se houver listagens em andamento, o número de listagens aparecerá em uma mensagem acima das guias.

![Listas incompletas de Amazon](assets/amazon-incomplete-listings.png)

As home pages do canal de vendas do Amazon compartilham alguns [controles do espaço de trabalho](./workspace-controls.md) comuns que permitem personalizar os dados exibidos.

| Coluna | Descrição |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | A SKU (Stock Keeping Unit) atribuída pela Amazon a um produto para identificar o produto, as opções, o preço e o fabricante. |
| [!UICONTROL ASIN] | Um bloco exclusivo de 10 letras e/ou números que identifica itens.<br><br>ASIN significa  [!DNL Amazon Standard Identification Number]. Um ASIN é um bloco exclusivo de 10 letras e/ou números que identifica itens. Para livros, o ASIN é o mesmo que o número ISBN, mas para todos os outros produtos, um novo ASIN é criado quando o item é carregado em seu catálogo. Você pode encontrar um ASIN de itens na página de detalhes do produto no Amazon, juntamente com mais detalhes relacionados ao item. |
| [!UICONTROL Product Listing Name] | O nome do produto. |
| [!UICONTROL Condition] | A [condição](./product-listing-condition.md) do produto. |
| [!UICONTROL Landed Price] | O preço de listagem do produto mais seu preço de frete. |
| [!UICONTROL Amazon Quantity] | A quantidade disponível quando o produto é listado ativamente na Amazon. |
| [!UICONTROL Status] | O status da listagem, definido pela Amazon. Consulte a tabela Status acima. |
| [!UICONTROL Action] | Lista de ações disponíveis que podem ser aplicadas a uma lista específica. Para aplicar uma ação, clique em **[!UICONTROL Select]** na coluna _[!UICONTROL Action]_e selecione uma opção:<ul><li>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
