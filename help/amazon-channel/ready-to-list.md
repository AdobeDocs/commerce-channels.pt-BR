---
title: Canal de vendas do Amazon - [!UICONTROL Ready to List]
description: O canal de vendas do Amazon fornece a guia Pronto para listar para ajudar você a revisar os produtos do Commerce que atendem à qualificação, mas não são listados automaticamente.
feature: Sales Channels, Products, Merchandising
exl-id: f62017fb-964f-43f0-b76b-8f39f447466a
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# [!UICONTROL Ready to List]

A variável _[!UICONTROL Ready to List]_A guia mostra o [!DNL Commerce] catalogar produtos que atendam às configurações da lista e estejam prontos para publicar no Amazon as a **novo**listagem. Ao contrário de outras guias de listagem, essa guia nem sempre aparece no [_[!UICONTROL Product Listings]_](./managing-product-listings.md) página.

A variável _[!UICONTROL Ready to List]_aparece somente quando [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) nas configurações da sua lista está definida como `Do Not Automatically List Eligible Products`. Essa configuração informa ao canal de vendas da Amazon que as novas listagens do Amazon devem ser publicadas manualmente.

Quando [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) está definida como `Automatically List Eligible Products`, o canal de vendas da Amazon publica automaticamente novas listas para seus produtos de catálogo qualificados. Como as novas listagens são publicadas automaticamente, a variável _[!UICONTROL Ready to List]_não é exibida.

Em _[!UICONTROL Actions]_:

- **[!UICONTROL Publish Product to Amazon]**: Opte por republicar a listagem na [!DNL Amazon Marketplace]. Consulte [Publicar uma listagem do Amazon](./publish-listings-manually.md)

Em **[!UICONTROL Select]** no _[!UICONTROL Action]_coluna:

- **[!UICONTROL Publish On Amazon]**: Opte por republicar a listagem na [!DNL Amazon Marketplace]. Consulte [Publicar uma listagem do Amazon](./publish-listings-manually.md).

- **[!UICONTROL View Details]**: Opte por exibir os detalhes da listagem, incluindo o [Log de atividades de listagem](./product-listing-details.md#listing-activity-log), [Preços do Concorrente Buy Box](./product-listing-details.md#buy-box-competitor-pricing), e [Menor preço para concorrentes](./product-listing-details.md#lowest-competitor-pricing). Esta ação é somente para exibição. Nenhuma alteração pode ser feita nos detalhes da lista. Consulte [Exibir detalhes](./product-listing-details.md).

Você tem algumas opções para fazer manualmente [publicar uma nova lista no Amazon](./publish-listings-manually.md).

>[!NOTE]
>Se você tiver listagens em andamento, o número de listagens será exibido em uma mensagem acima das guias.

![Pronto para listar](assets/amazon-ready-to-list.png){width="600" zoomable="yes"}

## Colunas padrão

| Coluna | Descrição |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | A SKU (Unidade de manutenção de estoque) atribuída pela Amazon a um produto para identificar o produto, as opções, o preço e o fabricante. |
| [!UICONTROL ASIN] | Um bloco exclusivo de 10 letras e/ou números que identificam itens.<br><br>ASIN significa [!DNL Amazon Standard Identification Number]. Um ASIN é um bloco exclusivo de 10 letras e/ou números que identificam itens. Para livros, o ASIN é o mesmo que o número ISBN, mas para todos os outros produtos, um novo ASIN é criado quando o item é carregado para o seu catálogo. Você pode encontrar um ASIN de itens na página de detalhes do produto no Amazon, juntamente com mais detalhes relacionados ao item. |
| [!UICONTROL Product Listing Name] | O nome do produto. |
| [!UICONTROL Condition] | A variável [condição](./product-listing-condition.md) do produto. |
| [!UICONTROL Landed Price] | O preço de listagem do produto mais seu preço de envio. |
| [!UICONTROL Amazon Quantity] | A quantidade disponível quando o produto está ativamente listado no Amazon. |
| [!UICONTROL Status] | O status da lista, definido pelo Amazon. |
| [!UICONTROL Action] | Lista de ações disponíveis que podem ser aplicadas a uma lista específica. Para aplicar uma ação, clique em **[!UICONTROL Select]** no _[!UICONTROL Action]_e escolha uma opção:<ul><li>[[!UICONTROL Publish on Amazon]](./publish-listings-manually.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |

### Causas comuns de listagens prontas para uso

- **[!UICONTROL Ready to List]** - O produto corresponde a um Amazon ASIN e está programado para ser listado. Se [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) nas configurações da sua lista está definida como `Do Not Automatically List Eligible Products`, esse status representa os produtos que estão prontos para serem listados manualmente.

- **[!UICONTROL List in Progress]** - A lista de produtos foi enviada ao Amazon e está aguardando a confirmação da aceitação do Amazon.
