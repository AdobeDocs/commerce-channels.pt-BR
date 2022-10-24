---
title: Mapear atributos do catálogo
description: '''Mapear atributos para correspondência [DNL! Comércio] produtos para produtos existentes [!DNL Walmart Marketplace] listagens e sincronização de dados entre [!DNL Channel Manager] e [!DNL Walmart]."'
exl-id: 6678d81f-d167-460d-b656-d082d56f670c
source-git-commit: 3f6039ad78ff500c31129bee12d65e291e226567
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# Mapear atributos do catálogo

Antes de conectar listagens de [!DNL Commerce] para [!DNL Walmart Marketplace], você deve mapear pelo menos um identificador exclusivo de [!DNL Commerce] catálogo para o identificador correspondente do Walmart.

Esta etapa é necessária para corresponder a [!DNL Commerce] aos produtos existentes [!DNL Walmart] e para sincronizar os dados do produto entre [!DNL Commerce] e [!DNL Walmart]. O [!DNL Commerce] O produto deve ter pelo menos um atributo de produto que corresponda a um dos seguintes identificadores de produto (IDs de produto) exigidos pelo [!DNL Walmart].

**Obrigatório [!DNL Walmart] IDs de produto**

| **Tipo aceito** | **Nome** | **Finalidade** | **Dígitos aceitáveis** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | Item Comercial Global | Finalidade geral, usada no mundo inteiro | 14 dígitos |
| ISBN | Número do Livro Padrão Internacional | Paperback, capa dura e livros eletrônicos | 10 ou 13 dígitos |
| ISSN | Número de série padrão internacional | Número de série de 8 dígitos usado para identificar revistas, jornais, jornais e periódicos de todos os tipos emitidos em todos os meios de comunicação e eletrônicos | 8 dígitos |
| UPC | Código universal do produto | Código de rastreamento de varejo padrão | 12 dígitos |

Se o catálogo não tiver um atributo correspondente, [adicionar ou converter um atributo de catálogo existente](https://docs.magento.com/user-guide/catalog/product-attributes.html).

## Mapear identificadores exclusivos

1. No **[!UICONTROL Listings]** ou **[!UICONTROL Orders]** para o armazenamento do canal de vendas, selecione **[!UICONTROL Channel Settings]**.

1. Ligado **[!UICONTROL Channel Settings]**, selecione **[!UICONTROL Map Attributes]**.

   - Encontre a [!DNL Walmart Marketplace] atributo a ser mapeado.

   - Selecione o atributo correspondente no [!DNL Commerce] catálogo de loja.

      O exemplo a seguir mapeia a variável [!UICONTROL Walmart Marketplace UPC] para o atributo UPC no catálogo de produtos.

      ![Mapear atributos para critérios de correspondência do produto](assets/products-map-attributes-for-match.png)

   - Selecionar **[!UICONTROL Save]**.


