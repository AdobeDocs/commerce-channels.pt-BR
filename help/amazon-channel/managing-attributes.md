---
title: Gerenciar atributos
description: Você pode gerenciar o mapeamento dos atributos de produto do Commerce para os atributos do Amazon para garantir informações precisas do produto entre os sistemas.
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Gerenciar atributos

O Amazon e [!DNL Commerce] usam um sistema de propriedades do produto, conhecido como atributos, usados para definir um produto. Os atributos definem a descrição, o conteúdo, as imagens, os preços e vários dados para os seus produtos.

A comunicação bem-sucedida entre o Commerce e o Amazon requer que os atributos [!DNL Commerce] sejam mapeados corretamente (ou correspondam) ao atributo Amazon correspondente. Ao integrar com o Amazon, você mapeia esses atributos para atributos do Amazon. Quando concluído, [!DNL Commerce] poderá sincronizar e manter suas listagens do Amazon com seu catálogo de produtos [!DNL Commerce].

Por exemplo, imagine que você tem o mesmo item nas listagens [!DNL Commerce] e Amazon. Um atributo para o produto pode ser o preço de listagem do item. O nome do preço da listagem em [!DNL Commerce] pode ser nomeado `Price`, enquanto o preço da listagem para Amazon pode ser nomeado `ListingPrice`. Você deve instruir [!DNL Commerce] que, ao se comunicar com o Amazon, o atributo [!DNL Commerce] chamado `Price` é o mesmo do atributo Amazon chamado `ListingPrice`. Esse processo é chamado de _gerenciamento de atributos_ e inclui a criação de atributos novos e a edição de atributos existentes. Certificar-se de que os atributos estejam correspondentes corretamente garante a comunicação correta entre [!DNL Commerce] e o Amazon.

Quando o mapeamento de atributo é configurado, [!DNL Commerce] pode comunicar informações do produto de um lado para o outro com o Amazon. Se você tiver listas de produtos do Amazon, [!DNL Commerce] poderá importar seus produtos e detalhes do Amazon para o seu catálogo [!DNL Commerce], permitindo gerenciar suas listas do Amazon a partir de um único catálogo central de produtos.

O canal de vendas do Amazon permite acessar, revisar, criar e gerenciar atributos, conforme necessário, na [_[!UICONTROL Attributes]_visualização](./attributes-view.md) na home page do canal de vendas do Amazon. Se você adicionar um atributo ao seu catálogo [!DNL Commerce], poderá exigir uma atualização desses valores em todos os produtos.

Para obter mais informações sobre [!DNL Commerce] e conjuntos e valores de atributos do Amazon, consulte:

- [Gerenciar noções básicas de atributos](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}
- [Criar um atributo](./creating-attributes.md#create-an-attribute)
- [Editar um atributo existente](./creating-attributes.md#edit-an-attribute)
- [Visualizar mapeamento de atributo](./amazon-matching-attributes-values.md)
- [Editar ou criar mapeamento de atributo](./amazon-manually-update-incomplete-listing.md)
