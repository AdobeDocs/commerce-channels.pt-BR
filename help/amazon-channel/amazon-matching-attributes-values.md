---
title: Exibir mapeamento de atributos do Amazon
description: Verifique os valores dos atributos vinculados do Commerce para sincronizar corretamente entre o Commerce e o Amazon.
feature: Sales Channels, Products, Configuration
exl-id: 11a1fb25-6aa8-43d3-b5d8-772bbe1a5d53
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Exibir mapeamento de atributos do Amazon

À medida que você mapeia atributos do Amazon para [!DNL Commerce] atributos, o canal de vendas do Amazon rastreia e fornece uma lista filtrável de todos os valores do Amazon. Use esta página para verificar se os valores dos atributos [!DNL Commerce] vinculados são sincronizados corretamente entre o [!DNL Commerce] e a Amazon. Você pode revisar valores sincronizados para o atributo Amazon vinculado ou não vinculado a um atributo [!DNL Commerce]. Para criar ou editar os atributos do Amazon, consulte [Criação e edição de atributos](./creating-attributes.md).

O _Valor do Amazon_ difere dependendo do tipo de atributo e do atributo do Amazon que você visualiza. Por exemplo, um valor de Amazon listado para `Label` seria um valor de texto, enquanto `AmazonListPrice` seria um valor numérico. O status indica se o valor do Amazon foi importado.

## Visualizar seus valores de atributo

1. Na barra lateral _[!UICONTROL Admin]_, vá para **[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

1. Clique em **[!UICONTROL Attributes]** no menu do lado esquerdo, localize um atributo do Amazon e clique em **[!UICONTROL Create]** ou **[!UICONTROL Edit]** na coluna _[!UICONTROL Action]_.

1. Clique na guia **[!UICONTROL Matching Attribute Values]**.

   As listagens que têm um produto de catálogo [!DNL Commerce] correspondente mostram um valor vinculado na coluna _[!UICONTROL Magento Product SKU]_. Clicar em um link abre a página de detalhes do produto de catálogo correspondente. As alterações nos atributos do Amazon na página de detalhes do produto não são sincronizadas com o canal de vendas do Amazon.

>[!TIP]
>Para editar ou atribuir o mapeamento de uma listagem a um produto de catálogo, consulte [Atualizar Informações Necessárias](./amazon-manually-update-incomplete-listing.md).

![Exibir valores de atributo](assets/amazon-managing-attribute-values.png){width="600" zoomable="yes"}

| Campo | Descrição |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Region] | A região da atividade de vendas definida em **[!DNL Amazon Marketplace]País** durante a integração de loja. |
| [!UICONTROL Magento Product SKU] | Indica os [!DNL Commerce] produtos sincronizados com a loja da Amazon. O valor é uma ID de produto atribuída por [!DNL Commerce] e vinculada a um produto no catálogo. Para abrir o produto em [!DNL Commerce], clique no link. |
| [!UICONTROL ASIN] | Indica o identificador exclusivo alfanumérico de 10 caracteres do ASIN (Amazon Standard Identification Number) atribuído ao produto pela Amazon para identificação do produto. |
| [!UICONTROL Amazon Value] | Indica o valor do atributo selecionado. O Valor do Amazon difere dependendo do tipo de atributo e do atributo do Amazon que você visualiza. Por exemplo, um valor de Amazon listado para `Label` seria um valor de texto, enquanto `AmazonListPrice` seria um valor numérico. O status indica se o valor do Amazon foi importado. |
| [!UICONTROL Status] | Indica se os valores de atributo foram importados para [!DNL Commerce] e vinculados a um atributo [!DNL Commerce]. Opções: `Not Imported` / `Imported` |
