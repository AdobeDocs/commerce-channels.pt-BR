---
title: "Regra Inteligente de Reavaliação de Preços: Variações Condicionais do Concorrente"
description: Determine o preço de sua lista do Amazon com base no preço do concorrente e na condição do produto criando uma regra inteligente de reprecificação.
feature: Sales Channels, Configuration
exl-id: c52230e3-4e47-45bc-80e0-170530f58987
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Regra de Reavaliação de Preços Inteligente: Variações Condicionais do Concorrente

As seções de uma regra de reavaliação inteligente incluem:

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [!UICONTROL Competitor Conditional Variances]
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [[!UICONTROL Floor Price]](./floor-price.md)
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

Uma regra inteligente de reavaliação de preços usa os preços dos concorrentes da Amazon para determinar o preço de sua lista. Os concorrentes são outros vendedores que estão listando os mesmos produtos que você está listando no Amazon.

Se um produto existir com a mesma condição, o preço base de correspondência será o [concorrente mais baixo](./lowest-competitor-pricing.md) com a mesma condição. Se nenhum produto concorrente corresponder à sua condição, o preço base de correspondência passará por outras condições disponíveis do concorrente, começando com Novo, Recondicionado e continuando até as condições disponíveis. Depois que uma condição é encontrada, o preço base de correspondência será o preço mais baixo dentro dessa condição.

Se você tiver um produto listado com a condição `Used; Good` e o preço base de correspondência, e um concorrente tem o mesmo produto na mesma condição a um preço menor, o preço do concorrente é usado. Se um concorrente não existir com a mesma condição, o sistema verifica um concorrente com a próxima condição, que é `New`. Se um concorrente for encontrado com essa condição, o preço mais baixo será usado.

## Configurar variações condicionais do concorrente

Defina as variações de condição no _[!UICONTROL Competitor Conditional Variances]_seção.

Para **[!UICONTROL Conditional Variance]**, escolha uma opção:

- `Use all competitor's product conditions` - (Padrão) Escolha quando deseja que seu produto seja comparado com qualquer condição disponível (se não houver uma correspondência para a condição que você está listando).

- `Use Only Matching Competitor's Product Condition` - Escolha quando deseja que seu produto seja comparado somente com os produtos de concorrentes na mesma condição. Se não houver correspondência, o preço do produto será estabelecido no _Origem do Preço de Magento_ definido em seu [Preço de Listagem](./listing-price.md).

- `Apply Variance (if competitor's product condition differs)` - Escolha primeiro tentar comparar com a condição do produto correspondente. Se não existir uma condição de correspondência, uma variação (como uma porcentagem) será aplicada em relação à condição do seu produto e à condição do concorrente mais baixo.

  Quando a variável _[!UICONTROL Apply Variance]_for escolhido, campos de variação adicionais serão exibidos para cada uma das condições do Amazon. Esse recurso permite usar regras inteligentes de reavaliação de preços ao oferecer produtos que estão em uma condição diferente de seus concorrentes. Para entender o cálculo por trás da variação condicional, você deve primeiro entender que toda a variação é determinada a partir de um preço de correspondência base.

  As opções de variação condicional exibidas se baseiam nas configurações de lista para `Condition` que são mapeados para valores de condição usando um [!DNL Commerce] [atributo de produto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html). Para todas as condições mapeadas, é possível definir uma porcentagem de variação de 1-100. A exceção é cobrável, nesse caso, uma porcentagem maior que 100 pode ser aplicada.

![Regra inteligente de reavaliação de preços - Variações condicionais do concorrente](assets/amazon-competitor-cond-variances.png){width="500" zoomable="yes"}

| Campo | Descrição |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Competitor Conditional Variances] | Opções: <ul><li>**[!UICONTROL Use all competitor's product conditions]** - Se não houver uma correspondência para a condição com a qual você está listando seu produto, essa opção corresponderá a qualquer condição disponível. Primeiro, ele tenta corresponder à sua condição e, em seguida, funciona no modo `New` condição para `Used; Acceptable`.</li><li>**[!UICONTROL Use only matching competitor's product condition]** - Essa opção é compatível com a condição do seu produto. Se não houver correspondência, os preços do produto no _[!UICONTROL Magento Price Source]_.</li><li>>**[!UICONTROL Apply variance (if competitor's product condition differs)]** - Essa opção primeiro tenta corresponder à condição do seu produto. Se não houver nenhuma condição correspondente, ela aplicará uma variação (como uma porcentagem) relativa à condição do seu produto e à condição do concorrente mais baixo.</li></ul><br><br>As opções de variação condicional exibidas com base nas configurações de lista para Condição que são mapeadas para valores de condição usando um [!DNL Commerce] [atributo de produto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html). Para todas as condições mapeadas, você pode indicar uma porcentagem de variação de 1-100. A exceção é cobrável, nesse caso, uma porcentagem maior que 100 pode ser aplicada.<br><br>Esse recurso permite usar regras inteligentes de reavaliação de preços ao oferecer produtos que estão em uma condição diferente de seus concorrentes. Para entender o cálculo por trás da variação condicional, você deve primeiro entender que toda a variação é determinada a partir de um preço de correspondência base. |

## Calcular a base de variação condicional

- Variação da Condição de Correspondência Base (BMC) = A variação da condição do seu concorrente de preço de correspondência base. Usando o exemplo anterior, a BMC é a variação para a variável `New` condição.
- Variação da condição do comerciante (MCV) = A variação da condição do seu produto. Usando o exemplo anterior, MCV = a variação da variável `Used; Good` condição.
- Preço-Base de Vinculação (BMP) = US$ 7,99 (explicado acima)

A fórmula para calcular a base de variação condicional é a seguinte:

![fórmula de cálculo base de variação condicional](assets/amazon-cond-variance-calc-1.png){width="300"}

## Exemplo

As configurações de variação condicional são as seguintes:

![exemplo de configurações de variação condicional](assets/amazon-cond-variances.png){width="500" zoomable="yes"}

- BMC = 100 (Condição do concorrente = Novo)
- MCV = 80 (Condição do comerciante = Utilizado; Bom)
- BMP = US$ 7,99 (Preço base de correspondência = o preço mais baixo da condição do concorrente correspondente)

![exemplo de cálculo de base de variação condicional](assets/amazon-cond-variance-calc-2.png){width="300"}

Usando o cálculo da base de variação condicional acima, sua base de variação condicional = US$ 6,39. Esse cálculo é a fonte de preço do concorrente usada para suas ações de regra de preço, explicado mais detalhadamente em [Ajuste de Preço](./price-adjustment.md).
