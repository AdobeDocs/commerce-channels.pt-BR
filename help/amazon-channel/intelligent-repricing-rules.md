---
title: '"Regra de Reprecificação Inteligente: Selecionar tipo de regra'''
description: Determine seu preço de listagem do Amazon de acordo com os preços do concorrente criando uma regra de reprecificação inteligente.
exl-id: 2690323a-a076-484b-a437-adadb08094f5
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 0%

---

# Regra inteligente de reprecificação: selecionar tipo de regra

>[!IMPORTANT]
>
>Regras inteligentes de redefinição de preços não funcionam corretamente se a região do Amazon estiver definida como `Inactive` , como durante a integração. Seus cálculos de preços dependem das taxas de frete e sua região deve estar em `Active` status para suas taxas de frete sincronizarem do Amazon.<br><br>
>
>Para atualizar o status da região na conta do Amazon, acesse Configurações > Informações da conta > Configurações de férias. Consulte [Amazon: Status de Listagem para Férias](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620/&quot;target=&quot;_blank)

Uma regra inteligente de reprecificação usa o preço dos concorrentes da Amazon para determinar o preço da listagem. Os concorrentes são outros vendedores que listam os mesmos produtos que o seu no Amazon.

As seções de uma regra inteligente de redefinição de preços incluem:

- Selecionar tipo de regra
- [Variáveis condicionais do concorrente](./competitor-conditional-variances.md)
- [Ajuste de preço](./price-adjustment.md)
- [Preço Limite](./floor-price.md)
- [Preço Limite Opcional](./optional-ceiling-price.md)

## Configurar o tipo de regra

Defina o tipo de regra no _[!UICONTROL Select Rule Type]_seção.

1. Para **[!UICONTROL Rule Type]**, escolha `Intelligent repricing rule`.

   Essa configuração ativa o _[!UICONTROL Competitor Price Source]_e o [_[!UICONTROL Competitor Conditional Variances]_](./competitor-conditional-variances.md), [_[!UICONTROL Floor Price]_](./floor-price.md)e [_[!UICONTROL Optional Ceiling Price]_](./optional-ceiling-price.md) seções.

1. Para **[!UICONTROL Competitor Price Source]**, escolha uma opção:

   - **[!UICONTROL Use "Buy Box" Price]** - Escolha quando deseja ajustar o preço da Amazon com base na Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md) preço do vendedor. A [!DNL Buy Box] existe quando vários vendedores na Amazon oferecem o mesmo produto. A Amazon define a variável [!DNL Buy Box] vendedor baseado em requisitos de desempenho. Os comerciantes procuram ganhar a [!DNL Buy Box] status de vendedor e oferecer visibilidade máxima de suas listas de produtos.

   - **[!UICONTROL Use Lowest Competitor Price]** - Escolha quando deseja comparar e ajustar o preço da listagem ao preço do concorrente do mesmo produto. Quando escolhido, a variável _[!UICONTROL Minimum Positive Feedback]_e_[!UICONTROL Minimum Feedback Count]_ Os campos estão ativados.

1. Se estiver ativado, escolha uma opção para **[!UICONTROL Minimum Positive Feedback]**.

   - **[!UICONTROL All Competitor's Prices]** - Escolha quando deseja comparar e ajustar o preço com base em todos os preços da concorrência do mesmo produto.

   - **[!UICONTROL Minimum 80/90/95/98% positive feedback]** - Escolha quando deseja limitar os concorrentes aos quais o preço é comparado para o mesmo produto. Esta definição restringe ainda mais os concorrentes, exigindo que a sua cotação tenha um mínimo da percentagem escolhida de feedback positivo antes de aplicar a regra de preço mais baixa.

1. Se estiver ativado, insira um valor numérico para **[!UICONTROL Minimum Feedback Count]**.

   Este valor numérico opcional reduz ainda mais os preços competitivos. Por exemplo, se um comerciante tiver uma classificação de feedback 95% positiva, mas tiver apenas uma contagem de feedback de `20`, pode não ser um concorrente para o qual você deseja modificar seus preços. No entanto, se você inserir um valor de `1000`, isso exigiria que o comerciante tivesse um feedback positivo de 95% e um mínimo de 1000 revisões de comerciantes.

>[!NOTE]
>
>Você pode usar essas opções de preços e feedback de concorrentes para evitar basear seus preços em um concorrente que tem feedback ruim e está vendendo um produto de qualidade mais baixa.

![Regra de reprecificação inteligente - selecione o tipo de regra](assets/ob-intelligent-price-rule-type.png)

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Rule Type] | Selecione um tipo de regra. Opções:<ul><li>**[!UICONTROL Standard price rule]** - Esse tipo de regra permite aumentar ou diminuir o preço de listagem do Amazon em uma porcentagem específica ou um valor fixo do dólar em relação ao valor de _[!UICONTROL Magento Price Source]_. </li><li>**[!UICONTROL Intelligent repricing rule]** - Esse tipo de regra permite ajustar o preço da listagem do Amazon, com base no preço do concorrente. Quando escolhido, a variável _[!UICONTROL Minimum Positive Feedback]_e_[!UICONTROL Minimum Feedback Count]_ Os campos estão ativados.</li></ul> |
| [!UICONTROL Competitor Price Source] | Selecione a fonte de preço desejada. Opções:<ul><li>**[!UICONTROL Use "Buy Box" Price]** - Escolha esta opção quando quiser ajustar o preço do Amazon com base na Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md) preço do vendedor. A [!DNL Buy Box] existe quando vários vendedores na Amazon oferecem o mesmo produto. A Amazon define a variável [!DNL Buy Box] vendedor baseado em requisitos de desempenho. Os comerciantes procuram ganhar a [!DNL Buy Box] status de vendedor e oferecer visibilidade máxima de suas listas de produtos.</li><li>**[!UICONTROL Use Lowest Competitor Price]** - Escolha esta opção quando quiser comparar e ajustar o preço da sua listagem para a [preços mais baixos do concorrente](./lowest-competitor-pricing.md) para o mesmo produto. Quando escolhido, a variável _[!UICONTROL Minimum Positive Feedback]_e_[!UICONTROL Minimum Feedback Count]_ Os campos estão ativados.</li></ul> |
| [!UICONTROL Minimum Positive Feedback] | Somente ativo se `Use Lowest Competitor Price` é escolhido. Opções:<ul><li>**[!UICONTROL All Competitor's Prices]** - Escolha quando deseja comparar e ajustar o preço com base em todos os preços da concorrência do mesmo produto.</li><li>**[!UICONTROL Minimum 80/90/95/98% positive feedback]** - Escolha quando deseja limitar os concorrentes aos quais você compara e ajusta seus preços. Essa configuração restringe ainda mais seus concorrentes, exigindo que sua listagem tenha um mínimo da porcentagem escolhida de feedback positivo e, em seguida, use o preço mais baixo desse subconjunto de concorrentes.</li></ul> |
| [!UICONTROL Minimum Feedback Count] | Somente ativo se `Use Lowest Competitor Price` é escolhido. Este valor numérico opcional limita ainda mais a comparação competitiva de preços. Por exemplo, se um comerciante tiver uma classificação de feedback 95% positiva, mas tiver apenas uma contagem de feedback de `20`, pode não ser um concorrente para o qual você deseja modificar seus preços. No entanto, se você inserir um valor de `1000`, isso exigiria que o comerciante tivesse um feedback positivo de 95% e um mínimo de 1000 revisões de comerciantes. |
