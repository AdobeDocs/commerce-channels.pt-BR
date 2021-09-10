---
title: Pronto para listar
description: O canal de vendas Amazon fornece a guia Ready to List para ajudar você a revisar os produtos do Commerce que atendem à qualificação, mas não são listados automaticamente.
exl-id: f62017fb-964f-43f0-b76b-8f39f447466a
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# [!UICONTROL Ready to List]

A guia _[!UICONTROL Ready to List]_mostra seus produtos de catálogo [!DNL Commerce] que atendem às configurações de listagem e estão prontos para publicar no Amazon como uma listagem **new**. Diferente de outras guias de listagem, essa guia nem sempre aparece na página [_[!UICONTROL Product Listings]_](./managing-product-listings.md).

A guia _[!UICONTROL Ready to List]_aparece somente quando [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) nas configurações de listagem está definido como `Do Not Automatically List Eligible Products`. Essa configuração informa ao canal de vendas da Amazon que qualquer nova listagem do Amazon deve ser publicada manualmente.

Quando [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) é definido como `Automatically List Eligible Products`, o canal de vendas do Amazon publica automaticamente novas listagens para seus produtos de catálogo qualificados. Como novas listagens são publicadas automaticamente, a guia _[!UICONTROL Ready to List]_não é exibida.

Em _[!UICONTROL Actions]_:

- **[!UICONTROL Publish Product to Amazon]**: Escolha publicar novamente a listagem para o  [!DNL Amazon Marketplace]. Consulte [Publicar uma listagem do Amazon](./publish-listings-manually.md)

Em **[!UICONTROL Select]** na coluna _[!UICONTROL Action]_:

- **[!UICONTROL Publish On Amazon]**: Escolha publicar novamente a listagem para o  [!DNL Amazon Marketplace]. Consulte [Publicar uma listagem do Amazon](./publish-listings-manually.md).

- **[!UICONTROL View Details]**: opte por exibir os detalhes da lista, incluindo o  [Registro](./product-listing-details.md#listing-activity-log) de atividades de listagem, o  [Preço do concorrente do Buy Box](./product-listing-details.md#buy-box-competitor-pricing) e o Preço do  [concorrente mais baixo](./product-listing-details.md#lowest-competitor-pricing). Esta ação é apenas para visualização. Não podem ser feitas alterações nos detalhes da lista. Consulte [Exibir Detalhes](./product-listing-details.md).

Você tem algumas opções para [publicar manualmente uma nova listagem no Amazon](./publish-listings-manually.md).

>[!NOTE]
>Se houver listagens em andamento, o número de listagens será exibido em uma mensagem acima das guias.

![Pronto para listar](assets/amazon-ready-to-list.png)

## Colunas padrão

| Coluna | Descrição |
|---|---|
| [!UICONTROL Amazon Seller SKU] | A SKU (Stock Keeping Unit) atribuída pela Amazon a um produto para identificar o produto, as opções, o preço e o fabricante. |
| [!UICONTROL ASIN] | Um bloco exclusivo de 10 letras e/ou números que identifica itens.<br><br>ASIN significa  [!DNL Amazon Standard Identification Number]. Um ASIN é um bloco exclusivo de 10 letras e/ou números que identifica itens. Para livros, o ASIN é o mesmo que o número ISBN, mas para todos os outros produtos, um novo ASIN é criado quando o item é carregado em seu catálogo. Você pode encontrar um ASIN de itens na página de detalhes do produto no Amazon, juntamente com mais detalhes relacionados ao item. |
| [!UICONTROL Product Listing Name] | O nome do produto. |
| [!UICONTROL Condition] | A [condição](./product-listing-condition.md) do produto. |
| [!UICONTROL Landed Price] | O preço de listagem do produto mais seu preço de frete. |
| [!UICONTROL Amazon Quantity] | A quantidade disponível quando o produto é listado ativamente na Amazon. |
| [!UICONTROL Status] | O status da listagem, definido pela Amazon. |
| [!UICONTROL Action] | Lista de ações disponíveis que podem ser aplicadas a uma lista específica. Para aplicar uma ação, clique em **[!UICONTROL Select]** na coluna _[!UICONTROL Action]_e escolha uma opção:<ul><li>[[!UICONTROL Publish on Amazon]](./publish-listings-manually.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |

### Causas comuns das listagens Prontas para a Lista

- **[!UICONTROL Ready to List]** - O produto corresponde a um Amazon ASIN e está agendado para listagem. Se [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) em suas configurações de listagem estiver definido como `Do Not Automatically List Eligible Products`, esse status representará os produtos prontos para serem listados manualmente.

- **[!UICONTROL List in Progress]** - A lista de produtos foi enviada para a Amazon e está aguardando confirmação da aceitação da Amazon.
