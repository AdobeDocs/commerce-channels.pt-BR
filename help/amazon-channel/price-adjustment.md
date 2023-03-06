---
title: Ajuste de Preço
description: Configure ajustes de preço para definir o cálculo de preço quando tiver identificado a fonte de preço do concorrente do Amazon.
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# Ajuste de Preço

>[!NOTE]
>
>A seção Ajuste de Preço é ligeiramente diferente para as regras de reprecificação Padrão e Inteligente. **[!UICONTROL Match Competitor Price]** só está disponível em _[!UICONTROL Price Action]_quando **[!UICONTROL Rule Type]**está definida como `Intelligent repricing rule`.

As seções de uma regra de reavaliação inteligente incluem:

- [Selecionar tipo de regra](./intelligent-repricing-rules.md)
- [Variações condicionais do concorrente](./competitor-conditional-variances.md)
- Ajuste de Preço
- [Preço mínimo](./floor-price.md)
- [Preço máximo opcional](./optional-ceiling-price.md)

O ajuste de preço define o cálculo de preço quando você identifica a fonte de preço do concorrente.

## Configurar ajuste de preço

Defina o ajuste de preço no _[!UICONTROL Price Adjustment]_seção.

1. Para **[!UICONTROL Price Action]**, escolha uma opção:

   - `Decrease By` - Escolha quando deseja que o valor de origem do preço definido seja ajustado para baixo, criando um preço mais baixo para a regra, antes de listar para o Amazon.

   - `Increase By` - Escolha quando deseja que o valor de origem do preço definido seja ajustado, criando um preço mais alto para a regra, antes de listar para o Amazon.

   - `Match Competitor Price` - (Somente regra de reprecificação inteligente) Escolha quando deseja alterar o preço de lista do Amazon para corresponder ao [concorrente mais baixo](./lowest-competitor-pricing.md) preço, com base nos comentários do concorrente e nos parâmetros de variação. Quando definido como `Match Competitor Price`, o _[!UICONTROL Apply]_e_[!UICONTROL Adjustment Amount]_ Os campos do são removidos.

1. Para **[!UICONTROL Apply]**, escolha uma opção:

   - `Apply as percentage` - Escolha quando deseja definir o **[!UICONTROL Magento Price Source]** definido em seu [Preço de Listagem](./listing-price.md) ajustado por uma porcentagem.

   - `Apply as fixed amount` - Escolha quando deseja definir o **[!UICONTROL Magento Price Source]** definido em seu [Preço de Listagem](./listing-price.md) ajustado por um valor fixo.

1. Para **[!UICONTROL Adjustment Amount]** (obrigatório), informe o valor numérico para o ajuste de preço.

   - Quando **[!UICONTROL Apply]** está definida como `Apply as percentage`, insira o valor percentual (exemplo: insira `25` para um ajuste de 25%).

   - Quando **[!UICONTROL Apply]** está definida como `Apply as fixed amount`, insira o valor numérico para o valor fixo (exemplo: insira `25` para um ajuste fixo de US$ 25).

![Regra inteligente de reavaliação de preços - Ajuste de preços](assets/amazon-price-adjustment.png)

| Campo | Descrição |
|---|---|
| [!UICONTROL Price Action] | Escolha uma ação de ajuste de preço. Opções:<br>**[!UICONTROL Decrease By]**- Escolha quando deseja definir o _[!UICONTROL Magento Price Source]_definido em seu [Preço de Listagem](./listing-price.md) para ser ajustado, criando um preço mais baixo para a regra, antes de listar na Amazon.<br>**[!UICONTROL Increase By]**- Escolha quando deseja definir o_[!UICONTROL Magento Price Source]_ definido em seu [Preço de Listagem](./listing-price.md) para ser ajustado, criando um preço mais alto para a regra, antes de listar na Amazon.<br>**[!UICONTROL Match Competitor Price]**- (Somente regra de reprecificação inteligente) Escolha quando deseja alterar o preço de lista do Amazon para corresponder ao [concorrente mais baixo](./lowest-competitor-pricing.md) preço, com base nos comentários do concorrente e nos parâmetros de variação. Quando escolhido, o _Aplicar_ e _Valor do Ajuste_ Os campos do são removidos. |
| [!UICONTROL Apply] | Opções:<br>**[!UICONTROL Apply as percentage]**- Escolha quando deseja definir o _[!UICONTROL Magento Price Source]_definido em seu [Preço de Listagem](./listing-price.md) ajustado por uma porcentagem.<br>**[!UICONTROL Apply as fixed amount]**- Escolha quando deseja definir o_[!UICONTROL Magento Price Source]_ definido em seu [Preço de Listagem](./listing-price.md) ajustado por um valor fixo. |
| [!UICONTROL Adjustment Amount] | Obrigatório.<br>Se você escolher `Apply as percentage` para **[!UICONTROL Apply]**, insira o valor percentual (exemplo: insira `25` para um ajuste de 25%).<br>Se você escolher `Apply as fixed amount` para **[!UICONTROL Apply]**, insira o valor numérico para o valor fixo (exemplo: insira `25` para um ajuste fixo de US$ 25). |
