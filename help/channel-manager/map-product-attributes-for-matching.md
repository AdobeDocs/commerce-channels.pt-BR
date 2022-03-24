---
title: Configurar correspondência de produto
description: Mapear atributos para corresponder produtos do Commerce às listas existentes do Walmart
source-git-commit: 2a9bd2f8f91e672786c36f5e132f99bcab59dd00
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# Configurar correspondência de produto

Antes de publicar a listagem no Walmart Marketplace, mapeie pelo menos um identificador exclusivo dos atributos do catálogo de produtos para um dos identificadores de produtos Walmart necessários. Esta etapa é necessária para corresponder produtos no Walmart Marketplace.

Para a correspondência de produtos, o produto Commerce deve ter pelo menos um dos seguintes identificadores de produtos (IDs de produtos) nos atributos de catálogo.

**IDs de produto Walmart necessárias**

| **Tipo aceito** | **Nome** | **Finalidade** | **Dígitos aceitáveis** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | Item Comercial Global | Finalidade geral, usada no mundo inteiro | 14 dígitos |
| ISBN | Número do Livro Padrão Internacional | Paperback, capa dura e livros eletrônicos | 10 ou 13 dígitos |
| ISSN | Número de série padrão internacional | Número de série de 8 dígitos usado para identificar revistas, jornais, jornais e periódicos de todos os tipos emitidos em todos os meios de comunicação e eletrônicos | 8 dígitos |
| ISBN | Número do Livro Padrão Internacional | Paperback, Tampa e Eletrônica | 12 dígitos |

Se você tiver um tipo diferente de atributo de ID de produto em seu catálogo, converta-o em um dos tipos necessários. Em seguida, mapeie-o para o atributo do Walmart correspondente na configuração de Listagem para a loja do Gerenciador de Canais .

## Definir configurações de atributo do produto

1. Na página de listagem de produtos do canal de vendas conectado, selecione um ou mais produtos em *Rascunho* status.

1. Selecionar **[!UICONTROL Settings]**.

   - Encontre o atributo do Walmart Marketplace para mapear.

   - Selecione o atributo correspondente no catálogo de loja.

      O exemplo a seguir mapeia o atributo UPC do Walmart Marketplace para o atributo UPC no catálogo de produtos.
   ![Mapear atributos para critérios de correspondência do produto](assets/products-map-attributes-for--match.png)

   - Selecionar **[!UICONTROL Save]**.


## Atualizar configuração de atributo mapeado

Altere o identificador de produto do Commerce para produtos correspondentes atualizando as configurações de atributo mapeado.

Por exemplo, em vez de corresponder produtos com base no código de atributo de produto UPC do Commerce, você pode corresponder com base no SKU. Ou, mapeie atributos adicionais para melhorar a correspondência.

1. No **[!UICONTROL Listings]**, selecione **[!UICONTROL Settings]**.

1. No formulário de atributo Map , altere a configuração de atributo mapeado conforme necessário.
