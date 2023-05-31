---
title: Gerenciar atributos para listagens do Amazon
description: É possível gerenciar o mapeamento de atributos de produto do Commerce para os atributos do Amazon para garantir informações precisas do produto entre os sistemas.
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Gerenciar atributos para listagens do Amazon

AMAZON e [!DNL Commerce] ambos usam um sistema de propriedades de produto, conhecidas como atributos, usados para definir um produto. Os atributos definem a descrição, o conteúdo, as imagens, os preços e vários dados para seus produtos.

A comunicação bem-sucedida entre o Commerce e o Amazon exige que [!DNL Commerce] Os atributos devem ser mapeados corretamente (ou correspondidos) ao atributo correspondente do Amazon. Ao integrar com o Amazon, você mapeia esses atributos para atributos do Amazon. Quando concluído, [!DNL Commerce] O pode sincronizar e manter suas listagens do Amazon com as [!DNL Commerce] catálogo de produtos.

Por exemplo, imagine que você tem o mesmo item em seu [!DNL Commerce] catálogo e Amazon. Um atributo do produto pode ser o preço de lista do item. O nome do preço de listagem em [!DNL Commerce] pode ser nomeado `Price`, embora o preço de lista do Amazon possa ser nomeado `ListingPrice`. Você deve instruir [!DNL Commerce] que, ao se comunicar com o Amazon, a variável [!DNL Commerce] atributo nomeado `Price` é o mesmo que o atributo do Amazon chamado `ListingPrice`. Esse processo é chamado de _gerenciamento de atributos_, e inclui a criação de atributos novos e a edição de atributos existentes. Garantir que os atributos sejam correspondidos corretamente garante a comunicação correta entre [!DNL Commerce] e Amazon.

Quando o mapeamento de atributos é configurado, [!DNL Commerce] O pode comunicar informações sobre produtos com a Amazon. Se você tiver listagens de produtos Amazon, [!DNL Commerce] pode importar seus produtos e detalhes do Amazon para o [!DNL Commerce] catálogo, permitindo gerenciar suas listagens do Amazon a partir de um único catálogo central de produtos.

O canal de vendas da Amazon permite acessar, revisar, criar e gerenciar atributos, conforme necessário, na [_[!UICONTROL Attributes]_exibir](./attributes-view.md) na página inicial do canal de vendas do Amazon. Se você adicionar um atributo ao seu [!DNL Commerce] catálogo, pode exigir uma atualização desses valores em todos os produtos.

Para obter mais informações sobre [!DNL Commerce] e Amazon conjuntos de atributos e valores, consulte:

- [Gerenciar noções básicas de atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)
- [Criar um atributo](./creating-attributes.md#create-an-attribute)
- [Editar um atributo existente](./creating-attributes.md#edit-an-attribute)
- [Exibir mapeamento de atributos](./amazon-matching-attributes-values.md)
- [Editar ou Criar Mapeamento de Atributos](./amazon-manually-update-incomplete-listing.md)
