---
title: Adicionar produtos ao Gerenciador de canal
description: 'Crie um sortimento de produtos para  [!DNL Walmart Marketplace] vendas adicionando produtos do catálogo ao canal de vendas configurado no Gerenciador de Canais.'
feature: Sales Channels, Merchandising, Products
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: 0087d60791cf00e4ed2bffe992447ee8e592fd9b
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# Adicionar produtos a [!DNL Channel Manager]

Para adicionar produtos ao canal de vendas [!DNL Walmart Marketplace], selecione-os no catálogo de produtos [!DNL Commerce] e importe-os para [!DNL Channel Manager].
O processo de importação pode levar até 30 minutos ou mais, dependendo de quantos produtos você selecionar.

## Pré-requisito

**[Mapear atributos do catálogo](map-catalog-attributes.md)**—Na configuração [!DNL Channel Settings], mapeie pelo menos um atributo do catálogo de produtos [!DNL Commerce] para um dos Identificadores de Produto Walmart necessários—-GTIN, ISBN, ISSN, UPC, EAN.

## Requisitos de lista

As listagens de produtos do [!DNL Commerce] devem ter a seguinte configuração de atributo necessária:

- O atributo **[!UICONTROL Connect to Channel Manager]** está habilitado

- Forneça valores válidos para os atributos necessários do Walmart.

   - Pelo menos um atributo de produto que corresponda a um dos [!DNL Walmart Marketplace] identificadores de produto necessários: GTIN, ISBN, ISSN, UPC, EAN.

   - O preço do produto foi especificado com no máximo duas casas decimais, por exemplo `9.99`

   - Peso do produto especificado com no máximo duas casas decimais, por exemplo `1.25`

>[!TIP]
>
>Para obter informações adicionais sobre a otimização de listagens para seu canal de vendas, consulte o [Guia de Otimização de Qualidade de Listagem do Walmart Marketplace](https://marketplace.walmart.com/wp-content/uploads/2020/09/WMP_listing_quality_optimization_guide.pdf).

## Adicionar produtos

1. Em uma loja de canais de vendas conectada, selecione **Adicionar produtos** para abrir o catálogo de produtos.

   ![Adicionar produtos à loja de canal de vendas](assets/add-initial-products-to-connected-channel.png){width="600" zoomable="yes"}

   O catálogo abre em uma nova guia.

1. Na grade de produtos do catálogo, selecione produtos para vender em [!DNL Walmart Marketplace].

   ![Enviar produtos para a loja de canal de vendas](assets/select-products-from-catalog.png){width="600" zoomable="yes"}

1. Habilite o atributo **[!UICONTROL Connect to Channel Manager]** para os itens selecionados.

   - Em **[!UICONTROL Actions]**, selecione **[!UICONTROL Update attributes]**.

   - Role até o atributo **[!UICONTROL Connect to Channel Manager]** e habilite-o.

   - Verifique se os atributos do produto incluem pelo menos um dos [!DNL Walmart Product IDs] necessários.

   - Selecione **[!UICONTROL Save]**.

     Uma mensagem de confirmação é exibida.

     ![Mensagem de confirmação da importação do produto do catálogo para o canal de vendas](assets/product-import-from-catalog-confirmation.png){width="400"}

     Se a mensagem indicar que a atualização está agendada, use o comando [`queue:consumers:start`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) [!DNL CLI] para processar a atualização imediatamente.

     ```bash
     $ bin/magento queue:consumers:start product_action_attribute.update
     ```

1. Após concluir a operação de importação, verifique os produtos adicionados retornando para [!DNL Channel Manager] e selecionando **[!UICONTROL Listings]**.

   Inicialmente, os produtos estão com o status *Rascunho*. Selecione **[!UICONTROL Refresh products]** para atualizar a tabela.

1. Atualize a exibição para mostrar os novos produtos adicionados ao Gerenciador de Canais selecionando o cartão de status **[!UICONTROL Draft]**.

   ![Produtos importados para o canal de vendas conectado](assets/products-in-marketplace-sales-channel.png){width="400" zoomable="yes"}


