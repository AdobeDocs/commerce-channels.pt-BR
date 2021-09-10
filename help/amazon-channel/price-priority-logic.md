---
title: Lógica de Prioridade de Preço
description: O canal de vendas da Amazon aplica priorização ao determinar o preço publicado de uma listagem da Amazon.
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 4%

---

# Lógica de prioridade de preço

No exemplo a seguir, como o sistema determina se você deve publicar $31.99, $24.99 ou $27.99?

![Escopo do preço do comércio](assets/amazon-price-scope.png)

Para determinar qual preço é usado se um produto estiver em dois sites e tiver um preço por site variável, use a lógica de prioridade de preço (determinada pelo valor [Ordenar Ordem](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;} ).

Para exibir a ordem de classificação das suas lojas, vá para **[!UICONTROL Stores]** > **[!UICONTROL All Stores]** na barra lateral _Admin_. Na coluna _[!UICONTROL Web Site]_, clique no nome do site. A página_[!UICONTROL Web Site Information]_ mostra a configuração _[!UICONTROL Sort Order]_do site, que determina a prioridade do site. Um valor de `1` indica a prioridade mais alta.

Se o preço do produto for definido como `Use Default`, ele voltará para o valor padrão do preço em vez do valor do preço do site.

## Exemplo 1

|  | Prioridade do site | Preço (Site) | Usar padrão |
|---|---|---|---|
| Padrão | 0 | US$ 31,99 | — |
| Loja 1 | 1 | US$ 24,99 | Não |
| Loja 2 | 2 | US$ 27,99 | Sim |

- O **[!UICONTROL Magento Price Source]** (definido em seu [Preço de Listagem](./listing-price.md) é definido para o atributo `Price`.
- Examine o site com a maior prioridade de site, que é a Loja 1 (definida pelo valor [Ordenar](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;} ).
- Como a Loja 1 está definida para usar o preço do site (Usar Padrão = Não), o preço publicado é de $24,99.

## Exemplo 2

|  | Prioridade do site | Site de preços | Usar padrão |
|---|---|---|---|
| Padrão | 0 | US$ 31,99 | — |
| Loja 1 | 1 | US$ 24,99 | Sim |
| Loja 2 | 2 | US$ 27,99 | Não |

- O **[!UICONTROL Magento Price Source]** (definido em seu [Preço de Listagem](./listing-price.md) é definido para o atributo `Price`.
- Examine o site com a maior prioridade de site, que é a Loja 1 (definida pelo valor [sort order](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;} ).
- Como a Loja 1 **não é** definida para usar o preço do site (Usar Padrão = Sim), olhe para o próximo site na ordem de classificação.
- Como a Loja 2 **é** definida para usar o preço do site (Usar Padrão = Não), o preço publicado é $27,99.

## Exemplo 3

|  | Prioridade do site | Site de preços | Usar padrão |
|---|---|---|---|
| Padrão | 0 | US$ 31,99 | US$ 30,00 |
| Loja 1 | 1 | US$ 24,99 | — |
| Loja 2 | 2 | US$ 27,99 | US$ 20,00 |

Este exemplo adiciona o valor que não é de preço, que é usado se você selecionar outro valor para o _[!UICONTROL Magento Price Source_] (definido nas configurações de [Preço de Listagem](./listing-price.md)). O valor que não é de preço sempre usa preço como o preço de fallback.

- O **[!UICONTROL Magento Price Source]** (definido nas configurações [[!UICONTROL Listing Price]](./listing-price.md)) é definido como `Non-Price`.
- Examine o site com a prioridade mais alta do site, que é `Store 1`(definido pelo valor [Ordenar](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;}).
- Como a Loja 1 **não é** definida para usar o atributo `Non-Price`, olhe para o próximo site na ordem de classificação.
- Como a Loja 2 **é** definida para usar o atributo `Non-Price` (Não-Preço [Site] = $20,00), o preço publicado é $20,00.
