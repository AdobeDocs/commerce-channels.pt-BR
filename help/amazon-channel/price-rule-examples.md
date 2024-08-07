---
title: Canal de vendas da Amazon - Exemplos de regras de preço
description: Para ajudá-lo a criar suas regras de precificação para as listagens do Amazon, analise esses exemplos com base em cenários comuns.
feature: Sales Channels, Price Rules
exl-id: 4d9717ba-4ad6-468d-b4ca-99f8620b60b4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 1%

---

# Exemplos de regras de preço

## Exemplos de regras de preço padrão

### Descartar regras subsequentes

A capacidade de descartar regras subsequentes é um excelente recurso nas regras de preço que impedem que várias regras de preço sejam empilhadas e ofereçam descontos adicionais não intencionais. Para descartar regras subsequentes, uma regra de preço deve usar as prioridades definidas na seção _[!UICONTROL Priority]_das [Configurações Gerais da Regra de Preço](./pricing-rule-general-settings.md).

Se **[!UICONTROL Discard Subsequent Rules]** estiver definido como `Yes`, as regras com prioridade mais baixa (números maiores) não se aplicam aos produtos qualificados.

Por exemplo, digamos que existam três regras de preço:

| Exemplo | Nome da regra | Prioridade | Descartar Regra Subsequente |
|---------|-----------------------|----------|-------------------------|
| 1 | Produtos com 10% de desconto | 1 | Não |
| 2 | Produtos de US$ 2,00 de desconto | 2 | Sim |
| 3 | 5% de desconto em todos os produtos | 3 | Não |

Nesse cenário, as regras #1 e #2 se aplicam aos produtos qualificados. A regra #3 se aplica somente a produtos qualificados não contidos na regra #2 porque ela tem uma prioridade mais baixa que o exemplo #2 e **[!UICONTROL Discard Subsequent Rules]** está definido como `Yes`. Portanto, os produtos elegíveis na categoria de venda receberiam um desconto de 10% e US$ 2 de desconto sobre o preço de tabela da Amazon.

### Aplicando duas regras de preço padrão

| Campo | Configuração - Regra 1 | Configuração - Regra 2 |
|--------------------------------|---------------------|-----------------------|
| [!UICONTROL Rule Name] | Regra-1 | Regra-2 |
| [!UICONTROL Priority] | 1 | 2 |
| [!UICONTROL Rule Type] | Regra de preço padrão | Regra de preço padrão |
| [!UICONTROL Price action] | Diminuir em | Diminuir em |
| [!UICONTROL Apply] | Aplicar como porcentagem | Aplicar como valor fixo |
| [!UICONTROL Adjustment Amount] | 10 | 10 |

#### Product 1

Preço: US$ 45,49

Regra 1 aplicada: $ 45,49 x (0,9) = $ 40,94

Regra 2 aplicada: $ 40,94 - $ 10,00 = $ 30,94

O preço final após a Regra 1 e a Regra 2 é aplicado: US$ 30,94

#### Product 2

Preço: US$ 47,76

Regra 1 aplicada: $ 47,76 x (0,9) = $ 42,98

Regra 2 aplicada: $ 42,98 - $ 10,00 = $ 32,98

O preço final após a regra 1 e a regra 2 é aplicado: US$ 32,98

## Exemplos de regras de reprecificação inteligente

### Preço de Buy Box com Preço Mínimo Source = Preço

| Campo | Configuração |
|--------------------------------------|----------------------------|
| [!UICONTROL Rule Name] | Regra-1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Regra inteligente de reavaliação de preços |
| [!UICONTROL Competitor Price Source] | Usar preço de &quot;Buy Box&quot; |
| [!UICONTROL Price Action] | Corresponder Preço do Concorrente |
| [!UICONTROL Floor Price Source] | Preço |
| [!UICONTROL Floor Price Action] | Corresponder |

#### Product 1

Preço: US$ 15

Preço de [Buy Box](./buy-box-competitor-pricing.md) da Amazon: $10

Como o preço [Buy Box](./buy-box-competitor-pricing.md) é menor que o preço original, o produto está listado no preço original.

O preço final após a aplicação da regra: US$ 15

#### Product 2

Preço: US$ 5

Preço de [Buy Box](./buy-box-competitor-pricing.md) da Amazon: $10

Como o preço [Buy Box](./buy-box-competitor-pricing.md) é maior que o preço original, o produto está listado ao preço [Buy Box](./buy-box-competitor-pricing.md).

O preço final após a aplicação da regra: US$ 10

### Preço de Buy Box com Preço Mínimo Source = Preço e 20% de redução de preço

| Campo | Configuração |
|--------------------------------------|----------------------------|
| [!UICONTROL Rule Name] | Regra-1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Regra inteligente de reavaliação de preços |
| [!UICONTROL Competitor Price Source] | Usar preço de &quot;Buy Box&quot; |
| [!UICONTROL Price Action] | Corresponder Preço do Concorrente |
| [!UICONTROL Floor Price Source] | Preço |
| [!UICONTROL Floor Price Action] | Diminuir em |
| [!UICONTROL Apply] | Aplicar como uma porcentagem |
| [!UICONTROL Floor Adjustment Amount] | 20 |

#### Product 1

Preço: US$ 20

Preço mínimo calculado: US$ 16

Preço de [Buy Box](./buy-box-competitor-pricing.md) da Amazon: $15

Como o preço [Buy Box](./buy-box-competitor-pricing.md) é menor que o [Preço mínimo](./floor-price.md) calculado, o produto está listado no [Preço mínimo](./floor-price.md) calculado.

O preço final após a aplicação da regra: US$ 16

#### Product 2

Preço: US$ 15

Calculado [Preço Mínimo](./floor-price.md): $12

Preço de [Buy Box](./buy-box-competitor-pricing.md) da Amazon: $15

Como o preço [Buy Box](./buy-box-competitor-pricing.md) é maior que o [Preço mínimo](./floor-price.md) calculado, o produto está listado ao preço [Buy Box](./buy-box-competitor-pricing.md).

O preço final após a aplicação da regra: US$ 15

#### Product 3

Preço: US$ 17

Preço mínimo calculado: US$ 13,60

Preço de [Buy Box](./buy-box-competitor-pricing.md) da Amazon: $15

Como o preço [Buy Box](./buy-box-competitor-pricing.md) é maior que o [Preço mínimo](./floor-price.md) calculado, o produto está listado ao preço [Buy Box](./buy-box-competitor-pricing.md).

O preço final após a aplicação da regra: US$ 15

### Menor preço com todos os preços do concorrente e usar todas as condições de produto do concorrente

| Campo | Configuração |
|----------------------------------------|-----------------------------------------|
| [!UICONTROL Rule Name] | Regra-1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Regra inteligente de reavaliação de preços |
| [!UICONTROL Competitor Price Source] | Usar o preço mais baixo da concorrência |
| [!UICONTROL Minimum Positive Feedback] | Todos os Preços de Concorrentes |
| [!UICONTROL Conditional Variance] | Usar todas as condições de produto do concorrente |
| [!UICONTROL Price Action] | Corresponder Preço do Concorrente |
| [!UICONTROL Floor Price Source] | Preço |
| [!UICONTROL Floor Price Action] | Corresponder |

| Preço | Condição |
|-------|-----------------|
| $ 17 | Novo |
| $ 15 | Novo |
| $ 14 | Usado; Muito bom |
| $ 13 | Usado; Bom |

#### Product 1

Preço: US$ 10

Condição: Nova

Como o preço mais baixo do concorrente para a condição Novo é de US$ 15, o produto está listado em US$ 15.

O preço final após a aplicação da regra: US$ 15

#### Product 2

Preço: US$ 10

Condição: Usado; Aceitável

Como o [preço mais baixo do concorrente](./lowest-competitor-pricing.md) para a condição Utilizado é de $13, o produto está listado em $13.

O preço final após a aplicação da regra: US$ 13

### Regra inteligente de reavaliação de preços combinando preço máximo, conversão de moeda e IVA

| Campo | Configuração |
|-----------------------------------|---------------|
| [!UICONTROL VAT] | 10% |
| [!UICONTROL Ceiling price source] | $ 10 |
| [!UICONTROL Currency conversion] | 1,25 Euro:1USD |

[Preço no teto](./optional-ceiling-price.md) no mercado europeu (VAT): $10 x 1,25 = $12,50

Quando o [preço máximo](./optional-ceiling-price.md) no mercado europeu (VAT) é atingido, o VAT é calculado e adicionado.

Preço final após IVA: US$ 12,50 x (1,1) = US$ 13,75

### Combinação de várias regras de precificação, preço máximo, conversão de moeda e IVA

#### Regra de preço inteligente (do exemplo anterior)

| Campo | Configuração |
|----------------------|---------------|
| Prioridade | 1 |
| IVA | 10% |
| Fonte de preço limite | $ 10 |
| Conversão de moeda | 1,25 Euro:1USD |

[Preço no teto](./optional-ceiling-price.md) no mercado europeu (VAT): $10 x 1,25 = $12,50

Preço final após IVA: US$ 12,50 x (1,1) = US$ 13,75

#### Regra de preço padrão

| Campo | Configuração |
|--------------------------------|-----------------------|
| [!UICONTROL Priority] | 2 |
| [!UICONTROL Price Action] | Aumentar em |
| [!UICONTROL Apply] | Aplicar como valor fixo |
| [!UICONTROL Adjustment Amount] | $ 5,00 |

Quando o [preço máximo](./optional-ceiling-price.md) é atingido, a regra de preço padrão é aplicada sobre a regra de preço inteligente.

Preço final após a aplicação da regra de preço padrão: US$ 13,75 + US$ 5,00 = US$ 18,75

### Ajuste de preço

Neste exemplo, o preço mais competitivo é definido observando o [preço mais baixo do concorrente](./lowest-competitor-pricing.md) da Amazon, com 95% de feedback positivo e uma contagem mínima de feedback de 1.000 comentários do comerciante.

![Exemplo de ajuste de preço](assets/amazon-price-adjustment-example.png){width="600" zoomable="yes"}

Depois de realizar essa pesquisa com base nesses parâmetros, o preço competitivo volta a US$ 25.

Aqui, há três opções diferentes de [ação de regra de preço](./pricing-rule-actions.md) com base nesse preço mais baixo.

| Campo | Descrição |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Action] | Opções:<ul><li>**[!UICONTROL Decrease By]** - Esta opção diminui o preço de sua lista em relação ao [preço mais baixo do concorrente](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Increase By]** - Essa opção aumenta o preço de sua lista em relação ao [preço mais baixo do concorrente](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Match Competitor Price]** - Essa opção altera o preço de listagem do Amazon para corresponder ao preço mais baixo com base nos parâmetros. No exemplo, o preço de tabela do Amazon é de US$ 25.</li></ul> |
| [!UICONTROL Apply] | Opções: Aplicar como porcentagem / Aplicar como valor fixo |
| [!UICONTROL Adjustment Amount] | Valor numérico para definir a porcentagem ou o valor fixo do desconto a ser aplicado. <br>Essas seleções resultam no preço mais baixo e na configuração de US$ 0,01 a menos. |

### Preço mínimo

| Campo | Configuração |
|--------------------------------------|---------------------|
| [!UICONTROL Floor Price Source] | Custo = US$ 5 |
| [!UICONTROL Floor Price Action] | Aumentar em |
| [!UICONTROL Apply] | Aplicar como porcentagem |
| [!UICONTROL Floor Adjustment Amount] | 5 |

[Preço mínimo](./floor-price.md) cálculo = Preço mínimo Source `$5` x Valor do Ajuste de Limite Mínimo `5%` = $5,25

Quando a regra de preço inteligente é aplicada, ela permite que o preço de lista seja inferior a US$ 5,25 para esse produto específico quando o custo é de US$ 5.
