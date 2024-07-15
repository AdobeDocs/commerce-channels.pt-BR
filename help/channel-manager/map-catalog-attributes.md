---
title: Mapear atributos do catálogo
description: '"Mapear atributos para correspondência [DNL! Commerce] para  [!DNL Walmart Marketplace] listagens existentes e sincronização de dados entre  [!DNL Channel Manager] e [!DNL Walmart].'''
feature: Sales Channels, Merchandising, Products
exl-id: 6678d81f-d167-460d-b656-d082d56f670c
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# Mapear atributos do catálogo

Antes de conectar as listagens de [!DNL Commerce] a [!DNL Walmart Marketplace], você deve mapear pelo menos um identificador exclusivo do catálogo [!DNL Commerce] para o identificador correspondente do Walmart.

Esta etapa é necessária para corresponder produtos do [!DNL Commerce] às listagens existentes do [!DNL Walmart] e para sincronizar dados de produtos entre [!DNL Commerce] e [!DNL Walmart]. O produto [!DNL Commerce] deve ter pelo menos um atributo de produto que corresponda a um dos seguintes Identificadores de Produto (IDs de Produto) exigidos por [!DNL Walmart].

**IDs de produto [!DNL Walmart] obrigatórias**

| **Tipo Aceito** | **Nome** | **Finalidade** | **Dígitos Aceitáveis** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | Item Comercial Global | Uso geral, usado no mundo todo | 14 dígitos |
| ISBN | Número do Livro Padrão Internacional | Paperback, capa dura e livros eletrônicos | 10 ou 13 dígitos |
| ISSN | Número de Série Padrão Internacional | Número de série de oito dígitos usado para identificar revistas, jornais e periódicos de todos os tipos entregues em todos os tipos de mídia impressa e eletrônica | 8 dígitos |
| UPC | Código universal do produto | Código de rastreamento padrão de varejo | 12 dígitos |

Se o catálogo não tiver um atributo correspondente, [adicione ou converta um atributo de catálogo existente](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

## Mapear identificadores exclusivos

1. Na página **[!UICONTROL Listings]** ou **[!UICONTROL Orders]** do armazenamento de canal de vendas, selecione **[!UICONTROL Channel Settings]**.

1. Em **[!UICONTROL Channel Settings]**, selecione **[!UICONTROL Map Attributes]**.

   - Localize o atributo [!DNL Walmart Marketplace] a ser mapeado.

   - Selecione o atributo correspondente do catálogo de armazenamento [!DNL Commerce].

     O exemplo a seguir mapeia o atributo [!UICONTROL Walmart Marketplace UPC] para o atributo UPC no catálogo de produtos.

     ![Mapear atributos para os critérios de correspondência de produtos](assets/products-map-attributes-for-match.png){width="600" zoomable="yes"}

   - Selecione **[!UICONTROL Save]**.
