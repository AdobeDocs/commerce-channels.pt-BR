---
title: Listagens do Amazon inelegíveis
description: O canal de vendas da Amazon fornece a guia [!UICONTROL Ineligible] para ajudar você a gerenciar itens que não estão qualificados como uma lista com base nas regras de lista atuais.
feature: Sales Channels, Products
exl-id: ae63898d-ff5c-43eb-b759-5bc80829d4d4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Listagens do Amazon inelegíveis

A guia _[!UICONTROL Ineligible]_mostra uma lista de todos os produtos que estão atualmente publicados no Amazon, mas que não estão qualificados como uma lista com base nas regras de listagem atuais. Se um produto anterior foi qualificado e as regras de listagem foram modificadas para torná-lo inelegível, a quantidade associada a um produto cai para 0 e o produto é marcado como_ inelegível _. No entanto, ela ainda está presente em seu [!DNL Amazon Seller Account].

Para mover um produto para fora da guia _[!UICONTROL Ineligible]_, você pode [modificar suas regras de listagem](./listing-rules.md) para permitir que seus produtos sejam qualificados.

As ações disponíveis na guia _[!UICONTROL Ineligible]_incluem:

Em _[!UICONTROL Actions]_:

- **[!UICONTROL End Listing(s) on Amazon]**: Opte por remover todas as listagens selecionadas de [!DNL Amazon Marketplace]. Consulte [Encerrar uma listagem do Amazon](./end-listings-manually.md).

- **[!UICONTROL Edit Listing Overrides]**: escolha alterar as configurações de substituição da lista. Consulte [Substituições](./overrides.md) ou [Editar ou remover uma substituição](./creating-editing-overrides.md#edit-override-single-listing).

Em **[!UICONTROL Select]**, na coluna _[!UICONTROL Action]_:

- **[!UICONTROL View Details]**: Opte por exibir os detalhes da listagem, incluindo o [Log de Atividades da Listagem](./product-listing-details.md#listing-activity-log), [Preços de Concorrentes de Buy Box](./product-listing-details.md#buy-box-competitor-pricing) e [Preços de Concorrentes Mais Baixos](./product-listing-details.md#lowest-competitor-pricing). Esta ação é somente para exibição. Nenhuma alteração pode ser feita nos detalhes da lista. Consulte [Exibir Detalhes](./product-listing-details.md).

- **[!UICONTROL Create Override]**: Opte por criar uma substituição e aplicá-la a esta lista. Consulte [Criar uma substituição](./creating-editing-overrides.md).

- **[!UICONTROL Edit Assigned ASIN]**: escolha modificar a ASIN atribuída ao produto de catálogo. Essa ação é usada se um produto no catálogo corresponder à ASIN errada. Consulte [Editar um ASIN atribuído](./edit-assigned-asin.md).

- **[!UICONTROL Create Alias Seller SKU]**: escolha criar um SKU de Alias que possa ser usado para criar uma lista do Amazon do mesmo produto de catálogo. Consulte [Criar um SKU de Vendedor de Alias](./create-alias-seller-sku.md).

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**: escolha alterar o método de preenchimento associado ao pedido. Consulte [Definir configurações de Preenchido por](./fulfilled-by.md#configure-fulfilled-by-settings).

- **[!UICONTROL End Listing]**: escolha remover a listagem de [!DNL Amazon Marketplace]. Consulte [Encerrar uma listagem do Amazon](./end-listings-manually.md).

>[!NOTE]
>Se você tiver listagens em andamento, o número de listagens será exibido em uma mensagem acima das guias.

![Listagens de Amazon não qualificadas](assets/amazon-ineligible-listings.png){width="600" zoomable="yes"}

As home pages dos canais de vendas do Amazon compartilham alguns [controles de espaço de trabalho](./workspace-controls.md) comuns que permitem personalizar os dados exibidos.

## Colunas padrão

| Coluna | Descrição |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | A SKU (Unidade de manutenção de estoque) atribuída pela Amazon a um produto para identificar o produto, as opções, o preço e o fabricante. |
| [!UICONTROL ASIN] | Um bloco exclusivo de 10 letras e/ou números que identificam itens.<br><br>ASIN significa [!DNL Amazon Standard Identification Number]. Um ASIN é um bloco exclusivo de 10 letras e/ou números que identificam itens. Para livros, o ASIN é o mesmo que o número ISBN, mas para todos os outros produtos, um novo ASIN é criado quando o item é carregado para o seu catálogo. Você pode encontrar um ASIN de itens na página de detalhes do produto no Amazon, juntamente com mais detalhes relacionados ao item. |
| [!UICONTROL Product Listing Name] | O nome do produto. |
| [!UICONTROL Condition] | A [condição](./product-listing-condition.md) do produto. |
| [!UICONTROL Landed Price] | O preço de listagem do produto mais seu preço de envio. |
| [!UICONTROL Amazon Quantity] | A quantidade disponível quando o produto está ativamente listado no Amazon. |
| [!UICONTROL Action] | Lista de ações disponíveis que podem ser aplicadas a uma lista específica. Para aplicar uma ação, clique em **[!UICONTROL Select]** na coluna _[!UICONTROL Action]_e selecione uma opção:<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[Criar Substituição](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
