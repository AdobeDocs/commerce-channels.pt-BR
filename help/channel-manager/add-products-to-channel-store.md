---
title: Adicionar produtos ao Gerenciador de canal
description: '"Criar sortimento de produtos para [!DNL Walmart Marketplace] vendas adicionando produtos do catálogo ao canal de vendas configurado no Gerenciador de Canais.'' '
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---


# Adicionar produtos a [!DNL Channel Manager]

Para adicionar produtos à [!DNL Walmart Marketplace] canal de vendas, selecione-os na lista suspensa [!DNL Commerce] catálogo de produtos e importá-los para [!DNL Channel Manager].
O processo de importação pode levar até 30 minutos ou mais, dependendo de quantos produtos você selecionar.

## Pré-requisito

**[Mapear atributos do catálogo](map-catalog-attributes.md)**—No campo [!DNL Channel Settings] configuração, mapeie pelo menos um atributo da variável [!DNL Commerce] catálogo de produtos a um dos identificadores de produtos Walmart necessários—-GTIN, ISBN, ISSN, UPC, EAN.

## Requisitos de lista

[!DNL Commerce] as listagens de produtos devem ter a seguinte configuração de atributo necessária:

- **[!UICONTROL Connect to Channel Manager]** atributo está ativado

- Forneça valores válidos para os atributos necessários do Walmart.

   - Pelo menos um atributo de produto que corresponda a um dos [!DNL Walmart Marketplace] identificadores de produtos: GTIN, ISBN, ISSN, UPC, EAN.

   - O preço do produto é especificado com no máximo duas casas decimais, por exemplo `9.99`

   - Peso do produto especificado com no máximo duas casas decimais, por exemplo `1.25`

>[!TIP]
>
>Para obter informações adicionais sobre como otimizar listagens para seu canal de vendas, consulte [Guia de otimização de qualidade de listagem do Walmart Marketplace](https://marketplace.walmart.com/wp-content/uploads/2020/09/WMP_listing_quality_optimization_guide.pdf).

## Adicionar produtos

1. Em uma loja de canal de vendas conectada, selecione **Adicionar produtos** para abrir o catálogo de produtos.

   ![Adicionar produtos à loja de canal de vendas](assets/add-initial-products-to-connected-channel.png){width="600" zoomable="yes"}

   O catálogo abre em uma nova guia.

1. Na grade de produtos do catálogo, selecione os produtos que serão vendidos [!DNL Walmart Marketplace].

   ![Enviar produtos para a loja de canal de vendas](assets/select-products-from-catalog.png){width="600" zoomable="yes"}

1. Ativar o **[!UICONTROL Connect to Channel Manager]** para os itens selecionados.

   - De **[!UICONTROL Actions]**, selecione **[!UICONTROL Update attributes]**.

   - Role para a **[!UICONTROL Connect to Channel Manager]** e ative-o.

   - Verifique se os atributos do produto incluem pelo menos um dos [!DNL Walmart Product IDs].

   - Selecionar **[!UICONTROL Save]**.

      Uma mensagem de confirmação é exibida.

      ![Mensagem de confirmação da importação do produto do catálogo para o canal de vendas](assets/product-import-from-catalog-confirmation.png){width="400"}

      Se a mensagem indicar que a atualização está programada, use o [fila:consumers:start](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) [!DNL CLI] para processar a atualização imediatamente.

      ```bash
      $ bin/magento queue:consumers:start product_action_attribute.update
      ```

1. Após a conclusão da operação de importação, verifique os produtos adicionados, retornando para [!DNL Channel Manager] e seleção **[!UICONTROL Listings]**.

   Inicialmente, os produtos estão *Rascunho* status. Selecionar **[!UICONTROL Refresh products]** para atualizar a tabela.

1. Atualize a exibição para mostrar os novos produtos adicionados ao Gerenciador de canal selecionando o **[!UICONTROL Draft]** Cartão de status.

   ![Produtos importados para o canal de vendas conectado](assets/products-in-marketplace-sales-channel.png){width="400" zoomable="yes"}


