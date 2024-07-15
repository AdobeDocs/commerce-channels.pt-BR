---
title: Canal de vendas da Amazon - [!UICONTROL Listing Price]
description: Use as configurações de Preço da Lista para determinar a origem do preço e o valor de preço-base (padrão) para as listas do Amazon.
feature: Sales Channels, Products, Price Rules
redirect_from: sales-channels/asc/ob-listing-price.html
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1455'
ht-degree: 0%

---

# [!UICONTROL Listing Price]

As configurações de [!UICONTROL Listing Price] fazem parte das configurações da lista de lojas. As configurações de listagem são acessadas no [painel de armazenamento](./amazon-store-dashboard.md).

Essas configurações definem qual atributo de preço do [!DNL Commerce] usar como fonte de preço, que é o valor de preço base (padrão) para suas listagens do Amazon. Essas configurações são usadas pelas [regras de preços](./pricing-rule-general-settings.md) para ajustar automaticamente o preço de lista do Amazon em relação ao valor definido para _[!UICONTROL Magento Price Source]_.

Você pode configurar seu [escopo de preços](./price-scope.md) como global ou site. Se o escopo de preços estiver definido como `Global`, há uma única fonte de preço para todas as suas lojas/sites. Se o escopo de precificação estiver definido como `Website`, a fonte de preço usará uma lógica de fallback do preço do site (se disponível) seguida pelo preço padrão (global).

Se uma regra de listagem for definida para ser aplicada a mais de um site, a ordem na qual o preço do site será usado será determinada pela configuração de prioridade do site definida na [regra de listagem](./listing-rules.md). Essas regras permitem definir o preço do produto no catálogo. Para ver se você está usando o escopo de preço de site, consulte [Escopo de Preço de Catálogo](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html).

As opções listadas em _[!UICONTROL Magento Price Source]_,_[!UICONTROL Minimum Advertised Price (Map)]_ e _[!UICONTROL Strike Through Price (MSRP)]_incluem os atributos de preço configurados. Os atributos de preço são [!DNL Commerce] atributos de produto com o Tipo de Entrada de Catálogo para o valor Proprietário da Loja definido como `Price`. Consulte [Tipos de Entrada de Atributo](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/attributes-input-types.html).

## Configurar definições de Preço de Listagem {#configure-listing-price-settings}

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda a seção _[!UICONTROL Listing Price]_.

1. Para **[!UICONTROL Magento Price Source]** (obrigatório), escolha uma opção.

   O padrão é `Price`. Essa configuração determina a fonte de preço usada para suas listagens do Amazon. Se você criar [regras de preços](./pricing-products.md), elas serão aplicadas ao valor definido para o atributo selecionado aqui. Você pode selecionar qualquer atributo de precificação configurado. No entanto, se o atributo selecionado não for preenchido para um produto, a origem de preço do produto assumirá `Price` como padrão quando as regras de preço forem aplicadas para determinar o preço de listagem do Amazon publicado.

1. Para **[!UICONTROL Minimum Advertised Price (MAP)**], escolha uma opção.

   O padrão é nenhuma seleção. Essa configuração permite um preço mínimo anunciado (MAP) para um produto. Quando você define um atributo de precificação e o preço da lista de um produto cai abaixo do preço mínimo determinado (com base na origem e nas regras de precificação), esse valor se torna o MAPA para a lista. Essa configuração permite implementar [regras de preços](./pricing-products.md), enquanto ainda controla o preço mínimo de um produto. Para evitar que um preço de lista seja muito baixo, escolha um atributo de precificação para usar como o MAPA. No entanto, se o campo de preço selecionado não estiver definido para um produto, o MAPA não será usado.

1. Para **[!UICONTROL Strike Through Price (MSRP)]**, escolha uma opção.

   O padrão é nenhuma seleção. Essa configuração determina qual atributo de preço é usado como preço de varejo sugerido pelo fabricante (MSRP) para um produto. Se o preço de lista for menor que o MSRP definido, a lista do Amazon será exibida com um tachado do preço MSRP com o preço de lista mais baixo, juntamente com a quantia e a porcentagem calculadas &quot;Você Economiza&quot;. No entanto, se o campo de preço selecionado não estiver definido para um produto, o MSRP não será calculado.

   >[!NOTE]
   >
   >Esta configuração só se aplica às listas que ganharam a posição [Buy Box](./buy-box-competitor-pricing.md). O Buy Box é concedido pela Amazon ao vendedor que tem o produto listado geralmente ao melhor preço, juntamente com outros fatores, como a oferta de envio FBA/Prime, disponibilidade e desempenho do vendedor.

1. Para **Aplicar IVA (Imposto sobre Valor Agregado)**, escolha uma opção:

   - `Disabled` - (Padrão) Escolha quando você não deseja aplicar o IVA ao preço de lista.

   - `Enabled` - Escolha quando deseja aplicar o IVA ao preço da lista. O IVA é normalmente usado como um imposto sobre vendas em países europeus e é adicionado ao preço listado final na Amazon. O IVA não se aplica ao preço final de listagens usadas em uma regra de preço inteligente, a menos que o [preço mínimo](./floor-price.md) seja atingido.

   >[!NOTE]
   >
   >As empresas da União Europeia (UE) devem enviar faturas aos compradores de empresas para que o cliente possa remeter o imposto. Você pode gerar essas NFFs e calcular os impostos ou usar um serviço de cálculo de imposto, como o Serviço de Cálculo de IVA da Amazon. A Amazon recomenda se inscrever no [Serviço de Cálculo de IVA da Amazon](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;). Se você escolher um método diferente, será responsável pela conformidade com o IVA.>
   >
   >Pode levar de 10 a 14 dias para que a Amazon verifique e ative sua conta do Serviço de Cálculo de IVA.

1. Para **[!UICONTROL VAT Percentage]**, insira o valor da sua taxa de IVA.

   O padrão é `0.00`. Este valor é usado para calcular o valor de IVA a ser adicionado ao preço de listagem. Se `10.2` for inserido, 10,20% de IVA será aplicado ao preço da lista. Este campo está desabilitado quando o campo Aplicar Imposto sobre Valor Agregado (VAT) está definido como `Disabled`.

1. **(Somente Lojas no Reino Unido)** Para **[!UICONTROL Amazon Product Tax Code (PTC)]**, escolha uma opção:

   - `Do Not Manage PTC` - (Padrão) Escolha se você está usando um serviço de cálculo de imposto de terceiros ou se já tem todos os cálculos de imposto configurados na conta [!DNL Amazon Seller Central]. Quando escolhido, o canal de vendas da Amazon não envia informações de código de imposto do produto para a conta [!DNL Amazon Seller Central].

   - `Set Default PTC` - Escolha se você tem um PTC (Universal Product Tax Code) que deseja usar para todos os seus produtos. Quando escolhido, você deve concluir _[!UICONTROL Default PTC]_.

      - Para **[!UICONTROL Default PTC]**, insira o PTC padrão a ser usado para todas as listagens qualificadas do Amazon. Se o PTC padrão estiver definido na conta do [!DNL Amazon Seller Central], deixe esse campo em branco. As alterações feitas nesse campo não afetam as listagens existentes do Amazon. Para alterar o PTC Padrão de uma listagem existente, a listagem deve ser [encerrada](./end-listings-manually.md) e uma nova listagem criada.

   >[!NOTE]
   >
   >Se você usar o Serviço de Cálculo de IVA da Amazon, deverá saber a categoria de imposto para seus produtos. Um PTC é o código de ID de categoria de imposto da Amazon para compras B2B na UE. Consulte [Códigos de Imposto de Produto da Amazon](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}.

1. Para **[!UICONTROL Currency Conversion]**, escolha uma opção.

   O padrão é `Disabled`. Estas opções dependem das configurações de [!DNL Commerce] [moeda](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html). Se nenhuma opção estiver disponível, defina as configurações de moeda.

1. Quando terminar, clique em **[!UICONTROL Save listing settings]**.

![Preço de Listagem](assets/amazon-listing-price.png){width="500" zoomable="yes"}

| Campo | Descrição |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Magento Price Source] | Determina a origem de preço usada ao criar suas listagens do Amazon. O padrão é `Price`. Se você escolher um atributo diferente, como `Amazon Price` ou `Special Price`, o valor definido para o atributo será usado para sua lista do Amazon. No entanto, se o atributo selecionado não estiver definido, `Price` será usado. |
| [!UICONTROL Minimum Advertised Price (MAP)] | O atributo [!DNL Commerce] para preço do MAP. Escolher a opção MAPA define automaticamente a lista do Amazon para o preço MAPA se o preço da lista for menor que o preço MAPA. |
| [!UICONTROL Strike Through Price (MSRP)] | O atributo [!DNL Commerce] que representa o preço MSRP. Se o preço de listagem do Amazon for menor que o MSRP, ele exibe um tachado do preço do MSRP e do preço de listagem. Esta configuração também é usada para calcular o valor e a porcentagem de &quot;Você Salva&quot;, mas esse recurso se aplica somente às listas que ganharam a posição [Buy Box](./buy-box-competitor-pricing.md). |
| [!UICONTROL Apply Value Added Tax (VAT)] | O IVA é utilizado pelos vendedores na União Europeia.<br><br>Escolha `Disabled` se não quiser que o IVA seja adicionado aos preços de listagem.<br><br>Escolha `Enabled` e insira a Porcentagem de IVA para aplicar IVA aos preços da sua lista. |
| [!UICONTROL VAT Percentage] | Defina a porcentagem a ser usada para calcular o valor do IVA a ser adicionado ao preço de listagem para suas listagens do Amazon. <br><br>Se você inserir `5`, 5% de IVA será aplicado ao preço de listagem final depois que todas as regras de preços forem aplicadas. O imposto IVA não se aplica ao preço final de listagens usadas em uma regra de preço inteligente, a menos que o [limite mínimo](./floor-price.md) ou o [limite máximo](./optional-ceiling-price.md) seja atingido. |
| [!UICONTROL Amazon Product Tax Code (PTC)] | (Aparece Somente para Lojas no Reino Unido) Determina se o canal de vendas da Amazon envia informações de código de imposto do produto para sua conta [!DNL Amazon Seller Central]. <br><br>Selecione **Não Gerenciar PTC** se estiver usando um serviço de cálculo de imposto de terceiros ou se já tiver todos os cálculos de imposto configurados na conta [!DNL Amazon Seller Central]. Quando definido como esta opção, o canal de vendas da Amazon não envia informações de código de imposto do produto para a conta [!DNL Amazon Seller Central].<br><br>Selecione **Definir PTC Padrão** se tiver um código de imposto de produto universal que deseja usar para todos os seus produtos.<br><br>Consulte [Códigos de Imposto de Produto da Amazon](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}. |
| [!UICONTROL Default PTC] | Aparece somente quando o **Código de Imposto do Produto (PTC)** do Amazon está definido como `Set Default PTC`. Informe o PTC padrão a ser usado para todas as listagens qualificadas do Amazon. Se o PTC padrão estiver definido na conta do [!DNL Amazon Seller Central], deixe esse campo em branco. <br><br>As alterações feitas neste campo não afetam as listagens existentes. A listagem deve ser [encerrada](./end-listings-manually.md) e uma nova listagem criada para que a alteração tenha efeito. |
| [!UICONTROL Currency Conversion] | Permite que a moeda padrão da loja [!DNL Commerce] seja convertida com precisão para a moeda padrão do Amazon para publicar os preços de lista na moeda apropriada. A conversão de moeda é sempre baseada na sua moeda padrão [!DNL Commerce].<br><br>Você ainda poderá exibir o [!DNL Commerce] padrão e as moedas do Amazon quando outras moedas estiverem disponíveis. Se a moeda padrão [!DNL Commerce] corresponder à moeda padrão do Amazon, deixe a opção Conversão de moeda desativada.<br><br>Por exemplo, se a moeda padrão de [!DNL Commerce] for CAD (Dólares canadenses) e a moeda padrão de Amazon for USD, você deverá habilitar a Conversão de Moeda e escolher a Taxa de Conversão CAD em USD. As opções apresentadas são baseadas nas [!DNL Commerce] conversões de moeda internas. Se você não vir a opção que está procurando, [configure a moeda em [!DNL Commerce]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html). |

**Acesso rápido** - [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
