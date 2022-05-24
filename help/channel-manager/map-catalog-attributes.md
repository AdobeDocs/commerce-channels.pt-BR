---
title: Mapear atributos do catálogo
description: Mapear atributos para correspondência [DNL! Comércio] produtos para produtos existentes [!DNL Walmart Marketplace] listagens e sincronização de dados entre [!DNL Channel Manager] e [!DNL Walmart].
exl-id: 6678d81f-d167-460d-b656-d082d56f670c
source-git-commit: fac4bbd3985e07b919f986c877b8584da797e6fe
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 0%

---

# Mapear atributos do catálogo

Antes de publicar listagens de [!DNL Commerce] para [!DNL Walmart Marketplace], você deve mapear pelo menos um identificador exclusivo de [!DNL Commerce] catálogo para o identificador correspondente do Walmart.
Esta etapa é necessária para corresponder a [!DNL Commerce] aos produtos existentes [!DNL Walmart] e para sincronizar os dados do produto entre [!DNL Commerce] e [!DNL Walmart].

Para a correspondência de produtos, o produto Commerce deve ter pelo menos um atributo de produto que corresponda a um dos seguintes Identificadores de produto (IDs de produto), exigidos pelo [!DNL Walmart].

**IDs de produto Walmart necessárias**

| **Tipo aceito** | **Nome** | **Finalidade** | **Dígitos aceitáveis** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | Item Comercial Global | Finalidade geral, usada no mundo inteiro | 14 dígitos |
| ISBN | Número do Livro Padrão Internacional | Paperback, capa dura e livros eletrônicos | 10 ou 13 dígitos |
| ISSN | Número de série padrão internacional | Número de série de 8 dígitos usado para identificar revistas, jornais, jornais e periódicos de todos os tipos emitidos em todos os meios de comunicação e eletrônicos | 8 dígitos |
| UPC | Código universal do produto | Código de rastreamento de varejo padrão | 12 dígitos |

Se o catálogo não tiver um atributo correspondente, [adicionar ou converter um atributo de catálogo existente](https://docs.magento.com/user-guide/catalog/product-attributes.html).

## Mapear identificadores exclusivos

1. No [!UICONTROL Listings] para o armazenamento do canal de vendas, selecione **[!UICONTROL Settings]**.

   - Encontre o atributo do Walmart Marketplace para mapear.

   - Selecione o atributo correspondente no [!DNL Commerce] catálogo de loja.

      O exemplo a seguir mapeia o atributo UPC do Walmart Marketplace para o atributo UPC no catálogo de produtos.
   ![Mapear atributos para critérios de correspondência do produto](assets/products-map-attributes-for-match.png)
   - Como opção, você pode mapear vários atributos para aumentar as correspondências. Se mapear mais de um atributo, selecione um como **Identificador principal**. Essa

   - Selecionar **[!UICONTROL Save]**.


## Atualizar configuração de atributo mapeado

Altere o identificador de produto do Commerce para produtos correspondentes atualizando as configurações de atributo mapeado.

Por exemplo, em vez de corresponder produtos com base no código de atributo de produto UPC do Commerce, você pode corresponder com base no SKU. Ou, mapeie atributos adicionais para melhorar a correspondência.

1. No **[!UICONTROL Listings]**, selecione **[!UICONTROL Settings]**.

1. No formulário de atributo Map , altere a configuração de atributo mapeado conforme necessário.
