---
title: '"Regra de Reprecificação Inteligente: Preço Limite Opcional'''
description: Use as configurações opcionais de preço de teto para proteger seu preço de produto mais alto contra as regras de preços inteligentes que gerenciam suas listagens do Amazon.
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Regra inteligente de reprecificação: preço máximo opcional

As seções de uma regra inteligente de redefinição de preços incluem:

- [Selecionar tipo de regra](./intelligent-repricing-rules.md)
- [Variáveis condicionais do concorrente](./competitor-conditional-variances.md)
- [Ajuste de preço](./price-adjustment.md)
- [Preço Limite](./floor-price.md)
- Preço Limite Opcional

As configurações automatizadas de preço de teto protegem automaticamente seu preço de produto mais alto em relação às regras de preços inteligentes, permitindo que você defina um limite (preço mais alto) para suas regras de preços inteligentes.

## Configurar o preço máximo opcional

Defina suas configurações de preço mais alto opcionais na _[!UICONTROL Optional Ceiling Price]_seção.

1. Para **[!UICONTROL Ceiling Price Source]**, escolha um atributo.

   Selecione seu [!DNL Commerce] [atributo do produto](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} que indica o limite de teto relativo. Por exemplo, se você não quiser que o preço de listagem da Amazon ultrapasse o MSRP do seu item, escolha a variável `Manufacturer's Suggested Retail Price` atributo.

1. Para **[!UICONTROL Ceiling Price Action]**, escolha uma opção.

   - `Decrease By` - Escolha quando deseja definir _[!UICONTROL Ceiling Price Source]_valor a ser ajustado, criando um preço limite mais baixo para a regra, antes de listar para o Amazon.

   - `Increase By` - Escolha quando deseja definir _[!UICONTROL Ceiling Price Source]_valor a ser ajustado, criando um preço limite mais alto para a regra, antes de listar para a Amazon.

   - `Match` - Escolha quando você não deseja que o preço da listagem flutue acima do valor definido _[!UICONTROL Ceiling Price Source]_valor. Quando definido como `Match`, o_[!UICONTROL Apply]_ e _[!UICONTROL Ceiling Adjustment Amount]_os campos estão desativados.

1. Deixe o **[!UICONTROL Apply]** padrão como `Apply as percentage`.

1. Para **[!UICONTROL Ceiling Adjustment Price]**, insira o valor numérico da porcentagem para ajustar a _[!UICONTROL Ceiling Price Source]_valor.

Neste exemplo, o preço limite é fixado em 2% abaixo do MSRP do item.

![Regra de reprecificação inteligente - preço máximo opcional](assets/ob-intelligent-price-rule-ceiling.png)

| Campo | Descrição |
|---|---|
| [!UICONTROL Ceiling Price Source] | Escolha a [!DNL Commerce] [atributo do produto](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} que indica o limite de teto relativo. Por exemplo, se você não quiser que o preço da listagem de produtos ultrapasse o MSRP do seu item, escolha a variável `Manufacturer's Suggested Retail Price` atributo. |
| [!UICONTROL Ceiling Price Action] | Escolha uma ação de ajuste de preço. Opções:<ul><li>**[!UICONTROL Decrease By]** - Escolha quando deseja definir _[!UICONTROL Ceiling Price Source]_valor a ser ajustado, criando um preço limite mais baixo para a regra, antes de listar para o Amazon.</li><li>**[!UICONTROL Increase By]** - Escolha quando deseja definir _[!UICONTROL Ceiling Price Source]_valor a ser ajustado, criando um preço limite mais alto para a regra, antes de listar para a Amazon.</li><li>**[!UICONTROL Match]** - Escolha quando você não deseja que o preço da listagem flutue acima do valor definido _[!UICONTROL Ceiling Price Source]_valor. Quando definido como `Match`, o_[!UICONTROL Apply]_ e _[!UICONTROL Ceiling Adjustment Amount]_os campos estão desativados.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Um ajustamento percentual em relação ao valor de _[!UICONTROL Ceiling Price Source]_valor. |
| [!UICONTROL Ceiling Price Adjustment] | Insira o valor numérico da porcentagem para ajustar a _[!UICONTROL Ceiling Price Source]_valor. |
