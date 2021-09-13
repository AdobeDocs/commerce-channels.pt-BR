---
title: Gerenciar preços da Amazon
description: Você pode definir preços diferentes para suas listagens do Amazon no armazenamento de comércio eletrônico usando as regras de preços.
redirect_from: /sales-channels/asc/ob-pricing-rules.html
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 0%

---

# Gerenciar preços do Amazon

O canal de vendas da Amazon permite definir regras de preços, que permitem definir seu preço de listagem do Amazon diferente do **[!UICONTROL Magento Price Source]** definido em seu [preço de listagem](./listing-price.md). Você também pode empilhar várias regras e até mesmo usar o preço inteligente para ajustar seu preço de listagem do Amazon com base no preço [[!DNL Buy Box]](./buy-box-competitor-pricing.md) dos concorrentes ou no [preço do concorrente mais baixo](./lowest-competitor-pricing.md).

Existem dois tipos de regras de preços:

- [Regra de Preços Padrão](./standard-price-rules.md)
- [Regra de Reprecificação Inteligente](./intelligent-repricing-rules.md)

   >[!IMPORTANT]
   >
   >As regras inteligentes de reprecificação não funcionam corretamente se a região do Amazon estiver definida como status `Inactive` , como durante a integração. Seus cálculos de preços dependem das taxas de frete e sua região deve estar com o status `Active` para que as taxas de frete sejam sincronizadas do Amazon.
   >
   >Para atualizar o status da região na conta do Amazon, acesse Configurações > Informações da conta > Configurações de férias. Consulte [Amazon: Listando Status de Férias](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620){:target=&quot;_blank&quot;} (é necessário o logon Central do vendedor).

Este recurso permite manipular os preços do Amazon de uma maneira semelhante às [!DNL Commerce] [regras de preço do catálogo](https://docs.magento.com/user-guide/catalog/pricing.html){:target=&quot;_blank&quot;}. Você pode criar regras complexas que permitem alterar os preços de produtos específicos, produtos dentro de categorias específicas ou mesmo com atributos específicos.

Você pode adicionar regras de preços para suas listas do Amazon. As regras de preço podem ser usadas para ajustar automaticamente seus preços de listagem, com base em um conjunto de condições definidas. As regras de preço são acionadas e calculadas antes que o produto seja listado na Amazon.

>[!NOTE]
>
>A fonte de preço das listagens do Amazon é definida para **[!UICONTROL Magento Price Source]** nas configurações de [preço de listagem](./listing-price.md). Qualquer cálculo de ajuste definido na regra de precificação usa a fonte de preço como o valor inicial.

As regras de preços permitem que você defina seu preço de listagem do Amazon diferente de seu **[!UICONTROL Magento Price Source]** nas configurações de [preço de listagem](./listing-price.md). Você também pode empilhar várias regras que trabalham juntas para ajustar seu preço.

Uma regra de precificação/reprecificação requer três conjuntos de informações durante sua configuração:

- [Configurações](./pricing-rule-general-settings.md) gerais: Define o nome, a descrição, as datas ativas, a prioridade de uma regra e define o comportamento das regras subsequentes, com base em sua configuração de prioridade.
- [Condições](./pricing-rule-conditions.md): Determine quais produtos estão qualificados para a regra de preço.
- [Ações](./pricing-rule-actions.md): Defina os cálculos de ajuste que são aplicados à fonte de preço para determinar o preço da listagem.

Você pode criar [regras de preços padrão](./standard-price-rules.md) que ajustam automaticamente seu preço de listagem do Amazon em relação ao **[!UICONTROL Magento Price Source]** selecionado em suas configurações de [preço de listagem](./listing-price.md). Este recurso permite manipular os preços do Amazon de uma maneira semelhante às [!DNL Commerce] [regras de preço do catálogo](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){:target=&quot;_blank&quot;}. Você pode criar regras complexas que alteram automaticamente os preços de produtos específicos, produtos dentro de categorias específicas ou produtos com atributos específicos. Você pode concluir as configurações tradicionais e reprecificar seus produtos para aumentar ou diminuir com base em um valor fixo ou em uma porcentagem.

Outra ferramenta poderosa é o recurso [Reprecificação Inteligente](./intelligent-repricing-rules.md) que ajusta o preço de listagem da Amazon com base no preço do concorrente [[!DNL Buy Box]](./buy-box-competitor-pricing.md) ou no [Preço do Concorrente Mais Baixo](./lowest-competitor-pricing.md). Semelhante às [!DNL Commerce] [regras de preço do catálogo](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){:target=&quot;_blank&quot;}, esse recurso avançado permite manipular os preços do Amazon criando regras complexas. As regras podem definir o escopo de uma alteração de preço para produtos específicos, produtos dentro de categorias específicas ou mesmo com atributos de produto específicos.

Usar reprecificação inteligente para ajustar os preços da listagem do Amazon, com base nos preços do concorrente. O canal de vendas da Amazon criou proteções para você configurar o para proteger margens ou evitar a correspondência dos preços de um comerciante com pouco feedback. Usando [regras inteligentes de reprecificação](./intelligent-repricing-rules.md), os preços de listagem da Amazon podem ser manipulados automaticamente como um valor fixo ou porcentagem (para cima ou para baixo) ou até mesmo sincronizados com o preço [[!DNL Buy Box]](./buy-box-competitor-pricing.md) ou [Menor Preço da Concorrência](./lowest-competitor-pricing.md) com base no item. As regras podem até ser empilhadas para proporcionar flexibilidade ilimitada.

Você pode controlar aspectos importantes das regras, como status ativo/inativo, elegibilidade do site, intervalos de datas opcionais e níveis de prioridade opcionais (usados para empilhamento de regras).

Por exemplo, você pode definir e definir as condições para uma regra de preço que, quando as condições forem atendidas, ajusta automaticamente o preço da listagem antes de ela ser enviada para a Amazon.

Outra opção de precificação é uma [substituição de preço](./overrides.md), que é definida no nível da listagem individual. Uma [substituição de preço](./overrides.md) pode ser definida e uma substituição ignora/tem prioridade sobre todos os outros padrões, configurações e regras. Um [override](./overrides.md) pode ser definido para notas de preço, tempo de manuseio, condição e vendedor (com algumas exceções).

![Regras de preços](assets/amazon-pricing-rules.png)

## Colunas padrão

| Coluna | Descrição |
|---|---|
| [!UICONTROL Name] | O nome da regra de precificação, conforme definido em [Configurações Gerais da Regra de Precificação](./pricing-rule-general-settings.md) |
| [!UICONTROL Rule Type] | O tipo de regra, conforme definido em [Ações da Regra de Precificação](./pricing-rule-actions.md) (Regra de preço padrão ou Regra de reprecificação inteligente) |
| [!UICONTROL Is Active] | Se a regra está ativa, conforme definido em [Configurações Gerais da Regra de Precificação](./pricing-rule-general-settings.md) |
| [!UICONTROL Priority] | A prioridade sobre outras condições de precificação, conforme definido em [Configurações Gerais da Regra de Precificação](./pricing-rule-general-settings.md) |
| [!UICONTROL Stop Further Rules Processing] | Indica se outras regras de preço são processadas em produtos elegíveis para esta regra, conforme definido em [configurações gerais da regra de precificação](./pricing-rule-general-settings.md) |
| [!UICONTROL From Date] | O início do período em que a regra está ativa |
| [!UICONTROL To Date] | O fim do período em que a regra está ativa |
| [!UICONTROL Action] | Lista todas as ações que podem ser aplicadas a uma lista específica. Para aplicar uma ação, clique em **[!UICONTROL Select]** na coluna _[!UICONTROL Action]_. Opções: `Edit Price Rule` / `Delete Price Rule` |
