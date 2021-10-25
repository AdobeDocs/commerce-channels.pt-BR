---
title: Criar e atribuir produtos
description: O Sales Channel Amazon fornece a variável [!UICONTROL New Third Party] para ajudar a criar e atribuir produtos de catálogo do Commerce correspondentes às listas do Amazon.
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 0%

---

# Criar e atribuir produtos

Ao visualizar _[!UICONTROL New Third Party]_, você pode corresponder a sua [!DNL Commerce] catálogo de produtos para uma lista existente do Amazon. Há duas opções para essa correspondência. Você pode atribuir uma listagem a um produto de catálogo existente, ou usar as informações da listagem para criar produtos de catálogo. Essas opções são úteis quando as listagens do Amazon não correspondem automaticamente às [!DNL Commerce] catálogo.

A correspondência (ou atribuição) de seus produtos às suas listagens do Amazon é necessária para usar o conjunto completo de recursos do canal de vendas do Amazon.

Ao criar um produto de catálogo a partir de uma listagem do Amazon:

- O **ASIN** torna-se o [!DNL Commerce] SKU
- O **Nome da listagem de produtos** se torna o Nome da listagem do catálogo
- O **Preço** e **Quantidade** são importados da listagem do Amazon

O restante das configurações necessárias são determinadas pela variável [!DNL Commerce] configurações de produto selecionadas durante a criação.

Quando criadas e correspondidas, as listagens são removidas do _[!UICONTROL New Third Party]_e aparecerão na guia_[!UICONTROL Active]_ guia .

## Atribuir um único produto de catálogo a uma lista da Amazon

1. Veja as listagens de produtos no [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) guia .

1. Encontre a listagem que deseja atribuir na lista, clique em **[!UICONTROL Select]** no _[!UICONTROL Action]_e clique em **[!UICONTROL Assign Catalog Product]**.

   Essa ação abre o _[!UICONTROL Assign Magento Catalog Product]_página.

1. Procure ou filtre a lista usando o [controles do espaço de trabalho](./workspace-controls.md) e localize o produto de catálogo apropriado para corresponder à lista.

1. Quando o produto correto aparecer na lista, clique em **[!UICONTROL Assign Catalog Product]** no _[!UICONTROL Action]_coluna.

Seu produto e sua lista agora são correspondidos. O canal de vendas da Amazon agora pode compartilhar dados de produto e listar com a Amazon e gerenciar sua listagem e suas informações, incluindo a listagem de preço, preço de envio, estoque/quantidade, informações e status do pedido e muito mais.

## Criar um produto de catálogo único usando as informações da listagem do Amazon

1. Veja as listagens de produtos no [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) guia .

1. Encontre a listagem que deseja criar no [!DNL Commerce] catálogo, clique em **[!UICONTROL Select]** no _[!UICONTROL Action]_e clique em **[!UICONTROL Create New Catalog Product]**.

   Essa ação abre o _[!UICONTROL Create Magento Catalog Product]_página.

1. Preencha as configurações de catálogo do produto.

   - Definir **[!UICONTROL Enable Product(s)]** alternar para `Yes` ou `No` (obrigatório).

      |Sim|Escolha tornar o produto qualificado para o seu [!DNL Commerce] vendas da loja.| |Não|Escolha tornar o produto inelegível para o seu [!DNL Commerce] vendas da loja.|

   - Para **[!UICONTROL Categories]**, atribua uma categoria ao produto (opcional).

      Para selecionar a categoria do produto, clique na seta para baixo e marque uma caixa de seleção de categoria. Clique em **[!UICONTROL Done]** quando terminar.

   - Para **[!UICONTROL Website Ids]**, escolha o site (loja) para o qual o produto será associado.

      As opções desta lista dependem do [!DNL Commerce] [configuração de armazenamento](https://docs.magento.com/user-guide/stores/websites-stores-views.html)Configurações {target=&quot;_blank&quot;}.

   - Para **[!UICONTROL Attribute Set Id]** (obrigatório), escolha uma opção.

      `Default` é a seleção padrão. As opções desta lista dependem do [!DNL Commerce] [conjuntos de atributos](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;} você configurou.

   - Para **[!UICONTROL Visibility]**, escolha uma opção para o novo produto.

      |**[!UICONTROL Not Visible Individually]** (padrão)|O produto não está incluído nas listas de vitrine, embora possa estar disponível como uma variação de outro produto.| |**[!UICONTROL Catalog]**|O produto aparece nas listagens do catálogo.| |**[!UICONTROL Search]**|O produto está disponível para operações de pesquisa.| |**[!UICONTROL Catalog and Search]**|O produto está incluído nas listas de catálogos e disponível para operações de pesquisa.|

   - Para **[!UICONTROL Assign Tax Class]**, escolha uma opção para o produto.

      As opções exibidas nessa lista dependem do [classes fiscais](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;} você configurou.

   - Ao concluir, clique em **[!UICONTROL Create Catalog Products]**.

O produto do catálogo é criado em seu [!DNL Commerce] e atribuído à listagem do Amazon a partir da qual foi criado. Com a listagem agora correspondendo a uma listagem existente do Amazon, a listagem é removida do _[!UICONTROL New Third Party]_e aparecerão na guia_[!UICONTROL Active]_ guia .

## Criar vários produtos de catálogo usando suas informações de listagem do Amazon

1. Veja as listagens de produtos no [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) guia .

1. Selecione as listagens para as quais criar produtos de catálogo.

   Você pode marcar caixas de seleção individuais na coluna do lado esquerdo, ou pode clicar na seta para baixo na coluna superior esquerda e escolher **[!UICONTROL Select All]** ou **[!UICONTROL Select All on this Page]**.

1. Em _[!UICONTROL Actions]_, clique em **[!UICONTROL Create New Catalog Product(s)]**.

1. Para aceitar a mensagem de confirmação e abrir o _[!UICONTROL Create Magento Catalog Product]_página, clique em **[!UICONTROL OK]**.

1. Preencha as configurações de catálogo dos produtos.

   >[!NOTE]
   >Ao criar produtos de catálogo para várias listagens selecionadas, as configurações de produto inseridas são aplicadas a todas as listagens.

   - Definir **[!UICONTROL Enable Product(s)]** alternar para `Yes` ou `No` (obrigatório).

      |Sim|Escolha tornar o produto qualificado para o seu [!DNL Commerce] vendas da loja.| |Não|Escolha tornar o produto inelegível para o seu [!DNL Commerce] vendas da loja.|

   - Para **[!UICONTROL Categories]**, atribua uma categoria ao produto (opcional).

      Para selecionar a categoria do produto, clique na seta para baixo e marque uma caixa de seleção de categoria. Clique em **Concluído** quando terminar.

   - Para **[!UICONTROL Website Ids]**, escolha o site (loja) para o qual o produto será associado.

      As opções desta lista dependem do [!DNL Commerce] [configuração de armazenamento](https://docs.magento.com/user-guide/stores/websites-stores-views.html)Configurações {target=&quot;_blank&quot;}.

   - Para **[!UICONTROL Attribute Set Id]** (obrigatório), escolha uma opção.

      `Default` é a seleção padrão. As opções desta lista dependem do [!DNL Commerce] [conjuntos de atributos](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;} você configurou.

   - Para **[!UICONTROL Visibility]**, escolha uma opção para o novo produto.

      |**[!UICONTROL Not Visible Individually]** (padrão)|O produto não está incluído nas listas de vitrine, embora possa estar disponível como uma variação de outro produto.| |**[!UICONTROL Catalog]**|O produto aparece nas listagens do catálogo.| |**[!UICONTROL Search]**|O produto está disponível para operações de pesquisa.| |**[!UICONTROL Catalog and Search]**|O produto está incluído nas listas de catálogos e disponível para operações de pesquisa.|

   - Para **[!UICONTROL Assign Tax Class]**, escolha uma opção para o produto.

      As opções exibidas nessa lista dependem do [classes fiscais](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;} você configurou.

   - Ao concluir, clique em **[!UICONTROL Create Catalog Products]**.

Os produtos do catálogo são criados em [!DNL Commerce] e atribuído à listagem do Amazon a partir da qual foi criado. Com as listagens agora correspondendo às respectivas listagens do Amazon, elas são removidas do [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) e aparecerão na guia [_[!UICONTROL Active]_](./active-listings.md) guia .

![Criar produto de catálogo do Commerce](assets/amazon-magento-catalog-product.png)

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Enable Product(s)] | (Obrigatório) Se estiver habilitado, o produto estará visível em sua [!DNL Commerce] loja. Se estiver desativado, o produto não será exibido no [!DNL Commerce] loja. |
| [!UICONTROL Categories] | É possível inserir o nome da categoria do novo produto ou selecionar uma categoria clicando na seta para baixo para exibir as opções. As opções dependem do [categorias](https://docs.magento.com/user-guide/catalog/category-create.html)Configuração {target=&quot;_blank&quot;}. |
| [!UICONTROL Website Ids] | (Obrigatório) Escolha o site (loja) para o qual o produto será associado. As opções dependem do [!DNL Commerce] [configuração de armazenamento](https://docs.magento.com/user-guide/stores/websites-stores-views.html)configurações {target=&quot;_blank&quot;} |
| ID do conjunto de atributos | Escolha um conjunto de atributos. As opções dependem do [!DNL Commerce] [conjuntos de atributos](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;}. |
| [!UICONTROL Visibility] | Opções:<ul><li>**[!UICONTROL Not Visible Individually]** - O produto não está visível no seu [!DNL Commerce] storefront (mais comum em produtos variantes).</li><li>**[!UICONTROL Catalog]** - Permite que o produto seja acessado por meio da categoria à qual está associado no site.</li><li>**Pesquisar** - Permite que o produto seja encontrado somente por meio da ferramenta de pesquisa.</li><li>**[!UICONTROL Catalog and Search]** - Permite que os produtos sejam acessados por meio da estrutura de categoria e com o uso da ferramenta de pesquisa.</li></ul> |
| [!UICONTROL Assign Tax Class] | Atribua uma classe de imposto ao novo produto. As opções dependem do [classes fiscais](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;}. |
