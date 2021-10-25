---
title: Criar e editar atributos
description: O Amazon Sales Channel fornece a visualização Atributos para ajudar você a revisar os atributos atuais do Amazon e os atributos vinculados do Commerce.
exl-id: 3cd5fb7e-68a3-45fd-8f50-72d3cc0244b5
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '1063'
ht-degree: 0%

---

# Criar e editar atributos

Criar ou atualizar [!DNL Commerce] atributos à medida que você vende por meio da Amazon e atualiza suas lojas. Revise os atributos atuais do Amazon e os links [!DNL Commerce] atributos por meio da [_[!UICONTROL Attributes]_exibir](./attributes-view.md) da página inicial do canal de vendas da Amazon. O_[!UICONTROL Action]_ mostra as ações disponíveis para o atributo. Você pode criar e mapear um novo [!DNL Commerce] para um atributo do Amazon desvinculado, ou você pode editar um atributo existente [!DNL Commerce] e seu mapeamento para um atributo do Amazon.

À medida que você cria e atualiza atributos, talvez queira verificar os valores do atributo para [!DNL Commerce] e produtos Amazon. Esses valores podem ser diferentes se você não sincronizar e importar valores do Amazon. Para revisar os valores do Amazon para esses atributos, consulte [Revisar o mapeamento de atributos do Amazon](./amazon-matching-attributes-values.md). Se quiser alterar esses valores, poderá [editar ou criar um mapeamento](./amazon-manually-update-incomplete-listing.md) entre a Amazon e [!DNL Commerce].

## Criar um atributo {#create-an-attribute}

Essas etapas criam uma [!DNL Commerce] e mapeá-lo para um atributo do Amazon. Dependendo das configurações, os valores podem iniciar a sincronização entre catálogos.

1. No _Administrador_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Clique em **[!UICONTROL Attributes]** no menu à esquerda, localize um atributo do Amazon e clique em **[!UICONTROL Create Attribute]** no _[!UICONTROL Action]_coluna.

1. Para habilitar a sincronização dos valores do Amazon com o link [!DNL Commerce] atributo, conjunto **[!UICONTROL Is Active]** para `Yes`.

   Quando definido como `Yes`, os valores são sincronizados de acordo com sua configuração.

1. Choose `Create New Magento Attribute` para **[!UICONTROL Select Magento Product Attribute]**.

   O atributo mapeia para o **[!UICONTROL Amazon Attribute Name]**.

1. Insira um **[!UICONTROL Magento Product Attribute Name]**.

1. Insira um **[!UICONTROL Magento Product Attribute Code]**.

   Esse valor deve estar em letras minúsculas sem espaços.

1. Para **[!UICONTROL Attribute Set Ids]**, escolha um Conjunto de atributos a ser atribuído.

   Normalmente, os atributos são parte de um conjunto de atributos, como um conjunto para cores que têm atributos para azul, verde, amarelo e vermelho.

1. Para **[!UICONTROL Type]**, escolha o tipo do valor do atributo, como texto e números.

   Essa opção afeta o valor permitido para o atributo.

1. Para **[!UICONTROL Use for Promo Rule Conditions]**, defina como `Yes` para permitir que o atributo fique disponível para um parâmetro em suas condições promocionais.

1. Para **[!UICONTROL Used in Search]**, defina como `Yes` se o atributo e o valor puderem ser usados em pesquisas de produtos.

1. Para **[!UICONTROL Comparable on Storefront]**, defina como `Yes` se o valor do atributo puder ser usado na funcionalidade &quot;Comparar por&quot; do Amazon.

1. Escolha a [!DNL Commerce] [escopo](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;} para o atributo e, em seguida, selecione uma ou mais Exibições da loja para importar os valores do Amazon.

   Se o escopo estiver definido como `Global`, o _[!UICONTROL Store View]_não pode ser alterado após a criação do atributo.

   Se você escolher `All Store Views (Global)`, sincroniza e salva valores em todas as exibições da loja da Amazon. Você pode querer sincronizar apenas valores para exibições de loja específicas.

1. Ao concluir, clique em **[!UICONTROL Save Attribute Settings]**.

Depois de salvar, você pode editar o atributo para revisar as configurações e o Amazon correspondente e [!DNL Commerce] para o atributo. Também é possível indicar se os valores do Amazon devem substituir [!DNL Commerce] valores.

![criar configurações do atributo](assets/amazon-attribute-settings-create.png)

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Is Active] | Indica se esse atributo está ativo e se sincroniza ativamente entre o Amazon e a [!DNL Commerce]. Defina como `Yes` para garantir os valores de atributo do Amazon e [!DNL Commerce] manter-se sincronizado para o atributo selecionado. |
| Selecione Atributo do produto Magento | Indica o atributo selecionado que você deseja vincular ao Nome de Atributo do Amazon listado. Ao criar um atributo, escolha `Create New Magento Attribute`. |
| [!UICONTROL Amazon Attribute Name] | Mostra o nome do atributo Amazon escolhido. O atributo selecionado vincula a este atributo do Amazon. Não é possível editar esse valor por meio de [!DNL Commerce]. |
| [!UICONTROL Magento Product Attribute Name] | Indica o nome do atributo ou &quot;rótulo&quot;. |
| [!UICONTROL Magento Product Attribute Code] | Indica o código do atributo, tudo em caracteres em minúsculas sem espaços. |
| [!UICONTROL Attribute Set Ids] | Indica o Conjunto de Atributos ao qual o atributo será atribuído. Os atributos tendem a fazer parte de um conjunto de atributos, como um conjunto para cores que têm atributos para azul, verde, amarelo e vermelho. |
| [!UICONTROL Type] | Indica o tipo de valor do valor do atributo, como texto e números. A seleção afeta o valor permitido para o atributo. |
| [!UICONTROL Use for Promo Rule Conditions] | Alternar para `Yes` para permitir que o atributo fique disponível para um parâmetro em suas condições promocionais. |
| [!UICONTROL Used in Search] | Indica se o atributo e o valor podem ser usados em pesquisas de produtos. |
| [!UICONTROL Comparable on Storefront] | Indica se o valor do atributo pode ser usado na funcionalidade &quot;Comparar por&quot; do Amazon. |
| [!UICONTROL Magento Product Attribute Scope] | Indica o [escopo](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;} para o atributo . Opções: Exibição global / de loja<br>Quando definido como `Global`, a Exibição de loja não pode ser editada depois que o atributo é criado. |
| [!UICONTROL Store Views (to import values into to)] | Aparece apenas quando o escopo é definido como `Store View`. Escolha a [exibição de loja](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;} ao qual os valores de atributo do Amazon são sincronizados. Escolha `All Store Views (Global)` atualiza o valor em todos [!DNL Commerce] visualizações de loja. |

## Editar um atributo {#edit-an-attribute}

1. No _Administrador_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Clique em **[!UICONTROL Attributes]** no menu à esquerda, localize um atributo do Amazon e clique em **[!UICONTROL Edit]** no _[!UICONTROL Action]_coluna.

1. Para ativar ou desativar a sincronização dos valores do Amazon com o link [!DNL Commerce] atributo, conjunto **Está ativo** para `Yes` ou `No`.

   Quando definido como `Yes`, os valores são sincronizados de acordo com sua configuração.

1. Para **[!UICONTROL Select Magento Product Attribute]**, verifique ou atualize o atributo para mapear para o **[!UICONTROL Amazon Attribute Name]**.

1. Indique se deseja que o valor de atributo de entrada do Amazon substitua o valor de atributo existente.

   Por exemplo, talvez você não queira substituir os preços da Amazon em [!DNL Commerce].

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]** - Mantém o valor, mantendo valores diferentes para a [!DNL Commerce] e lojas Amazon.

   - **[!UICONTROL Overwrite Existing Magento Values]** - Substitui o valor no [!DNL Commerce] catálogo de produtos com o valor de entrada do Amazon.

1. Se disponível para edição, escolha um ou mais **[!UICONTROL Store Views (to import Amazon values into)]**.

   Se o atributo foi criado com um `Global` , o _Exibição da loja_ não pode ser alterado após a criação do atributo.

   Se você escolher `All Store Views (Global)`, sincroniza e salva valores em todas as exibições de loja. Você pode querer sincronizar apenas valores para exibições de loja específicas.

1. Ao concluir, clique em **[!UICONTROL Save Attribute Settings]**.

![editar configurações do atributo](assets/amazon-attribute-settings-edit.png)

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Is Active] | Indica se esse atributo está ativo e se sincroniza ativamente entre o Amazon e a [!DNL Commerce]. Defina como `Yes` para garantir os valores de atributo do Amazon e [!DNL Commerce] manter-se sincronizado para o atributo selecionado. |
| [!UICONTROL Select Magento Product Attribute] | Indica o [!DNL Commerce] que você deseja vincular ao Nome de atributo do Amazon listado. Se desejar alterar o [!DNL Commerce] , escolha um atributo diferente na lista suspensa. Os valores são sincronizados de acordo com as configurações. |
| [!UICONTROL Amazon Attribute Name] | Mostra o nome do atributo Amazon, conforme definido em [!DNL Amazon Seller Central]. O [!DNL Commerce] links de atributo para este atributo do Amazon. Não é possível editar esse valor por meio de [!DNL Commerce]. |
| [!UICONTROL Overwrite Existing Value] | Indica se os valores de atributo do Amazon substituem os existentes [!DNL Commerce] , afetando todos os produtos com essa [!DNL Commerce] atributo.<ul><li>**Não substitua os valores de Magento existentes** - (Padrão) Retém o valor [!DNL Commerce] , mantendo valores diferentes para [!DNL Commerce] e lojas Amazon.</li><li>**Substituir valores de Magento existentes** - Salva o valor do Amazon sobre o [!DNL Commerce] na variável [!DNL Commerce] catálogo de produtos.</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | Não aparece ao editar um atributo se ele foi criado com o `Global` escopo. Indica o [!DNL Commerce] [escopo](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;} foi criado e definido como `Store View`. |
| [!UICONTROL Store Views (to import values into to)] | Escolha sua [!DNL Commerce] [exibição de loja](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;} para o qual sincronizar os valores de atributo do Amazon. Escolha `All Store Views (Global)` atualiza o valor em todas as exibições de loja. |
