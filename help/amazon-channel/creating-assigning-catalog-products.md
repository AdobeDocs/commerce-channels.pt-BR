---
title: Criar e atribuir produtos
description: O Amazon Sales Channel fornece a guia [!UICONTROL New Third Party] para ajudar a criar e atribuir produtos de catálogo comercial correspondentes às listagens do Amazon.
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 0%

---

# Criar e atribuir produtos

Ao visualizar a guia _[!UICONTROL New Third Party]_, é possível corresponder os produtos do catálogo [!DNL Commerce] a uma listagem existente do Amazon. Há duas opções para essa correspondência. Você pode atribuir uma listagem a um produto de catálogo existente, ou usar as informações da listagem para criar produtos de catálogo. Essas opções são úteis quando as listagens do Amazon não correspondem automaticamente ao catálogo [!DNL Commerce].

A correspondência (ou atribuição) de seus produtos às suas listagens do Amazon é necessária para usar o conjunto completo de recursos do canal de vendas do Amazon.

Ao criar um produto de catálogo a partir de uma listagem do Amazon:

- O **ASIN** torna-se o SKU [!DNL Commerce]
- O **Nome da Lista de Produtos** torna-se o Nome da Lista de Catálogo
- O **Preço** e **Quantidade** são importados da listagem do Amazon

O restante das configurações necessárias são determinadas pelas [!DNL Commerce] configurações de produto selecionadas durante a criação.

Quando criadas e correspondidas, as listagens são removidas da guia _[!UICONTROL New Third Party]_e exibidas na guia_[!UICONTROL Active]_.

## Atribuir um único produto de catálogo a uma lista da Amazon

1. Exiba as listagens de produtos na guia [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Encontre a listagem que deseja atribuir na lista, clique em **[!UICONTROL Select]** na coluna _[!UICONTROL Action]_e clique em **[!UICONTROL Assign Catalog Product]**.

   Essa ação abre a página _[!UICONTROL Assign Magento Catalog Product]_.

1. Procure ou filtre a lista usando o [workspace controls](./workspace-controls.md) e localize o produto de catálogo apropriado para corresponder à lista.

1. Quando o produto correto aparecer na lista, clique em **[!UICONTROL Assign Catalog Product]** na coluna _[!UICONTROL Action]_.

Seu produto e sua lista agora são correspondidos. O canal de vendas da Amazon agora pode compartilhar dados de produto e listar com a Amazon e gerenciar sua listagem e suas informações, incluindo a listagem de preço, preço de envio, estoque/quantidade, informações e status do pedido e muito mais.

## Criar um produto de catálogo único usando as informações da listagem do Amazon

1. Exiba as listagens de produtos na guia [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Encontre a listagem que deseja criar no catálogo [!DNL Commerce], clique em **[!UICONTROL Select]** na coluna _[!UICONTROL Action]_e clique em **[!UICONTROL Create New Catalog Product]**.

   Essa ação abre a página _[!UICONTROL Create Magento Catalog Product]_.

1. Preencha as configurações de catálogo do produto.

   - Defina **[!UICONTROL Enable Product(s)]** como `Yes` ou `No` (obrigatório).

      |Sim|Escolha tornar o produto qualificado para as vendas da loja [!DNL Commerce].|
|Não|Escolha tornar o produto inelegível para as vendas da loja [!DNL Commerce].|

   - Para **[!UICONTROL Categories]**, atribua uma categoria ao produto (opcional).

      Para selecionar a categoria do produto, clique na seta para baixo e marque uma caixa de seleção de categoria. Clique em **[!UICONTROL Done]** quando terminar.

   - Para **[!UICONTROL Website Ids]**, escolha o site (vitrine) ao qual o produto será associado.

      As opções nesta lista dependem das suas configurações [!DNL Commerce] [de configuração de armazenamento](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}.

   - Para **[!UICONTROL Attribute Set Id]** (obrigatório), escolha uma opção.

      `Default` é a seleção padrão. As opções nesta lista dependem dos [!DNL Commerce] [conjuntos de atributos](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;} que você configurou.

   - Para **[!UICONTROL Visibility]**, escolha uma opção para o novo produto.

      |**[!UICONTROL Not Visible Individually]** (padrão)|O produto não está incluído em suas listas de vitrine, embora possa estar disponível como uma variação de outro produto.|
|**[!UICONTROL Catalog]**|O produto aparece nas listagens do catálogo.|
|**[!UICONTROL Search]**|O produto está disponível para operações de pesquisa.|
|**[!UICONTROL Catalog and Search]**|O produto está incluído nas listas de catálogos e disponível para operações de pesquisa.|

   - Para **[!UICONTROL Assign Tax Class]**, escolha uma opção para o produto.

      As opções exibidas nessa lista dependem das [classes de imposto](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;} que você configurou.

   - Quando terminar, clique em **[!UICONTROL Create Catalog Products]**.

O produto do catálogo é criado em seu catálogo [!DNL Commerce] e atribuído à listagem do Amazon a partir da qual foi criado. Com a listagem agora correspondendo a uma listagem existente do Amazon, a listagem é removida da guia _[!UICONTROL New Third Party]_e exibida na guia_[!UICONTROL Active]_.

## Criar vários produtos de catálogo usando suas informações de listagem do Amazon

1. Exiba as listagens de produtos na guia [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Selecione as listagens para as quais criar produtos de catálogo.

   Você pode marcar caixas de seleção individuais na coluna à esquerda ou clicar na seta para baixo na coluna superior à esquerda e escolher **[!UICONTROL Select All]** ou **[!UICONTROL Select All on this Page]**.

1. Em _[!UICONTROL Actions]_, clique em **[!UICONTROL Create New Catalog Product(s)]**.

1. Para aceitar a mensagem de confirmação e abrir a página _[!UICONTROL Create Magento Catalog Product]_, clique em **[!UICONTROL OK]**.

1. Preencha as configurações de catálogo dos produtos.

   >[!NOTE]
   >Ao criar produtos de catálogo para várias listagens selecionadas, as configurações de produto inseridas são aplicadas a todas as listagens.

   - Defina **[!UICONTROL Enable Product(s)]** como `Yes` ou `No` (obrigatório).

      |Sim|Escolha tornar o produto qualificado para as vendas da loja [!DNL Commerce].|
|Não|Escolha tornar o produto inelegível para as vendas da loja [!DNL Commerce].|

   - Para **[!UICONTROL Categories]**, atribua uma categoria ao produto (opcional).

      Para selecionar a categoria do produto, clique na seta para baixo e marque uma caixa de seleção de categoria. Clique em **Concluído** quando terminar.

   - Para **[!UICONTROL Website Ids]**, escolha o site (vitrine) ao qual o produto será associado.

      As opções nesta lista dependem das suas configurações [!DNL Commerce] [de configuração de armazenamento](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}.

   - Para **[!UICONTROL Attribute Set Id]** (obrigatório), escolha uma opção.

      `Default` é a seleção padrão. As opções nesta lista dependem dos [!DNL Commerce] [conjuntos de atributos](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;} que você configurou.

   - Para **[!UICONTROL Visibility]**, escolha uma opção para o novo produto.

      |**[!UICONTROL Not Visible Individually]** (padrão)|O produto não está incluído em suas listas de vitrine, embora possa estar disponível como uma variação de outro produto.|
|**[!UICONTROL Catalog]**|O produto aparece nas listagens do catálogo.|
|**[!UICONTROL Search]**|O produto está disponível para operações de pesquisa.|
|**[!UICONTROL Catalog and Search]**|O produto está incluído nas listas de catálogos e disponível para operações de pesquisa.|

   - Para **[!UICONTROL Assign Tax Class]**, escolha uma opção para o produto.

      As opções exibidas nessa lista dependem das [classes de imposto](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;} que você configurou.

   - Quando terminar, clique em **[!UICONTROL Create Catalog Products]**.

Os produtos do catálogo são criados em seu catálogo [!DNL Commerce] e atribuídos à lista do Amazon a partir da qual foram criados. Com as listagens agora correspondendo à respectiva listagem do Amazon, elas são removidas da guia [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) e exibidas na guia [_[!UICONTROL Active]_](./active-listings.md).

![Criar produto de catálogo do Commerce](assets/amazon-magento-catalog-product.png)

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Enable Product(s)] | (Obrigatório) Se estiver habilitado, o produto estará visível em sua loja [!DNL Commerce]. Se estiver desativado, o produto não será exibido na loja [!DNL Commerce]. |
| [!UICONTROL Categories] | É possível inserir o nome da categoria do novo produto ou selecionar uma categoria clicando na seta para baixo para exibir as opções. As opções dependem da sua configuração [categories](https://docs.magento.com/user-guide/catalog/category-create.html){target=&quot;_blank&quot;}. |
| [!UICONTROL Website Ids] | (Obrigatório) Escolha o site (loja) para o qual o produto será associado. As opções dependem das configurações [!DNL Commerce] [do armazenamento](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;} |
| ID do conjunto de atributos | Escolha um conjunto de atributos. As opções dependem dos [!DNL Commerce] [conjuntos de atributos](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;} configurados. |
| [!UICONTROL Visibility] | Opções:<ul><li>**[!UICONTROL Not Visible Individually]** - O produto não é visível em sua  [!DNL Commerce] vitrine (mais comum em produtos variantes).</li><li>**[!UICONTROL Catalog]** - Permite que o produto seja acessado por meio da categoria à qual está associado no site.</li><li>**Pesquisa**  - permite que o produto seja encontrado somente por meio da ferramenta de pesquisa.</li><li>**[!UICONTROL Catalog and Search]** - Permite que os produtos sejam acessados por meio da estrutura de categoria e com o uso da ferramenta de pesquisa.</li></ul> |
| [!UICONTROL Assign Tax Class] | Atribua uma classe de imposto ao novo produto. As opções dependem das [classes de imposto](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;} configuradas. |
