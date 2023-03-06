---
title: Ações da Regra de Preço Padrão
description: Use as ações da regra de preço padrão para aumentar ou diminuir um preço de lista do Amazon relativo ao preço do catálogo de Comércio (ou à origem de preço).
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Ações da Regra de Preço Padrão

Uma ação de regra de preço padrão permite aumentar ou diminuir um preço de listagem do Amazon por uma porcentagem específica ou quantia fixa em dólar em relação ao [!DNL Commerce] preço de catálogo (ou origem de preço).

As seções de uma ação de regra de preço padrão incluem:

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## Configurar ações de regra de preço

1. Para **[!UICONTROL Rule Type]**, escolha `Standard price rule`.

   Essa opção desativa os outros campos no _[!UICONTROL Select Rule Type]_seção.

1. Expanda a _[!UICONTROL Price Adjustment]_seção, se necessário.

1. Para **[!UICONTROL Price Action]**, escolha uma opção para determinar como você deseja alterar a *[!UICONTROL Magento Price Source]* (definido em seu [Preço de Listagem](./listing-price.md)).

   - `Decrease By` - Escolha quando deseja que o valor seja diminuído antes de listar na Amazon.

   - `Increase By` - Escolha quando deseja que o valor seja aumentado antes de listar para o Amazon.

1. Para **[!UICONTROL Apply]**, escolha uma opção e uma opção para determinar como você deseja definir a variável *[!UICONTROL Magento Price Source]* definido em seu [Preço de Listagem](./listing-price.md) valor a ser ajustado:

   - `Apply as percentage` - Escolha quando deseja definir o *[!UICONTROL Magento Price Source]* definido em seu [Preço de Listagem](./listing-price.md) valor ajustado por uma porcentagem

   - `Apply as fixed amount` - Escolha quando deseja definir o *[!UICONTROL Magento Price Source]* definido em seu [Preço de Listagem](./listing-price.md) valor ajustado por um valor fixo.

1. Para **[!UICONTROL Adjustment Amount]** (obrigatório), informe o valor numérico para o ajuste de preço.

   - Quando *[!UICONTROL Apply]* está definida como `Apply as percentage`, insira o valor percentual (exemplo: insira `25` 25 %).

   - Quando *[!UICONTROL Apply]* está definida como `Apply as fixed amount`, insira o valor numérico para o valor fixo (exemplo: insira `25` para um ajuste de preço fixo de US$ 25).

1. Quando terminar, clique em **[!UICONTROL Save pricing rule]**.

![Regra de preço padrão](assets/ob-price-rule-action-standard-example.png)

| Campo | Descrição |
|---|---|
| [!UICONTROL Rule Type] | Selecionar `Standard price rule`. |
| [!UICONTROL Price Action] | Opções:<ul><li>**[!UICONTROL Decrease By]** - Escolha quando deseja definir o [!DNL Commerce] valor de origem do preço a ser diminuído antes de listar na Amazon.</li><li>**[!UICONTROL Increase By]** - Escolha quando deseja definir o [!DNL Commerce] valor de origem do preço a ser aumentado antes da listagem à Amazon.</li></ul> |
| [!UICONTROL Apply] | Opções:<ul><li>**[!UICONTROL Apply as percentage]** - Escolha quando deseja definir o [!DNL Commerce] valor de origem do preço ajustado por uma porcentagem.</li><li>**[!UICONTROL Apply as fixed amount]** - Escolha quando deseja definir o [!DNL Commerce] valor de origem do preço ajustado por um valor fixo.</li></ul> |
| [!UICONTROL Adjustment Amount] | Obrigatório.<br><br>Se você escolher `Apply as percentage` para *[!UICONTROL Apply]*, insira o valor percentual (exemplo: insira `25` para um ajuste de 25%).<br><br>Se você escolher `Apply as fixed amount` para *[!UICONTROL Apply]*, insira o valor numérico para o valor fixo (exemplo: insira `25` para um ajuste fixo de US$ 25). |
