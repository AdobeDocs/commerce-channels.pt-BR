---
title: Mapear atributos do catálogo
description: "Mapear atributos para correspondência [DNL! Commerce] para produtos existentes [!DNL Walmart Marketplace] listagens e sincronização de dados entre [!DNL Channel Manager] e [!DNL Walmart]."
feature: Sales Channels, Merchandising, Products
exl-id: 6678d81f-d167-460d-b656-d082d56f670c
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Mapear atributos do catálogo

Antes de conectar as listagens do [!DNL Commerce] para [!DNL Walmart Marketplace], você deve mapear pelo menos um identificador exclusivo do [!DNL Commerce] ao identificador correspondente do Walmart.

Esta etapa é necessária para corresponder a [!DNL Commerce] produtos para os existentes [!DNL Walmart] listagens e para sincronizar dados de produtos entre [!DNL Commerce] e [!DNL Walmart]. A variável [!DNL Commerce] O produto deve ter pelo menos um atributo de produto que corresponda a um dos seguintes Identificadores de Produto (IDs de Produto) exigidos pelo [!DNL Walmart].

**Obrigatório [!DNL Walmart] IDs de produto**

| **Tipo aceito** | **Nome** | **Finalidade** | **Dígitos aceitáveis** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | Item Comercial Global | Uso geral, usado no mundo todo | 14 dígitos |
| ISBN | Número do Livro Padrão Internacional | Paperback, capa dura e livros eletrônicos | 10 ou 13 dígitos |
| ISSN | Número de Série Padrão Internacional | Número de série de oito dígitos usado para identificar revistas, jornais e periódicos de todos os tipos entregues em todos os tipos de mídia impressa e eletrônica | 8 dígitos |
| UPC | Código universal do produto | Código de rastreamento padrão de varejo | 12 dígitos |

Se o catálogo não tiver um atributo correspondente, [adicionar ou converter um atributo de catálogo existente](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

## Mapear identificadores exclusivos

1. No **[!UICONTROL Listings]** ou **[!UICONTROL Orders]** para a loja de canal de vendas, selecione **[!UICONTROL Channel Settings]**.

1. Ligado **[!UICONTROL Channel Settings]**, selecione **[!UICONTROL Map Attributes]**.

   - Localize o [!DNL Walmart Marketplace] atributo a ser mapeado.

   - Selecione o atributo correspondente na [!DNL Commerce] catálogo da loja.

     O exemplo a seguir mapeia a variável [!UICONTROL Walmart Marketplace UPC] ao atributo UPC no catálogo de produtos.

     ![Mapear atributos para critérios de correspondência de produtos](assets/products-map-attributes-for-match.png){width="600" zoomable="yes"}

   - Selecionar **[!UICONTROL Save]**.
