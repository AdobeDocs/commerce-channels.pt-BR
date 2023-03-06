---
title: Gerenciar listas de produtos por status/guia
description: Ao gerenciar as listagens do Amazon, você pode aplicar ações às suas listagens de acordo com o status.
exl-id: 33effdd8-baa9-4fc5-8c7e-313175eb7e9c
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Gerenciar listas de produtos por status/guia

A variável _[!UICONTROL Product Listings]_Esta página contém várias guias, nas quais você pode visualizar os status de todas as suas listas e corresponder seus produtos às listas do Amazon.

As tarefas de listagem disponíveis diferem um pouco em cada guia, mas as [controles do espaço de trabalho](./workspace-controls.md) são os mesmos e permitem personalizar os dados exibidos para suas listagens.

Opções em **[!UICONTROL Actions]** pode aplicar a ação a várias listagens, enquanto as opções em **[!UICONTROL Select]** no _[!UICONTROL Action]_aplicar a ação somente à lista individual.

Consulte também [Gerenciar Listas por Ação](./managing-listings-by-action.md).

![Guias Listas de produtos](assets/amazon-product-listings-tabs.png)

| Guia | Descrição | Ações |
|--- |--- |--- |
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | Mostra o [!DNL Commerce] produtos de catálogo que atendem às configurações de lista definidas, mas que não têm as informações exigidas pela Amazon para uma lista.<br><br>Se _[!UICONTROL Automatic List Action]_está definida como `Automatically List Eligible Products` no seu [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) configurações, esses itens são seus **[!UICONTROL In Progress Listings]**. | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | Mostra suas listas existentes do Amazon (com base nas informações recebidas do Amazon) que não correspondem a um produto em sua [!DNL Commerce] catálogo. | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br>Tentar correspondência automática<br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | Mostra os produtos de catálogo prontos para criar as listagens do Amazon, mas a loja está configurada para não publicar automaticamente novas listagens. Essa guia é usada para publicar manualmente as novas listagens.<br><br>Se _[!UICONTROL Automatic List Action]_está definida como `Do Not Automatically List Eligible Products` no seu [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) configurações, esses itens são seus **[!UICONTROL In Progress Listings]**. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | Mostra os produtos de catálogo que foram publicados no Amazon, mas que a Amazon não aprovou a lista com o status Ativo. | [Fim Listagem(ões) no Amazon](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Alternar para Atendido pela Amazon/Comerciante<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | Mostra as listagens do Amazon que foram correspondidas a um produto no [!DNL Commerce] catálogo, foram publicados no Amazon e foram publicados pelo Amazon para o status Ativo. | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Alternar para Atendido pela Amazon/Comerciante<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | Mostra as listagens do Amazon que atendem aos critérios para uma substituição definida e à qual a substituição foi aplicada. As substituições têm prioridade sobre qualquer outra configuração de conta. | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | Mostra suas listagens existentes do Amazon que não estão mais qualificadas, com base nas [configurações de listagem](./listing-settings.md). | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Alternar para Atendido pela Amazon/Comerciante<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | Mostra as listagens do Amazon que foram encerradas (removidas) manualmente do Amazon. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## Acessar listas de produtos

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Clique em **[!UICONTROL View Store]** no cartão de loja.

1. No painel da loja, clique em **[!UICONTROL Manage Listings]** no _[!UICONTROL Store Listings]_seção.
