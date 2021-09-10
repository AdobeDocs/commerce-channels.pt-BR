---
title: Preço de Listagem
description: Use as configurações de Preço de Listagem para determinar a fonte de preço e o valor de preço base (padrão) para suas listagens do Amazon.
redirect_from: /sales-channels/asc/ob-listing-price.html: 
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 1509
ht-degree: 0%

---

# Preço de Listagem

[!UICONTROL Listing Price] As configurações fazem parte das configurações da listagem de loja. As configurações de listagem são acessadas no [painel de armazenamento](./amazon-store-dashboard.md).

Essas configurações definem qual [!DNL Commerce] atributo de preço usar como fonte de preço, que é o valor base (padrão) do preço para suas listagens do Amazon. Essas configurações são usadas pelas [regras de precificação](./pricing-rule-general-settings.md) para ajustar automaticamente o preço de listagem do Amazon em relação ao valor definido para _[!UICONTROL Magento Price Source]_.

Você pode configurar seu [escopo de precificação](./price-scope.md) como global ou site. Se o escopo de precificação estiver definido como `Global`, haverá uma única fonte de preço para todas as suas lojas/sites. Se seu escopo de precificação estiver definido como `Website`, a fonte de preço usará a lógica de fallback do preço do site (se disponível) seguido pelo preço padrão (global).

Se uma regra de listagem for definida para ser aplicada a mais de um site, a ordem em que o preço do site é usado é determinada pela configuração de prioridade do site definida na [regra de listagem](./listing-rules.md). Essas regras permitem definir preços de produtos no catálogo. Para ver se você está usando o escopo de preço do site, consulte [Escopo do Preço do Catálogo](https://docs.magento.com/user-guide/catalog/catalog-price-scope.html){target=&quot;_blank&quot;}.

As opções listadas em _[!UICONTROL Magento Price Source]_,_[!UICONTROL Minimum Advertised Price (Map)]_ e _[!UICONTROL Strike Through Price (MSRP)]_incluem os atributos de preços configurados. Os atributos de preço são [!DNL Commerce] atributos de produto com o Tipo de entrada do catálogo para o Valor do proprietário da loja definido como `Price`. Consulte [Tipos de Entrada de Atributo](https://docs.magento.com/user-guide/stores/attributes-input-types.html){target=&quot;_blank&quot;}.

## Definir configurações de Preço de Listagem {#configure-listing-price-settings}

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda a seção _[!UICONTROL Listing Price]_.

1. Para **[!UICONTROL Magento Price Source]** (obrigatório), escolha uma opção.

   O padrão é `Price`. Essa configuração determina a fonte de preço usada para suas listagens do Amazon. Se você criar [regras de precificação](./pricing-products.md), as regras serão aplicadas ao valor definido para o atributo selecionado aqui. Você pode selecionar qualquer atributo de preço configurado. No entanto, se o atributo selecionado não for preenchido em um produto, a fonte de preço do produto volta ao padrão `Price` quando as regras de preço são aplicadas para determinar o preço da listagem do Amazon publicado.

1. Para **[!UICONTROL Minimum Advertised Price (MAP)**], escolha uma opção.

   O padrão é nenhuma seleção. Esta configuração permite um preço mínimo anunciado (MAP) para um produto. Ao definir um atributo de preço e o preço listado de um produto cair abaixo do preço mínimo determinado (com base na fonte de preço e nas regras), esse valor se torna o MAPA para a listagem. Essa configuração permite implementar [regras de precificação](./pricing-products.md), enquanto ainda controla seu preço mínimo para um produto. Para evitar que o preço da listagem seja muito baixo, escolha um atributo de preço a ser usado como MAPA. No entanto, se o campo de preço selecionado não estiver definido para um produto, o MAP não será usado.

1. Para **[!UICONTROL Strike Through Price (MSRP)]**, escolha uma opção.

   O padrão é nenhuma seleção. Essa configuração determina qual atributo de preço é usado como o preço de varejo sugerido pelo fabricante (MSRP) para um produto. Se o seu preço de listagem for menor que o MSRP definido, sua listagem do Amazon será exibida com um aumento do preço do MSRP com o menor preço de listagem, juntamente com o valor e a porcentagem de &quot;Você economiza&quot; calculados. No entanto, se o campo de preço selecionado não estiver definido para um produto, o MSRP não será calculado.

   >[!NOTE]
   >
   >Essa configuração se aplica somente a listagens que ganharam a posição [Buy Box](./buy-box-competitor-pricing.md). O Buy Box é concedido pela Amazon ao vendedor que tem o produto listado normalmente pelo melhor preço, juntamente com outros fatores, como FBA/Prime Shipping oferecido, disponibilidade e desempenho do vendedor.

1. Para **Aplicar Imposto sobre o Valor Acrescentado (IVA)**, escolha uma opção:

   - `Disabled` - (Padrão) Escolha quando você não deseja aplicar IVA ao seu preço de listagem.

   - `Enabled` - Escolha quando deseja aplicar o IVA ao seu preço de listagem. O IVA é normalmente usado como imposto de vendas em países europeus e é adicionado ao seu preço listado final na Amazon. O IVA não se aplica ao preço final de listagens que são usadas em uma regra de preço inteligente, a menos que o [preço mínimo](./floor-price.md) seja atingido.
   >[!NOTE]
   >
   >As empresas da União Europeia (UE) são obrigadas a enviar faturas aos compradores de empresas, para que o cliente possa cobrar impostos. Você pode gerar essas NFFs e calcular os impostos por conta própria ou usar um serviço de cálculo de imposto, como o Serviço de Cálculo de IVA da Amazon. A Amazon recomenda se inscrever no [Serviço de Cálculo de IVA da Amazon](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;){target=&quot;_blank&quot;}. Se escolher um método diferente, você será responsável pela conformidade com o IVA.>
   >
   >Pode levar de 10 a 14 dias para a Amazon verificar e ativar sua conta do Serviço de Cálculo de IVA.

1. Para **[!UICONTROL VAT Percentage]**, insira o valor da sua taxa de IVA.

   O padrão é `0.00`. Este valor é utilizado para calcular o montante do IVA a adicionar ao preço de cotação. Se `10.2` for inserido, um IVA de 10,20% será aplicado ao seu preço de listagem. Este campo é desativado quando o campo Aplicar imposto sobre valor agregado (IVA) está definido como `Disabled`.

1. **(Somente lojas do Reino Unido)** Para  **[!UICONTROL Amazon Product Tax Code (PTC)]**, escolha uma opção:

   - `Do Not Manage PTC` - (Padrão) Escolha se você está usando um serviço de cálculo de imposto de terceiros ou já tem todos os cálculos de imposto configurados em sua  [!DNL Amazon Seller Central] conta. Quando escolhido, o canal de vendas do Amazon não envia informações de código de imposto do produto para sua conta [!DNL Amazon Seller Central].

   - `Set Default PTC` - Escolha se você tem um código de imposto do produto universal (PTC) que deseja usar para todos os seus produtos. Quando escolhido, você deve concluir _[!UICONTROL Default PTC]_.

      - Para **[!UICONTROL Default PTC]**, insira o PTC padrão a ser usado para todas as listagens elegíveis do Amazon. Se o PTC padrão estiver definido em sua conta [!DNL Amazon Seller Central], deixe este campo em branco. As alterações feitas nesse campo não afetam as listagens existentes do Amazon. Para alterar o PTC padrão para uma listagem existente, a listagem deve ser [encerrado](./end-listings-manually.md) e uma nova listagem deve ser criada.
   >[!NOTE]
   >
   >Se você usa o Serviço de Cálculo de IVA do Amazon, é necessário saber a categoria de imposto para seus produtos. Um PTC é o código de ID da categoria de imposto da Amazon para compras B2B na UE. Consulte [Códigos de Imposto do Produto Amazon](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;}.

1. Para **[!UICONTROL Currency Conversion]**, escolha uma opção.

   O padrão é `Disabled`. Essas opções dependem das configurações [!DNL Commerce] [currency](https://docs.magento.com/user-guide/configuration/general/currency-setup.html){target=&quot;_blank&quot;}. Se nenhuma opção estiver disponível, configure as configurações de moeda.

1. Quando terminar, clique em **[!UICONTROL Save listing settings]**.

![Preço de Listagem](assets/amazon-listing-price.png)

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Magento Price Source] | Determina a fonte de preço usada ao criar as listagens do Amazon. O padrão é `Price`. Se você escolher um atributo diferente, como `Amazon Price` ou `Special Price`, o valor definido para o atributo será usado para sua listagem do Amazon. No entanto, se o atributo selecionado não estiver definido, `Price` será usado. |
| [!UICONTROL Minimum Advertised Price (MAP)] | O atributo [!DNL Commerce] para preços MAP. Escolher a opção MAP define automaticamente sua listagem do Amazon para o preço MAPA se o preço da listagem for menor que o preço do MAPA. |
| [!UICONTROL Strike Through Price (MSRP)] | O atributo [!DNL Commerce] que representa o preço do MSRP. Se o seu preço de listagem do Amazon for menor que o MSRP, ele exibirá um aumento do preço do MSRP e o preço da listagem. Essa configuração também é usada para calcular o valor e a porcentagem &quot;Você Salva&quot;, mas esse recurso se aplica somente a listagens que ganharam a posição [Buy Box](./buy-box-competitor-pricing.md). |
| [!UICONTROL Apply Value Added Tax (VAT)] | O IVA é utilizado pelos vendedores na União Europeia.<br><br>Escolha  `Disabled` se você não deseja adicionar o IVA à listagem de preços.<br><br>Escolha  `Enabled` e então insira a Porcentagem de IVA para aplicar IVA aos seus preços de listagem. |
| [!UICONTROL VAT Percentage] | Defina a porcentagem a ser usada para calcular o valor do IVA a ser adicionado ao preço de listagem das suas listagens do Amazon. <br><br>Se você inserir  `5`, um IVA de 5% será aplicado ao preço final da listagem depois que todas as regras de preços forem aplicadas. O imposto sobre o IVA não se aplica ao preço final das listagens que são usadas dentro de uma regra de preços inteligente, a menos que o [floor](./floor-price.md) ou [teto](./optional-ceiling-price.md) seja atingido. |
| [!UICONTROL Amazon Product Tax Code (PTC)] | (Aparece somente para lojas do Reino Unido) Determina se o canal de vendas da Amazon envia informações de código de imposto do produto para sua conta [!DNL Amazon Seller Central]. <br><br>Selecione  **Não gerenciar** PTC se estiver usando um serviço de cálculo de imposto de terceiros ou já tiver todos os cálculos de imposto configurados em sua  [!DNL Amazon Seller Central] conta. Quando definido para essa opção, o canal de vendas do Amazon não envia informações de código de imposto do produto para sua conta [!DNL Amazon Seller Central].<br><br>Selecione  **Definir** PTC padrão se você tiver um código de imposto do produto universal que deseja usar para todos os seus produtos.<br><br>Consulte Códigos de Imposto do Produto  [Amazon](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;}. |
| [!UICONTROL Default PTC] | Somente é exibido quando **Código de Imposto do Produto (PTC) do Amazon** está definido como `Set Default PTC`. Insira o PTC padrão a ser usado para todas as listagens Amazon qualificadas. Se o PTC padrão estiver definido em sua conta [!DNL Amazon Seller Central], deixe este campo em branco. <br><br>As alterações feitas nesse campo não afetam as listagens existentes. A listagem deve ser [encerrado](./end-listings-manually.md) e uma nova listagem criada para que a alteração tenha efeito. |
| [!UICONTROL Currency Conversion] | Permite que a moeda padrão da loja [!DNL Commerce] seja convertida com precisão na moeda padrão do Amazon para publicar os preços da listagem na moeda correta. A conversão de moeda é sempre baseada na moeda padrão [!DNL Commerce].<br><br>Você ainda pode exibir suas moedas padrão  [!DNL Commerce] e do Amazon quando outras moedas estiverem disponíveis. Se a moeda padrão [!DNL Commerce] corresponder à moeda padrão do Amazon, deixe a Conversão de Moeda desativada.<br><br>Por exemplo, se a moeda  [!DNL Commerce] padrão for CAD (Dólar canadense) e a moeda padrão do Amazon for USD, você deverá ativar Conversão de moeda e escolher o CAD da Taxa de conversão em USD. As opções apresentadas são baseadas nas conversões de moeda [!DNL Commerce] incorporadas. Se você não vir a opção que está procurando, [configure a moeda em [!DNL Commerce]](https://docs.magento.com/user-guide/stores/currency-configuration.html){target=&quot;_blank&quot;}. |

**Acesso rápido**  -  [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
