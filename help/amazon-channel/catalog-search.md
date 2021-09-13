---
title: Pesquisa no catálogo
description: 'Para definir a correspondência de atributos que ajuda a mapear produtos qualificados do catálogo de comércio com as listagens do Amazon, atualize as configurações da Pesquisa de catálogo.'
redirect_from: /sales-channels/asc/ob-catalog-search.html: 
exl-id: 9fcaa924-cba3-498f-8e21-1a1f91b1ad04
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 0
ht-degree: 0%

---

# Pesquisa no catálogo

_As configurações de_ pesquisa de catálogo fazem parte das configurações de listagem da sua loja. As configurações de listagem são acessadas no [painel de armazenamento](./amazon-store-dashboard.md).

Essas configurações permitem definir a correspondência de atributos que ajuda a mapear produtos [!DNL Commerce] qualificados com as listagens do Amazon. Quando mapeado, o Amazon ativa ações relacionadas a preços, quantidade, substituições e sincronização de pedido e produto.

A definição desses valores de mapeamento aumenta o potencial para correspondências exatas, minimizando a necessidade de corresponder manualmente as listas de produtos. Adicionando os atributos como parte de suas [Tarefas de pré-configuração](./amazon-pre-setup-tasks.md), o canal de vendas da Amazon tem um potencial maior para automaticamente corresponder seus produtos durante a integração e sincroniza dados de produtos entre o Amazon e [!DNL Commerce].

Se você criar apenas o atributo Amazon ASIN (sem adicionar valores ASIN por produto), seus produtos [!DNL Commerce] podem não corresponder automaticamente às suas listagens Amazon. Você pode [atribuir](./creating-assigning-catalog-products.md) manualmente seus produtos. No entanto, a correspondência manual não cria os elementos de dados necessários para compartilhar e sincronizar os dados do produto.

>[!IMPORTANT]
>
>Se você correspondeu manualmente a um produto e deseja atualizar um elemento de dados ASIN, UPC ou outro para o produto, é necessário atualizar os dados em dois lugares. Atualize-o em seu catálogo [!DNL Commerce] e em sua listagem do Amazon em sua conta [!DNL Amazon Seller Central].

É uma prática recomendada mapear esses atributos e valores, se disponíveis. A conclusão deste mapeamento não é necessária, mas é benéfica para a correspondência de produtos e necessária para a sincronização de catálogo adequada entre o Amazon e [!DNL Commerce].

Se quiser adicionar atributos, consulte [Criar atributos de produto para Amazon Matching](./ob-creating-magento-attributes.md).

## Definir configurações [!UICONTROL Catalog Search]

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda a seção _[!UICONTROL Catalog Search]_.

1. Para **[!UICONTROL ASIN]**, escolha o atributo de produto que você criou para o valor de ASIN do Amazon.

   Um ASIN ([!DNL Amazon Standard Identification Number]) é um bloco exclusivo de dez letras e/ou números que identifica itens. Para livros, o ASIN é o mesmo que o número ISBN, mas para todos os outros produtos, um novo ASIN é criado quando o item é carregado em seu catálogo. Você pode encontrar um ASIN de itens na página de detalhes do produto no Amazon, juntamente com mais detalhes relacionados ao item.

1. Para **[!UICONTROL EAN]**, escolha o atributo de produto que você criou para o valor Amazon EAN.

   O EAN (European Article Number) é uma norma de códigos de barras, um código de identificação de produtos de 12 ou 13 dígitos. Cada EAN identifica exclusivamente o produto, o fabricante e seus atributos; normalmente, o EAN é impresso em um rótulo de produto ou embalagem como um código de barras. O Amazon requer códigos EAN para melhorar a qualidade dos resultados da pesquisa e a qualidade do catálogo. Você pode obter EANs do fabricante.

1. Para **[!UICONTROL GCID]**, escolha o atributo de produto criado para o valor GCIN do Amazon.

   O Identificador de catálogo global (GCID) é uma ID para produtos que não têm um código UPC ou ISBN. O Registro de marca da Amazon permite que você se registre como um proprietário de marca e crie uma ID exclusiva para produtos.

1. Para **[!UICONTROL ISBN]**, escolha o atributo de produto que você criou para o valor ISBN do Amazon.

   O ISBN (International Standard Book Number) é um código de barras identificador de livro comercial exclusivo. Cada código ISBN identifica exclusivamente um livro. Um ISBN tem dez ou 13 dígitos. Todos os ISBN atribuídos após 1º de janeiro de 2007 têm 13 dígitos.

1. Para **[!UICONTROL UPC]**, escolha o atributo de produto criado para o valor UPC do Amazon.

   O código de produto universal (UPC) é um código de barras de 12 dígitos usado extensivamente para embalagens de varejo nos Estados Unidos.

1. Para **[!UICONTROL General Search]**, escolha o atributo de produto que deseja usar para uma correspondência de pesquisa geral.

   Esse atributo é aquele que você pode selecionar para corresponder [!DNL Commerce] produtos à lista apropriada do Amazon. A pesquisa geral usa pesquisas de palavras-chave do catálogo. Dessa forma, é recomendável usar um atributo [!DNL Commerce] que contenha palavras-chave relevantes, como o SKU do produto ou o nome do produto. A pesquisa geral pode retornar muitas correspondências possíveis e, nesses casos, você pode selecionar a listagem apropriada do Amazon entre as possíveis correspondências. Uma seleção comum para este campo é `Product Name`.

1. Quando terminar, clique em **[!UICONTROL Save listing settings]**.

![Pesquisa no catálogo](assets/amazon-catalog-search.png)

| Campo | Descrição |
|--- |--- |
| [!UICONTROL ASIN] | Um bloco exclusivo de 10 letras e/ou números que identifica itens.<br><br>ASIN significa  [!DNL Amazon Standard Identification Number]. Um ASIN é um bloco exclusivo de 10 letras e/ou números que identifica itens. Para livros, o ASIN é o mesmo que o número ISBN, mas para todos os outros produtos, um novo ASIN é criado quando o item é carregado em seu catálogo. Você pode encontrar um ASIN de itens na página de detalhes do produto no Amazon, juntamente com mais detalhes relacionados ao item. |
| [!UICONTROL EAN (European Article Number)] | Um código de identificação de produto de 12 ou 13 dígitos. O EAN (European Article Number) é uma norma de códigos de barras, um código de identificação de produtos de 12 ou 13 dígitos. Cada EAN identifica exclusivamente o produto, o fabricante e seus atributos; normalmente, o EAN é impresso em um rótulo de produto ou embalagem como um código de barras. O Amazon requer códigos EAN para melhorar a qualidade dos resultados da pesquisa e a qualidade do catálogo. Você pode obter EANs do fabricante. |
| [!UICONTROL GCID (Global Catalog Identifier)] | O Identificador de catálogo global (GCID) é uma ID para produtos que não têm um código UPC ou ISBN. O Registro de marca da Amazon permite que você se registre como um proprietário de marca e crie uma ID exclusiva para produtos que podem não ter um UPC ou ISBN. |
| [!UICONTROL ISBN (International Standard Book Number)] | Um código de barras identificador exclusivo do livro comercial de 10 ou 13 dígitos. O ISBN (International Standard Book Number) é um código de barras identificador de livro comercial exclusivo. Cada código ISBN identifica exclusivamente um livro. Um ISBN tem dez ou 13 dígitos. Todos os ISBN atribuídos após 1º de janeiro de 2007 têm 13 dígitos. |
| UPC (código universal do produto) | Um código de barras de 12 dígitos. O código de produto universal (UPC) é um código de barras de 12 dígitos usado extensivamente para embalagens de varejo nos Estados Unidos. |
| [!UICONTROL General Search] | Selecione um atributo. Esse atributo é aquele que você pode selecionar para corresponder [!DNL Commerce] produtos à lista apropriada do Amazon. A pesquisa geral usa pesquisas de palavras-chave do catálogo. Dessa forma, é recomendável usar um atributo [!DNL Commerce] que contenha palavras-chave relevantes, como o SKU do produto ou o nome do produto. A pesquisa geral pode retornar muitas correspondências possíveis e, nesses casos, você pode selecionar a listagem apropriada do Amazon entre as possíveis correspondências. Uma seleção comum para este campo é `Product Name`. |

**Acesso rápido**  -  [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
