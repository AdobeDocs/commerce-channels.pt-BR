---
title: Canal de vendas da Amazon - Escopo de preço
description: Use o escopo de preços do Commerce para gerenciar os preços de acordo com vários sites ou globalmente.
feature: Sales Channels, Price Rules
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# Escopo de preço

O [!DNL Commerce] fornece a configuração para o seu [escopo de preços](https://experienceleague.adobe.com/docs/commerce-admin/config/catalog/catalog.html#price) a ser definido como `Global` ou `Website`. Se o preço estiver definido como `Global`, há uma única fonte de preço para todos os sites. Se o preço estiver definido como `Website`, seus sites poderão variar o preço entre eles e também ter um valor de preço padrão de fallback (consulte [Escopo de preço](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html)).

Se você alterar o escopo de preço do catálogo de `Global` para `Website`, todos os atributos de tipo de preço também serão alterados para `Website`. Consulte [Adicionando Sites](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html#add-websites).

Quando um preço de site é escolhido, há duas fontes de preço:

- O preço do site
- O preço padrão (fallback)

Para a integração do canal de vendas da Amazon, com base em suas [regras de listagem](./listing-rules.md), você pode mapear produtos de vários sites em um único País [!DNL Amazon Marketplace] (definido durante a [integração de lojas](./store-integration.md)). No entanto, esse mapeamento introduz a questão de qual preço deve ser publicado se o produto existir em vários sites com preços diferentes.
