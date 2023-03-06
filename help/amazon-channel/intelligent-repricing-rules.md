---
title: "Regra de Reprecificação Inteligente: Selecionar Tipo de Regra"
description: Determine o preço da lista do Amazon de acordo com os preços da concorrência criando uma regra de reavaliação inteligente.
exl-id: 2690323a-a076-484b-a437-adadb08094f5
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 0%

---

# Regra de Reprecificação Inteligente: Selecionar Tipo de Regra

>[!IMPORTANT]
>
>As regras de reprecificação inteligentes não funcionarão adequadamente se a região do Amazon estiver definida como `Inactive` status, como está durante a integração. Os cálculos de preço dependem das taxas de entrega e sua região deve estar em `Active` Status das taxas de envio para sincronização no Amazon.<br><br>
>
>Para atualizar o status da região na conta do Amazon, acesse Configurações > Informações da conta > Configurações de férias. Consulte [Amazon: Status de Listagem para Férias](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620/&quot;target=&quot;_blank)

Uma regra inteligente de reavaliação de preços usa os preços dos concorrentes da Amazon para determinar o preço de sua lista. Os concorrentes são outros vendedores que listam os mesmos produtos que os seus no Amazon.

As seções de uma regra de reavaliação inteligente incluem:

- Selecionar tipo de regra
- [Variações condicionais do concorrente](./competitor-conditional-variances.md)
- [Ajuste de Preço](./price-adjustment.md)
- [Preço mínimo](./floor-price.md)
- [Preço máximo opcional](./optional-ceiling-price.md)

## Configurar o tipo de regra

Defina o tipo de regra no _[!UICONTROL Select Rule Type]_seção.

1. Para **[!UICONTROL Rule Type]**, escolha `Intelligent repricing rule`.

   Essa configuração habilita a _[!UICONTROL Competitor Price Source]_e o campo [_[!UICONTROL Competitor Conditional Variances]_](./competitor-conditional-variances.md), [_[!UICONTROL Floor Price]_](./floor-price.md), e [_[!UICONTROL Optional Ceiling Price]_](./optional-ceiling-price.md) seções.

1. Para **[!UICONTROL Competitor Price Source]**, escolha uma opção:

   - **[!UICONTROL Use "Buy Box" Price]** - Escolha quando deseja ajustar os preços do Amazon com base na Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md) preço de venda. A [!DNL Buy Box] o preço existe quando vários vendedores na Amazon oferecem o mesmo produto. O Amazon define o [!DNL Buy Box] com base nos requisitos de desempenho. Os comerciantes buscam conquistar a [!DNL Buy Box] O status do vendedor e a visibilidade máxima de suas listagens de produtos.

   - **[!UICONTROL Use Lowest Competitor Price]** - Escolha quando deseja comparar e ajustar o preço de sua lista ao preço de um concorrente para o mesmo produto. Quando escolhido, o _[!UICONTROL Minimum Positive Feedback]_e_[!UICONTROL Minimum Feedback Count]_ campos são ativados.

1. Se estiver habilitado, escolha uma opção para **[!UICONTROL Minimum Positive Feedback]**.

   - **[!UICONTROL All Competitor's Prices]** - Escolha quando deseja comparar e ajustar seus preços com base em todos os preços de concorrentes para o mesmo produto.

   - **[!UICONTROL Minimum 80/90/95/98% positive feedback]** - Escolha quando deseja limitar os concorrentes com preços comparados para o mesmo produto. Essa configuração restringe ainda mais os concorrentes, exigindo que sua lista tenha um mínimo da porcentagem escolhida de feedback positivo antes de aplicar a regra de preço mais baixo.

1. Se ativado, informe um valor numérico para **[!UICONTROL Minimum Feedback Count]**.

   Esse valor numérico opcional reduz ainda mais o preço competitivo. Por exemplo, se um comerciante tiver uma classificação de feedback positiva de 95%, mas apenas uma contagem de feedback de `20`, pode não ser um concorrente com o qual você deseja modificar seus preços. No entanto, se você inserir um valor de `1000`, exigiria que o comerciante tivesse 95% de feedback positivo e um mínimo de 1.000 comentários do comerciante.

>[!NOTE]
>
>Você pode usar essas opções de preço e feedback do concorrente para evitar basear seus preços em um concorrente que tenha feedback insatisfatório e esteja vendendo um produto de qualidade inferior.

![Regra inteligente de reavaliação de preços - selecionar tipo de regra](assets/ob-intelligent-price-rule-type.png)

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Rule Type] | Selecione um tipo de regra. Opções:<ul><li>**[!UICONTROL Standard price rule]** - Esse tipo de regra permite aumentar ou diminuir o preço de listagem do Amazon em uma porcentagem específica ou valor fixo em dólar relativo ao _[!UICONTROL Magento Price Source]_. </li><li>**[!UICONTROL Intelligent repricing rule]** - Esse tipo de regra permite ajustar o preço de sua lista do Amazon com base nos preços do concorrente. Quando escolhido, o _[!UICONTROL Minimum Positive Feedback]_e_[!UICONTROL Minimum Feedback Count]_ campos são ativados.</li></ul> |
| [!UICONTROL Competitor Price Source] | Selecione a origem de preço desejada. Opções:<ul><li>**[!UICONTROL Use "Buy Box" Price]** - Escolha esta opção quando quiser ajustar os preços do Amazon com base no Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md) preço de venda. A [!DNL Buy Box] o preço existe quando vários vendedores na Amazon oferecem o mesmo produto. O Amazon define o [!DNL Buy Box] com base nos requisitos de desempenho. Os comerciantes buscam conquistar a [!DNL Buy Box] O status do vendedor e a visibilidade máxima de suas listagens de produtos.</li><li>**[!UICONTROL Use Lowest Competitor Price]** - Escolha esta opção quando quiser comparar e ajustar o preço da sua lista à [preço mais baixo do concorrente](./lowest-competitor-pricing.md) para o mesmo produto. Quando escolhido, o _[!UICONTROL Minimum Positive Feedback]_e_[!UICONTROL Minimum Feedback Count]_ campos são ativados.</li></ul> |
| [!UICONTROL Minimum Positive Feedback] | Somente ativo se `Use Lowest Competitor Price` for escolhida. Opções:<ul><li>**[!UICONTROL All Competitor's Prices]** - Escolha quando deseja comparar e ajustar seus preços com base em todos os preços de concorrentes para o mesmo produto.</li><li>**[!UICONTROL Minimum 80/90/95/98% positive feedback]** - Escolha quando deseja limitar os concorrentes com os quais você compara e ajusta seus preços. Essa configuração restringe ainda mais seus concorrentes, exigindo que sua lista tenha um mínimo da porcentagem escolhida de feedback positivo e, em seguida, use o preço mais baixo desse subconjunto de concorrentes.</li></ul> |
| [!UICONTROL Minimum Feedback Count] | Somente ativo se `Use Lowest Competitor Price` for escolhida. Esse valor numérico opcional reduz ainda mais a comparação de preços competitivos. Por exemplo, se um comerciante tiver uma classificação de feedback positiva de 95%, mas apenas uma contagem de feedback de `20`, pode não ser um concorrente com o qual você deseja modificar seus preços. No entanto, se você inserir um valor de `1000`, exigiria que o comerciante tivesse 95% de feedback positivo e um mínimo de 1.000 comentários do comerciante. |
