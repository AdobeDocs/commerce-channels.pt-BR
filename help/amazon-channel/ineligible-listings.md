---
title: Listagens Inelegíveis
description: O canal de vendas da Amazon fornece o [!UICONTROL Ineligible] para ajudá-lo a gerenciar os itens não são elegíveis como uma lista com base nas regras de lista atuais.
exl-id: ae63898d-ff5c-43eb-b759-5bc80829d4d4
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Listagens Inelegíveis

A variável _[!UICONTROL Ineligible]_A guia mostra uma lista de todos os produtos que estão publicados no Amazon, mas não são qualificados como uma lista com base nas regras de lista atuais. Se um produto anterior foi qualificado e as regras de listagem foram modificadas para torná-lo inelegível, a quantidade associada a um produto cai para 0 e o produto é marcado como_ inelegível _. No entanto, ela ainda está presente no seu [!DNL Amazon Seller Account].

Para mover um produto para fora do _[!UICONTROL Ineligible]_, é possível [modificar suas regras de listagem](./listing-rules.md) para permitir que seus produtos sejam qualificados.

As ações disponíveis no _[!UICONTROL Ineligible]_incluem:

Em _[!UICONTROL Actions]_:

- **[!UICONTROL End Listing(s) on Amazon]**: selecione para remover todas as listagens selecionadas da [!DNL Amazon Marketplace]. Consulte [Encerrar uma listagem do Amazon](./end-listings-manually.md).

- **[!UICONTROL Edit Listing Overrides]**: Opte por alterar as definições de substituição da lista. Consulte [Substituições](./overrides.md) ou [Editar ou remover uma sobreposição](./creating-editing-overrides.md#edit-override-single-listing).

Em **[!UICONTROL Select]** no _[!UICONTROL Action]_coluna:

- **[!UICONTROL View Details]**: Opte por exibir os detalhes da listagem, incluindo o [Log de atividades de listagem](./product-listing-details.md#listing-activity-log), [Preços do Concorrente Buy Box](./product-listing-details.md#buy-box-competitor-pricing), e [Menor preço para concorrentes](./product-listing-details.md#lowest-competitor-pricing). Esta ação é somente para exibição. Nenhuma alteração pode ser feita nos detalhes da lista. Consulte [Exibir detalhes](./product-listing-details.md).

- **[!UICONTROL Create Override]**: escolha criar uma sobreposição e aplicá-la a esta lista. Consulte [Criar uma substituição](./creating-editing-overrides.md).

- **[!UICONTROL Edit Assigned ASIN]**: escolha modificar a ASIN atribuída ao produto de catálogo. Essa ação é usada se um produto no catálogo corresponder à ASIN errada. Consulte [Editar uma ASIN atribuída](./edit-assigned-asin.md).

- **[!UICONTROL Create Alias Seller SKU]**: escolha criar um SKU de alias que possa ser usado para criar uma lista do Amazon do mesmo produto de catálogo. Consulte [Criar um SKU de Vendedor Alias](./create-alias-seller-sku.md).

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**: Opte por alterar o método de preenchimento associado à ordem. Consulte [Definir configurações de Preenchido por](./fulfilled-by.md#configure-fulfilled-by-settings).

- **[!UICONTROL End Listing]**: selecione para remover a lista da lista [!DNL Amazon Marketplace]. Consulte [Encerrar uma listagem do Amazon](./end-listings-manually.md).

>[!NOTE]
>Se você tiver listagens em andamento, o número de listagens será exibido em uma mensagem acima das guias.

![Listagens do Amazon inelegíveis](assets/amazon-ineligible-listings.png)

As home pages dos canais de vendas do Amazon compartilham algumas informações [controles do espaço de trabalho](./workspace-controls.md) que permitem personalizar os dados exibidos.

## Colunas padrão

| Coluna | Descrição |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | A SKU (Unidade de manutenção de estoque) atribuída pela Amazon a um produto para identificar o produto, as opções, o preço e o fabricante. |
| [!UICONTROL ASIN] | Um bloco exclusivo de 10 letras e/ou números que identificam itens.<br><br>ASIN significa [!DNL Amazon Standard Identification Number]. Um ASIN é um bloco exclusivo de 10 letras e/ou números que identificam itens. Para livros, o ASIN é o mesmo que o número ISBN, mas para todos os outros produtos, um novo ASIN é criado quando o item é carregado para o seu catálogo. Você pode encontrar um ASIN de itens na página de detalhes do produto no Amazon, juntamente com mais detalhes relacionados ao item. |
| [!UICONTROL Product Listing Name] | O nome do produto. |
| [!UICONTROL Condition] | A variável [condição](./product-listing-condition.md) do produto. |
| [!UICONTROL Landed Price] | O preço de listagem do produto mais seu preço de envio. |
| [!UICONTROL Amazon Quantity] | A quantidade disponível quando o produto está ativamente listado no Amazon. |
| [!UICONTROL Action] | Lista de ações disponíveis que podem ser aplicadas a uma lista específica. Para aplicar uma ação, clique em **[!UICONTROL Select]** no _[!UICONTROL Action]_e selecione uma opção:<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[Criar substituição](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
