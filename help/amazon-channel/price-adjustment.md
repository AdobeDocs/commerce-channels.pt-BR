---
title: Canal de vendas da Amazon - [!UICONTROL Price Adjustment]
description: Configure ajustes de preço para definir o cálculo de preço quando tiver identificado a fonte de preço do concorrente do Amazon.
feature: Sales Channels, Price Rules
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# [!UICONTROL Price Adjustment]

>[!NOTE]
>
>A seção Ajuste de Preço é ligeiramente diferente para as regras de reprecificação Padrão e Inteligente. **[!UICONTROL Match Competitor Price]** está disponível somente em _[!UICONTROL Price Action]_quando **[!UICONTROL Rule Type]**está definido como `Intelligent repricing rule`.

As seções de uma regra de reavaliação inteligente incluem:

- [Selecionar tipo de regra](./intelligent-repricing-rules.md)
- [Variações condicionais do concorrente](./competitor-conditional-variances.md)
- Ajuste de Preço
- [Preço mínimo](./floor-price.md)
- [Preço máximo opcional](./optional-ceiling-price.md)

O ajuste de preço define o cálculo de preço quando você identifica a fonte de preço do concorrente.

## Configurar ajuste de preço

Defina seu ajuste de preço na seção _[!UICONTROL Price Adjustment]_.

1. Para **[!UICONTROL Price Action]**, escolha uma opção:

   - `Decrease By` - Escolha quando deseja que o valor de origem do preço definido seja ajustado para baixo, criando um preço mais baixo para a regra, antes de listar na Amazon.

   - `Increase By` - Escolha quando deseja que o valor de origem do preço definido seja ajustado, criando um preço mais alto para a regra, antes de listar na Amazon.

   - `Match Competitor Price` - (Somente regra de reavaliação inteligente de preços) Escolha quando deseja alterar o preço de listagem do Amazon para corresponder ao preço do [concorrente mais baixo](./lowest-competitor-pricing.md), com base nos comentários do concorrente e nos parâmetros de variação. Quando definido como `Match Competitor Price`, os campos _[!UICONTROL Apply]_e_[!UICONTROL Adjustment Amount]_ são removidos.

1. Para **[!UICONTROL Apply]**, escolha uma opção:

   - `Apply as percentage` - Escolha quando deseja que o **[!UICONTROL Magento Price Source]** definido em seu [Preço de Listagem](./listing-price.md) seja ajustado por uma porcentagem.

   - `Apply as fixed amount` - Escolha quando deseja que o **[!UICONTROL Magento Price Source]** definido em seu [Preço de Listagem](./listing-price.md) seja ajustado por um valor fixo.

1. Para **[!UICONTROL Adjustment Amount]** (obrigatório), insira o valor numérico para o ajuste de preço.

   - Quando **[!UICONTROL Apply]** estiver definido como `Apply as percentage`, insira o valor percentual (exemplo: insira `25` para um ajuste percentual de 25%).

   - Quando **[!UICONTROL Apply]** estiver definido como `Apply as fixed amount`, insira o valor numérico para o valor fixo (exemplo: insira `25` para um ajuste fixo de $25).

![Regra inteligente de reavaliação de preços - ajuste de preço](assets/amazon-price-adjustment.png){width="600" zoomable="yes"}

| Campo | Descrição |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Action] | Escolha uma ação de ajuste de preço. Opções:<br>**[!UICONTROL Decrease By]**- Escolha quando deseja que o _[!UICONTROL Magento Price Source]_definido em seu [Preço de Listagem](./listing-price.md) seja ajustado para baixo, criando um preço mais baixo para a regra, antes de listar na Amazon.<br>**[!UICONTROL Increase By]**- Escolha quando deseja que o_[!UICONTROL Magento Price Source]_ definido em seu [Preço de Listagem](./listing-price.md) seja ajustado, criando um preço mais alto para a regra, antes de listar na Amazon.<br>**[!UICONTROL Match Competitor Price]**- (Somente regra de reavaliação inteligente de preços) Escolha quando deseja alterar o preço de listagem do Amazon para corresponder ao preço do [concorrente mais baixo](./lowest-competitor-pricing.md), com base nos comentários do concorrente e nos parâmetros de variação. Quando selecionados, os campos _Aplicar_ e _Valor de Ajuste_ são removidos. |
| [!UICONTROL Apply] | Opções:<br>**[!UICONTROL Apply as percentage]**- Escolha quando deseja que o _[!UICONTROL Magento Price Source]_definido em seu [Preço de Listagem](./listing-price.md) seja ajustado por uma porcentagem.<br>**[!UICONTROL Apply as fixed amount]**- Escolha quando deseja que o_[!UICONTROL Magento Price Source]_ definido em seu [Preço de Listagem](./listing-price.md) seja ajustado por um valor fixo. |
| [!UICONTROL Adjustment Amount] | Obrigatório.<br>Se você escolheu `Apply as percentage` para **[!UICONTROL Apply]**, insira o valor percentual (exemplo: insira `25` para um ajuste percentual de 25%).<br>Se você escolheu `Apply as fixed amount` para **[!UICONTROL Apply]**, insira o valor numérico para o valor fixo (exemplo: insira `25` para um ajuste fixo de $25). |
