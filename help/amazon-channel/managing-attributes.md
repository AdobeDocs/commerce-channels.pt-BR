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

Amazon e [!DNL Commerce] ambos usam um sistema de propriedades do produto, conhecido como atributos, usado para definir um produto. Os atributos definem a descrição, o conteúdo, as imagens, os preços e vários dados para os seus produtos.

A comunicação bem-sucedida entre o Commerce e o Amazon requer que [!DNL Commerce] Os atributos devem ser mapeados corretamente (ou corresponder) ao atributo correspondente do Amazon. Ao integrar com o Amazon, você mapeia esses atributos para atributos do Amazon. Ao concluir, [!DNL Commerce] pode sincronizar e manter suas listagens do Amazon com seu [!DNL Commerce] catálogo de produtos.

Por exemplo, imagine que você tem o mesmo item em seu [!DNL Commerce] listas de catálogo e Amazon. Um atributo para o produto pode ser o preço de listagem do item. O nome do preço da listagem em [!DNL Commerce] pode ser nomeado `Price`, enquanto o preço da listagem do Amazon pode ser nomeado `ListingPrice`. Você deve instruir [!DNL Commerce] que, ao se comunicar com o Amazon, a variável [!DNL Commerce] nome do atributo `Price` é igual ao atributo do Amazon chamado `ListingPrice`. Esse processo é chamado de _gerenciamento de atributos_ e inclui a criação e edição de atributos existentes. Garantir que os atributos sejam correspondidos corretamente garante a comunicação correta entre [!DNL Commerce] e Amazon.

Quando o mapeamento de atributo é configurado, [!DNL Commerce] O pode comunicar informações do produto diretamente com o Amazon. Se você tiver listas de produtos Amazon, [!DNL Commerce] pode importar os produtos e detalhes da Amazon para o [!DNL Commerce] , permitindo gerenciar suas listas do Amazon a partir de um único catálogo central de produtos.

O canal de vendas da Amazon permite acessar, revisar, criar e gerenciar atributos, conforme necessário, na [_[!UICONTROL Attributes]_exibir](./attributes-view.md) na página inicial do canal de vendas da Amazon. Se você adicionar um atributo à sua [!DNL Commerce] pode exigir uma atualização desses valores em todos os produtos.

Para obter mais informações sobre [!DNL Commerce] e conjuntos e valores de atributos do Amazon, consulte:

- [Gerenciar noções básicas de atributos](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}
- [Criar um atributo](./creating-attributes.md#create-an-attribute)
- [Editar um atributo existente](./creating-attributes.md#edit-an-attribute)
- [Visualizar mapeamento de atributo](./amazon-matching-attributes-values.md)
- [Editar ou criar mapeamento de atributo](./amazon-manually-update-incomplete-listing.md)
