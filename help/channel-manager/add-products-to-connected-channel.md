---
title: Adicionar produtos à loja de canais
description: Crie uma variedade de produtos para vendas do Marketplace adicionando produtos do catálogo ao canal de vendas
source-git-commit: 905bedaf1eacdc45b2b7f222e7703e1f7b3dfd9c
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---


# Adicionar produtos à loja de canais

No Gerenciador de canais, selecione os produtos da [!DNL Commerce] catálogo de vendas do Walmart Marketplace.

Para sincronizar produtos no canal de vendas, os produtos selecionados devem ter a seguinte configuração de atributo:

- **[!UICONTROL Publish to Channel Manager]** atributo está ativado

- Pelo menos um atributo de produto deve corresponder a um dos [atributos necessários do Walmart Marketplace](map-product-attributes-for-matching.md)-GTIN, ISBN, ISSN, UPC, EAN

Depois que você salvar as seleções, o Gerenciador de canais importa os dados do produto para o canal. Esse processo pode levar até 30 minutos.

## Adicionar produtos ao canal de vendas

1. Abra o catálogo de produtos associado à loja do Gerenciador de canais.

   Em um armazenamento de canal de vendas conectado, selecione **Adicionar produtos**.

   ![Adicionar produtos ao canal conectado](assets/add-initial-products-to-connected-channel.png)

   O catálogo é aberto em uma nova guia.

1. Na grade de produtos do catálogo, selecione produtos para vender no Walmart Marketplace.

   ![Enviar produtos para o canal conectado](assets/select-products-from-catalog.png)

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

1. Retorne ao canal de vendas conectado em [!DNL Channel Manager].

   Depois que a operação de importação for concluída, exiba os produtos de **[!UICONTROL Listings]**. Inicialmente, os produtos estão em *Rascunho* status. Selecionar [!UICONTROL Refresh products]** para atualizar a tabela.

   ![Produtos importados para o canal de vendas conectado](assets/products-in-marketplace-sales-channel.png)
