---
title: Canal de vendas do Amazon - [!UICONTROL Listing Rules]
description: Usar regras de listagem determina os produtos do catálogo do Commerce publicados como listagens do Amazon Marketplace.
feature: Sales Channels, Products
exl-id: b28a625b-64cf-4119-98bb-f1ea33043c8f
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 0%

---

# [!UICONTROL Listing Rules]

É possível acessar as regras de listagem para armazenamento na [painel de armazenamento](./amazon-store-dashboard.md).

As regras de listagem definem as regras para determinar quais produtos o canal de vendas da Amazon publica para a Amazon. Essas regras fornecem muitas opções para criar regras simples a complexas para incluir ou excluir produtos como listas. Cada regra consiste em condições que definem os requisitos de qualificação para a lista de produtos.

As regras de listagem são continuamente sincronizadas com as [!DNL Commerce] catálogo. Ao adicionar novas [!DNL Commerce] produtos que atendem aos requisitos de qualificação definidos pelas regras de listagem, os produtos são processados automaticamente para listagem no Amazon.

- Se quiser que todos os seus produtos sejam publicados em uma lista do Amazon, não defina condições para as regras da lista.

- Se quiser limitar quais dos seus produtos de catálogo são publicados no Amazon, defina as condições da regra de listagem. A definição das condições para as regras de listagem do Amazon segue a mesma lógica e processo que a definição das condições para [Regras de preço do carrinho](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html).

- Se as regras de lista excluírem um produto, o status de qualificação desse produto será alterado para `Ineligible`. Produtos não qualificados não são publicados no Amazon.

- Se um produto inelegível já estiver listado no Amazon e você corresponder a lista do Amazon ao seu [!DNL Commerce] produto de catálogo, a quantidade da lista do Amazon muda para `0` para impedir as vendas do produto. As listagens do Amazon podem ser [removido manualmente](./end-listings-manually.md).

As alterações na quantidade e no status de qualificação afetam todas as listagens que compartilham o SKU do Vendedor Amazon nos mercados existentes para lojas que vendem na mesma região (conforme definido em _[!UICONTROL Amazon Marketplace Country]_durante [integração de loja](./store-integration.md)). No entanto, uma alteração em um [!DNL Amazon Seller SKU] em uma região não afeta as listagens do Amazon do produto em outro país.

![Regras de listagem](assets/ob-listing-rules.png){width="600" zoomable="yes"}

## Definir configurações de Regras de Listagem

1. Clique em **[!UICONTROL Listing Rules]** no painel da loja.

1. Defina as condições desejadas para a qualificação de produtos a serem listados no Amazon.

Consulte [Exemplo: definir uma condição](./ob-define-condition-example.md).

| Campo | Descrição |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Websites] | As opções disponíveis dependem do [sites](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) você configurou o em seu [!DNL Commerce] configuração. Selecione o site dos produtos qualificados listados no Amazon. Somente um site pode ser selecionado, pois cada site requer uma loja exclusiva do Amazon criada no canal de vendas do Amazon. |
| [!UICONTROL Conditions] | Usado para definir o [!DNL Commerce] atributos para qualificação de produto na região do Amazon. Consulte [Exemplo: definir uma condição](./ob-define-condition-example.md). |

## Espaço de trabalho Condições

É possível clicar em qualquer área nas condições em negrito para ver as várias opções.

- Não adicione condições se todos os produtos nos sites selecionados estiverem qualificados.
- Há um conjunto complexo de processos de back-end para se comunicar diretamente com os sistemas da Amazon. Com base no número de itens que você está tentando listar e na ocupação dos sistemas da Amazon (como Black Friday), pode levar algum tempo para que seus itens sejam listados no Amazon.

Para obter mais informações sobre condições, consulte [Descrever as condições](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html).

## Visualização da regra de listagem

Ao modificar as definições de condição para as regras de lista, você pode clicar em **[!UICONTROL Preview Changes]** para aplicar as alterações nas regras e visualizar como as listagens são afetadas. Verifique suas listas neste recurso de visualização de lista antes de salvar as alterações na regra de lista.

As listagens do Amazon são comparadas com as regras e condições definidas. Em seguida, é possível revisar:

- Quais produtos são movidos para um status inelegível com base em seu atual [!DNL Amazon Seller Central] account
- Quais produtos mudam de um estado inelegível para o status elegível
- Quais produtos são as Novas listagens do Amazon e adicionados à sua lista do Amazon a partir de seus produtos elegíveis [!DNL Commerce] products

A Visualização de listagens permite que você visualize suas listagens potenciais do Amazon e faça os ajustes necessários nas regras da listagem.

Suas possíveis listagens do Amazon são preenchidas no _[!UICONTROL Listing Preview]_em uma das três guias:

- **[!UICONTROL Ineligible Listings]** - Os produtos listados não são qualificados para a lista do Amazon com base nas regras e condições atuais da lista.

  Produtos não qualificados não são publicados no Amazon. Se um produto inelegível já estiver listado no Amazon e você corresponder a lista do Amazon ao seu [!DNL Commerce] produto de catálogo, a quantidade da lista do Amazon muda para `0` para impedir as vendas do produto. Para remover manualmente uma listagem, consulte [Encerramento de uma listagem do Amazon](./end-listings-manually.md). Os produtos que não estão qualificados pelos requisitos do Amazon não estão listados aqui. Esses produtos estão listados no [Guia Listings inativos](./inactive-listings.md).

- **[!UICONTROL Eligible Listings]** - Os produtos listados são qualificados para a lista do Amazon com base nas regras e condições atuais da lista e também são qualificados pelos requisitos da Amazon. Essa lista inclui suas listas existentes do Amazon que importam (se você tiver **Importar Listagens de Terceiros** definir como `Import Listing` in [Configurações de listagem](./third-party-listing-settings.md)).

- **[!UICONTROL New Listings]** - Os produtos listados incluem o [!DNL Commerce] catalogar produtos que são recém-qualificados para a listagem do Amazon com base nas regras e condições atuais da listagem, além de criar e publicar novas listagens do Amazon.

### Visualizar sua lista

1. Clique em **[!UICONTROL Listing Rules]** no painel da loja.

1. Exibir ou adicionar seu [regras de listagem](./listing-rules.md).

1. Modifique o seu [Condições da regra de listagem](./ob-define-condition-example.md).

1. Clique em **[!UICONTROL Preview Changes]**.

1. Revise e confirme suas listas no _[!UICONTROL Ineligible Listings]_,_[!UICONTROL Eligible Listings]_, e _[!UICONTROL New Listings]_guias.

1. Se suas listagens corresponderem às suas expectativas, clique em **[!UICONTROL Save and close]**.

   Se suas listagens não forem exibidas conforme esperado, clique em **[!UICONTROL Back]** e modifique suas regras e condições até que suas listas atendam às suas expectativas.

![Visualização da regra de listagem](assets/amazon-listing-rule-preview.png){width="600" zoomable="yes"}

### Listando registros de visualização

| Campo | Descrição |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product ID] | O número sequencial exclusivo atribuído a um [!DNL Commerce] produto de catálogo quando adicionado. |
| [!UICONTROL Thumbnail] | Mostra uma miniatura da imagem principal do produto. |
| [!UICONTROL Name] | O nome do produto, gerenciado no [!DNL Commerce] [grade de produtos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html). |
| [!UICONTROL Type] | O tipo de produto, gerenciado no [!DNL Commerce] grade de produtos. |
| [!UICONTROL Attribute Set] | O nome do conjunto de atributos usado como modelo para o produto, gerenciado na [!DNL Commerce] grade de produtos. |
| [!UICONTROL SKU] | A Unidade de Manutenção de Estoque exclusiva atribuída ao produto, gerenciada na [!DNL Commerce] grade de produtos. |
| [!UICONTROL Visibility] | Indica onde o produto está visível, gerenciado na [!DNL Commerce] grade de produtos. Opções:<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| Status | Indica o status do produto, gerenciado na [!DNL Commerce] grade de produtos. Opções: `Enabled` / `Disabled` |

![Fluxo de trabalho de visualização da listagem](assets/listing-preview-flowchart.png){width="500" zoomable="yes"}
