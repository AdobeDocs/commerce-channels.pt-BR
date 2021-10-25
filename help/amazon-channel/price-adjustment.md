---
title: Ajuste de preço
description: Configure ajustes de preço para definir o cálculo de preço quando tiver identificado a fonte de preço do concorrente da Amazon.
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# Ajuste de preço

>[!NOTE]
>
>A seção Ajuste de preço difere um pouco para as regras de reprecificação padrão e inteligente. **[!UICONTROL Match Competitor Price]** está disponível somente em _[!UICONTROL Price Action]_when **[!UICONTROL Rule Type]**está definida como `Intelligent repricing rule`.

As seções de uma regra inteligente de redefinição de preços incluem:

- [Selecionar tipo de regra](./intelligent-repricing-rules.md)
- [Variáveis condicionais do concorrente](./competitor-conditional-variances.md)
- Ajuste de preço
- [Preço Limite](./floor-price.md)
- [Preço Limite Opcional](./optional-ceiling-price.md)

O ajuste de preço define o cálculo de preço quando você identifica a fonte de preço do concorrente.

## Configurar ajuste de preço

Defina seu ajuste de preço na _[!UICONTROL Price Adjustment]_seção.

1. Para **[!UICONTROL Price Action]**, escolha uma opção:

   - `Decrease By` - Escolha quando deseja ajustar o valor da fonte de preço definido, criando um preço mais baixo para a regra, antes de listar para a Amazon.

   - `Increase By` - Escolha quando deseja ajustar o valor da fonte de preço definido, criando um preço mais alto para a regra, antes de listar para a Amazon.

   - `Match Competitor Price` - (Somente regra de reprecificação inteligente) Escolha quando deseja alterar o preço da listagem do Amazon para corresponder ao valor da variável [concorrente mais baixo](./lowest-competitor-pricing.md) preço, com base no feedback e nos parâmetros de variação de seu concorrente. Quando definido como `Match Competitor Price`, o _[!UICONTROL Apply]_e_[!UICONTROL Adjustment Amount]_ são removidos.

1. Para **[!UICONTROL Apply]**, escolha uma opção:

   - `Apply as percentage` - Escolha quando deseja definir **[!UICONTROL Magento Price Source]** definido no [Preço de Listagem](./listing-price.md) ajustado por uma percentagem.

   - `Apply as fixed amount` - Escolha quando deseja definir **[!UICONTROL Magento Price Source]** definido no [Preço de Listagem](./listing-price.md) ajustado por um montante fixo.

1. Para **[!UICONTROL Adjustment Amount]** (obrigatório), insira o valor numérico do ajuste de preço.

   - When **[!UICONTROL Apply]** está definida como `Apply as percentage`, insira o valor percentual (por exemplo: enter `25` para um ajuste de 25%).

   - When **[!UICONTROL Apply]** está definida como `Apply as fixed amount`, insira o valor numérico da quantia fixa (por exemplo: enter `25` para um ajuste fixo de US$ 25).

![Regra inteligente de reprecificação - ajuste de preço](assets/amazon-price-adjustment.png)

| Campo | Descrição |
|---|---|
| [!UICONTROL Price Action] | Escolha uma ação de ajuste de preço. Opções:<br>**[!UICONTROL Decrease By]**- Escolha quando deseja definir _[!UICONTROL Magento Price Source]_definido no [Preço de Listagem](./listing-price.md) para ser ajustado, criando um preço mais baixo para a regra, antes de listar no Amazon.<br>**[!UICONTROL Increase By]**- Escolha quando deseja definir_[!UICONTROL Magento Price Source]_ definido no [Preço de Listagem](./listing-price.md) para ser ajustado, criando um preço mais alto para a regra, antes de listar para a Amazon.<br>**[!UICONTROL Match Competitor Price]**- (Somente regra de reprecificação inteligente) Escolha quando deseja alterar o preço da listagem do Amazon para corresponder ao valor da variável [concorrente mais baixo](./lowest-competitor-pricing.md) preço, com base no feedback e nos parâmetros de variação de seu concorrente. Quando escolhido, a variável _Aplicar_ e _Valor do Ajuste_ são removidos. |
| [!UICONTROL Apply] | Opções:<br>**[!UICONTROL Apply as percentage]**- Escolha quando deseja definir _[!UICONTROL Magento Price Source]_definido no [Preço de Listagem](./listing-price.md) ajustado por uma percentagem.<br>**[!UICONTROL Apply as fixed amount]**- Escolha quando deseja definir_[!UICONTROL Magento Price Source]_ definido no [Preço de Listagem](./listing-price.md) ajustado por um montante fixo. |
| [!UICONTROL Adjustment Amount] | Obrigatório.<br>Se você escolher `Apply as percentage` para **[!UICONTROL Apply]**, insira o valor percentual (por exemplo: enter `25` para um ajuste de 25%).<br>Se você escolher `Apply as fixed amount` para **[!UICONTROL Apply]**, insira o valor numérico da quantia fixa (por exemplo: enter `25` para um ajuste fixo de US$ 25). |
