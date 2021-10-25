---
title: Gerenciar preços da Amazon
description: Você pode definir preços diferentes para suas listagens do Amazon no armazenamento de comércio eletrônico usando as regras de preços.
redirect_from: /sales-channels/asc/ob-pricing-rules.html
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 0%

---

# Gerenciar preços do Amazon

O canal de vendas da Amazon permite definir regras de preços, que permitem definir seu preço de listagem do Amazon diferente do definido **[!UICONTROL Magento Price Source]** em seu [preço de cotação](./listing-price.md). Você também pode empilhar várias regras e até mesmo usar o preço inteligente para ajustar seu preço de listagem do Amazon com base em concorrentes [[!DNL Buy Box]](./buy-box-competitor-pricing.md) ou [preço mais baixo do concorrente](./lowest-competitor-pricing.md).

Existem dois tipos de regras de preços:

- [Regra de Preços Padrão](./standard-price-rules.md)
- [Regra de Reprecificação Inteligente](./intelligent-repricing-rules.md)

   >[!IMPORTANT]
   >
   >Regras inteligentes de redefinição de preços não funcionam corretamente se a região do Amazon estiver definida como `Inactive` , como durante a integração. Seus cálculos de preços dependem das taxas de frete e sua região deve estar em `Active` status para suas taxas de frete sincronizarem do Amazon.
   >
   >Para atualizar o status da região na conta do Amazon, acesse Configurações > Informações da conta > Configurações de férias. Consulte [Amazon: Status de Listagem para Férias](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620){target=&quot;_blank&quot;} (logon do Seller Central necessário).

Esse recurso permite manipular os preços da Amazon de uma maneira semelhante à [!DNL Commerce] [regras de preço de catálogo](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}. Você pode criar regras complexas que permitem alterar os preços de produtos específicos, produtos dentro de categorias específicas ou mesmo com atributos específicos.

Você pode adicionar regras de preços para suas listas do Amazon. As regras de preço podem ser usadas para ajustar automaticamente seus preços de listagem, com base em um conjunto de condições definidas. As regras de preço são acionadas e calculadas antes que o produto seja listado na Amazon.

>[!NOTE]
>
>A fonte de preço das listagens do Amazon é definida para **[!UICONTROL Magento Price Source]** em seu [preço de cotação](./listing-price.md) configurações. Qualquer cálculo de ajuste definido na regra de precificação usa a fonte de preço como o valor inicial.

As regras de preços permitem que você defina o preço da listagem da Amazon diferente de seu **[!UICONTROL Magento Price Source]** em seu [preço de cotação](./listing-price.md) configurações. Você também pode empilhar várias regras que trabalham juntas para ajustar seu preço.

Uma regra de precificação/reprecificação requer três conjuntos de informações durante sua configuração:

- [Configurações gerais](./pricing-rule-general-settings.md): Define o nome, a descrição, as datas ativas, a prioridade de uma regra e define o comportamento das regras subsequentes, com base em sua configuração de prioridade.
- [Condições](./pricing-rule-conditions.md): Determine quais produtos estão qualificados para a regra de preço.
- [Ações](./pricing-rule-actions.md): Defina os cálculos de ajuste que são aplicados à fonte de preço para determinar o preço da listagem.

Você pode criar [regras padrão de preços](./standard-price-rules.md) que ajustam automaticamente o preço da listagem do Amazon em relação ao selecionado **[!UICONTROL Magento Price Source]** em seu [preço de cotação](./listing-price.md) configurações. Esse recurso permite manipular os preços da Amazon de uma maneira semelhante à [!DNL Commerce] [regras de preço de catálogo](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;}. Você pode criar regras complexas que alteram automaticamente os preços de produtos específicos, produtos dentro de categorias específicas ou produtos com atributos específicos. Você pode concluir as configurações tradicionais e reprecificar seus produtos para aumentar ou diminuir com base em um valor fixo ou em uma porcentagem.

Outra ferramenta poderosa é a [Reprecificação inteligente](./intelligent-repricing-rules.md) recurso que ajusta o preço da listagem do Amazon com base no concorrente [[!DNL Buy Box]](./buy-box-competitor-pricing.md) preço ou [Menor preço do concorrente](./lowest-competitor-pricing.md). Semelhante ao [!DNL Commerce] [regras de preço de catálogo](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;}, esse recurso avançado permite manipular os preços do Amazon criando regras complexas. As regras podem definir o escopo de uma alteração de preço para produtos específicos, produtos dentro de categorias específicas ou mesmo com atributos de produto específicos.

Usar reprecificação inteligente para ajustar os preços da listagem do Amazon, com base nos preços do concorrente. O canal de vendas da Amazon criou proteções para você configurar o para proteger margens ou evitar a correspondência dos preços de um comerciante com pouco feedback. Usando [regras inteligentes de redefinição de preços](./intelligent-repricing-rules.md), os preços da listagem do Amazon podem ser manipulados automaticamente como um valor fixo ou porcentagem (para cima ou para baixo) ou até mesmo sincronizados com a variável [[!DNL Buy Box]](./buy-box-competitor-pricing.md) preço ou [Menor preço do concorrente](./lowest-competitor-pricing.md) por item. As regras podem até ser empilhadas para proporcionar flexibilidade ilimitada.

Você pode controlar aspectos importantes das regras, como status ativo/inativo, elegibilidade do site, intervalos de datas opcionais e níveis de prioridade opcionais (usados para empilhamento de regras).

Por exemplo, você pode definir e definir as condições para uma regra de preço que, quando as condições forem atendidas, ajusta automaticamente o preço da listagem antes de ela ser enviada para a Amazon.

Outra opção de preço é uma [substituição de preço](./overrides.md), que é definido no nível da listagem individual. A [substituição de preço](./overrides.md) pode ser definida e uma substituição ignora/tem prioridade sobre todos os outros padrões, configurações e regras. Um [override](./overrides.md) pode ser definido para preço, tempo de manuseio, condição e notas de vendedor (com algumas exceções).

![Regras de preços](assets/amazon-pricing-rules.png)

## Colunas padrão

| Coluna | Descrição |
|---|---|
| [!UICONTROL Name] | O nome da regra de precificação, conforme definido em [Configurações gerais da regra de preços](./pricing-rule-general-settings.md) |
| [!UICONTROL Rule Type] | O tipo de regra, como definido em [Ações das Regras de Preços](./pricing-rule-actions.md) (Regra de preço padrão ou Regra de reprecificação inteligente) |
| [!UICONTROL Is Active] | Se a regra está ativa, como definido em [Configurações gerais da regra de preços](./pricing-rule-general-settings.md) |
| [!UICONTROL Priority] | A prioridade em relação a outras condições de fixação de preços, tal como definido em [Configurações gerais da regra de preços](./pricing-rule-general-settings.md) |
| [!UICONTROL Stop Further Rules Processing] | Indica se novas regras de preços são transformadas em produtos elegíveis para esta regra, como definido em [configurações gerais da regra de preços](./pricing-rule-general-settings.md) |
| [!UICONTROL From Date] | O início do período em que a regra está ativa |
| [!UICONTROL To Date] | O fim do período em que a regra está ativa |
| [!UICONTROL Action] | Lista todas as ações que podem ser aplicadas a uma lista específica. Para aplicar uma ação, clique em **[!UICONTROL Select]** no _[!UICONTROL Action]_coluna. Opções: `Edit Price Rule` / `Delete Price Rule` |
