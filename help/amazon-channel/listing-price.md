---
title: Preço de Listagem
description: Use as configurações de Preço de Listagem para determinar a fonte de preço e o valor de preço base (padrão) para suas listagens do Amazon.
redirect_from: sales-channels/asc/ob-listing-price.html
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '1509'
ht-degree: 0%

---

# Preço de Listagem

[!UICONTROL Listing Price] As configurações fazem parte das configurações da listagem de loja. As configurações de listagem são acessadas do [painel de loja](./amazon-store-dashboard.md).

Essas configurações definem qual [!DNL Commerce] atributo de preço a ser usado como fonte de preço, que é o valor de preço base (padrão) das listagens do Amazon. Essas configurações são usadas pelo [regras de preços](./pricing-rule-general-settings.md) para ajustar automaticamente o preço da listagem do Amazon em relação ao valor definido para _[!UICONTROL Magento Price Source]_.

Você pode configurar [escopo de preços](./price-scope.md) como global ou site. Se o escopo de preços estiver definido como `Global`, há uma única fonte de preço para todas as suas lojas/sites. Se o escopo de preços estiver definido como `Website`, a fonte de preço usa a lógica de fallback do preço do site (se disponível) seguida pelo preço padrão (global).

Se uma regra de listagem for definida para ser aplicada a mais de um site, a ordem em que o preço do site é usado é determinada pela configuração de prioridade do site definida na variável [regra de listagem](./listing-rules.md). Essas regras permitem definir preços de produtos no catálogo. Para ver se você está usando o escopo de preço do site, consulte [Escopo do Preço do Catálogo](https://docs.magento.com/user-guide/catalog/catalog-price-scope.html){target=&quot;_blank&quot;}.

As opções listadas em _[!UICONTROL Magento Price Source]_,_[!UICONTROL Minimum Advertised Price (Map)]_ e _[!UICONTROL Strike Through Price (MSRP)]_inclua os atributos de preços configurados. Os atributos de preço são [!DNL Commerce] atributos de produto com o Tipo de entrada de catálogo do Proprietário da loja definido como `Price`. Consulte [Tipos de entrada de atributo](https://docs.magento.com/user-guide/stores/attributes-input-types.html){target=&quot;_blank&quot;}.

## Definir configurações de Preço de Listagem {#configure-listing-price-settings}

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda o _[!UICONTROL Listing Price]_seção.

1. Para **[!UICONTROL Magento Price Source]** (obrigatório), escolha uma opção.

   O padrão é `Price`. Essa configuração determina a fonte de preço usada para suas listagens do Amazon. Se você criar [regras de preços](./pricing-products.md), as regras são aplicadas ao valor definido para o atributo selecionado aqui. Você pode selecionar qualquer atributo de preço configurado. No entanto, se o atributo selecionado não for preenchido em um produto, a fonte de preço do produto volta ao padrão `Price` quando as regras de preços são aplicadas para determinar o preço publicado da listagem do Amazon.

1. Para **[!UICONTROL Minimum Advertised Price (MAP)**], escolha uma opção.

   O padrão é nenhuma seleção. Esta configuração permite um preço mínimo anunciado (MAP) para um produto. Ao definir um atributo de preço e o preço listado de um produto cair abaixo do preço mínimo determinado (com base na fonte de preço e nas regras), esse valor se torna o MAPA para a listagem. Essa configuração permite implementar [regras de preços](./pricing-products.md), enquanto ainda controla o preço mínimo de um produto. Para evitar que o preço da listagem seja muito baixo, escolha um atributo de preço a ser usado como MAPA. No entanto, se o campo de preço selecionado não estiver definido para um produto, o MAP não será usado.

1. Para **[!UICONTROL Strike Through Price (MSRP)]**, escolha uma opção.

   O padrão é nenhuma seleção. Essa configuração determina qual atributo de preço é usado como o preço de varejo sugerido pelo fabricante (MSRP) para um produto. Se o seu preço de listagem for menor que o MSRP definido, sua listagem do Amazon será exibida com um aumento do preço do MSRP com o menor preço de listagem, juntamente com o valor e a porcentagem de &quot;Você economiza&quot; calculados. No entanto, se o campo de preço selecionado não estiver definido para um produto, o MSRP não será calculado.

   >[!NOTE]
   >
   >Essa configuração se aplica somente às listagens que ganharam o [Buy Box](./buy-box-competitor-pricing.md) posição. O Buy Box é concedido pela Amazon ao vendedor que tem o produto listado normalmente pelo melhor preço, juntamente com outros fatores, como FBA/Prime Shipping oferecido, disponibilidade e desempenho do vendedor.

1. Para **Aplicar Imposto sobre Valor Acrescentado (IVA)**, escolha uma opção:

   - `Disabled` - (Padrão) Escolha quando você não deseja aplicar IVA ao seu preço de listagem.

   - `Enabled` - Escolha quando deseja aplicar o IVA ao seu preço de listagem. O IVA é normalmente usado como imposto de vendas em países europeus e é adicionado ao seu preço listado final na Amazon. O IVA não se aplica ao preço final das listas utilizadas no âmbito de uma regra de preços inteligente, a menos que a variável [preço mínimo](./floor-price.md) é atingida.
   >[!NOTE]
   >
   >As empresas da União Europeia (UE) são obrigadas a enviar faturas aos compradores de empresas, para que o cliente possa cobrar impostos. Você pode gerar essas NFFs e calcular os impostos por conta própria ou usar um serviço de cálculo de imposto, como o Serviço de Cálculo de IVA da Amazon. A Amazon recomenda se inscrever na [Serviço de Cálculo de IVA Amazon](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;){target=&quot;_blank&quot;}. Se escolher um método diferente, você será responsável pela conformidade com o IVA.>
   >
   >Pode levar de 10 a 14 dias para a Amazon verificar e ativar sua conta do Serviço de Cálculo de IVA.

1. Para **[!UICONTROL VAT Percentage]**, insira o valor da sua taxa de IVA.

   O padrão é `0.00`. Este valor é utilizado para calcular o montante do IVA a adicionar ao preço de cotação. If `10.2` for inserido, um IVA de 10,20% será aplicado ao seu preço de listagem. Este campo é desativado quando o campo Aplicar Imposto sobre o Valor Acrescentado (IVA) está definido como `Disabled`.

1. **(Somente lojas do Reino Unido)** Para **[!UICONTROL Amazon Product Tax Code (PTC)]**, escolha uma opção:

   - `Do Not Manage PTC` - (Padrão) Escolha se você está usando um serviço de cálculo de imposto de terceiros ou já tem todos os seus cálculos de imposto configurados em [!DNL Amazon Seller Central] conta. Quando escolhido, o canal de vendas da Amazon não envia informações sobre o código de imposto do produto para a [!DNL Amazon Seller Central] conta.

   - `Set Default PTC` - Escolha se você tem um código de imposto do produto universal (PTC) que deseja usar para todos os seus produtos. Quando escolhido, é necessário concluir _[!UICONTROL Default PTC]_.

      - Para **[!UICONTROL Default PTC]**, insira o PTC padrão a ser usado para todas as listas elegíveis do Amazon. Se o seu PTC padrão estiver definido em [!DNL Amazon Seller Central] deixe este campo em branco. As alterações feitas nesse campo não afetam as listagens existentes do Amazon. Para alterar o PTC padrão de uma listagem existente, a listagem deve ser [encerrado](./end-listings-manually.md) e uma nova listagem foi criada.
   >[!NOTE]
   >
   >Se você usa o Serviço de Cálculo de IVA do Amazon, é necessário saber a categoria de imposto para seus produtos. Um PTC é o código de ID da categoria de imposto da Amazon para compras B2B na UE. Consulte [Códigos de imposto do produto Amazon](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;}.

1. Para **[!UICONTROL Currency Conversion]**, escolha uma opção.

   O padrão é `Disabled`. Essas opções dependem do [!DNL Commerce] [currency](https://docs.magento.com/user-guide/configuration/general/currency-setup.html)Configurações {target=&quot;_blank&quot;}. Se nenhuma opção estiver disponível, configure as configurações de moeda.

1. Ao concluir, clique em **[!UICONTROL Save listing settings]**.

![Preço de Listagem](assets/amazon-listing-price.png)

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Magento Price Source] | Determina a fonte de preço usada ao criar as listagens do Amazon. O padrão é `Price`. Se você escolher um atributo diferente, como `Amazon Price` ou `Special Price`, o valor definido para o atributo é usado para sua listagem do Amazon. No entanto, se o atributo selecionado não estiver definido, `Price` é usada. |
| [!UICONTROL Minimum Advertised Price (MAP)] | O [!DNL Commerce] para preços MAP. Escolher a opção MAP define automaticamente sua listagem do Amazon para o preço MAPA se o preço da listagem for menor que o preço do MAPA. |
| [!UICONTROL Strike Through Price (MSRP)] | O [!DNL Commerce] que representa o preço do MSRP. Se o seu preço de listagem do Amazon for menor que o MSRP, ele exibirá um aumento do preço do MSRP e o preço da listagem. Essa configuração também é usada para calcular a quantidade e a porcentagem de &quot;Você Salva&quot;, mas esse recurso se aplica somente às listagens que venceram a variável [Buy Box](./buy-box-competitor-pricing.md) posição. |
| [!UICONTROL Apply Value Added Tax (VAT)] | O IVA é utilizado pelos vendedores na União Europeia.<br><br>Choose `Disabled` se você não quiser que o IVA seja adicionado aos preços de listagem.<br><br>Choose `Enabled` e, em seguida, informe a Porcentagem de IVA para aplicar IVA aos seus preços de listagem. |
| [!UICONTROL VAT Percentage] | Defina a porcentagem a ser usada para calcular o valor do IVA a ser adicionado ao preço de listagem das suas listagens do Amazon. <br><br>Se você inserir `5`, o IVA de 5% será aplicado ao preço final de cotação após a aplicação de todas as regras de fixação de preços. O imposto sobre o IVA não se aplica ao preço final das listas utilizadas no âmbito de uma regra de preços inteligente, a menos que a variável [chão](./floor-price.md) ou [limite](./optional-ceiling-price.md) é atingida. |
| [!UICONTROL Amazon Product Tax Code (PTC)] | (Aparece somente para lojas do Reino Unido) Determina se o canal de vendas da Amazon envia informações de código de imposto do produto para sua [!DNL Amazon Seller Central] conta. <br><br>Selecionar **Não Gerenciar PTC** se você estiver usando um serviço de cálculo de imposto de terceiros ou já tiver todos os cálculos de imposto configurados em [!DNL Amazon Seller Central] conta. Quando definido para essa opção, o canal de vendas do Amazon não envia informações de código de imposto do produto para sua [!DNL Amazon Seller Central] conta.<br><br>Selecionar **Definir PTC padrão** se você tem um código de imposto universal do produto, deseja usar para todos os seus produtos.<br><br>Consulte [Códigos de imposto do produto Amazon](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;}. |
| [!UICONTROL Default PTC] | Somente aparece quando **Código de imposto do produto Amazon (PTC)** está definida como `Set Default PTC`. Insira o PTC padrão a ser usado para todas as listagens Amazon qualificadas. Se o seu PTC padrão estiver definido em [!DNL Amazon Seller Central] deixe este campo em branco. <br><br>As alterações feitas nesse campo não afetam as listagens existentes. A listagem deve ser [encerrado](./end-listings-manually.md) e uma nova listagem criada para a alteração entrar em vigor. |
| [!UICONTROL Currency Conversion] | Permite que [!DNL Commerce] moeda padrão da loja para converter com precisão para sua moeda padrão do Amazon para publicar seus preços de listagem na moeda correta. A conversão de moeda é sempre baseada em seu [!DNL Commerce] moeda padrão.<br><br>Você ainda pode exibir seu padrão [!DNL Commerce] e moedas Amazon quando outras moedas estiverem disponíveis. Se o seu padrão [!DNL Commerce] A moeda corresponde à moeda padrão do Amazon, deixe a Conversão de moeda desativada.<br><br>Por exemplo, se a variável [!DNL Commerce] a moeda padrão é CAD (Dólar canadense) e a moeda padrão do Amazon é USD, você deve ativar Conversão de moeda e escolher o CAD da Taxa de conversão como USD. As opções apresentadas são baseadas no [!DNL Commerce] conversões de moeda. Se você não vir a opção que está procurando, [configure a moeda em [!DNL Commerce]](https://docs.magento.com/user-guide/stores/currency-configuration.html){target=&quot;_blank&quot;}. |

**Acesso rápido** - [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
