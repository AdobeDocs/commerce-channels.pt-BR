---
title: "Regra de Reprecificação Inteligente: Preço Mínimo"
description: Use as configurações de preço mínimo para determinar o preço mais baixo de uma regra de preço inteligente para gerenciar suas listagens do Amazon.
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Regra de Reprecificação Inteligente: Preço Mínimo

As seções de uma regra de reavaliação inteligente incluem:

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

A variável [preço mínimo](./floor-price.md) As configurações do protegem automaticamente o preço mais baixo do produto contra as regras de preços inteligentes. Use essas configurações para definir um limite mínimo (preço mais baixo) para suas regras de preços inteligentes, garantindo que seus produtos não sejam listados abaixo do preço desejado.

Os atributos de preço mínimo são baseados no escopo do site se seu [!DNL Commerce] a loja está usando o escopo de preços do site. Consulte [Escopo de preços](./price-scope.md).

O preço mínimo só é usado quando **[!UICONTROL Rule Type]** está definida como `Intelligent repricing rule`.

## Configurar preço mínimo

Defina sua configuração de preço mais baixo no _[!UICONTROL Floor Price]_seção.

1. Para **[!UICONTROL Floor Price Source]**, escolha um atributo de origem de preço.

   Escolha o [!DNL Commerce] [atributo de produto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) que indica o limite mínimo relativo. Por exemplo, se você não quiser que o preço de tabela do Amazon fique abaixo do custo do item, escolha a opção *Custo* atributo.

1. Para **[!UICONTROL Floor Price Action]**, escolha uma opção.

   - `Decrease By` - Escolha quando deseja definir o _[!UICONTROL Floor Price Source]_valor a ser ajustado para baixo, criando um preço mínimo mais baixo para a regra, antes de listar na Amazon.

   - `Increase By` - Escolha quando deseja definir o _[!UICONTROL Floor Price Source]_valor a ser ajustado, criando um preço mínimo mais alto para a regra, antes de listar na Amazon.

   - `Match` - Escolha quando não deseja que o preço de tabela flutue abaixo do valor definido _[!UICONTROL Floor Price Source]_valor. Quando definido como `Match`, o_[!UICONTROL Apply]_ e _[!UICONTROL Floor Adjustment Amount]_Os campos do estão desativados.

1. Deixe a **[!UICONTROL Apply]** padrão como `Apply as percentage`.

1. Para **[!UICONTROL Floor Adjustment Price]**, insira o valor numérico para o percentual para ajustar _[!UICONTROL Floor Price Source]_valor.

Neste exemplo, o preço mínimo está definido como 3% acima do custo do item.

![Exemplo de regra de reprecificação inteligente - preço mínimo](assets/ob-intelligent-pricde-rule-floor-price.png){width="600" zoomable="yes"}

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Floor Price Source] | Escolha o [!DNL Commerce] atributo que indica seu limite mínimo relativo (preço mais baixo). Por exemplo, se você não quiser que o preço de tabela do Amazon fique abaixo do custo do item, escolha a opção `Cost` atributo. |
| [!UICONTROL Floor Price Action] | Escolha uma ação de ajuste de preço. Opções:<ul><li>**[!UICONTROL Decrease By]** - Escolha quando deseja definir o _[!UICONTROL Floor Price Source]_valor a ser ajustado para baixo, criando um preço mínimo mais baixo para a regra, antes de listar na Amazon.</li><li>**[!UICONTROL Increase By]** - Escolha quando deseja definir o _[!UICONTROL Floor Price Source]_valor a ser ajustado, criando um preço mínimo mais alto para a regra, antes de listar na Amazon.</li><li>**[!UICONTROL Match]** - Escolha quando não deseja que o preço de tabela flutue abaixo do valor definido _[!UICONTROL Floor Price Source]_valor. Quando escolhido, o_[!UICONTROL Apply]_ e _[!UICONTROL Floor Adjustment Amount]_Os campos do estão desativados.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Um ajuste percentual em relação ao _[!UICONTROL Floor Price Source]_valor. |
| [!UICONTROL Floor Adjustment Amount] | Insira o valor numérico para o percentual a ser ajustado _[!UICONTROL Floor Price Source]_valor. |
