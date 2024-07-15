---
title: "Regra Inteligente de Reprecificação: Preço Máximo Opcional"
description: Use configurações opcionais de preço máximo para proteger seu preço de produto mais alto contra as regras de preços inteligentes que gerenciam suas listas do Amazon.
feature: Sales Channels, Price Rules
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: b2e608a633b760672044653a22be757ecffc9540
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# Regra de Reprecificação Inteligente: Preço de Teto Opcional

As seções de uma regra de reavaliação inteligente incluem:

- [Selecionar tipo de regra](./intelligent-repricing-rules.md)
- [Variações condicionais do concorrente](./competitor-conditional-variances.md)
- [Ajuste de Preço](./price-adjustment.md)
- [Preço mínimo](./floor-price.md)
- Preço máximo opcional

As configurações automatizadas de preço máximo protegem automaticamente o preço mais alto do seu produto contra as regras de preços inteligentes, permitindo que você defina um teto (preço mais alto) para suas regras de preços inteligentes.

## Configurar preço máximo opcional

Defina suas configurações opcionais de preço mais alto na seção _[!UICONTROL Optional Ceiling Price]_.

1. Para **[!UICONTROL Ceiling Price Source]**, escolha um atributo.

   Selecione seu [!DNL Commerce] [atributo de produto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) que indica seu limite máximo relativo. Por exemplo, se você não quiser que o preço de listagem do Amazon fique acima do MSRP do seu item, escolha o atributo `Manufacturer's Suggested Retail Price`.

1. Para **[!UICONTROL Ceiling Price Action]**, escolha uma opção.

   - `Decrease By` - Escolha quando deseja que o valor _[!UICONTROL Ceiling Price Source]_definido seja ajustado para baixo, criando um preço máximo mais baixo para a regra, antes de listar na Amazon.

   - `Increase By` - Escolha quando deseja que o valor _[!UICONTROL Ceiling Price Source]_definido seja ajustado, criando um preço máximo mais alto para a regra, antes de listar na Amazon.

   - `Match` - Escolha quando não deseja que o preço de lista flutue acima do valor _[!UICONTROL Ceiling Price Source]_definido. Quando definido como `Match`, os campos_[!UICONTROL Apply]_ e _[!UICONTROL Ceiling Adjustment Amount]_são desabilitados.

1. Deixe o padrão **[!UICONTROL Apply]** como `Apply as percentage`.

1. Para **[!UICONTROL Ceiling Adjustment Price]**, insira o valor numérico da porcentagem para ajustar o valor de _[!UICONTROL Ceiling Price Source]_.

Neste exemplo, o preço máximo está definido como 2% abaixo do MSRP do item.

![Regra inteligente de reavaliação de preços - preço máximo opcional](assets/ob-intelligent-price-rule-ceiling.png){width="600" zoomable="yes"}

| Campo | Descrição |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Ceiling Price Source] | Escolha o [!DNL Commerce] [atributo de produto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) que indica seu limite máximo relativo. Por exemplo, se você não quiser que o preço da lista de produtos fique acima do MSRP do seu item, escolha o atributo `Manufacturer's Suggested Retail Price`. |
| [!UICONTROL Ceiling Price Action] | Escolha uma ação de ajuste de preço. Opções:<ul><li>**[!UICONTROL Decrease By]** - Escolha quando deseja que o valor _[!UICONTROL Ceiling Price Source]_definido seja ajustado para baixo, criando um preço máximo mais baixo para a regra, antes de listar na Amazon.</li><li>**[!UICONTROL Increase By]** - Escolha quando deseja que o valor _[!UICONTROL Ceiling Price Source]_definido seja ajustado, criando um preço máximo mais alto para a regra, antes de listar na Amazon.</li><li>**[!UICONTROL Match]** - Escolha quando não deseja que o preço de lista flutue acima do valor _[!UICONTROL Ceiling Price Source]_definido. Quando definido como `Match`, os campos_[!UICONTROL Apply]_ e _[!UICONTROL Ceiling Adjustment Amount]_são desabilitados.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Um ajuste de porcentagem relativo ao valor _[!UICONTROL Ceiling Price Source]_. |
| [!UICONTROL Ceiling Price Adjustment] | Insira o valor numérico para a porcentagem para ajustar o valor _[!UICONTROL Ceiling Price Source]_. |
