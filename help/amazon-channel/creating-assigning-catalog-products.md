---
title: Criar e atribuir produtos ao canal de vendas do Amazon
description: O Sales Channel da Amazon fornece a [!UICONTROL New Third Party] para ajudar a criar e atribuir produtos de catálogo do Commerce correspondentes às listagens do Amazon.
feature: Sales Channels, Products, Configuration
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1094'
ht-degree: 0%

---

# Criar e atribuir produtos

Ao visualizar _[!UICONTROL New Third Party]_, você pode corresponder ao seu [!DNL Commerce] produtos de catálogo para uma lista existente do Amazon. Há duas opções para essa correspondência. Você pode atribuir uma lista a um produto de catálogo existente ou pode usar as informações da lista para criar produtos de catálogo. Essas opções são úteis quando suas listagens do Amazon não correspondem automaticamente às suas [!DNL Commerce] catálogo.

É necessário corresponder (ou atribuir) seus produtos às suas listagens do Amazon para usar o conjunto completo de recursos do canal de vendas da Amazon.

Ao criar um produto de catálogo em uma lista do Amazon:

- A variável **ASIN** torna-se o [!DNL Commerce] SKU
- A variável **Nome da lista de produtos** torna-se o Nome da Listagem de Catálogos
- A variável **Preço** e **Quantidade** são importados da Listagem do Amazon

O restante das configurações necessárias é determinado pelo parâmetro [!DNL Commerce] configurações do produto selecionadas durante a criação.

Quando criadas e correspondidas, as listagens são removidas da variável _[!UICONTROL New Third Party]_e aparecerão na guia_[!UICONTROL Active]_ guia.

## Atribuir um único produto de catálogo a uma lista do Amazon

1. Exibir suas listagens de produtos no [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) guia.

1. Localize a lista que deseja atribuir na lista, clique em **[!UICONTROL Select]** no _[!UICONTROL Action]_e clique em **[!UICONTROL Assign Catalog Product]**.

   Essa ação abre a variável _[!UICONTROL Assign Magento Catalog Product]_página.

1. Procure ou filtre a lista usando o [controles do espaço de trabalho](./workspace-controls.md) e localize o produto de catálogo apropriado para corresponder à lista.

1. Quando o produto correto aparecer na lista, clique em **[!UICONTROL Assign Catalog Product]** no _[!UICONTROL Action]_coluna.

Seu produto e sua lista agora são correspondidos. O canal de vendas da Amazon agora pode compartilhar dados de produtos e listas com a Amazon e gerenciar sua lista e suas informações, incluindo preço de lista, preço de envio, estoque/quantidade, informações e status de pedidos e muito mais.

## Criar um único produto de catálogo usando as informações da lista do Amazon

1. Exibir suas listagens de produtos no [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) guia.

1. Localize a lista que deseja criar em seu [!DNL Commerce] catálogo, clique em **[!UICONTROL Select]** no _[!UICONTROL Action]_e clique em **[!UICONTROL Create New Catalog Product]**.

   Essa ação abre a variável _[!UICONTROL Create Magento Catalog Product]_página.

1. Conclua as configurações do catálogo do produto.

   - Definir **[!UICONTROL Enable Product(s)]** alternar para `Yes` ou `No` (obrigatório).

     |Sim|Escolha tornar o produto qualificado para a sua [!DNL Commerce] vendas de vitrine.| |Não|Escolha tornar o produto inelegível para sua [!DNL Commerce] vendas de vitrine.|

   - Para **[!UICONTROL Categories]**, atribua uma categoria ao produto (opcional).

     Para selecionar a categoria do produto, clique na seta para baixo e marque uma caixa de seleção de categoria. Clique em **[!UICONTROL Done]** quando terminar.

   - Para **[!UICONTROL Website Ids]**, escolha o site (loja) ao qual o produto será associado.

     As opções nessa lista dependem do seu [!DNL Commerce] [configuração da loja](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) configurações.

   - Para **[!UICONTROL Attribute Set Id]** (obrigatório), escolha uma opção.

     `Default` é a seleção padrão. As opções nessa lista dependem do seu [!DNL Commerce] [conjuntos de atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) você configurou o.

   - Para **[!UICONTROL Visibility]**, escolha uma opção para o novo produto.

     |**[!UICONTROL Not Visible Individually]** (padrão)|O produto não está incluído nas listagens de vitrines, embora possa estar disponível como uma variação de outro produto.| |**[!UICONTROL Catalog]**|O produto aparece nas listagens do catálogo.| |**[!UICONTROL Search]**|O produto está disponível para operações de pesquisa.| |**[!UICONTROL Catalog and Search]**|O produto está incluído nas listagens de catálogo e disponível para operações de pesquisa.|

   - Para **[!UICONTROL Assign Tax Class]**, escolha uma opção para o produto.

     As opções exibidas nessa lista dependem das [classes de imposto](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) você configurou o.

   - Quando terminar, clique em **[!UICONTROL Create Catalog Products]**.

O produto de catálogo é criado no [!DNL Commerce] catálogo e atribuído à listagem do Amazon da qual foi criado. Como a lista agora corresponde a uma lista existente do Amazon, a lista é removida da _[!UICONTROL New Third Party]_e aparecerão na guia_[!UICONTROL Active]_ guia.

## Criar vários produtos de catálogo usando as informações de lista do Amazon

1. Exibir suas listagens de produtos no [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) guia.

1. Selecione as listagens para as quais criar produtos de catálogo.

   Você pode marcar caixas de seleção individuais na coluna do lado esquerdo ou clicar na seta para baixo na coluna do lado superior esquerdo e escolher **[!UICONTROL Select All]** ou **[!UICONTROL Select All on this Page]**.

1. Em _[!UICONTROL Actions]_, clique em **[!UICONTROL Create New Catalog Product(s)]**.

1. Para aceitar a mensagem de confirmação e abrir a _[!UICONTROL Create Magento Catalog Product]_clique em **[!UICONTROL OK]**.

1. Conclua as configurações do catálogo dos produtos.

   >[!NOTE]
   >Ao criar produtos de catálogo para várias listagens selecionadas, as configurações de produto inseridas são aplicadas a todas as listagens.

   - Definir **[!UICONTROL Enable Product(s)]** alternar para `Yes` ou `No` (obrigatório).

     |Sim|Escolha tornar o produto qualificado para a sua [!DNL Commerce] vendas de vitrine.| |Não|Escolha tornar o produto inelegível para sua [!DNL Commerce] vendas de vitrine.|

   - Para **[!UICONTROL Categories]**, atribua uma categoria ao produto (opcional).

     Para selecionar a categoria do produto, clique na seta para baixo e marque uma caixa de seleção de categoria. Clique em **Concluído** quando terminar.

   - Para **[!UICONTROL Website Ids]**, escolha o site (loja) ao qual o produto será associado.

     As opções nessa lista dependem do seu [!DNL Commerce] [configuração da loja](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) configurações.

   - Para **[!UICONTROL Attribute Set Id]** (obrigatório), escolha uma opção.

     `Default` é a seleção padrão. As opções nessa lista dependem do seu [!DNL Commerce] [conjuntos de atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) você configurou o.

   - Para **[!UICONTROL Visibility]**, escolha uma opção para o novo produto.

     |**[!UICONTROL Not Visible Individually]** (padrão)|O produto não está incluído nas listagens de vitrines, embora possa estar disponível como uma variação de outro produto.| |**[!UICONTROL Catalog]**|O produto aparece nas listagens do catálogo.| |**[!UICONTROL Search]**|O produto está disponível para operações de pesquisa.| |**[!UICONTROL Catalog and Search]**|O produto está incluído nas listagens de catálogo e disponível para operações de pesquisa.|

   - Para **[!UICONTROL Assign Tax Class]**, escolha uma opção para o produto.

     As opções exibidas nessa lista dependem das [classes de imposto](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) você configurou o.

   - Quando terminar, clique em **[!UICONTROL Create Catalog Products]**.

Os produtos do catálogo são criados no [!DNL Commerce] catálogo e atribuído à listagem do Amazon da qual foi criado. Com as listagens agora correspondidas às respectivas listagens do Amazon, as listagens são removidas da [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) e aparecerão na guia [_[!UICONTROL Active]_](./active-listings.md) guia.

![Criar produto de catálogo do Commerce](assets/amazon-magento-catalog-product.png){width="600" zoomable="yes"}

| Campo | Descrição |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Product(s)] | (Obrigatório) Se ativado, o produto fica visível no [!DNL Commerce] vitrine eletrônica. Se estiver desativado, o produto não será exibido no [!DNL Commerce] vitrine eletrônica. |
| [!UICONTROL Categories] | É possível inserir o nome da categoria do novo produto ou selecionar uma categoria clicando na seta para baixo para mostrar as opções. As opções dependem do seu [categorias](https://experienceleague.adobe.com/docs/commerce-admin/catalog/categories/create/category-create.html) configuração. |
| [!UICONTROL Website Ids] | (Obrigatório) Escolha o site (loja) ao qual o produto será associado. As opções dependem do seu [!DNL Commerce] [configuração da loja](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) configurações |
| ID do conjunto de atributos | Escolha um conjunto de atributos. As opções dependem do que foi configurado [!DNL Commerce] [conjuntos de atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html). |
| [!UICONTROL Visibility] | Opções:<ul><li>**[!UICONTROL Not Visible Individually]** - O produto não está visível no seu [!DNL Commerce] vitrine (mais comum para produtos variantes).</li><li>**[!UICONTROL Catalog]** - Permite que o produto seja acessado por meio da categoria à qual está associado no site.</li><li>**Pesquisar** - Permite que o produto só seja encontrado através da ferramenta de pesquisa.</li><li>**[!UICONTROL Catalog and Search]** - Permite que os produtos sejam acessados por meio da estrutura de categorias e usando a ferramenta de pesquisa.</li></ul> |
| [!UICONTROL Assign Tax Class] | Atribua uma classe de imposto ao novo produto. As opções dependem do que foi configurado [classes de imposto](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html). |
