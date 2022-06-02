---
title: Adicionar produtos à loja de canais de vendas
description: Criar uma classificação de produto para [!DNL Walmart Marketplace] vendas adicionando produtos do catálogo ao canal de vendas
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: 0acf063aeadd464824d1d0fce9eed1532d638c12
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---


# Adicionar produtos à loja de canais de vendas

Você pode adicionar produtos à [!DNL Walmart Marketplace] canal de vendas selecionando produtos do [!DNL Commerce] catálogo de produtos e sua importação para [!DNL Channel Manager].
O processo de importação pode levar até 30 minutos ou mais, dependendo de quantos produtos você selecionar.

## Pré-requisito

**[Mapear atributos do catálogo](map-catalog-attributes.md)**—Na [!DNL Channel Settings] , mapeie pelo menos um atributo do [!DNL Commerce] catálogo de produtos para um dos identificadores de produtos Walmart necessários —-GTIN, ISBN, ISSN, UPC, EAN.

## Requisitos de listagem

[!DNL Commerce] as listas de produtos devem ter a seguinte configuração de atributo necessária:

- **[!UICONTROL Publish to Channel Manager]** atributo está ativado

- Forneça valores válidos para os atributos Walmart necessários.

   - Pelo menos um atributo de produto que corresponda a um dos [!DNL Walmart Marketplace] identificadores de produtos-GTIN, ISBN, ISSN, UPC, EAN.

   - O preço do produto especificado com no máximo duas casas decimais, por exemplo `9.99`

   - Peso do produto especificado até um máximo de duas casas decimais, por exemplo `1.25`

>[!TIP]
>
>Para obter informações adicionais sobre otimização de listagens para seu canal de vendas, consulte o [Guia de otimização de qualidade da listagem do Walmart Marketplace](https://marketplace.walmart.com/wp-content/uploads/2020/09/WMP_listing_quality_optimization_guide.pdf).

## Adicionar produtos

1. Em um armazenamento de canal de vendas conectado, selecione **Adicionar produtos** para abrir o catálogo de produtos.

   ![Adicionar produtos à loja de canais de vendas](assets/add-initial-products-to-connected-channel.png)

   O catálogo é aberto em uma nova guia.

1. Na grade de produtos do catálogo, selecione produtos para vender [!DNL Walmart Marketplace].

   ![Enviar produtos para a loja de canais de vendas](assets/select-products-from-catalog.png)

1. Ative o **[!UICONTROL Publish to Channel Manager]** para os itens selecionados.

   - De **[!UICONTROL Actions]**, selecione **[!UICONTROL Update attributes]**.

   - Role para **[!UICONTROL Publish to Channel Manager]** e habilite-o.

   - Verifique se os atributos do produto incluem pelo menos um dos atributos necessários [!DNL Walmart Product IDs].

   - Selecionar **[!UICONTROL Save]**.

      Uma mensagem de confirmação é exibida.

      ![Importação de produto do catálogo para a mensagem de confirmação do canal de vendas](assets/product-import-from-catalog-confirmation.png)

      Se a mensagem indicar que a atualização está agendada, use a variável [fila:consumers:start](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-queue.html) [!DNL CLI] para processar a atualização imediatamente.

      ```bash
      $ bin/magento queue:consumers:start product_action_attribute.update
      ```

1. Após a conclusão da operação de importação, verifique os produtos adicionados, retornando para [!DNL Channel Manager] e seleção **[!UICONTROL Listings]**.

   ![Produtos importados para o canal de vendas conectado](assets/products-in-marketplace-sales-channel.png)

   Inicialmente, os produtos estão em *Rascunho* status. Selecionar **[!UICONTROL Refresh products]** para atualizar a tabela.

