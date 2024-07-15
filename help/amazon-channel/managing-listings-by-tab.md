---
title: Gerenciar listas de produtos do Amazon por status/guia
description: Ao gerenciar as listagens do Amazon, você pode aplicar ações às suas listagens de acordo com o status.
feature: Sales Channels, Products
exl-id: 33effdd8-baa9-4fc5-8c7e-313175eb7e9c
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Gerenciar listas de produtos do Amazon por status/guia

A página _[!UICONTROL Product Listings]_contém várias guias para exibir os status de todas as suas listas e corresponder seus produtos às listas do Amazon.

As tarefas de listagem disponíveis diferem um pouco em cada guia, mas os [controles do espaço de trabalho](./workspace-controls.md) são iguais e permitem personalizar os dados exibidos nas listagens.

As opções em **[!UICONTROL Actions]** podem aplicar a ação a várias listagens, enquanto as opções em **[!UICONTROL Select]** na coluna _[!UICONTROL Action]_aplicam a ação somente à listagem individual.

Consulte também [Gerenciar Listas por Ação](./managing-listings-by-action.md).

![Guias de Listagens de Produtos](assets/amazon-product-listings-tabs.png){width="600" zoomable="yes"}

| Guia | Descrição | Ações |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | Mostra os produtos do catálogo do [!DNL Commerce] que atendem às configurações de lista definidas, mas que não têm as informações necessárias exigidas pela Amazon para uma lista.<br><br>Se _[!UICONTROL Automatic List Action]_estiver definido como `Automatically List Eligible Products` nas configurações de [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md), esses itens serão seus **[!UICONTROL In Progress Listings]**. | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | Mostra suas listas existentes do Amazon (com base nas informações recebidas do Amazon) que não correspondem a um produto em seu catálogo [!DNL Commerce]. | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br>Tentativa de Correspondência Automática<br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | Mostra os produtos de catálogo prontos para criar as listagens do Amazon, mas a loja está configurada para não publicar automaticamente novas listagens. Essa guia é usada para publicar manualmente as novas listagens.<br><br>Se _[!UICONTROL Automatic List Action]_estiver definido como `Do Not Automatically List Eligible Products` nas configurações de [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md), esses itens serão seus **[!UICONTROL In Progress Listings]**. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | Mostra os produtos de catálogo que foram publicados no Amazon, mas que a Amazon não aprovou a lista com o status Ativo. | [Encerrar Listagem(ões) no Amazon](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Alternar para Atendido(s) pela Amazon/Comerciante<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | Mostra suas listas do Amazon que corresponderam a um produto no catálogo [!DNL Commerce], que foram publicadas no Amazon e que foram atualizadas pelo Amazon para o status Ativo. | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Alternar para Atendido pela Amazon/Comerciante<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | Mostra as listagens do Amazon que atendem aos critérios para uma substituição definida e à qual a substituição foi aplicada. As substituições têm prioridade sobre qualquer outra configuração de conta. | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | Mostra suas listas existentes do Amazon que não estão mais qualificadas, com base nas [configurações de listagem](./listing-settings.md) definidas. | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Alternar para Atendido pela Amazon/Comerciante<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | Mostra as listagens do Amazon que foram encerradas (removidas) manualmente do Amazon. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## Acessar listas de produtos

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Clique em **[!UICONTROL View Store]** no cartão de armazenamento.

1. No painel de armazenamento, clique em **[!UICONTROL Manage Listings]** na seção _[!UICONTROL Store Listings]_.
