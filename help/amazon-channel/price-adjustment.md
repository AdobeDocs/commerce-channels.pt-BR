---
title: Ajuste de preço
description: Configure ajustes de preço para definir o cálculo de preço quando tiver identificado a fonte de preço do concorrente da Amazon.
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Ajuste de preço

>[!NOTE]
>
>A seção Ajuste de preço difere um pouco para as regras de reprecificação padrão e inteligente. **[!UICONTROL Match Competitor Price]** só está disponível em  _[!UICONTROL Price Action]_quando **[!UICONTROL Rule Type]**está definido como  `Intelligent repricing rule`.

As seções de uma regra inteligente de redefinição de preços incluem:

- [Selecionar tipo de regra](./intelligent-repricing-rules.md)
- [Variáveis condicionais do concorrente](./competitor-conditional-variances.md)
- Ajuste de preço
- [Preço Limite](./floor-price.md)
- [Preço Limite Opcional](./optional-ceiling-price.md)

O ajuste de preço define o cálculo de preço quando você identifica a fonte de preço do concorrente.

## Configurar ajuste de preço

Defina seu ajuste de preço na seção _[!UICONTROL Price Adjustment]_.

1. Para **[!UICONTROL Price Action]**, escolha uma opção:

   - `Decrease By` - Escolha quando deseja ajustar o valor da fonte de preço definido, criando um preço mais baixo para a regra, antes de listar para a Amazon.

   - `Increase By` - Escolha quando deseja ajustar o valor da fonte de preço definido, criando um preço mais alto para a regra, antes de listar para a Amazon.

   - `Match Competitor Price` - (Somente na regra de reprecificação inteligente) Escolha quando deseja alterar o preço da listagem do Amazon para corresponder ao  [menor ](./lowest-competitor-pricing.md) preço competitivo, com base no feedback e nos parâmetros de variação do seu concorrente. Quando definido como `Match Competitor Price`, os campos _[!UICONTROL Apply]_e_[!UICONTROL Adjustment Amount]_ são removidos.

1. Para **[!UICONTROL Apply]**, escolha uma opção:

   - `Apply as percentage` - Escolha quando deseja que o valor definido  **[!UICONTROL Magento Price Source]** na  [Lista ](./listing-price.md) seja ajustado em uma porcentagem.

   - `Apply as fixed amount` - Escolha quando deseja que o  **[!UICONTROL Magento Price Source]** definido em seu  [ ](./listing-price.md) Preço de Listagem seja ajustado por um valor fixo.

1. Para **[!UICONTROL Adjustment Amount]** (obrigatório), insira o valor numérico do ajuste de preço.

   - Quando **[!UICONTROL Apply]** estiver definido como `Apply as percentage`, insira o valor percentual (exemplo: insira `25` para um ajuste de 25%).

   - Quando **[!UICONTROL Apply]** estiver definido como `Apply as fixed amount`, insira o valor numérico da quantia fixa (por exemplo: insira `25` para um ajuste fixo de $25).

![Regra inteligente de reprecificação - ajuste de preço](assets/amazon-price-adjustment.png)

| Campo | Descrição |
|---|---|
| [!UICONTROL Price Action] | Escolha uma ação de ajuste de preço. Opções:<br>**[!UICONTROL Decrease By]**- Escolha quando deseja que o _[!UICONTROL Magento Price Source]_definido em seu [Preço de Listagem](./listing-price.md) seja ajustado, criando um preço mais baixo para a regra, antes de listar para o Amazon.<br>**[!UICONTROL Increase By]**- Escolha quando deseja que o valor definido_[!UICONTROL Magento Price Source]_ em seu Preço de  [ ](./listing-price.md) Listagem seja ajustado, criando um preço mais alto para a regra, antes de listar para a Amazon.<br>**[!UICONTROL Match Competitor Price]**- (Somente na regra de reprecificação inteligente) Escolha quando deseja alterar o preço da listagem do Amazon para corresponder ao  [menor ](./lowest-competitor-pricing.md) preço competitivo, com base no feedback e nos parâmetros de variação do seu concorrente. Quando escolhidos, os campos _Aplicar_ e _Quantia de Ajuste_ são removidos. |
| [!UICONTROL Apply] | Opções:<br>**[!UICONTROL Apply as percentage]**- Escolha quando quiser que o _[!UICONTROL Magento Price Source]_definido em seu [Preço de Listagem](./listing-price.md) seja ajustado por uma porcentagem.<br>**[!UICONTROL Apply as fixed amount]**- Escolha quando deseja que o_[!UICONTROL Magento Price Source]_ definido em seu  [ ](./listing-price.md) Preço de Listagem seja ajustado por um valor fixo. |
| [!UICONTROL Adjustment Amount] | Obrigatório.<br>Se você escolher  `Apply as percentage` , insira  **[!UICONTROL Apply]** o valor percentual (por exemplo: insira  `25` para um ajuste de 25%).<br>Se você escolher  `Apply as fixed amount` , digite o valor numérico  **[!UICONTROL Apply]** para a quantia fixa (por exemplo: insira  `25` para um ajuste fixo de $25). |
