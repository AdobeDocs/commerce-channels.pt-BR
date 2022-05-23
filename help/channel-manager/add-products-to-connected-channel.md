---
title: Adicionar produtos à loja de canais de vendas
description: Criar uma classificação de produto para [!DNL Walmart Marketplace] vendas adicionando produtos do catálogo ao canal de vendas
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: 76aa7451c9df83fbb7ea808fc14ef2d306235da2
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Adicionar produtos à loja de canais de vendas

Para sincronizar produtos com o canal de vendas do Walmart, você seleciona produtos do [!DNL Commerce] catálogo de produtos e importe-os para o Gerenciador de canais. Os produtos selecionados devem ter a seguinte configuração de atributo:

- **[!UICONTROL Publish to Channel Manager]** atributo está ativado

- Pelo menos um atributo de produto deve corresponder a um dos [atributos necessários do Walmart Marketplace](map-product-attributes-for-matching.md)-GTIN, ISBN, ISSN, UPC, EAN

O processo para importar produtos de [!DNL Commerce] para o Channel Manager pode levar até 30 minutos ou mais, dependendo de quantos produtos você selecionar.

## Adicionar produtos

1. Em um armazenamento de canal de vendas conectado, selecione **Adicionar produtos** para abrir o catálogo de produtos.

   ![Adicionar produtos à loja de canais de vendas](assets/add-initial-products-to-connected-channel.png)

   O catálogo é aberto em uma nova guia.

1. Na grade de produtos do catálogo, selecione produtos para vender [!DNL Walmart Marketplace].

   ![Enviar produtos para a loja de canais de vendas](assets/select-products-from-catalog.png)

1. Ative o **[!UICONTROL Publish to Channel Manager]** para os itens selecionados.

   - De **[!UICONTROL Actions]**, selecione **[!UICONTROL Update attributes]**.

   - Role para **[!UICONTROL Publish to Channel Manager]** e habilite-o.

   - Verifique se os atributos de produto incluem pelo menos uma das IDs de produto Walmart necessárias.

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

