---
title: Canal de vendas da Amazon - Lógica de prioridade de preço
description: O canal de vendas da Amazon aplica priorização ao determinar o preço publicado para uma lista do Amazon.
feature: Sales Channels, Price Rules
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 2%

---

# Lógica de prioridade de preço

No exemplo a seguir, como o sistema determina se você deve publicar US$ 31,99, US$ 24,99 ou US$ 27,99?

![escopo de preços do Commerce](assets/amazon-price-scope.png){width="400"}

Para determinar qual preço será usado se um produto estiver em dois sites e tiver um preço variável por site, use a lógica de prioridade de preço (determinada pelo valor [Ordem de classificação](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html)).

Para exibir a ordem de classificação das suas lojas, vá para **[!UICONTROL Stores]** > **[!UICONTROL All Stores]** na barra lateral _Admin_. Na coluna _[!UICONTROL Web Site]_, clique no nome do site. A página_[!UICONTROL Web Site Information]_ mostra a configuração _[!UICONTROL Sort Order]_do site, que determina a prioridade do site. Um valor de `1` indica a prioridade mais alta.

Se o preço do produto estiver definido como `Use Default`, ele voltará ao valor de preço padrão em vez do valor de preço do site.

## Exemplo 1

|         | Prioridade do site | Preço (Site) | Usar padrão |
|---------|------------------|-----------------|-------------|
| Padrão | 0 | $ 31,99 | — |
| Loja 1 | 1 | $ 24,99 | Não |
| Loja 2 | 2 | $ 27,99 | Sim |

- O **[!UICONTROL Magento Price Source]** (definido em seu [Preço de Listagem](./listing-price.md) está definido como o atributo `Price`.
- Examine o site com a prioridade mais alta, que é a Loja 1 (definida pelo valor [Ordem de classificação](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html)).
- Como a Loja 1 está definida para usar o preço do site (Usar padrão = Não), o preço publicado é de US$ 24,99.

## Exemplo 2

|         | Prioridade do site | Preço do site | Usar padrão |
|---------|------------------|---------------|-------------|
| Padrão | 0 | $ 31,99 | — |
| Loja 1 | 1 | $ 24,99 | Sim |
| Loja 2 | 2 | $ 27,99 | Não |

- O **[!UICONTROL Magento Price Source]** (definido em seu [Preço de Listagem](./listing-price.md) está definido como o atributo `Price`.
- Examine o site com a prioridade mais alta, que é a Loja 1 (definida pelo valor [ordem de classificação](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html)).
- Como a Loja 1 **não** está definida para usar o preço do site (Usar Padrão = Sim), verifique o próximo site na ordem de classificação.
- Como a Loja 2 **está** definida para usar o preço do site (Usar Padrão = Não), o preço publicado é de $27,99.

## Exemplo 3

|         | Prioridade do site | Preço do site | Usar padrão |
|---------|------------------|---------------|-------------|
| Padrão | 0 | $ 31,99 | $ 30,00 |
| Loja 1 | 1 | $ 24,99 | — |
| Loja 2 | 2 | $ 27,99 | $ 20,00 |

Este exemplo adiciona o valor sem preço, que é usado se você selecionar outro valor para o _[!UICONTROL Magento Price Source_] (definido nas configurações de [Preço de Listagem](./listing-price.md)). O valor sem preço sempre usa preço como preço de fallback.

- O **[!UICONTROL Magento Price Source]** (definido nas configurações de [[!UICONTROL Listing Price]](./listing-price.md)) está definido como `Non-Price`.
- Examine o site com a prioridade mais alta, que é `Store 1`(definida pelo valor [Ordem de Classificação](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html)).
- Como a Loja 1 **não está** definida para usar o atributo `Non-Price`, verifique o próximo site na ordem de classificação.
- Como a Loja 2 **está** definida para usar o atributo `Non-Price` (Não é Preço [Site] = $20,00), o preço publicado é $20,00.
