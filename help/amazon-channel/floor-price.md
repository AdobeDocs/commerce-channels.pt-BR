---
title: "Regra de Reprecificação Inteligente: Preço Mínimo"
description: Use as configurações de preço mínimo para determinar o preço mais baixo de uma regra de preço inteligente para gerenciar suas listagens do Amazon.
feature: Sales Channels, Price Rules
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Regra de Reprecificação Inteligente: Preço Mínimo

As seções de uma regra de reavaliação inteligente incluem:

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

As configurações de [preço mínimo](./floor-price.md) protegem automaticamente o preço mais baixo do produto contra as regras de preços inteligentes. Use essas configurações para definir um limite mínimo (preço mais baixo) para suas regras de preços inteligentes, garantindo que seus produtos não sejam listados abaixo do preço desejado.

Os atributos de preço mínimo são baseados no escopo do site se a sua loja [!DNL Commerce] estiver usando o escopo de preços do site. Consulte [Escopo de Preços](./price-scope.md).

Preço mínimo só é usado quando **[!UICONTROL Rule Type]** está definido como `Intelligent repricing rule`.

## Configurar preço mínimo

Defina sua configuração de preço mais baixo na seção _[!UICONTROL Floor Price]_.

1. Para **[!UICONTROL Floor Price Source]**, escolha um atributo de origem de preço.

   Escolha o [!DNL Commerce] [atributo de produto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) que indica seu limite mínimo relativo. Por exemplo, se você não quiser que o preço de sua lista do Amazon fique abaixo do custo do seu item, escolha o atributo *Custo*.

1. Para **[!UICONTROL Floor Price Action]**, escolha uma opção.

   - `Decrease By` - Escolha quando deseja que o valor _[!UICONTROL Floor Price Source]_definido seja ajustado para baixo, criando um preço inferior para a regra, antes de listar na Amazon.

   - `Increase By` - Escolha quando deseja que o valor _[!UICONTROL Floor Price Source]_definido seja ajustado, criando um preço mínimo mais alto para a regra, antes de listar na Amazon.

   - `Match` - Escolha quando não deseja que o preço de lista flutue abaixo do valor _[!UICONTROL Floor Price Source]_definido. Quando definido como `Match`, os campos_[!UICONTROL Apply]_ e _[!UICONTROL Floor Adjustment Amount]_são desabilitados.

1. Deixe o padrão **[!UICONTROL Apply]** como `Apply as percentage`.

1. Para **[!UICONTROL Floor Adjustment Price]**, insira o valor numérico da porcentagem para ajustar o valor de _[!UICONTROL Floor Price Source]_.

Neste exemplo, o preço mínimo está definido como 3% acima do custo do item.

![Exemplo de regra de reavaliação de preço inteligente - preço mínimo](assets/ob-intelligent-pricde-rule-floor-price.png){width="600" zoomable="yes"}

| Campo | Descrição |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Floor Price Source] | Escolha o atributo [!DNL Commerce] que indica seu limite mínimo relativo (preço mais baixo). Por exemplo, se você não quiser que o preço de sua lista do Amazon fique abaixo do custo do seu item, escolha o atributo `Cost`. |
| [!UICONTROL Floor Price Action] | Escolha uma ação de ajuste de preço. Opções:<ul><li>**[!UICONTROL Decrease By]** - Escolha quando deseja que o valor _[!UICONTROL Floor Price Source]_definido seja ajustado para baixo, criando um preço inferior para a regra, antes de listar na Amazon.</li><li>**[!UICONTROL Increase By]** - Escolha quando deseja que o valor _[!UICONTROL Floor Price Source]_definido seja ajustado, criando um preço mínimo mais alto para a regra, antes de listar na Amazon.</li><li>**[!UICONTROL Match]** - Escolha quando não deseja que o preço de lista flutue abaixo do valor _[!UICONTROL Floor Price Source]_definido. Quando escolhidos, os campos_[!UICONTROL Apply]_ e _[!UICONTROL Floor Adjustment Amount]_são desabilitados.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Um ajuste de porcentagem relativo ao valor _[!UICONTROL Floor Price Source]_. |
| [!UICONTROL Floor Adjustment Amount] | Insira o valor numérico para a porcentagem para ajustar o valor _[!UICONTROL Floor Price Source]_. |
