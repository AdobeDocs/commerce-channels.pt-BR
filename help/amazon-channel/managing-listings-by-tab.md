---
title: Gerenciar listas de produtos por status/guia
description: À medida que gerencia suas listagens do Amazon, você pode aplicar ações às suas listagens de acordo com o status.
exl-id: 33effdd8-baa9-4fc5-8c7e-313175eb7e9c
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Gerenciar listas de produtos por status/guia

O _[!UICONTROL Product Listings]_A página contém várias guias das quais você pode visualizar os status de todas as suas listagens e corresponder seus produtos às listagens do Amazon.

As tarefas de listagem disponíveis diferem um pouco em cada guia, mas a variável [controles do espaço de trabalho](./workspace-controls.md) são iguais e permitem personalizar os dados exibidos para suas listagens.

Opções em **[!UICONTROL Actions]** pode aplicar a ação a várias listagens, enquanto as opções em **[!UICONTROL Select]** no _[!UICONTROL Action]_aplicar a ação somente à lista individual.

Consulte também [Gerenciar listagens por ação](./managing-listings-by-action.md).

![Guias Listagens do Produto](assets/amazon-product-listings-tabs.png)

| Tabulação | Descrição | Ações |
|--- |--- |--- |
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | Mostra seu [!DNL Commerce] produtos do catálogo que atendem às configurações de listagem definidas, mas não têm informações necessárias para uma listagem da Amazon.<br><br>If _[!UICONTROL Automatic List Action]_está definida como `Automatically List Eligible Products` em seu [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) , esses itens são **[!UICONTROL In Progress Listings]**. | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | Mostra suas listas existentes do Amazon (com base nas informações recebidas do Amazon) que não correspondem a um produto em seu [!DNL Commerce] catálogo. | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br>Tentar Correspondência Automática<br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | Mostra seus produtos de catálogo prontos para criar listas do Amazon, mas sua loja não está configurada para publicar novas listas automaticamente. Essa guia é usada para publicar manualmente as novas listagens.<br><br>If _[!UICONTROL Automatic List Action]_está definida como `Do Not Automatically List Eligible Products` em seu [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) , esses itens são **[!UICONTROL In Progress Listings]**. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | Mostra seus produtos de catálogo que foram publicados na Amazon, mas a Amazon não aprovou a listagem para o status Ativo. | [End Listagem(ões) no Amazon](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Alterar para preenchido pelo Amazon/Merchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | Mostra as listagens do Amazon que foram correspondidas a um produto em seu [!DNL Commerce] , foram publicados no Amazon e foram publicados pela Amazon para o status de ativo. | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Alterar para preenchido pelo Amazon/Merchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | Mostra as listagens do Amazon que atendem aos critérios de uma substituição definida e à qual a substituição foi aplicada. As substituições têm prioridade sobre qualquer outra configuração de conta. | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | Mostra suas listagens existentes do Amazon que não são mais elegíveis, com base em sua [listar configurações](./listing-settings.md). | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Alterar para preenchido pelo Amazon/Merchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | Mostra as listagens do Amazon que foram manualmente encerradas (removidas) no Amazon. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## Acessar listas de produtos

1. No _Administrador_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Clique em **[!UICONTROL View Store]** no cartão da loja.

1. No painel da loja, clique em **[!UICONTROL Manage Listings]** no _[!UICONTROL Store Listings]_seção.
