---
title: "Regra Inteligente de Reprecificação: Preço Máximo Opcional"
description: Use configurações opcionais de preço máximo para proteger seu preço de produto mais alto contra as regras de preços inteligentes que gerenciam suas listas do Amazon.
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '387'
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

Defina suas configurações opcionais de preço mais alto na _[!UICONTROL Optional Ceiling Price]_seção.

1. Para **[!UICONTROL Ceiling Price Source]**, escolha um atributo.

   Selecione o [!DNL Commerce] [atributo de produto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) isso indica seu limite máximo relativo. Por exemplo, se você não quiser que o preço de listagem do Amazon fique acima do MSRP do seu item, escolha o `Manufacturer's Suggested Retail Price` atributo.

1. Para **[!UICONTROL Ceiling Price Action]**, escolha uma opção.

   - `Decrease By` - Escolha quando deseja definir o _[!UICONTROL Ceiling Price Source]_valor a ser ajustado para baixo, criando um preço máximo mais baixo para a regra, antes de listar na Amazon.

   - `Increase By` - Escolha quando deseja definir o _[!UICONTROL Ceiling Price Source]_valor a ser ajustado, criando um preço máximo mais alto para a regra, antes de listar na Amazon.

   - `Match` - Escolha quando não deseja que o preço de tabela flutue acima do valor definido _[!UICONTROL Ceiling Price Source]_valor. Quando definido como `Match`, o_[!UICONTROL Apply]_ e _[!UICONTROL Ceiling Adjustment Amount]_Os campos do estão desativados.

1. Deixe a **[!UICONTROL Apply]** padrão como `Apply as percentage`.

1. Para **[!UICONTROL Ceiling Adjustment Price]**, insira o valor numérico para o percentual para ajustar _[!UICONTROL Ceiling Price Source]_valor.

Neste exemplo, o preço máximo está definido como 2% abaixo do MSRP do item.

![Regra inteligente de reavaliação de preços - preço máximo opcional](assets/ob-intelligent-price-rule-ceiling.png){width="600" zoomable="yes"}

| Campo | Descrição |
|---|---|
| [!UICONTROL Ceiling Price Source] | Escolha o [!DNL Commerce] [atributo de produto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) isso indica seu limite máximo relativo. Por exemplo, se você não quiser que o preço da lista de produtos fique acima do MSRP do seu item, escolha a opção `Manufacturer's Suggested Retail Price` atributo. |
| [!UICONTROL Ceiling Price Action] | Escolha uma ação de ajuste de preço. Opções:<ul><li>**[!UICONTROL Decrease By]** - Escolha quando deseja definir o _[!UICONTROL Ceiling Price Source]_valor a ser ajustado para baixo, criando um preço máximo mais baixo para a regra, antes de listar na Amazon.</li><li>**[!UICONTROL Increase By]** - Escolha quando deseja definir o _[!UICONTROL Ceiling Price Source]_valor a ser ajustado, criando um preço máximo mais alto para a regra, antes de listar na Amazon.</li><li>**[!UICONTROL Match]** - Escolha quando não deseja que o preço de tabela flutue acima do valor definido _[!UICONTROL Ceiling Price Source]_valor. Quando definido como `Match`, o_[!UICONTROL Apply]_ e _[!UICONTROL Ceiling Adjustment Amount]_Os campos do estão desativados.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Um ajuste percentual em relação ao _[!UICONTROL Ceiling Price Source]_valor. |
| [!UICONTROL Ceiling Price Adjustment] | Insira o valor numérico para o percentual a ser ajustado _[!UICONTROL Ceiling Price Source]_valor. |
