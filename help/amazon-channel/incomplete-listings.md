---
title: Listagens incompletas
description: O canal de vendas da Amazon fornece a variável [!UICONTROL Incomplete] para ajudar a identificar e atender aos requisitos de qualificação para suas listas de Amazon incompletas.
exl-id: f943c9cc-fa1d-4f3e-a3de-3a8d00f87890
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# Listas incompletas

O _[!UICONTROL Incomplete]_lista a variável [!DNL Commerce] produtos de catálogo que atendem aos requisitos de qualificação da Amazon (definidos em [regras de listagem](./listing-rules.md)), mas não têm informações exigidas pelo Amazon (como o Amazon ASIN ou uma condição de produto definida).

Existem quatro causas possíveis para uma listagem incompleta, cada uma identificada pelo seu status.

| Status | Motivo | Ação |
|--- |--- |--- |
| Condição ausente | O Amazon aceita listas em várias condições (como _Novo_, _Refurbado_, _Usado: Curtir Novo_) a listagem requer uma condição definida. | Atualize as informações necessárias e manualmente [atribuir uma condição](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) para uma listagem. |
| Não é possível atribuir à listagem do Amazon | Falha na correspondência automática desta listagem ao catálogo. Se nenhuma correspondência for encontrada, a listagem não poderá ser gerenciada pelo Amazon Sales Channel | Atualize as informações necessárias e manualmente [atribuir um ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) ao produto do catálogo para corresponder à lista. |
| Várias Correspondências Encontradas | Falha na correspondência automática desta listagem ao catálogo. Se várias correspondências possíveis forem encontradas, você deverá selecionar a correspondência correta para seu produto. | Atualize as informações necessárias e manualmente [escolha uma correspondência de produto](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) para o produto e listagem. |
| Possui variantes | Se o seu produto tiver variantes, como uma camiseta disponível em diferentes tamanhos ou cores, você deverá escolher a variante no catálogo para ser atribuída corretamente e corresponder à listagem | Atualize as informações necessárias e manualmente [escolha a variante correta](./amazon-manually-update-incomplete-listing.md#update-required-info-has-variants) para atribuir e corresponder a esta listagem. |

>[!NOTE]
>Quando as listagens incompletas correspondem corretamente aos produtos do catálogo, a listagem é movida da variável _[!UICONTROL Incomplete]_e são publicados na Amazon com base em sua [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) configurações.

As ações disponíveis no _[!UICONTROL Incomplete]_incluem:

Em _[!UICONTROL Actions]_:

- **[!UICONTROL Re-attempt to auto match to Amazon listings]**: Escolha iniciar o processo automático para corresponder seus dados de listagem do Amazon ao seu [!DNL Commerce] catálogo. Se os produtos não corresponderem automaticamente, revisite seu [_[!UICONTROL Catalog Search]_](./catalog-search.md) nas suas cartas na lista. Se as listagens não corresponderem automaticamente após a atualização do _[!UICONTROL Catalog Search]_, é possível fazer a correspondência manual de produtos na [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) ação.

Em **[!UICONTROL Select]** no _[!UICONTROL Action]_coluna:

- **[!UICONTROL Update Required Info]**: Escolha quando as listagens não correspondem automaticamente ao catálogo. Você pode manualmente [corresponder produtos de catálogo a listas](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found), manualmente [atribuir um ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) para uma correspondência de catálogo, ou [atribuir uma condição ausente](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) para listagem.

- **[!UICONTROL View Details]**: escolha exibir detalhes da lista, incluindo o [Listando log de atividades](./product-listing-details.md#listing-activity-log), [Preços do concorrente do Buy Box](./product-listing-details.md#buy-box-competitor-pricing)e [Preços dos Concorrentes Mais Baixos](./product-listing-details.md#lowest-competitor-pricing). Esta ação é apenas para visualização. Não podem ser feitas alterações nos detalhes da lista. Consulte [Exibir detalhes](./product-listing-details.md).

>[!NOTE]
>
>Se houver listagens em andamento, o número de listagens aparecerá em uma mensagem acima das guias.

![Listas incompletas de Amazon](assets/amazon-incomplete-listings.png)

As home pages do canal de vendas da Amazon compartilham algumas informações comuns [controles do espaço de trabalho](./workspace-controls.md) que permitem personalizar os dados exibidos.

| Coluna | Descrição |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | A SKU (Stock Keeping Unit) atribuída pela Amazon a um produto para identificar o produto, as opções, o preço e o fabricante. |
| [!UICONTROL ASIN] | Um bloco exclusivo de 10 letras e/ou números que identifica itens.<br><br>ASIN significa [!DNL Amazon Standard Identification Number]. Um ASIN é um bloco exclusivo de 10 letras e/ou números que identifica itens. Para livros, o ASIN é o mesmo que o número ISBN, mas para todos os outros produtos, um novo ASIN é criado quando o item é carregado em seu catálogo. Você pode encontrar um ASIN de itens na página de detalhes do produto no Amazon, juntamente com mais detalhes relacionados ao item. |
| [!UICONTROL Product Listing Name] | O nome do produto. |
| [!UICONTROL Condition] | O [condição](./product-listing-condition.md) do produto. |
| [!UICONTROL Landed Price] | O preço de listagem do produto mais seu preço de frete. |
| [!UICONTROL Amazon Quantity] | A quantidade disponível quando o produto é listado ativamente na Amazon. |
| [!UICONTROL Status] | O status da listagem, definido pela Amazon. Consulte a tabela Status acima. |
| [!UICONTROL Action] | Lista de ações disponíveis que podem ser aplicadas a uma lista específica. Para aplicar uma ação, clique em **[!UICONTROL Select]** no _[!UICONTROL Action]_e selecione uma opção:<ul><li>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
