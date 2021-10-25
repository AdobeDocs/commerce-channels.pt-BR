---
title: Lógica de Prioridade de Preço
description: O canal de vendas da Amazon aplica priorização ao determinar o preço publicado de uma listagem da Amazon.
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 4%

---

# Lógica de prioridade de preço

No exemplo a seguir, como o sistema determina se você deve publicar $31.99, $24.99 ou $27.99?

![Escopo do preço do comércio](assets/amazon-price-scope.png)

Para determinar qual preço é usado se um produto estiver em dois sites e tiver um preço por site variável, use a lógica de prioridade de preço (determinada pela variável [Ordem de classificação](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target=&quot;_blank&quot;} valor).

Para exibir a ordem de classificação das suas lojas, acesse **[!UICONTROL Stores]** > **[!UICONTROL All Stores]** no _Administrador_ barra lateral. No _[!UICONTROL Web Site]_, clique no nome do site. O_[!UICONTROL Web Site Information]_ mostra a _[!UICONTROL Sort Order]_para o site, que determina a prioridade do site. Um valor de `1` indica a prioridade mais alta.

Se o preço do produto estiver definido como `Use Default`, ele volta ao valor de preço padrão em vez do valor de preço do site.

## Exemplo 1

|  | Prioridade do site | Preço (Site) | Usar padrão |
|---|---|---|---|
| Padrão | 0 | US$ 31,99 | — |
| Loja 1 | 1 | US$ 24,99 | Não |
| Loja 2 | 2 | US$ 27,99 | Sim |

- O **[!UICONTROL Magento Price Source]** (definido em [Preço de Listagem](./listing-price.md) é definido como `Price` atributo.
- Examine o site com a maior prioridade de site, que é a Loja 1 (definida pela variável [Ordem de classificação](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target=&quot;_blank&quot;} valor).
- Como a Loja 1 está definida para usar o preço do site (Usar Padrão = Não), o preço publicado é de $24,99.

## Exemplo 2

|  | Prioridade do site | Site de preços | Usar padrão |
|---|---|---|---|
| Padrão | 0 | US$ 31,99 | — |
| Loja 1 | 1 | US$ 24,99 | Sim |
| Loja 2 | 2 | US$ 27,99 | Não |

- O **[!UICONTROL Magento Price Source]** (definido em [Preço de Listagem](./listing-price.md) é definido como `Price` atributo.
- Examine o site com a maior prioridade de site, que é a Loja 1 (definida pela variável [ordenar ordem](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target=&quot;_blank&quot;} valor).
- Desde a Loja 1 **não é** definido para usar o preço do site (Usar Padrão = Sim), olhe o próximo site na ordem de classificação.
- Desde a Loja 2 **é** definido para usar o preço do site (Usar Padrão = Não), o preço publicado é de $27,99.

## Exemplo 3

|  | Prioridade do site | Site de preços | Usar padrão |
|---|---|---|---|
| Padrão | 0 | US$ 31,99 | US$ 30,00 |
| Loja 1 | 1 | US$ 24,99 | — |
| Loja 2 | 2 | US$ 27,99 | US$ 20,00 |

Este exemplo adiciona o valor que não é de preço, que é usado se você selecionar outro valor para o _[!UICONTROL Magento Price Source_] (definido em [Preço de Listagem](./listing-price.md) configurações). O valor que não é de preço sempre usa preço como o preço de fallback.

- O **[!UICONTROL Magento Price Source]** (definido em [[!UICONTROL Listing Price]](./listing-price.md) está definida como `Non-Price`.
- Examine o site com a maior prioridade de site, que é `Store 1`(definido pelo [Ordem de classificação](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target=&quot;_blank&quot;} valor).
- Desde a Loja 1 **não é** defina para usar o `Non-Price` , veja o próximo site na ordem de classificação.
- Desde a Loja 2 **é** defina para usar o `Non-Price` atributo (não preço) [Site] = US$ 20,00), o preço publicado é US$ 20,00.
