---
title: Novas listagens de Amazon de terceiros
description: Gerencie novas listagens do Amazon associando-as a um produto no catálogo de Comércio.
exl-id: ace9d334-d1d1-4f4b-88c8-60a9e7d1d17c
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---

# Novas listagens de Amazon de terceiros

A variável _[!UICONTROL New Third Party]_mostra suas listagens existentes do Amazon que não foram correspondidas a um produto em sua [!DNL Commerce] catálogo. Para usar o gerenciamento de listas para quantidade, preço, tempo de manuseio e muito mais, cada uma das suas listas do Amazon deve corresponder (ser atribuída) a um produto na sua [!DNL Commerce] catálogo. Você tem algumas opções para atribuir uma lista a um produto na [!DNL Commerce] catálogo.

Em _[!UICONTROL Actions]_:

- **[!UICONTROL Create New Catalog Product(s)]**: opte por usar as informações na lista do Amazon para criar automaticamente um produto na [!DNL Commerce] catálogo. Esse processo corresponde a listagem do Amazon ao novo produto de catálogo automaticamente. Consulte [Criar e atribuir produtos de catálogo](./creating-assigning-catalog-products.md).

- **[!UICONTROL Attempt Automatic Match]**: Opte por tentar a correspondência automática das listagens selecionadas com o catálogo com base na sua atual [Pesquisa no catálogo](./catalog-search.md) opções nas configurações da lista. Se você modificar o seu _[!UICONTROL Catalog Search]_opções, essa ação permite tentar novamente o processo de correspondência.

Em _[!UICONTROL Select]_:

- **[!UICONTROL Assign Catalog Product]**: opte por corresponder a lista a um produto na [!DNL Commerce] catálogo manualmente. Consulte [Criar e atribuir produtos de catálogo](./creating-assigning-catalog-products.md).

- **[!UICONTROL Create New Catalog Product]**: opte por usar as informações na lista do Amazon para criar automaticamente um produto na [!DNL Commerce] catálogo. Esse processo corresponde a listagem do Amazon ao novo produto de catálogo automaticamente. Consulte [Criar e atribuir produtos de catálogo](./creating-assigning-catalog-products.md).

- **[!UICONTROL View Details]**: Opte por exibir os detalhes da listagem, incluindo o [Log de atividades de listagem](./product-listing-details.md#listing-activity-log), [Preços do Concorrente Buy Box](./product-listing-details.md#buy-box-competitor-pricing), e [Menor preço para concorrentes](./product-listing-details.md#lowest-competitor-pricing). Esta ação é somente para exibição. Nenhuma alteração pode ser feita nos detalhes da lista. Consulte [Exibir detalhes](./product-listing-details.md).

>[!NOTE]
>
>Se você tiver listas em andamento, uma mensagem será exibida acima das guias indicando o número de listas.

![Novas listagens de terceiros](assets/amazon-listings-new-third-party.png){width="600" zoomable="yes"}

As home pages dos canais de vendas do Amazon compartilham algumas informações [controles do espaço de trabalho](./workspace-controls.md) que permitem personalizar os dados exibidos.

## Colunas padrão

| Coluna | Descrição |
|---|---|
| [!UICONTROL Amazon Seller SKU] | A SKU (Unidade de manutenção de estoque) atribuída pela Amazon a um produto para identificar o produto, as opções, o preço e o fabricante. |
| [!UICONTROL ASIN] | Um bloco exclusivo de 10 letras e/ou números que identificam itens.<br><br>ASIN significa [!DNL Amazon Standard Identification Number]. Um ASIN é um bloco exclusivo de 10 letras e/ou números que identificam itens. Para livros, o ASIN é o mesmo que o número ISBN, mas para todos os outros produtos, um novo ASIN é criado quando o item é carregado para o seu catálogo. Você pode encontrar um ASIN de itens na página de detalhes do produto no Amazon, juntamente com mais detalhes relacionados ao item. |
| [!UICONTROL Product Listing Name] | O nome do produto. |
| [!UICONTROL Condition] | A variável [condição](./product-listing-condition.md) do produto. |
| [!UICONTROL Listing Price] | Identifica o preço de lista para o item, conforme definido pela origem do preço e quaisquer regras de precificação aplicáveis. |
| [!UICONTROL Amazon Quantity] | A quantidade disponível quando o produto está ativamente listado no Amazon. |
| [!UICONTROL Status] | O status da lista, definido pelo Amazon. |
| [!UICONTROL Action] | Lista de ações disponíveis que podem ser aplicadas a uma lista específica. Para aplicar uma ação, clique em **[!UICONTROL Select]** no _[!UICONTROL Action]_e escolha uma opção:<ul><li>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)</li><li>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
