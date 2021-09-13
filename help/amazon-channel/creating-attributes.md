---
title: Criar e editar atributos
description: O Amazon Sales Channel fornece a visualização Atributos para ajudar você a revisar os atributos atuais do Amazon e os atributos vinculados do Commerce.
exl-id: 3cd5fb7e-68a3-45fd-8f50-72d3cc0244b5
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Criar e editar atributos

Crie ou atualize atributos [!DNL Commerce] à medida que você vende por meio do Amazon e atualize suas lojas. Revise os atributos atuais do Amazon e os atributos [!DNL Commerce] vinculados por meio da [_[!UICONTROL Attributes]_visualização](./attributes-view.md) da home page do canal de vendas do Amazon. A coluna_[!UICONTROL Action]_ mostra as ações disponíveis para o atributo. Você pode criar e mapear um novo atributo [!DNL Commerce] para um atributo Amazon desvinculado, ou pode editar um atributo [!DNL Commerce] existente e seu mapeamento para um atributo Amazon.

À medida que você cria e atualiza atributos, pode querer verificar os valores do atributo para [!DNL Commerce] e produtos do Amazon. Esses valores podem ser diferentes se você não sincronizar e importar valores do Amazon. Para revisar os valores do Amazon para esses atributos, consulte [Revisando o Mapeamento de Atributos do Amazon](./amazon-matching-attributes-values.md). Se quiser alterar esses valores, você poderá [editar ou criar um mapeamento](./amazon-manually-update-incomplete-listing.md) entre Amazon e [!DNL Commerce].

## Criar um atributo {#create-an-attribute}

Essas etapas criam um atributo [!DNL Commerce] e o mapeiam para um atributo do Amazon. Dependendo das configurações, os valores podem iniciar a sincronização entre catálogos.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Clique em **[!UICONTROL Attributes]** no menu à esquerda, localize um atributo Amazon e clique em **[!UICONTROL Create Attribute]** na coluna _[!UICONTROL Action]_.

1. Para habilitar a sincronização dos valores do Amazon com o atributo [!DNL Commerce] vinculado, defina **[!UICONTROL Is Active]** como `Yes`.

   Quando definido como `Yes`, os valores são sincronizados de acordo com sua configuração.

1. Escolha `Create New Magento Attribute` para **[!UICONTROL Select Magento Product Attribute]**.

   O atributo mapeia para o escolhido para **[!UICONTROL Amazon Attribute Name]**.

1. Insira um **[!UICONTROL Magento Product Attribute Name]**.

1. Insira um **[!UICONTROL Magento Product Attribute Code]**.

   Esse valor deve estar em letras minúsculas sem espaços.

1. Para **[!UICONTROL Attribute Set Ids]**, escolha um Conjunto de Atributos a ser atribuído.

   Normalmente, os atributos são parte de um conjunto de atributos, como um conjunto para cores que têm atributos para azul, verde, amarelo e vermelho.

1. Para **[!UICONTROL Type]**, escolha o tipo do valor do atributo, como texto e números.

   Essa opção afeta o valor permitido para o atributo.

1. Para **[!UICONTROL Use for Promo Rule Conditions]**, defina como `Yes` para permitir que o atributo fique disponível para um parâmetro em suas condições promocionais.

1. Para **[!UICONTROL Used in Search]**, defina como `Yes` se o atributo e o valor puderem ser usados em pesquisas de produtos.

1. Para **[!UICONTROL Comparable on Storefront]**, defina como `Yes` se o valor do atributo puder ser usado na funcionalidade &quot;Comparar por&quot; do Amazon.

1. Escolha o [!DNL Commerce] [escopo](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;} para o atributo e selecione uma ou mais Exibições de armazenamento para importar valores de Amazon.

   Se o escopo estiver definido como `Global`, _[!UICONTROL Store View]_não poderá ser alterado depois que o atributo for criado.

   Se você escolher `All Store Views (Global)`, ele sincronizará e salvará valores em todas as exibições de loja da Amazon. Você pode querer sincronizar apenas valores para exibições de loja específicas.

1. Quando terminar, clique em **[!UICONTROL Save Attribute Settings]**.

Depois de salvar, você pode editar o atributo para revisar as configurações e os valores Amazon e [!DNL Commerce] correspondentes para o atributo. Você também pode indicar se os valores de Amazon devem substituir [!DNL Commerce] valores.

![criar configurações do atributo](assets/amazon-attribute-settings-create.png)

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Is Active] | Indica se esse atributo está ativo e sincroniza ativamente entre o Amazon e [!DNL Commerce]. Defina como `Yes` para garantir que os valores de atributo do Amazon e [!DNL Commerce] permaneçam sincronizados para o atributo selecionado. |
| Selecione Atributo do produto Magento | Indica o atributo selecionado que você deseja vincular ao Nome de Atributo do Amazon listado. Ao criar um atributo, escolha `Create New Magento Attribute`. |
| [!UICONTROL Amazon Attribute Name] | Mostra o nome do atributo Amazon escolhido. O atributo selecionado vincula a este atributo do Amazon. Não é possível editar esse valor por meio de [!DNL Commerce]. |
| [!UICONTROL Magento Product Attribute Name] | Indica o nome do atributo ou &quot;rótulo&quot;. |
| [!UICONTROL Magento Product Attribute Code] | Indica o código do atributo, tudo em caracteres em minúsculas sem espaços. |
| [!UICONTROL Attribute Set Ids] | Indica o Conjunto de Atributos ao qual o atributo será atribuído. Os atributos tendem a fazer parte de um conjunto de atributos, como um conjunto para cores que têm atributos para azul, verde, amarelo e vermelho. |
| [!UICONTROL Type] | Indica o tipo de valor do valor do atributo, como texto e números. A seleção afeta o valor permitido para o atributo. |
| [!UICONTROL Use for Promo Rule Conditions] | Alterne para `Yes` para permitir que o atributo fique disponível para um parâmetro em suas condições promocionais. |
| [!UICONTROL Used in Search] | Indica se o atributo e o valor podem ser usados em pesquisas de produtos. |
| [!UICONTROL Comparable on Storefront] | Indica se o valor do atributo pode ser usado na funcionalidade &quot;Comparar por&quot; do Amazon. |
| [!UICONTROL Magento Product Attribute Scope] | Indica o [escopo](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;} para o atributo. Opções: Exibição global / de armazenamento<br>Quando definido como `Global`, a Exibição de armazenamento não pode ser editada após a criação do atributo. |
| [!UICONTROL Store Views (to import values into to)] | Aparece apenas quando o escopo está definido como `Store View`. Escolha o [modo de exibição de armazenamento](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;} para o qual os valores de atributo do Amazon são sincronizados. Escolher `All Store Views (Global)` atualiza o valor em todas as exibições de armazenamento [!DNL Commerce]. |

## Editar um atributo {#edit-an-attribute}

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Clique em **[!UICONTROL Attributes]** no menu à esquerda, localize um atributo Amazon e clique em **[!UICONTROL Edit]** na coluna _[!UICONTROL Action]_.

1. Para habilitar ou desabilitar a sincronização dos valores do Amazon com o atributo [!DNL Commerce] vinculado, defina **Está ativo** como `Yes` ou `No`.

   Quando definido como `Yes`, os valores são sincronizados de acordo com sua configuração.

1. Para **[!UICONTROL Select Magento Product Attribute]**, verifique ou atualize o atributo para mapear para o **[!UICONTROL Amazon Attribute Name]** escolhido.

1. Indique se deseja que o valor de atributo de entrada do Amazon substitua o valor de atributo existente.

   Por exemplo, talvez você não queira substituir os preços do Amazon em [!DNL Commerce].

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]** - Retém o valor, mantendo valores diferentes para as lojas do  [!DNL Commerce] e do Amazon.

   - **[!UICONTROL Overwrite Existing Magento Values]** - Substitui o valor no catálogo de  [!DNL Commerce] produtos pelo valor de entrada do Amazon.

1. Se disponível para edição, escolha um ou mais **[!UICONTROL Store Views (to import Amazon values into)]**.

   Se o atributo tiver sido criado com um escopo `Global`, a _Exibição de armazenamento_ não poderá ser alterada após a criação do atributo.

   Se você escolher `All Store Views (Global)`, ele sincronizará e salvará valores em todas as exibições de armazenamento. Você pode querer sincronizar apenas valores para exibições de loja específicas.

1. Quando terminar, clique em **[!UICONTROL Save Attribute Settings]**.

![editar configurações do atributo](assets/amazon-attribute-settings-edit.png)

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Is Active] | Indica se esse atributo está ativo e sincroniza ativamente entre o Amazon e [!DNL Commerce]. Defina como `Yes` para garantir que os valores de atributo do Amazon e [!DNL Commerce] permaneçam sincronizados para o atributo selecionado. |
| [!UICONTROL Select Magento Product Attribute] | Indica o atributo [!DNL Commerce] selecionado que você deseja vincular ao Nome de Atributo do Amazon listado. Se quiser alterar o atributo [!DNL Commerce] vinculado, escolha um atributo diferente na lista suspensa. Os valores são sincronizados de acordo com as configurações. |
| [!UICONTROL Amazon Attribute Name] | Mostra o nome do atributo Amazon, conforme definido em [!DNL Amazon Seller Central]. O atributo [!DNL Commerce] selecionado vincula a este atributo do Amazon. Não é possível editar esse valor por meio de [!DNL Commerce]. |
| [!UICONTROL Overwrite Existing Value] | Indica se os valores do atributo do Amazon substituem os valores [!DNL Commerce] existentes, afetando todos os produtos com esse atributo [!DNL Commerce].<ul><li>**Do Not Overwrite Existing Magento Values**  - (Padrão) Mantém o  [!DNL Commerce] valor, mantendo valores diferentes para  [!DNL Commerce] e lojas Amazon.</li><li>**Substituir valores Magento existentes**  - salva o valor Amazon sobre o  [!DNL Commerce] valor no catálogo de  [!DNL Commerce] produtos.</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | Não aparece ao editar um atributo se ele foi criado com o escopo `Global`. Indica que [!DNL Commerce] [escopo](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;} foi criado e definido como `Store View`. |
| [!UICONTROL Store Views (to import values into to)] | Escolha o [!DNL Commerce] [modo de exibição de armazenamento](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;} para o qual sincronizar os valores de atributo do Amazon. Escolher `All Store Views (Global)` atualiza o valor em todas as exibições de loja. |
