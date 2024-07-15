---
title: Gerenciar atributos para listagens do Amazon
description: É possível gerenciar o mapeamento de atributos de produto do Commerce para os atributos do Amazon para garantir informações precisas do produto entre os sistemas.
feature: Sales Channels, Products, Configuration
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Gerenciar atributos para listagens do Amazon

O Amazon e o [!DNL Commerce] usam um sistema de propriedades de produto, conhecidas como atributos, usados para definir um produto. Os atributos definem a descrição, o conteúdo, as imagens, os preços e vários dados para seus produtos.

A comunicação bem-sucedida entre o Commerce e o Amazon requer que os atributos [!DNL Commerce] sejam mapeados (ou correspondidos) corretamente ao atributo Amazon correspondente. Ao integrar com o Amazon, você mapeia esses atributos para atributos do Amazon. Quando concluído, o [!DNL Commerce] poderá sincronizar e manter suas listas do Amazon com seu catálogo de produtos do [!DNL Commerce].

Por exemplo, imagine que você tem o mesmo item no catálogo [!DNL Commerce] e nas listagens do Amazon. Um atributo do produto pode ser o preço de lista do item. O nome do preço de listagem em [!DNL Commerce] pode se chamar `Price`, enquanto o preço de listagem do Amazon pode se chamar `ListingPrice`. Você deve instruir [!DNL Commerce] que, ao se comunicar com o Amazon, o atributo [!DNL Commerce] chamado `Price` é o mesmo que o atributo Amazon chamado `ListingPrice`. Este processo é chamado de _gerenciamento de atributos_, e inclui a criação e edição de atributos novos e existentes. A verificação da correspondência adequada dos atributos garante a comunicação correta entre o [!DNL Commerce] e a Amazon.

Quando o mapeamento de atributos é configurado, o [!DNL Commerce] pode comunicar informações sobre o produto com a Amazon. Se você tiver listas de produtos da Amazon, o [!DNL Commerce] poderá importar seus produtos e detalhes da Amazon para o catálogo do [!DNL Commerce], permitindo que você gerencie suas listas do Amazon a partir de um único catálogo central de produtos.

O canal de vendas da Amazon permite acessar, revisar, criar e gerenciar atributos, conforme necessário, na [_[!UICONTROL Attributes]_exibição](./attributes-view.md) da home page do canal de vendas da Amazon. Se você adicionar um atributo ao catálogo [!DNL Commerce], poderá exigir uma atualização desses valores em todos os produtos.

Para obter mais informações sobre [!DNL Commerce] e conjuntos e valores de atributos do Amazon, consulte:

- [Gerenciar noções básicas de atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)
- [Criar um atributo](./creating-attributes.md#create-an-attribute)
- [Editar um atributo existente](./creating-attributes.md#edit-an-attribute)
- [Exibir mapeamento de atributos](./amazon-matching-attributes-values.md)
- [Editar ou Criar Mapeamento de Atributos](./amazon-manually-update-incomplete-listing.md)
