---
title: Exibir mapeamento de atributos do Amazon
description: Verifique os valores dos atributos vinculados do Commerce para sincronizar corretamente entre o Commerce e o Amazon.
exl-id: 11a1fb25-6aa8-43d3-b5d8-772bbe1a5d53
source-git-commit: 077d680da3c98ef9a48958eb548a9d5c1612f74e
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Exibir mapeamento de atributos do Amazon

Conforme você mapeia atributos do Amazon para [!DNL Commerce] atributos, o canal de vendas do Amazon rastreia e fornece uma lista filtrável de todos os valores do Amazon. Use esta página para verificar os valores dos seus [!DNL Commerce] os atributos são sincronizados corretamente entre [!DNL Commerce] e Amazon. É possível revisar valores sincronizados para o atributo do Amazon vinculado ou não vinculado a um [!DNL Commerce] atributo. Para criar ou editar os atributos do Amazon, consulte [Criar e editar atributos](./creating-attributes.md).

A variável _Valor do Amazon_ varia dependendo do tipo de atributo e do atributo Amazon que você visualiza. Por exemplo, um valor de Amazon listado para `Label` seria um valor de texto enquanto `AmazonListPrice` seria um valor numérico. O status indica se o valor do Amazon foi importado.

## Visualizar seus valores de atributo

1. No _[!UICONTROL Admin]_barra lateral, vá para **[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

1. Clique em **[!UICONTROL Attributes]** no menu à esquerda, localize um atributo do Amazon e clique em **[!UICONTROL Create]** ou **[!UICONTROL Edit]** no _[!UICONTROL Action]_coluna.

1. Clique em **[!UICONTROL Matching Attribute Values]** guia.

   Listagens que têm um correspondente [!DNL Commerce] produto de catálogo mostra um valor vinculado na variável _[!UICONTROL Magento Product SKU]_coluna. Clicar em um link abre a página de detalhes do produto de catálogo correspondente. As alterações nos atributos do Amazon na página de detalhes do produto não são sincronizadas com o canal de vendas do Amazon.

>[!TIP]
>Para editar ou atribuir o mapeamento de uma lista a um produto de catálogo, consulte [Atualização de informações necessárias](./amazon-manually-update-incomplete-listing.md).

![Exibir valores de atributo](assets/amazon-managing-attribute-values.png){width="600" zoomable="yes"}

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Region] | A região da atividade de vendas definida em **[!DNL Amazon Marketplace]País** durante a integração da loja. |
| [!UICONTROL Magento Product SKU] | Indica a [!DNL Commerce] produtos sincronizados com a loja da Amazon. O valor é uma ID de produto atribuída por [!DNL Commerce] e vinculado a um produto no catálogo. Para abrir o produto no [!DNL Commerce], clique no link. |
| [!UICONTROL ASIN] | Indica o identificador exclusivo alfanumérico de 10 caracteres do ASIN (Amazon Standard Identification Number) atribuído ao produto pela Amazon para identificação do produto. |
| [!UICONTROL Amazon Value] | Indica o valor do atributo selecionado. O Valor do Amazon difere dependendo do tipo de atributo e do atributo do Amazon que você visualiza. Por exemplo, um valor de Amazon listado para `Label` seria um valor de texto enquanto `AmazonListPrice` seria um valor numérico. O status indica se o valor do Amazon foi importado. |
| [!UICONTROL Status] | Indica se os valores de atributo foram importados para [!DNL Commerce] e vinculado a um [!DNL Commerce] atributo. Opções: `Not Imported` / `Imported` |
