---
title: Canal de vendas do Amazon - [!UICONTROL Listing Price]
description: Use as configurações de Preço da Lista para determinar a origem do preço e o valor de preço-base (padrão) para as listas do Amazon.
redirect_from: sales-channels/asc/ob-listing-price.html
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '1503'
ht-degree: 0%

---

# [!UICONTROL Listing Price]

[!UICONTROL Listing Price] as configurações fazem parte das configurações da lista de lojas. As configurações de listagem são acessadas no [painel de armazenamento](./amazon-store-dashboard.md).

Essas configurações definem quais [!DNL Commerce] atributo de precificação a ser usado como origem de preço, que é o valor de preço base (padrão) para suas listagens do Amazon. Essas configurações são usadas pelo seu [regras de preços](./pricing-rule-general-settings.md) para ajustar automaticamente o preço de listagem do Amazon em relação ao valor definido para _[!UICONTROL Magento Price Source]_.

Você pode configurar suas [escopo de precificação](./price-scope.md) como global ou site. Se o escopo de precificação estiver definido como `Global`, há uma única fonte de preço para todas as suas lojas/sites. Se o escopo de precificação estiver definido como `Website`, a fonte de preço usa a lógica de fallback do preço do site (se disponível) seguida pelo preço padrão (global).

Se uma regra de listagem for definida para ser aplicada a mais de um site, a ordem em que o preço do site é usado será determinada pela configuração de prioridade do site definida na [regra de listagem](./listing-rules.md). Essas regras permitem definir o preço do produto no catálogo. Para ver se você está usando o escopo de preço do site, consulte [Escopo do Preço de Catálogo](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html).

As opções listadas em _[!UICONTROL Magento Price Source]_,_[!UICONTROL Minimum Advertised Price (Map)]_, e _[!UICONTROL Strike Through Price (MSRP)]_inclua os atributos de Preço configurados. Os atributos de preço são [!DNL Commerce] atributos de produto com o valor Tipo de Entrada de Catálogo para Proprietário da Loja definido como `Price`. Consulte [Tipos de entrada de atributo](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/attributes-input-types.html).

## Configurar definições de Preço de Listagem {#configure-listing-price-settings}

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda a _[!UICONTROL Listing Price]_seção.

1. Para **[!UICONTROL Magento Price Source]** (obrigatório), escolha uma opção.

   O padrão é `Price`. Essa configuração determina a fonte de preço usada para suas listagens do Amazon. Se você criar [regras de preços](./pricing-products.md), as regras são aplicadas ao valor definido para o atributo selecionado aqui. Você pode selecionar qualquer atributo de precificação configurado. No entanto, se o atributo selecionado não for preenchido para um produto, a origem de preço do produto volta para `Price` quando as regras de precificação são aplicadas para determinar o preço de listagem do Amazon publicado.

1. Para **[!UICONTROL Minimum Advertised Price (MAP)**], escolha uma opção.

   O padrão é nenhuma seleção. Essa configuração permite um preço mínimo anunciado (MAP) para um produto. Quando você define um atributo de precificação e o preço da lista de um produto cai abaixo do preço mínimo determinado (com base na origem e nas regras de precificação), esse valor se torna o MAPA para a lista. Essa configuração permite implementar [regras de preços](./pricing-products.md), enquanto ainda controla o preço mínimo de um produto. Para evitar que um preço de lista seja muito baixo, escolha um atributo de precificação para usar como o MAPA. No entanto, se o campo de preço selecionado não estiver definido para um produto, o MAPA não será usado.

1. Para **[!UICONTROL Strike Through Price (MSRP)]**, escolha uma opção.

   O padrão é nenhuma seleção. Essa configuração determina qual atributo de preço é usado como preço de varejo sugerido pelo fabricante (MSRP) para um produto. Se o preço de lista for menor que o MSRP definido, a lista do Amazon será exibida com um tachado do preço MSRP com o preço de lista mais baixo, juntamente com a quantia e a porcentagem calculadas &quot;Você Economiza&quot;. No entanto, se o campo de preço selecionado não estiver definido para um produto, o MSRP não será calculado.

   >[!NOTE]
   >
   >Essa configuração se aplica somente às listagens que ganharam o [Buy Box](./buy-box-competitor-pricing.md) posição. O Buy Box é concedido pela Amazon ao vendedor que tem o produto listado geralmente ao melhor preço, juntamente com outros fatores, como a oferta de envio FBA/Prime, disponibilidade e desempenho do vendedor.

1. Para **Aplicar IVA (Imposto sobre Valor Agregado)**, escolha uma opção:

   - `Disabled` - (Padrão) Escolha quando você não deseja aplicar o IVA ao preço da lista.

   - `Enabled` - Escolha quando deseja aplicar o IVA ao preço da lista. O IVA é normalmente usado como um imposto sobre vendas em países europeus e é adicionado ao preço listado final na Amazon. o IVA não se aplica ao preço final das cotações utilizadas no âmbito de uma regra de tarifação inteligente, a menos [preço mínimo](./floor-price.md) é uma ocorrência.
   >[!NOTE]
   >
   >As empresas da União Europeia (UE) devem enviar faturas aos compradores de empresas para que o cliente possa remeter o imposto. Você pode gerar essas NFFs e calcular os impostos ou usar um serviço de cálculo de imposto, como o Serviço de Cálculo de IVA da Amazon. A Amazon recomenda se inscrever no [Serviço de Cálculo de IVA da Amazon](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;). Se você escolher um método diferente, será responsável pela conformidade com o IVA.>
   >
   >Pode levar de 10 a 14 dias para que a Amazon verifique e ative sua conta do Serviço de Cálculo de IVA.

1. Para **[!UICONTROL VAT Percentage]**, informe o valor da taxa de IVA.

   O padrão é `0.00`. Este valor é usado para calcular o valor de IVA a ser adicionado ao preço de listagem. Se `10.2` for informado, um IVA de 10,20% será aplicado ao preço da lista. Este campo fica desativado quando o campo Aplicar Imposto sobre Valor Agregado (IVA) é definido como `Disabled`.

1. **(Somente lojas no Reino Unido)** Para **[!UICONTROL Amazon Product Tax Code (PTC)]**, escolha uma opção:

   - `Do Not Manage PTC` - (Padrão) Escolha se você está usando um serviço de cálculo de imposto de terceiros ou se já tem todos os cálculos de imposto configurados no [!DNL Amazon Seller Central] conta. Quando escolhido, o canal de vendas do Amazon não envia informações de código de imposto do produto para o [!DNL Amazon Seller Central] conta.

   - `Set Default PTC` - Escolha se você tem um código de imposto de produto universal (PTC) que deseja usar para todos os seus produtos. Quando escolhido, você deve concluir _[!UICONTROL Default PTC]_.

      - Para **[!UICONTROL Default PTC]**, insira o PTC padrão a ser usado para todas as listagens qualificadas do Amazon. Se o PTC padrão estiver definido no seu [!DNL Amazon Seller Central] deixe este campo em branco. As alterações feitas nesse campo não afetam as listagens existentes do Amazon. Para alterar o PTC Padrão de uma listagem existente, a listagem deve ser [encerrado](./end-listings-manually.md) e uma nova lista criada.
   >[!NOTE]
   >
   >Se você usar o Serviço de Cálculo de IVA da Amazon, deverá saber a categoria de imposto para seus produtos. Um PTC é o código de ID de categoria de imposto da Amazon para compras B2B na UE. Consulte [Códigos de Imposto do Produto da Amazon](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}.

1. Para **[!UICONTROL Currency Conversion]**, escolha uma opção.

   O padrão é `Disabled`. Essas opções dependem do seu [!DNL Commerce] [moeda](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html) configurações. Se nenhuma opção estiver disponível, defina as configurações de moeda.

1. Quando terminar, clique em **[!UICONTROL Save listing settings]**.

![Preço de Listagem](assets/amazon-listing-price.png){width="500" zoomable="yes"}

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Magento Price Source] | Determina a origem de preço usada ao criar suas listagens do Amazon. O padrão é `Price`. Se você escolher um atributo diferente, como `Amazon Price` ou `Special Price`, o valor definido para o atributo é usado para sua lista do Amazon. No entanto, se o atributo selecionado não estiver definido, `Price` é usada. |
| [!UICONTROL Minimum Advertised Price (MAP)] | A variável [!DNL Commerce] atributo para precificação do MAP. Escolher a opção MAPA define automaticamente a lista do Amazon para o preço MAPA se o preço da lista for menor que o preço MAPA. |
| [!UICONTROL Strike Through Price (MSRP)] | A variável [!DNL Commerce] atributo que representa o preço do MSRP. Se o preço de listagem do Amazon for menor que o MSRP, ele exibe um tachado do preço do MSRP e do preço de listagem. Essa configuração também é usada para calcular o valor e a porcentagem de &quot;Você salva&quot;, mas esse recurso se aplica somente às listagens que ganharam o [Buy Box](./buy-box-competitor-pricing.md) posição. |
| [!UICONTROL Apply Value Added Tax (VAT)] | O IVA é utilizado pelos vendedores na União Europeia.<br><br>Escolher `Disabled` se você não quiser que o IVA seja adicionado aos preços da lista.<br><br>Escolher `Enabled` e, em seguida, informe a Porcentagem de IVA para aplicar IVA aos preços da lista. |
| [!UICONTROL VAT Percentage] | Defina a porcentagem a ser usada para calcular o valor do IVA a ser adicionado ao preço de listagem para suas listagens do Amazon. <br><br>Se você inserir `5`Em seguida, um IVA de 5% será aplicado ao preço de lista final após a aplicação de todas as regras de preços. o imposto sobre o valor acrescentado não se aplica ao preço final das cotações utilizadas no âmbito de uma regra de fixação [andar](./floor-price.md) ou [teto](./optional-ceiling-price.md) é uma ocorrência. |
| [!UICONTROL Amazon Product Tax Code (PTC)] | (Aparece Somente para Lojas no Reino Unido) Determina se o canal de vendas do Amazon envia informações de código de imposto do produto para o seu [!DNL Amazon Seller Central] conta. <br><br>Selecionar **Não gerenciar PTC** se você estiver usando um serviço de cálculo de imposto de terceiros ou já tiver todos os cálculos de imposto configurados no [!DNL Amazon Seller Central] conta. Quando definido para esta opção, o canal de vendas do Amazon não envia informações de código de imposto do produto para o [!DNL Amazon Seller Central] conta.<br><br>Selecionar **Definir PTC padrão** se você tiver um código de imposto de produto universal que deseja usar para todos os seus produtos.<br><br>Consulte [Códigos de Imposto do Produto da Amazon](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}. |
| [!UICONTROL Default PTC] | Aparece somente quando **Código de Imposto do Produto (PTC) do Amazon** está definida como `Set Default PTC`. Informe o PTC padrão a ser usado para todas as listagens qualificadas do Amazon. Se o PTC padrão estiver definido no seu [!DNL Amazon Seller Central] deixe este campo em branco. <br><br>As alterações feitas nesse campo não afetam as listagens existentes. A listagem deve ser [encerrado](./end-listings-manually.md) e uma nova lista criada para que a alteração entre em vigor. |
| [!UICONTROL Currency Conversion] | Permite que [!DNL Commerce] a moeda padrão da loja para converter com precisão para a sua moeda padrão do Amazon para publicar seus preços de lista na moeda apropriada. A conversão de moeda é sempre baseada em seus [!DNL Commerce] moeda padrão.<br><br>Você ainda pode exibir seu padrão [!DNL Commerce] e Amazon quando outras moedas estiverem disponíveis. Se o seu padrão [!DNL Commerce] A moeda corresponde à moeda padrão do Amazon. Deixe a opção Conversão de moeda desativada.<br><br>Por exemplo, se o [!DNL Commerce] A moeda padrão é CAD (Dólares canadenses) e a moeda padrão do Amazon é USD, você deve ativar a Conversão de moeda e escolher a Taxa de conversão CAD para USD. As opções apresentadas baseiam-se no modelo [!DNL Commerce] conversões de moeda. Se você não vir a opção que está procurando, [configurar a moeda em [!DNL Commerce]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html). |

**Acesso rápido** - [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
