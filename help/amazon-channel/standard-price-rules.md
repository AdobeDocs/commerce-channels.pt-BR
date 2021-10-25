---
title: Ações das Regras de Preço Padrão
description: Use as ações de regra de preço padrão para aumentar ou diminuir um preço de listagem da Amazon em relação ao preço do catálogo do Commerce (ou fonte de preço).
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Ações das regras de preço padrão

Uma ação de regra de preço padrão permite aumentar ou diminuir um preço de listagem da Amazon em uma porcentagem específica ou valor fixo do dólar em relação à [!DNL Commerce] preço do catálogo (ou fonte de preço).

As seções de uma ação de regra de preço padrão incluem:

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## Configurar ações de regra de preço

1. Para **[!UICONTROL Rule Type]**, escolha `Standard price rule`.

   Essa opção desativa os outros campos na variável _[!UICONTROL Select Rule Type]_seção.

1. Expanda o _[!UICONTROL Price Adjustment]_, se necessário.

1. Para **[!UICONTROL Price Action]**, escolha uma opção para determinar como você deseja alterar o *[!UICONTROL Magento Price Source]* (definido em [Preço de Listagem](./listing-price.md)).

   - `Decrease By` - Escolha quando deseja que o valor seja diminuído antes de listar para o Amazon.

   - `Increase By` - Escolha quando deseja aumentar o valor antes de listar o Amazon.

1. Para **[!UICONTROL Apply]**, escolha uma opção e uma opção para determinar como você deseja definir *[!UICONTROL Magento Price Source]* definido no [Preço de Listagem](./listing-price.md) valor a ajustar:

   - `Apply as percentage` - Escolha quando deseja definir *[!UICONTROL Magento Price Source]* definido no [Preço de Listagem](./listing-price.md) valor ajustado por uma percentagem

   - `Apply as fixed amount` - Escolha quando deseja definir *[!UICONTROL Magento Price Source]* definido no [Preço de Listagem](./listing-price.md) ajustado por um valor fixo.

1. Para **[!UICONTROL Adjustment Amount]** (obrigatório), insira o valor numérico do ajuste de preço.

   - When *[!UICONTROL Apply]* está definida como `Apply as percentage`, insira o valor percentual (por exemplo: enter `25` para um ajuste de preço de 25%).

   - When *[!UICONTROL Apply]* está definida como `Apply as fixed amount`, insira o valor numérico da quantia fixa (por exemplo: enter `25` para um ajuste de preço fixo de US$ 25).

1. Ao concluir, clique em **[!UICONTROL Save pricing rule]**.

![Regra de preço padrão](assets/ob-price-rule-action-standard-example.png)

| Campo | Descrição |
|---|---|
| [!UICONTROL Rule Type] | Selecionar `Standard price rule`. |
| [!UICONTROL Price Action] | Opções:<ul><li>**[!UICONTROL Decrease By]** - Escolha quando deseja definir [!DNL Commerce] valor da fonte de preço a ser diminuído antes de ser listado na Amazon.</li><li>**[!UICONTROL Increase By]** - Escolha quando deseja definir [!DNL Commerce] valor da fonte de preço a ser aumentado antes da listagem para o Amazon.</li></ul> |
| [!UICONTROL Apply] | Opções:<ul><li>**[!UICONTROL Apply as percentage]** - Escolha quando deseja definir [!DNL Commerce] valor da fonte de preço ajustado por uma porcentagem.</li><li>**[!UICONTROL Apply as fixed amount]** - Escolha quando deseja definir [!DNL Commerce] valor da fonte de preço ajustado por um valor fixo.</li></ul> |
| [!UICONTROL Adjustment Amount] | Obrigatório.<br><br>Se você escolher `Apply as percentage` para *[!UICONTROL Apply]*, insira o valor percentual (por exemplo: enter `25` para um ajuste de 25%).<br><br>Se você escolher `Apply as fixed amount` para *[!UICONTROL Apply]*, insira o valor numérico da quantia fixa (por exemplo: enter `25` para um ajuste fixo de US$ 25). |
