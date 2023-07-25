---
title: Canal de vendas da Amazon - Lógica de prioridade de preço
description: O canal de vendas da Amazon aplica priorização ao determinar o preço publicado para uma lista do Amazon.
feature: Sales Channels, Price Rules
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 4%

---

# Lógica de prioridade de preço

No exemplo a seguir, como o sistema determina se você deve publicar US$ 31,99, US$ 24,99 ou US$ 27,99?

![Escopo do preço de comércio](assets/amazon-price-scope.png){width="400"}

Para determinar qual preço é usado se um produto estiver em dois sites e tiver um preço variável por site, use a lógica de prioridade de preço (determinada pela variável [Ordem de classificação](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) valor).

Para exibir a ordem de classificação de suas lojas, acesse **[!UICONTROL Stores]** > **[!UICONTROL All Stores]** no _Admin_ barra lateral. No _[!UICONTROL Web Site]_clique no nome do site. A variável_[!UICONTROL Web Site Information]_ mostra a _[!UICONTROL Sort Order]_para o site, que determina a prioridade do site. Um valor de `1` indica a prioridade mais alta.

Se o preço do produto estiver definido como `Use Default`, ele retorna ao valor de preço padrão em vez do valor de preço do site.

## Exemplo 1

|         | Prioridade do site | Preço (Site) | Usar padrão |
|---------|------------------|-----------------|-------------|
| Padrão | 0 | $31.99 | -- |
| Loja 1 | 1 | $24.99 | Não |
| Loja 2 | 2 | $27.99 | Sim |

- A variável **[!UICONTROL Magento Price Source]** (definido em seu [Preço de Listagem](./listing-price.md) está definido como `Price` atributo.
- Verifique o site com a prioridade mais alta, que é a Loja 1 (definida pela [Ordem de classificação](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) valor).
- Como a Loja 1 está definida para usar o preço do site (Usar padrão = Não), o preço publicado é de US$ 24,99.

## Exemplo 2

|         | Prioridade do site | Preço do site | Usar padrão |
|---------|------------------|---------------|-------------|
| Padrão | 0 | $31.99 | -- |
| Loja 1 | 1 | $24.99 | Sim |
| Loja 2 | 2 | $27.99 | Não |

- A variável **[!UICONTROL Magento Price Source]** (definido em seu [Preço de Listagem](./listing-price.md) está definido como `Price` atributo.
- Verifique o site com a prioridade mais alta, que é a Loja 1 (definida pela [ordem de classificação](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) valor).
- Desde a Loja 1 **não é** Defina para usar o preço do site (Usar padrão = Sim), verifique o próximo site na ordem de classificação.
- Desde a Loja 2 **é** Definido para usar o preço do site (Usar padrão = Não), o preço publicado é de US$ 27,99.

## Exemplo 3

|         | Prioridade do site | Preço do site | Usar padrão |
|---------|------------------|---------------|-------------|
| Padrão | 0 | $31.99 | $30.00 |
| Loja 1 | 1 | $24.99 | -- |
| Loja 2 | 2 | $27.99 | $20.00 |

Esse exemplo adiciona o valor não relacionado ao preço, que é usado se você selecionar outro valor para o _[!UICONTROL Magento Price Source_] (definido em seu [Preço de Listagem](./listing-price.md) configurações). O valor sem preço sempre usa preço como preço de fallback.

- A variável **[!UICONTROL Magento Price Source]** (definido em [[!UICONTROL Listing Price]](./listing-price.md) configurações) está definida como `Non-Price`.
- Examine o site com a prioridade mais alta, que é `Store 1`(definido pela [Ordem de classificação](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) valor).
- Desde a Loja 1 **não é** defina para usar o `Non-Price` atributo, verifique o próximo site na ordem de classificação.
- Desde a Loja 2 **é** defina para usar o `Non-Price` atributo (Não-Preço [Site] = US$ 20,00), o preço publicado é US$ 20,00.
