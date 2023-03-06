---
title: Gerenciar preços do Amazon
description: Você pode definir os preços das suas listagens do Amazon para diferirem da sua loja de comércio usando as regras de preços.
redirect_from: /sales-channels/asc/ob-pricing-rules.html
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 0%

---

# Gerenciar preços do Amazon

O canal de vendas do Amazon permite definir regras de preços, que permitem definir o preço de lista do Amazon diferente do definido **[!UICONTROL Magento Price Source]** no seu [preço de lista](./listing-price.md). Você também pode empilhar várias regras e até mesmo usar os preços inteligentes para ajustar o preço de sua lista do Amazon com base nos preços dos concorrentes [[!DNL Buy Box]](./buy-box-competitor-pricing.md) preço ou o [preço mais baixo do concorrente](./lowest-competitor-pricing.md).

Há dois tipos de regras de precificação:

- [Regra de Preço Padrão](./standard-price-rules.md)
- [Regra inteligente de reprecificação](./intelligent-repricing-rules.md)

   >[!IMPORTANT]
   >
   >As regras de reprecificação inteligentes não funcionarão adequadamente se a região do Amazon estiver definida como `Inactive` status, como está durante a integração. Os cálculos de preço dependem das taxas de entrega e sua região deve estar em `Active` Status das taxas de envio para sincronização no Amazon.
   >
   >Para atualizar o status da região na conta do Amazon, acesse Configurações > Informações da conta > Configurações de férias. Consulte [Amazon: Status de Listagem para Férias](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620){target="_blank"} (logon da Central de Vendedores necessário).

Esse recurso permite manipular os preços do Amazon de uma forma semelhante ao [!DNL Commerce] [regras de preço de catálogo](https://docs.magento.com/user-guide/catalog/pricing.html){target="_blank"}. Você pode criar regras complexas que permitem alterar os preços de produtos específicos, produtos dentro de categorias específicas ou até mesmo com atributos específicos.

Você pode adicionar regras de preços para suas listagens do Amazon. As regras de preços podem ser usadas para ajustar automaticamente os preços da lista, com base em um conjunto de condições definidas. As regras de preço são acionadas e calculam o preço ajustado antes que seu produto seja listado no Amazon.

>[!NOTE]
>
>A origem de preço para suas listagens do Amazon é definida para **[!UICONTROL Magento Price Source]** no seu [preço de lista](./listing-price.md) configurações. Qualquer cálculo de ajuste definido na regra de precificação usa a origem de preço como o valor inicial.

As regras de preços permitem definir um preço de lista do Amazon diferente do seu **[!UICONTROL Magento Price Source]** no seu [preço de lista](./listing-price.md) configurações. Você também pode empilhar várias regras que funcionam juntas para ajustar o preço.

Uma regra de precificação/reprecificação requer três conjuntos de informações durante sua configuração:

- [Configurações gerais](./pricing-rule-general-settings.md): define o nome, a descrição, as datas ativas e a prioridade de uma regra, além de definir o comportamento das regras subsequentes com base em sua configuração de prioridade.
- [Condições](./pricing-rule-conditions.md): determine quais produtos estão qualificados para a regra de preço.
- [Ações](./pricing-rule-actions.md): Defina os cálculos de ajuste que são aplicados à origem de preço para determinar o preço da lista.

Você pode criar [regras de preço padrão](./standard-price-rules.md) que ajustam automaticamente seu preço de listagem do Amazon em relação ao **[!UICONTROL Magento Price Source]** no seu [preço de lista](./listing-price.md) configurações. Esse recurso permite manipular os preços do Amazon de uma forma semelhante ao [!DNL Commerce] [regras de preço de catálogo](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target="_blank"}. Você pode criar regras complexas que alteram automaticamente os preços de produtos específicos, produtos dentro de categorias específicas ou produtos com atributos específicos. É possível concluir as configurações tradicionais e reavaliar o preço dos produtos para aumentar ou diminuir com base em uma quantidade fixa ou porcentagem.

Outra ferramenta poderosa é a [Reavaliação inteligente de preços](./intelligent-repricing-rules.md) recurso que ajusta o preço de sua lista do Amazon com base no concorrente [[!DNL Buy Box]](./buy-box-competitor-pricing.md) preço ou [Menor preço de concorrente](./lowest-competitor-pricing.md). Semelhante ao [!DNL Commerce] [regras de preço de catálogo](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target="_blank"}, esse recurso avançado permite manipular os preços do Amazon criando regras complexas. As regras podem definir o escopo de uma alteração de preço para produtos específicos, produtos dentro de categorias específicas ou mesmo com atributos específicos do produto.

Usar a reavaliação de preços inteligente para ajustar os preços de sua lista do Amazon, com base nos preços do concorrente. O canal de vendas da Amazon tem proteções integradas para que você configure o para proteger as margens ou evitar a correspondência dos preços de um comerciante com pouco feedback. Usar [regras inteligentes de reavaliação de preços](./intelligent-repricing-rules.md), os preços de listagem do Amazon podem ser manipulados automaticamente como uma quantia fixa ou de porcentagem (para cima ou para baixo) ou até mesmo sincronizados com o [[!DNL Buy Box]](./buy-box-competitor-pricing.md) preço ou [Menor preço de concorrente](./lowest-competitor-pricing.md) por item. As regras podem até ser empilhadas para fornecer flexibilidade ilimitada.

Você pode controlar aspectos importantes das regras, como status ativo/inativo, elegibilidade do site, intervalos de datas opcionais e níveis de prioridade opcionais (usados para empilhamento de regras).

Por exemplo, você pode definir e definir as condições para uma regra de preço que, quando as condições forem atendidas, ajuste automaticamente o preço de lista antes de ser enviado ao Amazon.

Outra opção de preço é uma [substituição de preço](./overrides.md), que é definido no nível de lista individual. A [substituição de preço](./overrides.md) O pode ser definido e uma substituição ignora/tem prioridade sobre todos os outros padrões, configurações e regras. Um [substituir](./overrides.md) pode ser definido para preço, tempo de manuseio, condição e notas do vendedor (com algumas exceções).

![Regras de preços](assets/amazon-pricing-rules.png)

## Colunas padrão

| Coluna | Descrição |
|---|---|
| [!UICONTROL Name] | O nome da regra de precificação, conforme definido em [Configurações Gerais da Regra de Precificação](./pricing-rule-general-settings.md) |
| [!UICONTROL Rule Type] | O tipo de regra, conforme definido em [Ações da Regra de Precificação](./pricing-rule-actions.md) (regra de preço Padrão ou regra de reprecificação inteligente) |
| [!UICONTROL Is Active] | Se a regra está ativa, conforme definido em [Configurações Gerais da Regra de Precificação](./pricing-rule-general-settings.md) |
| [!UICONTROL Priority] | A prioridade sobre outras condições de fixação de preços, [Configurações Gerais da Regra de Precificação](./pricing-rule-general-settings.md) |
| [!UICONTROL Stop Further Rules Processing] | Indica se outras regras de preços são processadas em produtos elegíveis para essa regra, conforme definido em [configurações gerais da regra de preço](./pricing-rule-general-settings.md) |
| [!UICONTROL From Date] | O início do período em que a regra está ativa |
| [!UICONTROL To Date] | O fim do período em que a regra está ativa |
| [!UICONTROL Action] | Lista todas as ações que podem ser aplicadas a uma lista específica. Para aplicar uma ação, clique em **[!UICONTROL Select]** no _[!UICONTROL Action]_coluna. Opções: `Edit Price Rule` / `Delete Price Rule` |
