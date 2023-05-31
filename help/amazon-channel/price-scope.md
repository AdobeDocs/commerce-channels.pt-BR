---
title: Canal de vendas da Amazon - Escopo de preço
description: Use o escopo de preços do Commerce para gerenciar preços de acordo com vários sites ou globalmente.
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# Escopo de preço

[!DNL Commerce] fornece a configuração para o [escopo de precificação](https://experienceleague.adobe.com/docs/commerce-admin/config/catalog/catalog.html#price) a ser definido como `Global` ou `Website`. Se a precificação estiver definida como `Global`, há uma única fonte de preço para todos os sites. Se a precificação estiver definida como `Website`, seus sites podem variar os preços e também ter um valor de preço padrão de fallback (consulte [Escopo de preço](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html)).

Se você alterar o escopo de preço do catálogo de `Global` para `Website`, todos os atributos de tipo de preço também serão alterados para `Website`. Consulte [Adicionar sites](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html#add-websites).

Quando um preço de site é escolhido, há duas fontes de preço:

- O preço do site
- O preço padrão (fallback)

Para a integração do canal de vendas da Amazon, com base em suas [regras de listagem](./listing-rules.md), você pode mapear produtos de vários sites em um único [!DNL Amazon Marketplace] País (definido durante [integração de loja](./store-integration.md)). No entanto, esse mapeamento introduz a questão de qual preço deve ser publicado se o produto existir em vários sites com preços diferentes.
