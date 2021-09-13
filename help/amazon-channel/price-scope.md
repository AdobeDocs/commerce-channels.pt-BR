---
title: Escopo de preço
description: Use o escopo de preços do Commerce para gerenciar os preços de acordo com vários sites ou globalmente.
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Âmbito do preço

[!DNL Commerce] O fornece configuração para que seu escopo  [de preços](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){:target=&quot;_blank&quot;} seja definido como  `Global` ou  `Website`. Se o preço estiver definido como `Global`, haverá uma única fonte de preço para todos os sites. Se o preço estiver definido como `Website`, seus sites poderão variar seu preço e também ter um valor de preço padrão de fallback. Consulte [Preço do catálogo](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){:target=&quot;_blank&quot;} no guia do usuário principal do Commerce.

Se você alterar o escopo do preço do catálogo de `Global` para `Website`, todos os atributos de tipo de preço também serão alterados para `Website`. Consulte [Adicionar Sites](https://docs.magento.com/user-guide/stores/stores-all-create-website.html){:target=&quot;_blank&quot;}.

Quando o preço de um site é escolhido, há duas fontes de preço:

- O preço do site
- O preço padrão (queda para trás)

Para a integração do canal de vendas da Amazon, com base em suas [regras de listagem](./listing-rules.md), você pode mapear produtos de vários sites em um único [!DNL Amazon Marketplace] País (definido durante [integração de loja](./store-integration.md)). No entanto, este mapeamento introduz a questão de saber qual o preço a publicar se o produto existir em vários sites com preços diferentes.
