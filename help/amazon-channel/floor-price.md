---
title: '"Regra de Reprecificação Inteligente: Preço Limite'''
description: Use as configurações de preço mínimo para determinar o preço mais baixo de uma regra de preço inteligente para gerenciar suas listagens do Amazon.
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Regra inteligente de reprecificação: preço mínimo

As seções de uma regra inteligente de redefinição de preços incluem:

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

O [preço mínimo](./floor-price.md) as configurações protegem automaticamente o preço mais baixo do produto em relação às regras de preços inteligentes. Use essas configurações para definir um limite mínimo (preço mais baixo) para suas regras de preços inteligentes, garantindo que seus produtos não estejam listados abaixo do preço desejado.

Os atributos de preço mínimo são baseados no escopo do site se sua [!DNL Commerce] a loja está usando o escopo de preço do site. Consulte [Escopo de preço](./price-scope.md).

O preço mínimo é usado somente quando **[!UICONTROL Rule Type]** está definida como `Intelligent repricing rule`.

## Configurar preço mínimo

Defina sua configuração de preço mais baixo na _[!UICONTROL Floor Price]_seção.

1. Para **[!UICONTROL Floor Price Source]**, escolha um atributo de fonte de preço.

   Escolha a [!DNL Commerce] [atributo do produto](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} que indica o limite de chão relativo. Por exemplo, se você não quiser que o preço da listagem do Amazon fique abaixo do custo do item, escolha a variável *Custo* atributo.

1. Para **[!UICONTROL Floor Price Action]**, escolha uma opção.

   - `Decrease By` - Escolha quando deseja definir _[!UICONTROL Floor Price Source]_valor a ser ajustado, criando um preço mínimo para a regra, antes de listar para o Amazon.

   - `Increase By` - Escolha quando deseja definir _[!UICONTROL Floor Price Source]_valor a ser ajustado, criando um preço mínimo mais alto para a regra, antes de listar para a Amazon.

   - `Match` - Escolha quando você não deseja que o preço da listagem flutue abaixo do valor definido _[!UICONTROL Floor Price Source]_valor. Quando definido como `Match`, o_[!UICONTROL Apply]_ e _[!UICONTROL Floor Adjustment Amount]_os campos estão desativados.

1. Deixe o **[!UICONTROL Apply]** padrão como `Apply as percentage`.

1. Para **[!UICONTROL Floor Adjustment Price]**, insira o valor numérico da porcentagem para ajustar a _[!UICONTROL Floor Price Source]_valor.

Neste exemplo, o preço mínimo é definido como 3% acima do custo do item.

![Exemplo de regra de reprecificação inteligente - preço mínimo](assets/ob-intelligent-pricde-rule-floor-price.png)

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Floor Price Source] | Escolha a [!DNL Commerce] que indica seu limite mínimo relativo (preço mais baixo). Por exemplo, se você não quiser que o preço da listagem do Amazon fique abaixo do custo do item, escolha a variável `Cost` atributo. |
| [!UICONTROL Floor Price Action] | Escolha uma ação de ajuste de preço. Opções:<ul><li>**[!UICONTROL Decrease By]** - Escolha quando deseja definir _[!UICONTROL Floor Price Source]_valor a ser ajustado, criando um preço mínimo para a regra, antes de listar para o Amazon.</li><li>**[!UICONTROL Increase By]** - Escolha quando deseja definir _[!UICONTROL Floor Price Source]_valor a ser ajustado, criando um preço mínimo mais alto para a regra, antes de listar para a Amazon.</li><li>**[!UICONTROL Match]** - Escolha quando você não deseja que o preço da listagem flutue abaixo do valor definido _[!UICONTROL Floor Price Source]_valor. Quando escolhido, a variável_[!UICONTROL Apply]_ e _[!UICONTROL Floor Adjustment Amount]_os campos estão desativados.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Um ajustamento percentual em relação ao valor de _[!UICONTROL Floor Price Source]_valor. |
| [!UICONTROL Floor Adjustment Amount] | Insira o valor numérico da porcentagem para ajustar a _[!UICONTROL Floor Price Source]_valor. |
