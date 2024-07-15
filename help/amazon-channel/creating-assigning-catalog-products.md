---
title: Criar e atribuir produtos ao canal de vendas do Amazon
description: O Amazon Sales Channel fornece a guia [!UICONTROL New Third Party] para ajudar a criar e atribuir produtos de catálogo Commerce correspondentes com as listagens do Amazon.
feature: Sales Channels, Products, Configuration
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 0%

---

# Criar e atribuir produtos

Ao visualizar a guia _[!UICONTROL New Third Party]_, você pode combinar seus produtos de catálogo [!DNL Commerce] a uma lista existente do Amazon. Há duas opções para essa correspondência. Você pode atribuir uma lista a um produto de catálogo existente ou pode usar as informações da lista para criar produtos de catálogo. Essas opções são úteis quando suas listagens do Amazon não correspondem automaticamente ao catálogo do [!DNL Commerce].

É necessário corresponder (ou atribuir) seus produtos às suas listagens do Amazon para usar o conjunto completo de recursos do canal de vendas da Amazon.

Ao criar um produto de catálogo em uma lista do Amazon:

- A **ASIN** torna-se a SKU [!DNL Commerce]
- O **Nome da Listagem de Produtos** torna-se o Nome da Listagem de Catálogos
- O **Preço** e a **Quantidade** são importados da Listagem do Amazon

O restante das configurações necessárias é determinado pelas configurações de produto do [!DNL Commerce] selecionadas durante a criação.

Quando criadas e correspondidas, as listagens são removidas da guia _[!UICONTROL New Third Party]_e são exibidas na guia_[!UICONTROL Active]_.

## Atribuir um único produto de catálogo a uma lista do Amazon

1. Exiba suas listas de produtos na guia [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Localize a listagem que você deseja atribuir na lista, clique em **[!UICONTROL Select]** na coluna _[!UICONTROL Action]_e clique em **[!UICONTROL Assign Catalog Product]**.

   Esta ação abre a página _[!UICONTROL Assign Magento Catalog Product]_.

1. Procure ou filtre a lista usando os [controles de espaço de trabalho](./workspace-controls.md) e localize o produto de catálogo apropriado para corresponder à lista.

1. Quando o produto correto aparecer na lista, clique em **[!UICONTROL Assign Catalog Product]** na coluna _[!UICONTROL Action]_.

Seu produto e sua lista agora são correspondidos. O canal de vendas da Amazon agora pode compartilhar dados de produtos e listas com a Amazon e gerenciar sua lista e suas informações, incluindo preço de lista, preço de envio, estoque/quantidade, informações e status de pedidos e muito mais.

## Criar um único produto de catálogo usando as informações da lista do Amazon

1. Exiba suas listas de produtos na guia [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Localize a listagem que você deseja criar no catálogo [!DNL Commerce], clique em **[!UICONTROL Select]** na coluna _[!UICONTROL Action]_e em **[!UICONTROL Create New Catalog Product]**.

   Esta ação abre a página _[!UICONTROL Create Magento Catalog Product]_.

1. Conclua as configurações do catálogo do produto.

   - Defina a alternância de **[!UICONTROL Enable Product(s)]** para `Yes` ou `No` (obrigatório).

     |Sim|Escolha tornar o produto qualificado para as vendas de vitrine do [!DNL Commerce].|
|Não|Escolha não qualificar o produto para as vendas de vitrine do [!DNL Commerce].|

   - Para **[!UICONTROL Categories]**, atribua uma categoria ao produto (opcional).

     Para selecionar a categoria do produto, clique na seta para baixo e marque uma caixa de seleção de categoria. Clique em **[!UICONTROL Done]** quando terminar.

   - Para **[!UICONTROL Website Ids]**, escolha o site (loja) ao qual o produto será associado.

     As opções nesta lista dependem das configurações de [!DNL Commerce] [armazenamento](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html).

   - Para **[!UICONTROL Attribute Set Id]** (obrigatório), escolha uma opção.

     `Default` é a seleção padrão. As opções desta lista dependem dos seus [!DNL Commerce] [conjuntos de atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) configurados.

   - Para **[!UICONTROL Visibility]**, escolha uma opção para o novo produto.

     |**[!UICONTROL Not Visible Individually]** (padrão)|O produto não está incluído nas listagens de vitrines, embora possa estar disponível como uma variação de outro produto.|
|**[!UICONTROL Catalog]**|O produto aparece em suas listagens de catálogo.|
|**[!UICONTROL Search]**|O produto está disponível para operações de pesquisa.|
|**[!UICONTROL Catalog and Search]**|O produto está incluído nas listagens de catálogo e disponível para operações de pesquisa.|

   - Para **[!UICONTROL Assign Tax Class]**, escolha uma opção para o produto.

     As opções exibidas nessa lista dependem das [classes de imposto](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) configuradas.

   - Quando terminar, clique em **[!UICONTROL Create Catalog Products]**.

O produto de catálogo é criado no catálogo [!DNL Commerce] e atribuído à lista Amazon da qual foi criado. Com a lista agora correspondente a uma lista existente do Amazon, a lista é removida da guia _[!UICONTROL New Third Party]_e aparece na guia_[!UICONTROL Active]_.

## Criar vários produtos de catálogo usando as informações de lista do Amazon

1. Exiba suas listas de produtos na guia [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Selecione as listagens para as quais criar produtos de catálogo.

   Você pode marcar caixas de seleção individuais na coluna do lado esquerdo ou clicar na seta para baixo na coluna do canto superior esquerdo e escolher **[!UICONTROL Select All]** ou **[!UICONTROL Select All on this Page]**.

1. Em _[!UICONTROL Actions]_, clique em **[!UICONTROL Create New Catalog Product(s)]**.

1. Para aceitar a mensagem de confirmação e abrir a página _[!UICONTROL Create Magento Catalog Product]_, clique em **[!UICONTROL OK]**.

1. Conclua as configurações do catálogo dos produtos.

   >[!NOTE]
   >Ao criar produtos de catálogo para várias listagens selecionadas, as configurações de produto inseridas são aplicadas a todas as listagens.

   - Defina a alternância de **[!UICONTROL Enable Product(s)]** para `Yes` ou `No` (obrigatório).

     |Sim|Escolha tornar o produto qualificado para as vendas de vitrine do [!DNL Commerce].|
|Não|Escolha não qualificar o produto para as vendas de vitrine do [!DNL Commerce].|

   - Para **[!UICONTROL Categories]**, atribua uma categoria ao produto (opcional).

     Para selecionar a categoria do produto, clique na seta para baixo e marque uma caixa de seleção de categoria. Clique em **Concluído** quando terminar.

   - Para **[!UICONTROL Website Ids]**, escolha o site (loja) ao qual o produto será associado.

     As opções nesta lista dependem das configurações de [!DNL Commerce] [armazenamento](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html).

   - Para **[!UICONTROL Attribute Set Id]** (obrigatório), escolha uma opção.

     `Default` é a seleção padrão. As opções desta lista dependem dos seus [!DNL Commerce] [conjuntos de atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) configurados.

   - Para **[!UICONTROL Visibility]**, escolha uma opção para o novo produto.

     |**[!UICONTROL Not Visible Individually]** (padrão)|O produto não está incluído nas listagens de vitrines, embora possa estar disponível como uma variação de outro produto.|
|**[!UICONTROL Catalog]**|O produto aparece em suas listagens de catálogo.|
|**[!UICONTROL Search]**|O produto está disponível para operações de pesquisa.|
|**[!UICONTROL Catalog and Search]**|O produto está incluído nas listagens de catálogo e disponível para operações de pesquisa.|

   - Para **[!UICONTROL Assign Tax Class]**, escolha uma opção para o produto.

     As opções exibidas nessa lista dependem das [classes de imposto](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) configuradas.

   - Quando terminar, clique em **[!UICONTROL Create Catalog Products]**.

Os produtos do catálogo são criados no catálogo [!DNL Commerce] e atribuídos à lista da Amazon da qual foram criados. Com as listagens agora correspondentes às suas respectivas listagens do Amazon, as listagens são removidas da guia [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) e aparecem na guia [_[!UICONTROL Active]_](./active-listings.md).

![Criar produto de catálogo do Commerce](assets/amazon-magento-catalog-product.png){width="600" zoomable="yes"}

| Campo | Descrição |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Product(s)] | (Obrigatório) Se habilitado, o produto estará visível na loja [!DNL Commerce]. Se estiver desabilitado, o produto não será exibido na loja [!DNL Commerce]. |
| [!UICONTROL Categories] | É possível inserir o nome da categoria do novo produto ou selecionar uma categoria clicando na seta para baixo para mostrar as opções. As opções dependem da configuração de [categorias](https://experienceleague.adobe.com/docs/commerce-admin/catalog/categories/create/category-create.html). |
| [!UICONTROL Website Ids] | (Obrigatório) Escolha o site (loja) ao qual o produto será associado. As opções dependem das configurações de [!DNL Commerce] [armazenamento](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) |
| ID do conjunto de atributos | Escolha um conjunto de atributos. As opções dependem dos [!DNL Commerce] [conjuntos de atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) configurados. |
| [!UICONTROL Visibility] | Opções:<ul><li>**[!UICONTROL Not Visible Individually]** - O produto não está visível na sua vitrine do [!DNL Commerce] (mais comum para produtos de variantes).</li><li>**[!UICONTROL Catalog]** - Permite que o produto seja acessado por meio da categoria à qual está associado no site.</li><li>**Pesquisa** - Permite que o produto seja localizado somente pela ferramenta de pesquisa.</li><li>**[!UICONTROL Catalog and Search]** - Permite que os produtos sejam acessados por meio da estrutura de categorias e usando a ferramenta de pesquisa.</li></ul> |
| [!UICONTROL Assign Tax Class] | Atribua uma classe de imposto ao novo produto. As opções dependem das [classes de imposto](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) configuradas. |
