---
title: Gerenciar preços do Amazon
description: Você pode definir os preços das suas listagens do Amazon para diferirem da sua loja da Commerce usando as regras de preços.
feature: Sales Channels, Price Rules
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# Gerenciar preços do Amazon

O canal de vendas da Amazon permite definir regras de preços, que permitem definir um preço de lista do Amazon diferente do **[!UICONTROL Magento Price Source]** definido no [preço de lista](./listing-price.md). Você também pode empilhar várias regras e até mesmo usar o preço inteligente para ajustar o preço de sua lista do Amazon com base no preço [[!DNL Buy Box]](./buy-box-competitor-pricing.md) dos concorrentes ou no [preço mais baixo do concorrente](./lowest-competitor-pricing.md).

Há dois tipos de regras de precificação:

- [Regra de Preço Padrão](./standard-price-rules.md)
- [Regra inteligente de reprecificação](./intelligent-repricing-rules.md)

  >[!IMPORTANT]
  >
  >As regras inteligentes de reavaliação de preços não funcionarão corretamente se a região do Amazon estiver definida com o status `Inactive`, como acontece durante a integração. Seus cálculos de preços dependem das taxas de envio, e sua região deve ter o status `Active` para que suas taxas de envio sejam sincronizadas do Amazon.
  >
  >Para atualizar o status da região na conta do Amazon, acesse Configurações > Informações da conta > Configurações de férias. Consulte [Amazon: Status de Listagem para Férias](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620) (logon da Central de Vendedores necessário).

Este recurso permite manipular os preços do Amazon de uma forma semelhante às [!DNL Commerce] [regras de preço de catálogo](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html). Você pode criar regras complexas que permitem alterar os preços de produtos específicos, produtos dentro de categorias específicas ou até mesmo com atributos específicos.

Você pode adicionar regras de preços para suas listagens do Amazon. As regras de preços podem ser usadas para ajustar automaticamente os preços da lista, com base em um conjunto de condições definidas. As regras de preço são acionadas e calculam o preço ajustado antes que seu produto seja listado no Amazon.

>[!NOTE]
>
>A origem de preço das suas listagens do Amazon está definida para **[!UICONTROL Magento Price Source]** nas configurações de [preço de listagem](./listing-price.md). Qualquer cálculo de ajuste definido na regra de precificação usa a origem de preço como o valor inicial.

As regras de preços permitem definir um preço de lista do Amazon diferente do **[!UICONTROL Magento Price Source]** nas configurações de [preço de lista](./listing-price.md). Você também pode empilhar várias regras que funcionam juntas para ajustar o preço.

Uma regra de precificação/reprecificação requer três conjuntos de informações durante sua configuração:

- [Configurações gerais](./pricing-rule-general-settings.md): define o nome, a descrição, as datas ativas e a prioridade de uma regra, além de definir o comportamento das regras subsequentes com base em sua configuração de prioridade.
- [Condições](./pricing-rule-conditions.md): determine quais produtos estão qualificados para a regra de preço.
- [Ações](./pricing-rule-actions.md): defina os cálculos de ajuste aplicados à fonte de preço para determinar o preço de listagem.

Você pode criar [regras de preços padrão](./standard-price-rules.md) que ajustam automaticamente seu preço de lista do Amazon em relação ao **[!UICONTROL Magento Price Source]** selecionado nas configurações de [preço de lista](./listing-price.md). Este recurso permite manipular os preços do Amazon de uma forma semelhante às [!DNL Commerce] [regras de preço de catálogo](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html). Você pode criar regras complexas que alteram automaticamente os preços de produtos específicos, produtos dentro de categorias específicas ou produtos com atributos específicos. É possível concluir as configurações tradicionais e reavaliar o preço dos produtos para aumentar ou diminuir com base em uma quantidade fixa ou porcentagem.

Outra ferramenta poderosa é o recurso [Reprecificação Inteligente](./intelligent-repricing-rules.md), que ajusta o preço de sua lista do Amazon com base no preço do concorrente [[!DNL Buy Box]](./buy-box-competitor-pricing.md) ou no [Preço mais baixo do concorrente](./lowest-competitor-pricing.md). Semelhante às [!DNL Commerce] [regras de preço de catálogo](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html), este recurso avançado permite manipular os preços do Amazon criando regras complexas. As regras podem definir o escopo de uma alteração de preço para produtos específicos, produtos dentro de categorias específicas ou mesmo com atributos de produto específicos.

Usar a reavaliação de preços inteligente para ajustar os preços de sua lista do Amazon, com base nos preços do concorrente. O canal de vendas da Amazon tem proteções integradas para que você configure o para proteger as margens ou evitar a correspondência dos preços de um comerciante com pouco feedback. Usando [regras inteligentes de reavaliação de preços](./intelligent-repricing-rules.md), os preços de listagem da Amazon podem ser manipulados automaticamente como um valor fixo ou percentual (para cima ou para baixo) ou até mesmo sincronizado com o preço [[!DNL Buy Box]](./buy-box-competitor-pricing.md) ou com o [Preço mais baixo da concorrência](./lowest-competitor-pricing.md) por item. As regras podem até ser empilhadas para fornecer flexibilidade ilimitada.

Você pode controlar aspectos importantes das regras, como status ativo/inativo, elegibilidade do site, intervalos de datas opcionais e níveis de prioridade opcionais (usados para empilhamento de regras).

Por exemplo, você pode definir e definir as condições para uma regra de preço que, quando as condições forem atendidas, ajuste automaticamente o preço de lista antes de ser enviado ao Amazon.

Outra opção de preço é uma [substituição de preço](./overrides.md), que é definida no nível de lista individual. Uma [substituição de preço](./overrides.md) pode ser definida e uma substituição ignora/tem prioridade sobre todos os outros padrões, configurações e regras. Uma [substituição](./overrides.md) pode ser definida para preço, tempo de manipulação, condição e notas do vendedor (com algumas exceções).

![Regras de preços](assets/amazon-pricing-rules.png){width="600" zoomable="yes"}

## Colunas padrão

| Coluna | Descrição |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Name] | O nome da regra de preço, conforme definido em [Configurações gerais da regra de preço](./pricing-rule-general-settings.md) |
| [!UICONTROL Rule Type] | O tipo de regra, conforme definido em [Ações de Regra de Precificação](./pricing-rule-actions.md) (regra de preço Padrão ou regra de reprecificação inteligente) |
| [!UICONTROL Is Active] | Se a regra está ativa, conforme definido em [Configurações Gerais da Regra de Precificação](./pricing-rule-general-settings.md) |
| [!UICONTROL Priority] | A prioridade sobre outras condições de preço, conforme definido em [Configurações Gerais da Regra de Preços](./pricing-rule-general-settings.md) |
| [!UICONTROL Stop Further Rules Processing] | Indica se regras de preço adicionais são processadas em produtos qualificados para esta regra, como definido em [configurações gerais da regra de preços](./pricing-rule-general-settings.md) |
| [!UICONTROL From Date] | O início do período em que a regra está ativa |
| [!UICONTROL To Date] | O fim do período em que a regra está ativa |
| [!UICONTROL Action] | Lista todas as ações que podem ser aplicadas a uma lista específica. Para aplicar uma ação, clique em **[!UICONTROL Select]** na coluna _[!UICONTROL Action]_. Opções: `Edit Price Rule` / `Delete Price Rule` |
