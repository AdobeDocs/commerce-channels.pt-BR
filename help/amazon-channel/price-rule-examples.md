---
title: Exemplos de regras de preço
description: Para ajudar você a projetar suas regras de preços para listagens do Amazon, analise estes exemplos com base em cenários comuns.
exl-id: 4d9717ba-4ad6-468d-b4ca-99f8620b60b4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Exemplos de regras de preço

## Exemplos de regras de preço padrão

### Descartar Regras Subsequentes

A capacidade de descartar regras subsequentes é um excelente recurso dentro das regras de preços que impede que várias regras de preços sejam empilhadas e oferece descontos adicionais não intencionais. Para descartar regras subsequentes, uma regra de precificação deve usar as prioridades definidas na seção _[!UICONTROL Priority]_de [Configurações Gerais da Regra de Precificação](./pricing-rule-general-settings.md).

Se **[!UICONTROL Discard Subsequent Rules]** for definido como `Yes`, as regras com prioridade mais baixa (números mais altos) não se aplicam aos produtos elegíveis.

Por exemplo, digamos que existam três regras de preços:

| Exemplo | Nome da regra | Prioridade | Descartar Regra Subsequente |
|----------|----|----|----|
| 1 | 10% de produtos vendidos | 1 | Não |
| 2 | US$ 2 produtos fora da venda | 2 | Sim |
| 1 | 5% de desconto em todos os produtos | 1 | Não |

Neste cenário, as regras 1 e 2 se aplicam aos produtos qualificados. A regra nº 3 se aplica somente a produtos qualificados não contidos na regra nº 2, pois tem prioridade mais baixa que o exemplo nº 2 e **[!UICONTROL Discard Subsequent Rules]** está definido como `Yes`. Portanto, os produtos qualificados na categoria de venda receberiam um desconto de 10% e $2 do preço de listagem da Amazon.

### Aplicação de duas regras de preço padrão

| Campo | Configuração - Regra 1 | Configuração - Regra 2 |
|----------|----|----|
| [!UICONTROL Rule Name] | Regra 1 | Regra 2 |
| [!UICONTROL Priority] | 1 | 2 |
| [!UICONTROL Rule Type] | Regra de preço padrão | Regra de preço padrão |
| [!UICONTROL Price action] | Diminuir por | Diminuir por |
| [!UICONTROL Apply] | Aplicar como porcentagem | Aplicar como valor fixo |
| [!UICONTROL Adjustment Amount] | 10º | 10º |

#### Produto 1

Preço: US$ 45,49

Regra 1: $45,49 x (0,9) = $40,94

Regra 2: $40,94 - $10,00 = $30,94

O preço final após a aplicação do artigo 1.o e do artigo 2.o é o seguinte: US$ 30,94

#### Produto 2

Preço: US$ 47,76

Regra 1: $47,76 x (0,9) = $42,98

Regra 2: $42,98 - $10,00 = $32,98

Aplica-se o preço final após a regra 1 e a regra 2: US$ 32,98

## Exemplos de regras de reprecificação inteligentes

### Preço Buy Box com Origem de Preço Limite = Preço

| Campo | Configuração |
|----------|----|
| [!UICONTROL Rule Name] | Regra 1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Regra de reprecificação inteligente |
| [!UICONTROL Competitor Price Source] | Usar preço de &quot;Buy Box&quot; |
| [!UICONTROL Price Action] | Corresponder preço do concorrente |
| [!UICONTROL Floor Price Source] | Preço |
| [!UICONTROL Floor Price Action] | Corresponder |

#### Produto 1

Preço: US$ 15

[Compre ](./buy-box-competitor-pricing.md) Boxprice da Amazon: US$ 10

Como o preço [Buy Box](./buy-box-competitor-pricing.md) é menor que o preço original, o produto é listado pelo preço original.

O preço final após a aplicação da regra: US$ 15

#### Produto 2

Preço: US$ 5

[Compre ](./buy-box-competitor-pricing.md) Boxprice da Amazon: US$ 10

Como o preço [Buy Box](./buy-box-competitor-pricing.md) é maior que o preço original, o produto é listado no preço [Buy Box](./buy-box-competitor-pricing.md).

O preço final após a aplicação da regra: US$ 10

### Preço Buy Box com Origem de Preço Limite = Preço e uma diminuição de preço de 20%

| Campo | Configuração |
|----------|----|
| [!UICONTROL Rule Name] | Regra 1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Regra de reprecificação inteligente |
| [!UICONTROL Competitor Price Source] | Usar preço de &quot;Buy Box&quot; |
| [!UICONTROL Price Action] | Corresponder preço do concorrente |
| [!UICONTROL Floor Price Source] | Preço |
| [!UICONTROL Floor Price Action] | Diminuir por |
| [!UICONTROL Apply] | Aplicar como uma porcentagem |
| [!UICONTROL Floor Adjustment Amount] | 20º |

#### Produto 1

Preço: US$ 20

Preço de Limite Calculado: US$ 16

[Compre ](./buy-box-competitor-pricing.md) Boxprice da Amazon: US$ 15

Como o preço [Buy Box](./buy-box-competitor-pricing.md) é menor que o preço Calculado [Preço de Chão](./floor-price.md), o produto é listado no [Preço de Chão](./floor-price.md) Calculado.

O preço final após a aplicação da regra: US$ 16

#### Produto 2

Preço: US$ 15

Calculado [Preço Limite](./floor-price.md): US$ 12

[Compre ](./buy-box-competitor-pricing.md) Boxprice da Amazon: US$ 15

Como o preço [Buy Box](./buy-box-competitor-pricing.md) é maior que o preço Calculado [Preço Limite de Chão](./floor-price.md), o produto é listado no preço [Buy Box](./buy-box-competitor-pricing.md).

O preço final após a aplicação da regra: US$ 15

#### Product 3

Preço: US$ 17

Preço de Limite Calculado: US$ 13,60

[Compre ](./buy-box-competitor-pricing.md) Boxprice da Amazon: US$ 15

Como o preço [Buy Box](./buy-box-competitor-pricing.md) é maior que o preço Calculado [Preço Limite de Chão](./floor-price.md), o produto é listado no preço [Buy Box](./buy-box-competitor-pricing.md).

O preço final após a aplicação da regra: US$ 15

### Preço mais baixo com todos os preços do concorrente e utilizar todas as condições do produto do concorrente

| Campo | Configuração |
|----------|-----|
| [!UICONTROL Rule Name] | Regra 1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Regra de reprecificação inteligente |
| [!UICONTROL Competitor Price Source] | Usar o menor preço do concorrente |
| [!UICONTROL Minimum Positive Feedback] | Todos os preços do concorrente |
| [!UICONTROL Conditional Variance] | Usar todas as condições de produto do concorrente |
| [!UICONTROL Price Action] | Corresponder preço do concorrente |
| [!UICONTROL Floor Price Source] | Preço |
| [!UICONTROL Floor Price Action] | Corresponder |

| Preço | Condição |
|----------|----|
| US$ 17 | Novo |
| US$ 15 | Novo |
| US$ 14 | Usado; Muito bom |
| US$ 13 | Usado; Good |

#### Produto 1

Preço: US$ 10

Condição: Novo

Como o preço mais baixo do concorrente para a Nova condição é de US$ 15, o produto é listado em US$ 15.

O preço final após a aplicação da regra: US$ 15

#### Produto 2

Preço: US$ 10

Condição: Usado; Aceitável

Como o [menor preço do concorrente](./lowest-competitor-pricing.md) para a condição Usada é de $13, o produto é listado em $13.

O preço final após a aplicação da regra: US$ 13

### Regra inteligente de reprecificação combinando preço limite, conversão de moeda e IVA

| Campo | Configuração |
|----------|-----|
| [!UICONTROL VAT] | 10% |
| [!UICONTROL Ceiling price source] | US$ 10 |
| [!UICONTROL Currency conversion] | 1,25 Euro:1 USD |

[Preço ](./optional-ceiling-price.md) máximo no mercado europeu (IVA): $10 x 1,25 = $12,50

Quando o [preço limite](./optional-ceiling-price.md) no mercado europeu (IVA) é atingido, o IVA é calculado e adicionado.

Preço final após IVA: US$ 12,50 x (1,1) = US$ 13,75

### Combinação de várias regras de preço, preço limite, conversão de moeda e IVA

#### Regra de preços inteligente (do exemplo anterior)

| Campo | Configuração |
|----------|----|
| Prioridade | 1 |
| IVA | 10% |
| Fonte de preço limite | US$ 10 |
| Conversão de moeda | 1,25 Euro:1 USD |

[Preço ](./optional-ceiling-price.md) máximo no mercado europeu (IVA): $10 x 1,25 = $12,50

Preço final após IVA: US$ 12,50 x (1,1) = US$ 13,75

#### Regra de preços padrão

| Campo | Configuração |
|----------|-----|
| [!UICONTROL Priority] | 2 |
| [!UICONTROL Price Action] | Aumentar por |
| [!UICONTROL Apply] | Aplicar como valor fixo |
| [!UICONTROL Adjustment Amount] | US$ 5,00 |

Quando o [preço limite](./optional-ceiling-price.md) é atingido, a regra de preço padrão é aplicada sobre a regra de preço inteligente.

Preço final após a aplicação da regra de preços padrão: $13,75 + $5,00 = $18,75

### Ajuste de preço

Neste exemplo, o preço mais competitivo é definido observando o [preço mais baixo do concorrente da Amazon](./lowest-competitor-pricing.md) com um feedback positivo de 95% e uma contagem mínima de feedback de 1.000 revisões do comerciante.

![Exemplo de ajuste de preço](assets/amazon-price-adjustment-example.png)

Após executar essa pesquisa com base nesses parâmetros, o preço competitivo volta a US$ 25.

Aqui, há três opções diferentes de [price rule action](./pricing-rule-actions.md) com base nesse preço mais baixo.

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Price Action] | Opções:<ul><li>**[!UICONTROL Decrease By]** - Essa opção diminui o preço de cotação em relação ao  [menor preço](./lowest-competitor-pricing.md) do concorrente.</li><li>**[!UICONTROL Increase By]** - Essa opção aumenta o preço da listagem em relação ao  [menor preço](./lowest-competitor-pricing.md) do concorrente.</li><li>**[!UICONTROL Match Competitor Price]** - Essa opção altera o preço da listagem do Amazon para corresponder ao preço mais baixo com base nos parâmetros. No exemplo, o preço da listagem do Amazon é de US$ 25.</li></ul> |
| [!UICONTROL Apply] | Opções: Aplicar como porcentagem / Aplicar como valor fixo |
| [!UICONTROL Adjustment Amount] | Valor numérico para definir a porcentagem ou a quantia fixa do desconto a ser aplicado. <br>Essas seleções resultam em tomar o preço mais baixo e configurá-lo em US$ 0,01 a menos. |

### Preço mínimo

| Campo | Configuração |
|----------|----|
| [!UICONTROL Floor Price Source] | Custo = US$ 5 |
| [!UICONTROL Floor Price Action] | Aumentar por |
| [!UICONTROL Apply] | Aplicar como porcentagem |
| [!UICONTROL Floor Adjustment Amount] | 5 |

[Cálculo do ](./floor-price.md) preço do chão = Origem do preço do chão  `$5` x Quantia do ajuste do chão  `5%` = $5,25

Quando a regra de preço inteligente é aplicada, ela permite que o preço da listagem seja inferior a $5,25 para este produto específico quando o custo é de $5.
