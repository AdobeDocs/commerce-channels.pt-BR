---
title: Criar e editar atributos para o canal de vendas do Amazon
description: O Amazon Sales Channel fornece a visualização Atributos para ajudá-lo a revisar os atributos atuais do Amazon e os atributos vinculados do Commerce.
feature: Sales Channels, Products, Configuration
exl-id: 3cd5fb7e-68a3-45fd-8f50-72d3cc0244b5
source-git-commit: b2e608a633b760672044653a22be757ecffc9540
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# Criar e editar atributos

Crie ou atualize os atributos do [!DNL Commerce] à medida que você vende pela Amazon e atualiza suas lojas. Revise os atributos atuais do Amazon e os atributos [!DNL Commerce] vinculados por meio da [_[!UICONTROL Attributes]_visualização](./attributes-view.md) da home page do canal de vendas do Amazon. A coluna_[!UICONTROL Action]_ mostra as ações disponíveis para o atributo. Você pode criar e mapear um novo atributo do [!DNL Commerce] para um atributo do Amazon desvinculado ou editar um atributo existente do [!DNL Commerce] e seu mapeamento para um atributo do Amazon.

À medida que você cria e atualiza atributos, convém verificar os valores de atributo para os produtos [!DNL Commerce] e Amazon. Esses valores podem ser diferentes se você não sincronizar e importar valores do Amazon. Para revisar os valores de Amazon para esses atributos, consulte [Revisão do Mapeamento de Atributos do Amazon](./amazon-matching-attributes-values.md). Se quiser alterar esses valores, você pode [editar ou criar um mapeamento](./amazon-manually-update-incomplete-listing.md) entre o Amazon e [!DNL Commerce].

## Criar um atributo {#create-an-attribute}

Essas etapas criam um atributo [!DNL Commerce] e o mapeiam para um atributo Amazon. Dependendo das configurações, os valores podem começar a sincronizar entre catálogos.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Clique em **[!UICONTROL Attributes]** no menu do lado esquerdo, localize um atributo do Amazon e clique em **[!UICONTROL Create Attribute]** na coluna _[!UICONTROL Action]_.

1. Para habilitar a sincronização dos valores de Amazon com o atributo [!DNL Commerce] vinculado, defina **[!UICONTROL Is Active]** como `Yes`.

   Quando definido como `Yes`, os valores são sincronizados de acordo com sua configuração.

1. Escolha `Create New Magento Attribute` para **[!UICONTROL Select Magento Product Attribute]**.

   O atributo mapeia para o atributo escolhido para **[!UICONTROL Amazon Attribute Name]**.

1. Insira um **[!UICONTROL Magento Product Attribute Name]**.

1. Insira um **[!UICONTROL Magento Product Attribute Code]**.

   Esse valor deve estar em minúsculas sem espaços.

1. Para **[!UICONTROL Attribute Set Ids]**, escolha um Conjunto de Atributos a ser atribuído.

   Normalmente, os atributos fazem parte de um conjunto de atributos, como um conjunto de cores com atributos para azul, verde, amarelo e vermelho.

1. Para **[!UICONTROL Type]**, escolha o tipo do valor do atributo, como texto e números.

   Essa opção afeta o valor permitido para o atributo.

1. Para **[!UICONTROL Use for Promo Rule Conditions]**, defina como `Yes` para permitir que o atributo esteja disponível para um parâmetro em suas condições promocionais.

1. Para **[!UICONTROL Used in Search]**, defina como `Yes` se o atributo e o valor puderem ser usados em pesquisas de produtos.

1. Para **[!UICONTROL Comparable on Storefront]**, defina como `Yes` se o valor do atributo puder ser usado na funcionalidade &quot;Comparar por&quot; do Amazon.

1. Escolha o [!DNL Commerce] [escopo](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) para o atributo e selecione um ou mais Modos de Exibição de Armazenamento para os quais importar valores do Amazon.

   Se o escopo estiver definido como `Global`, _[!UICONTROL Store View]_não poderá ser alterado após a criação do atributo.

   Se você escolher `All Store Views (Global)`, ele será sincronizado e salvará valores em todas as suas exibições de loja da Amazon. Talvez você queira sincronizar valores somente para exibições de loja específicas.

1. Quando terminar, clique em **[!UICONTROL Save Attribute Settings]**.

Depois de salvar, talvez você queira editar o atributo para revisar as configurações e corresponder a Amazon e a [!DNL Commerce] valores para o atributo. Você também pode indicar se os valores de Amazon devem substituir [!DNL Commerce] valores.

![criar configurações de atributo](assets/amazon-attribute-settings-create.png){width="600" zoomable="yes"}

| Campo | Descrição |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | Indica se este atributo está ativo e sincroniza ativamente entre o Amazon e o [!DNL Commerce]. Defina como `Yes` para garantir que os valores de atributo do Amazon e [!DNL Commerce] permaneçam sincronizados para o atributo selecionado. |
| Selecionar atributo de produto do Magento | Indica o atributo selecionado que você deseja vincular ao Nome de atributo do Amazon listado. Ao criar um atributo, escolha `Create New Magento Attribute`. |
| [!UICONTROL Amazon Attribute Name] | Mostra o nome do atributo do Amazon que você escolheu. O atributo selecionado é vinculado a este atributo do Amazon. Você não pode editar este valor até [!DNL Commerce]. |
| [!UICONTROL Magento Product Attribute Name] | Indica o nome do atributo ou &quot;rótulo&quot;. |
| [!UICONTROL Magento Product Attribute Code] | Indica o código do atributo, tudo em caracteres minúsculos sem espaços. |
| [!UICONTROL Attribute Set Ids] | Indica o Conjunto de Atributos ao qual atribuir o atributo. Os atributos tendem a fazer parte de um conjunto de atributos, como um conjunto para cores com atributos para azul, verde, amarelo e vermelho. |
| [!UICONTROL Type] | Indica o tipo de valor do valor do atributo, como texto e números. A seleção afeta o valor permitido para o atributo. |
| [!UICONTROL Use for Promo Rule Conditions] | Alterne para `Yes` para permitir que o atributo esteja disponível para um parâmetro em suas condições promocionais. |
| [!UICONTROL Used in Search] | Indica se o atributo e o valor podem ser usados em pesquisas de produtos. |
| [!UICONTROL Comparable on Storefront] | Indica se o valor do atributo pode ser usado na funcionalidade &quot;Comparar por&quot; do Amazon. |
| [!UICONTROL Magento Product Attribute Scope] | Indica o [escopo](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) do atributo. Opções: Exibição Global/de Loja<br>Quando definida como `Global`, a Exibição de Loja não poderá ser editada após a criação do atributo. |
| [!UICONTROL Store Views (to import values into to)] | Aparece somente quando o escopo está definido como `Store View`. Escolha a [exibição de repositório](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) para a qual os valores de atributo do Amazon são sincronizados. Escolher `All Store Views (Global)` atualiza o valor em todas as [!DNL Commerce] exibições de armazenamento. |

## Editar um atributo {#edit-an-attribute}

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Clique em **[!UICONTROL Attributes]** no menu do lado esquerdo, localize um atributo do Amazon e clique em **[!UICONTROL Edit]** na coluna _[!UICONTROL Action]_.

1. Para habilitar ou desabilitar a sincronização dos valores de Amazon para o atributo [!DNL Commerce] vinculado, defina **Está Ativo** para `Yes` ou `No`.

   Quando definido como `Yes`, os valores são sincronizados de acordo com sua configuração.

1. Para **[!UICONTROL Select Magento Product Attribute]**, verifique ou atualize o atributo para mapear para o **[!UICONTROL Amazon Attribute Name]** escolhido.

1. Indique se deseja que o valor de atributo de entrada do Amazon substitua o valor de atributo existente.

   Por exemplo, talvez você não queira substituir os preços do Amazon em [!DNL Commerce].

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]** - Retém o valor, mantendo valores diferentes para seus armazenamentos [!DNL Commerce] e Amazon.

   - **[!UICONTROL Overwrite Existing Magento Values]** - Substitui o valor no catálogo de produtos [!DNL Commerce] pelo valor de entrada do Amazon.

1. Se estiver disponível para edição, escolha um ou mais **[!UICONTROL Store Views (to import Amazon values into)]**.

   Se o atributo foi criado com um escopo `Global`, a _Exibição de Repositório_ não poderá ser alterada após a criação do atributo.

   Se você escolher `All Store Views (Global)`, ele sincroniza e salva valores em todas as exibições de loja. Talvez você queira sincronizar valores somente para exibições de loja específicas.

1. Quando terminar, clique em **[!UICONTROL Save Attribute Settings]**.

![editar configurações de atributo](assets/amazon-attribute-settings-edit.png){width="600" zoomable="yes"}

| Campo | Descrição |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | Indica se este atributo está ativo e sincroniza ativamente entre o Amazon e o [!DNL Commerce]. Defina como `Yes` para garantir que os valores de atributo do Amazon e [!DNL Commerce] permaneçam sincronizados para o atributo selecionado. |
| [!UICONTROL Select Magento Product Attribute] | Indica o atributo [!DNL Commerce] selecionado que você deseja vincular ao Nome de Atributo Amazon listado. Se quiser alterar o atributo [!DNL Commerce] vinculado, escolha um atributo diferente na lista suspensa. Os valores são sincronizados de acordo com as configurações. |
| [!UICONTROL Amazon Attribute Name] | Mostra o nome do atributo Amazon conforme definido em [!DNL Amazon Seller Central]. O atributo [!DNL Commerce] selecionado está vinculado a este atributo Amazon. Você não pode editar este valor até [!DNL Commerce]. |
| [!UICONTROL Overwrite Existing Value] | Indica se os valores do atributo Amazon substituem os valores [!DNL Commerce] existentes, afetando todos os produtos com esse atributo [!DNL Commerce].<ul><li>**Não Substituir Valores de Magento Existentes** - (Padrão) Retém o valor [!DNL Commerce], mantendo valores diferentes para [!DNL Commerce] e armazenamentos Amazon.</li><li>**Substituir valores de Magento existentes** - Salva o valor de Amazon sobre o valor de [!DNL Commerce] no catálogo de produtos [!DNL Commerce].</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | Não aparece ao editar um atributo se o atributo foi criado com o escopo `Global`. Indica que o [!DNL Commerce] [escopo](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) foi criado e definido como `Store View`. |
| [!UICONTROL Store Views (to import values into to)] | Escolha sua [!DNL Commerce] [exibição de repositório](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) para a qual sincronizar os valores de atributo do Amazon. Escolher `All Store Views (Global)` atualiza o valor em todas as exibições de loja. |
