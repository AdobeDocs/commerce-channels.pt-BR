---
title: Ações das Regras de Preço Padrão
description: Use as ações de regra de preço padrão para aumentar ou diminuir um preço de listagem da Amazon em relação ao preço do catálogo do Commerce (ou fonte de preço).
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Ações das regras de preço padrão

Uma ação de regra de preço padrão permite aumentar ou diminuir um preço de listagem da Amazon em uma porcentagem específica ou valor fixo do dólar em relação ao preço do catálogo [!DNL Commerce] (ou fonte de preço).

As seções de uma ação de regra de preço padrão incluem:

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## Configurar ações de regra de preço

1. Para **[!UICONTROL Rule Type]**, escolha `Standard price rule`.

   Essa opção desativa os outros campos na seção _[!UICONTROL Select Rule Type]_.

1. Expanda a seção _[!UICONTROL Price Adjustment]_, se necessário.

1. Para **[!UICONTROL Price Action]**, escolha uma opção para determinar como você deseja alterar o valor *[!UICONTROL Magento Price Source]* (definido em seu valor [Preço de Listagem](./listing-price.md)).

   - `Decrease By` - Escolha quando deseja que o valor seja diminuído antes de listar para o Amazon.

   - `Increase By` - Escolha quando deseja aumentar o valor antes de listar o Amazon.

1. Para **[!UICONTROL Apply]**, escolha uma opção e uma opção para determinar como você deseja que o *[!UICONTROL Magento Price Source]* definido em seu valor [Preço de Listagem](./listing-price.md) seja ajustado:

   - `Apply as percentage` - Escolha quando deseja que o valor definido  *[!UICONTROL Magento Price Source]* na  [Lista de ](./listing-price.md) Preços seja ajustado por uma porcentagem

   - `Apply as fixed amount` - Escolha quando deseja que o valor definido  *[!UICONTROL Magento Price Source]* na  [Lista de ](./listing-price.md) Preços seja ajustado por um valor fixo.

1. Para **[!UICONTROL Adjustment Amount]** (obrigatório), insira o valor numérico do ajuste de preço.

   - Quando *[!UICONTROL Apply]* estiver definido como `Apply as percentage`, insira o valor percentual (exemplo: insira `25` para um ajuste de preço de 25%).

   - Quando *[!UICONTROL Apply]* estiver definido como `Apply as fixed amount`, insira o valor numérico da quantia fixa (por exemplo: insira `25` para um ajuste de preço fixo de $25).

1. Quando terminar, clique em **[!UICONTROL Save pricing rule]**.

![Regra de preço padrão](assets/ob-price-rule-action-standard-example.png)

| Campo | Descrição |
|---|---|
| [!UICONTROL Rule Type] | Selecione `Standard price rule`. |
| [!UICONTROL Price Action] | Opções:<ul><li>**[!UICONTROL Decrease By]** - Escolha quando deseja que o valor da fonte de  [!DNL Commerce] preço definido seja diminuído antes de listar para a Amazon.</li><li>**[!UICONTROL Increase By]** - Escolha quando você deseja que o valor da fonte de  [!DNL Commerce] preço definido seja aumentado antes de listar o Amazon.</li></ul> |
| [!UICONTROL Apply] | Opções:<ul><li>**[!UICONTROL Apply as percentage]** - Escolha quando deseja ajustar o valor da fonte de  [!DNL Commerce] preço definido em uma porcentagem.</li><li>**[!UICONTROL Apply as fixed amount]** - Escolha quando deseja ajustar o valor da fonte de  [!DNL Commerce] preço definido por uma quantia fixa.</li></ul> |
| [!UICONTROL Adjustment Amount] | Obrigatório.<br><br>Se você optar  `Apply as percentage` por  *[!UICONTROL Apply]*, insira o valor percentual (por exemplo: insira  `25` para um ajuste de 25%).<br><br>Se você escolher  `Apply as fixed amount` , digite o valor numérico  *[!UICONTROL Apply]* para a quantia fixa (por exemplo: insira  `25` para um ajuste fixo de $25). |
