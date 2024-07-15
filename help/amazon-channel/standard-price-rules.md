---
title: Canal de vendas do Amazon - Ações de regra de preço padrão
description: Use as ações da regra de preço padrão para aumentar ou diminuir um preço de lista do Amazon relativo ao preço do catálogo do Commerce (ou origem de preço).
feature: Sales Channels, Price Rules
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# Ações de regra de preço padrão

Uma ação de regra de preço padrão permite aumentar ou diminuir um preço de listagem do Amazon por uma porcentagem específica ou valor fixo em dólar relativo ao preço de catálogo [!DNL Commerce] (ou origem de preço).

As seções de uma ação de regra de preço padrão incluem:

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## Configurar ações de regra de preço

1. Para **[!UICONTROL Rule Type]**, escolha `Standard price rule`.

   Esta opção desabilita os outros campos na seção _[!UICONTROL Select Rule Type]_.

1. Expanda a seção _[!UICONTROL Price Adjustment]_, se necessário.

1. Para **[!UICONTROL Price Action]**, escolha uma opção para determinar como você deseja alterar o valor de *[!UICONTROL Magento Price Source]* (definido em seu [Preço de Listagem](./listing-price.md)).

   - `Decrease By` - Escolha quando deseja que o valor seja diminuído antes de listar na Amazon.

   - `Increase By` - Escolha quando deseja que o valor seja aumentado antes de listar na Amazon.

1. Para **[!UICONTROL Apply]**, escolha uma opção para determinar como você deseja que o *[!UICONTROL Magento Price Source]* definido no valor de seu [Preço de Listagem](./listing-price.md) seja ajustado:

   - `Apply as percentage` - Escolha quando deseja que o *[!UICONTROL Magento Price Source]* definido no valor de [Preço de Listagem](./listing-price.md) seja ajustado por uma porcentagem

   - `Apply as fixed amount` - Escolha quando deseja que o *[!UICONTROL Magento Price Source]* definido no valor de [Preço de Listagem](./listing-price.md) seja ajustado por um valor fixo.

1. Para **[!UICONTROL Adjustment Amount]** (obrigatório), insira o valor numérico para o ajuste de preço.

   - Quando *[!UICONTROL Apply]* estiver definido como `Apply as percentage`, insira o valor percentual (exemplo: insira `25` para um ajuste de preço percentual de 25%).

   - Quando *[!UICONTROL Apply]* estiver definido como `Apply as fixed amount`, insira o valor numérico para o valor fixo (exemplo: insira `25` para um ajuste de preço fixo de $25).

1. Quando terminar, clique em **[!UICONTROL Save pricing rule]**.

![Regra de preço padrão](assets/ob-price-rule-action-standard-example.png){width="600" zoomable="yes"}

| Campo | Descrição |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Rule Type] | Selecione `Standard price rule`. |
| [!UICONTROL Price Action] | Opções:<ul><li>**[!UICONTROL Decrease By]** - Escolha quando deseja que o valor de origem do preço [!DNL Commerce] seja reduzido antes de listar na Amazon.</li><li>**[!UICONTROL Increase By]** - Escolha quando deseja que o valor de origem do preço [!DNL Commerce] definido seja aumentado antes de listar na Amazon.</li></ul> |
| [!UICONTROL Apply] | Opções:<ul><li>**[!UICONTROL Apply as percentage]** - Escolha quando deseja que o valor de origem do preço [!DNL Commerce] definido seja ajustado por uma porcentagem.</li><li>**[!UICONTROL Apply as fixed amount]** - Escolha quando deseja que o valor de origem do preço [!DNL Commerce] seja ajustado por um valor fixo.</li></ul> |
| [!UICONTROL Adjustment Amount] | Obrigatório.<br><br>Se você escolher `Apply as percentage` para *[!UICONTROL Apply]*, insira o valor percentual (exemplo: insira `25` para um ajuste percentual de 25%).<br><br>Se você escolheu `Apply as fixed amount` para *[!UICONTROL Apply]*, insira o valor numérico para o valor fixo (exemplo: insira `25` para um ajuste fixo de $25). |
