---
title: '"Regra de Reprecificação Inteligente: Variações Condicionais do Concorrente'
description: Determine seu preço de listagem do Amazon com base no preço da concorrência e na condição do produto, criando uma regra de reprecificação inteligente.
exl-id: c52230e3-4e47-45bc-80e0-170530f58987
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Regra inteligente de reprecificação: variações condicionais do concorrente

As seções de uma regra inteligente de redefinição de preços incluem:

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [!UICONTROL Competitor Conditional Variances]
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [[!UICONTROL Floor Price]](./floor-price.md)
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

Uma regra inteligente de reprecificação usa o preço dos concorrentes da Amazon para determinar o preço da listagem. Os concorrentes são outros vendedores que listam os mesmos produtos que você está listando no Amazon.

Se um produto existir com a mesma condição, o preço de correspondência base é a [concorrente mais baixo](./lowest-competitor-pricing.md) com a mesma condição. Se nenhum produto concorrente corresponder à sua condição, o preço de correspondência base passará por outras condições de concorrentes disponíveis, começando com Novo, Refurbado e continuando pelas condições disponíveis. Depois que uma condição for encontrada, o preço de correspondência base será o preço mais baixo dentro dessa condição.

Se você tiver um produto listado com a condição `Used; Good` e o preço de jogo de base, e um concorrente tem o mesmo produto na mesma condição a um preço mais baixo, utiliza-se o preço do concorrente. Se um concorrente não existir com a mesma condição, o sistema verifica se há um concorrente com a condição seguinte, que é `New`. Se for encontrado um concorrente com essa condição, é utilizado o preço mais baixo.

## Configurar variações condicionais do concorrente

Defina as variações de condição na variável _[!UICONTROL Competitor Conditional Variances]_seção.

Para **[!UICONTROL Conditional Variance]**, escolha uma opção:

- `Use all competitor's product conditions` - (Padrão) Escolha quando deseja que seu produto seja comparado a qualquer condição disponível (se uma correspondência não existir para a condição que você está listando).

- `Use Only Matching Competitor's Product Condition` - Escolha quando deseja que o produto seja comparado somente com os produtos do concorrente na mesma condição. Se não houver correspondência, o produto terá seu preço definido na variável _Origem de Preço Magento_ definido no [Preço de Listagem](./listing-price.md).

- `Apply Variance (if competitor's product condition differs)` - Escolha primeiro tentar comparar com sua condição de produto correspondente. Se não houver nenhuma condição correspondente, uma variação (como uma porcentagem) será aplicada em relação à condição do produto e à condição do concorrente mais baixa.

   Quando a variável _[!UICONTROL Apply Variance]_for escolhido, campos de variação adicionais serão exibidos para cada uma das condições do Amazon. Esse recurso permite usar regras inteligentes de reprecificação ao oferecer produtos que estão em uma condição diferente da de seus concorrentes. Para entender o cálculo por trás da variação condicional, primeiro você deve entender que toda a variação é determinada a partir de um preço de correspondência base.

   As opções de variação condicional exibidas são baseadas nas configurações de listagem para `Condition` que são mapeadas para valores de condição usando um [!DNL Commerce] [atributo do produto](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}. Para todas as condições mapeadas, é possível definir uma porcentagem de variação de 1-100. A exceção são os materiais coletáveis, caso em que pode ser aplicada uma percentagem superior a 100.

![Regra de reprecificação inteligente - variações condicionais do concorrente](assets/amazon-competitor-cond-variances.png)

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Competitor Conditional Variances] | Opções: <ul><li>**[!UICONTROL Use all competitor's product conditions]** - Se não existir uma correspondência para a condição com a qual você está listando seu produto, essa opção corresponde a qualquer condição disponível. Primeiro, ele tenta corresponder à sua condição e, em seguida, funciona a partir do `New` condição para `Used; Acceptable`.</li><li>**[!UICONTROL Use only matching competitor's product condition]** - Essa opção corresponde à condição do seu produto. Se não houver correspondência, os preços do produto no _[!UICONTROL Magento Price Source]_.</li><li>>**[!UICONTROL Apply variance (if competitor's product condition differs)]** - Essa opção primeiro tenta corresponder à condição do produto. Se não houver nenhuma condição correspondente, ela aplicará uma variação (como uma porcentagem) em relação à condição do produto e à condição do concorrente mais baixa.</li></ul><br><br>As opções de variação condicional que aparecem com base nas configurações de listagem para Condição que são mapeadas para valores de condição usando um [!DNL Commerce] [atributo do produto](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}. Para todas as condições mapeadas, é possível indicar uma porcentagem de variação de 1 a 100. A exceção são os materiais coletáveis, caso em que pode ser aplicada uma percentagem superior a 100.<br><br>Esse recurso permite usar regras inteligentes de reprecificação ao oferecer produtos que estão em uma condição diferente da de seus concorrentes. Para entender o cálculo por trás da variação condicional, primeiro você deve entender que toda a variação é determinada a partir de um preço de correspondência base. |

## Calcular a base de variação condicional

- Variação da Condição de Correspondência Base (BMC) = A variação da condição do seu concorrente de preço de correspondência base. Usando o exemplo anterior, BMC é a variação da variável da variável `New` condição.
- Variação de condição de merchant (MCV) = variação da condição do seu produto. Usando o exemplo anterior, MCV = a variação da variável `Used; Good` condição.
- Preço de correspondência base (BMP) = US$ 7,99 (explicado acima)

A fórmula para calcular a base da variação condicional é a seguinte:

![fórmula de cálculo da base de variação condicional](assets/amazon-cond-variance-calc-1.png)

## Exemplo

As configurações de variação condicional são as seguintes:

![configurações de variação condicional de exemplo](assets/amazon-cond-variances.png)

- BMC = 100 (Condição do concorrente = Novo)
- MCV = 80 (Condição do comerciante = Utilizado; Bom)
- BMP = US$ 7,99 (Preço de correspondência base = O preço mais baixo da condição de concorrente correspondente)

![exemplo de cálculo da base de variação condicional](assets/amazon-cond-variance-calc-2.png)

Usando o cálculo da base de variação condicional acima, sua base de variação condicional = US$ 6,39. Esse cálculo é a fonte de preço do concorrente usada para suas ações de regra de preço, explicada ainda mais em [Ajuste de preço](./price-adjustment.md).
