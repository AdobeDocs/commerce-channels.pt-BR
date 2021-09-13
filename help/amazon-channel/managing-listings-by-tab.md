---
title: Gerenciar listas de produtos por status/guia
description: À medida que gerencia suas listagens do Amazon, você pode aplicar ações às suas listagens de acordo com o status.
exl-id: 33effdd8-baa9-4fc5-8c7e-313175eb7e9c
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Gerenciar listas de produtos por status/guia

A página _[!UICONTROL Product Listings]_contém várias guias a partir das quais você pode visualizar os status de todas as suas listagens e corresponder seus produtos às listagens do Amazon.

As tarefas de listagem disponíveis diferem um pouco em cada guia, mas os [controles do espaço de trabalho](./workspace-controls.md) são os mesmos e permitem personalizar os dados exibidos para suas listagens.

As opções em **[!UICONTROL Actions]** podem aplicar a ação a várias listagens, enquanto as opções em **[!UICONTROL Select]** na coluna _[!UICONTROL Action]_aplicam a ação somente à listagem individual.

Consulte também [Gerenciar listagens por Ação](./managing-listings-by-action.md).

![Guias Listagens do Produto](assets/amazon-product-listings-tabs.png)

| Tabulação | Descrição | Ações |
|--- |--- |--- |
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | Mostra seus produtos de catálogo [!DNL Commerce] que atendem às configurações de listagem definidas, mas não têm informações necessárias para uma listagem do Amazon.<br><br>Se  _[!UICONTROL Automatic List Action]_estiver definido como  `Automatically List Eligible Products` em suas  [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) configurações, esses itens serão seus **[!UICONTROL In Progress Listings]**. | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | Mostra suas listagens existentes do Amazon (com base nas informações recebidas do Amazon) que não correspondem a um produto em seu catálogo [!DNL Commerce]. | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br>Tentar Correspondência Automática<br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | Mostra seus produtos de catálogo prontos para criar listas do Amazon, mas sua loja não está configurada para publicar novas listas automaticamente. Essa guia é usada para publicar manualmente as novas listagens.<br><br>Se  _[!UICONTROL Automatic List Action]_estiver definido como  `Do Not Automatically List Eligible Products` em suas  [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) configurações, esses itens serão seus **[!UICONTROL In Progress Listings]**. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | Mostra seus produtos de catálogo que foram publicados na Amazon, mas a Amazon não aprovou a listagem para o status Ativo. | [ EndListing(s) no ](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>AmazonSwitch para Atendido pelo Amazon/Merchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | Mostra as listagens do Amazon que foram correspondidas a um produto no catálogo [!DNL Commerce], que foram publicadas no Amazon e que foram enviadas pela Amazon para o status Ativo. | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Alterar para preenchido pelo Amazon/Merchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | Mostra as listagens do Amazon que atendem aos critérios de uma substituição definida e à qual a substituição foi aplicada. As substituições têm prioridade sobre qualquer outra configuração de conta. | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | Mostra suas listagens existentes do Amazon que não são mais elegíveis, com base em suas [configurações de listagem](./listing-settings.md) definidas. | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Alterar para preenchido pelo Amazon/Merchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | Mostra as listagens do Amazon que foram manualmente encerradas (removidas) no Amazon. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## Acessar listas de produtos

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Clique em **[!UICONTROL View Store]** no cartão de armazenamento.

1. No painel da loja, clique em **[!UICONTROL Manage Listings]** na seção _[!UICONTROL Store Listings]_.
