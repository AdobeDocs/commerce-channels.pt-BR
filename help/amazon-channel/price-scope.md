---
title: Escopo de preços
description: Use o escopo de preços do Commerce para gerenciar preços de acordo com vários sites ou globalmente.
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# Escopo de preços

[!DNL Commerce] fornece a configuração para o [escopo de precificação](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target="_blank"} to be set to `Global` or `Website`. If pricing is set to `Global`, there is a single price source for all websites. If pricing is set to `Website`, your websites can vary their pricing across and also have a fallback default pricing value. See [Catalog Price](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target="_blank"} no guia do usuário principal do Commerce.

Se você alterar o escopo de preço do catálogo de `Global` para `Website`, todos os atributos de tipo de preço também serão alterados para `Website`. Consulte [Adicionar sites](https://docs.magento.com/user-guide/stores/stores-all-create-website.html){target="_blank"}.

Quando um preço de site é escolhido, há duas fontes de preço:

- O preço do site
- O preço padrão (fallback)

Para a integração do canal de vendas da Amazon, com base em suas [regras de listagem](./listing-rules.md), você pode mapear produtos de vários sites em um único [!DNL Amazon Marketplace] País (definido durante [integração de loja](./store-integration.md)). No entanto, esse mapeamento introduz a questão de qual preço deve ser publicado se o produto existir em vários sites com preços diferentes.
