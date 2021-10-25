---
title: Listas não elegíveis
description: O canal de vendas da Amazon fornece a variável [!UICONTROL Ineligible] para ajudá-lo a gerenciar os itens não são qualificados como uma lista com base nas regras de listagem atuais.
exl-id: ae63898d-ff5c-43eb-b759-5bc80829d4d4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Listas não elegíveis

O _[!UICONTROL Ineligible]_mostra uma lista de todos os produtos publicados atualmente no Amazon, mas que não são qualificados como uma lista com base nas regras de listagem atuais. Se um produto anterior tiver sido qualificado e as regras de listagem forem modificadas para torná-lo agora inelegível, a quantidade associada a um produto cairá para 0 e o produto será marcado como_ inelegível _. No entanto, ele ainda está presente no seu [!DNL Amazon Seller Account].

Para remover um produto do _[!UICONTROL Ineligible]_, é possível [modificar suas regras de listagem](./listing-rules.md) para permitir que seus produtos sejam qualificados.

As ações disponíveis no _[!UICONTROL Ineligible]_incluem:

Em _[!UICONTROL Actions]_:

- **[!UICONTROL End Listing(s) on Amazon]**: Escolha remover todas as listagens selecionadas do [!DNL Amazon Marketplace]. Consulte [Encerrar uma listagem do Amazon](./end-listings-manually.md).

- **[!UICONTROL Edit Listing Overrides]**: Escolha alterar as configurações de substituição da listagem. Consulte [Substituições](./overrides.md) ou [Editar ou remover uma substituição](./creating-editing-overrides.md#edit-override-single-listing).

Em **[!UICONTROL Select]** no _[!UICONTROL Action]_coluna:

- **[!UICONTROL View Details]**: escolha exibir detalhes da lista, incluindo o [Listando log de atividades](./product-listing-details.md#listing-activity-log), [Preços do concorrente do Buy Box](./product-listing-details.md#buy-box-competitor-pricing)e [Preços dos Concorrentes Mais Baixos](./product-listing-details.md#lowest-competitor-pricing). Esta ação é apenas para visualização. Não podem ser feitas alterações nos detalhes da lista. Consulte [Exibir detalhes](./product-listing-details.md).

- **[!UICONTROL Create Override]**: escolha criar uma substituição e aplicá-la a esta listagem. Consulte [Criar uma substituição](./creating-editing-overrides.md).

- **[!UICONTROL Edit Assigned ASIN]**: escolha modificar o ASIN atribuído ao produto do catálogo. Essa ação é usada se um produto em seu catálogo correspondeu ao ASIN incorreto. Consulte [Editar uma ASIN atribuída](./edit-assigned-asin.md).

- **[!UICONTROL Create Alias Seller SKU]**: escolha criar um SKU Alias que possa ser usado para criar uma lista do Amazon a partir do mesmo produto de catálogo. Consulte [Criar um SKU de vendedor de alias](./create-alias-seller-sku.md).

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**: escolha alterar o método de preenchimento associado à ordem. Consulte [Configurar Preenchido por](./fulfilled-by.md#configure-fulfilled-by-settings).

- **[!UICONTROL End Listing]**: escolha remover a listagem do [!DNL Amazon Marketplace]. Consulte [Encerrar uma listagem do Amazon](./end-listings-manually.md).

>[!NOTE]
>Se houver listagens em andamento, o número de listagens será exibido em uma mensagem acima das guias.

![Listas Amazon não elegíveis](assets/amazon-ineligible-listings.png)

As home pages do canal de vendas da Amazon compartilham algumas informações comuns [controles do espaço de trabalho](./workspace-controls.md) que permitem personalizar os dados exibidos.

## Colunas padrão

| Coluna | Descrição |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | A SKU (Stock Keeping Unit) atribuída pela Amazon a um produto para identificar o produto, as opções, o preço e o fabricante. |
| [!UICONTROL ASIN] | Um bloco exclusivo de 10 letras e/ou números que identifica itens.<br><br>ASIN significa [!DNL Amazon Standard Identification Number]. Um ASIN é um bloco exclusivo de 10 letras e/ou números que identifica itens. Para livros, o ASIN é o mesmo que o número ISBN, mas para todos os outros produtos, um novo ASIN é criado quando o item é carregado em seu catálogo. Você pode encontrar um ASIN de itens na página de detalhes do produto no Amazon, juntamente com mais detalhes relacionados ao item. |
| [!UICONTROL Product Listing Name] | O nome do produto. |
| [!UICONTROL Condition] | O [condição](./product-listing-condition.md) do produto. |
| [!UICONTROL Landed Price] | O preço de listagem do produto mais seu preço de frete. |
| [!UICONTROL Amazon Quantity] | A quantidade disponível quando o produto é listado ativamente na Amazon. |
| [!UICONTROL Action] | Lista de ações disponíveis que podem ser aplicadas a uma lista específica. Para aplicar uma ação, clique em **[!UICONTROL Select]** no _[!UICONTROL Action]_e selecione uma opção:<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[Criar Substituição](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
