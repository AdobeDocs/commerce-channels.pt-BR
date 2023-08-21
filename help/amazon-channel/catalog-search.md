---
title: Pesquisa no catálogo de listagens do Amazon
description: Para definir a correspondência de atributos que ajuda a mapear produtos de catálogo do Commerce qualificados com listagens do Amazon, atualize as configurações de Pesquisa de catálogo.
feature: Sales Channels, Search, Catalog Management, Products, Configuration
exl-id: 9fcaa924-cba3-498f-8e21-1a1f91b1ad04
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 0%

---

# Pesquisa no catálogo de listagens do Amazon

_Pesquisa no catálogo_ as configurações fazem parte das configurações da lista de lojas. As configurações de listagem são acessadas no [painel de armazenamento](./amazon-store-dashboard.md).

Essas configurações permitem que você defina a correspondência de atributos que ajudam a mapear elegíveis [!DNL Commerce] produtos com listagens do Amazon. Quando mapeado, o Amazon ativa ações relacionadas a preço, quantidade, substituições e sincronização de pedidos e produtos.

A definição desses valores de mapeamento aumenta o potencial para correspondências exatas, minimizando a necessidade de corresponder manualmente as listas de produtos. Adicionar os atributos como parte de sua [Tarefas de Pré-configuração](./amazon-pre-setup-tasks.md), o canal de vendas da Amazon tem um maior potencial para corresponder automaticamente seus produtos durante a integração e sincroniza dados de produto entre o Amazon e o [!DNL Commerce].

Se você criar apenas o atributo ASIN do Amazon (sem adicionar valores ASIN por produto), seu [!DNL Commerce] Os produtos do podem não corresponder automaticamente às suas listagens do Amazon. Você pode [atribuir manualmente](./creating-assigning-catalog-products.md) seus produtos. No entanto, a correspondência manual não cria os elementos de dados necessários para compartilhar e sincronizar os dados do produto.

>[!IMPORTANT]
>
>Se você corresponder manualmente um produto e quiser atualizar um ASIN, UPC ou outro elemento de dados do produto, será necessário atualizar os dados em dois lugares. Atualize-o no seu [!DNL Commerce] catálogo e na sua lista do Amazon em seu [!DNL Amazon Seller Central] conta.

É uma prática recomendada mapear esses atributos e valores, se disponíveis. A conclusão desse mapeamento não é necessária, mas é benéfica para a correspondência de produtos e necessária para a sincronização adequada do catálogo entre o Amazon e o [!DNL Commerce].

Se quiser adicionar atributos, consulte [Criar atributos de produto para correspondência do Amazon](./ob-creating-magento-attributes.md).

## Configurar [!UICONTROL Catalog Search] configurações

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda a _[!UICONTROL Catalog Search]_seção.

1. Para **[!UICONTROL ASIN]**, escolha o atributo de produto criado para o valor ASIN do Amazon.

   Uma ASIN ([!DNL Amazon Standard Identification Number]) é um bloco exclusivo de dez letras e/ou números que identificam itens. Para livros, o ASIN é o mesmo que o número ISBN, mas para todos os outros produtos, um novo ASIN é criado quando o item é carregado para o seu catálogo. Você pode encontrar um ASIN de itens na página de detalhes do produto no Amazon, juntamente com mais detalhes relacionados ao item.

1. Para **[!UICONTROL EAN]**, escolha o atributo de produto que você criou para o valor EAN do Amazon.

   O Número Europeu de Artigo (EAN) é um padrão de código de barras, um código de identificação de produto de 12 ou 13 dígitos. Cada EAN identifica exclusivamente o produto, o fabricante e seus atributos; normalmente, o EAN é impresso em um rótulo de produto ou embalagem como um código de barras. O Amazon exige códigos EAN para melhorar a qualidade dos resultados de pesquisa e a qualidade do catálogo. Você pode obter EANs do fabricante.

1. Para **[!UICONTROL GCID]**, escolha o atributo de produto que você criou para o valor de GCIN do Amazon.

   O Identificador de catálogo global (GCID) é uma ID para produtos que não têm um código UPC ou ISBN. O Registro de marca da Amazon permite que você se registre como proprietário da marca e crie um identificador exclusivo para os produtos.

1. Para **[!UICONTROL ISBN]**, escolha o atributo de produto criado para o valor ISBN do Amazon.

   O International Standard Book Number (ISBN) é um identificador de livro comercial exclusivo. Cada código ISBN identifica exclusivamente um livro. Um ISBN tem dez ou 13 dígitos. Todos os ISBN atribuídos após 1° de janeiro de 2007 têm 13 dígitos.

1. Para **[!UICONTROL UPC]**, escolha o atributo de produto que você criou para o valor UPC do Amazon.

   O Universal Product Code (UPC) é um código de barras de 12 dígitos usado extensivamente para embalagens de varejo nos Estados Unidos.

1. Para **[!UICONTROL General Search]**, escolha o atributo de produto que deseja usar para uma correspondência de pesquisa geral.

   Este atributo é aquele que você pode selecionar para corresponder [!DNL Commerce] produtos para a lista apropriada do Amazon. A pesquisa geral usa pesquisas por palavras-chave do catálogo. Assim, recomenda-se a utilização de um [!DNL Commerce] atributo que contém palavras-chave relevantes, como SKU do produto ou nome do produto. A pesquisa geral pode retornar muitas correspondências possíveis e, nesses casos, você pode selecionar a lista apropriada do Amazon nas correspondências possíveis. Uma seleção comum para esse campo é `Product Name`.

1. Quando terminar, clique em **[!UICONTROL Save listing settings]**.

![Pesquisa no catálogo](assets/amazon-catalog-search.png){width="500" zoomable="yes"}

| Campo | Descrição |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL ASIN] | Um bloco exclusivo de 10 letras e/ou números que identificam itens.<br><br>ASIN significa [!DNL Amazon Standard Identification Number]. Um ASIN é um bloco exclusivo de 10 letras e/ou números que identificam itens. Para livros, o ASIN é o mesmo que o número ISBN, mas para todos os outros produtos, um novo ASIN é criado quando o item é carregado para o seu catálogo. Você pode encontrar um ASIN de itens na página de detalhes do produto no Amazon, juntamente com mais detalhes relacionados ao item. |
| [!UICONTROL EAN (European Article Number)] | Um código de identificação do produto de 12 ou 13 dígitos. O Número Europeu de Artigo (EAN) é um padrão de código de barras, um código de identificação de produto de 12 ou 13 dígitos. Cada EAN identifica exclusivamente o produto, o fabricante e seus atributos; normalmente, o EAN é impresso em um rótulo de produto ou embalagem como um código de barras. O Amazon exige códigos EAN para melhorar a qualidade dos resultados de pesquisa e a qualidade do catálogo. Você pode obter EANs do fabricante. |
| [!UICONTROL GCID (Global Catalog Identifier)] | O Identificador de catálogo global (GCID) é uma ID para produtos que não têm um código UPC ou ISBN. O Registro de marca da Amazon permite que você se registre como proprietário da marca e crie um identificador exclusivo para produtos que podem não ter um UPC ou ISBN. |
| [!UICONTROL ISBN (International Standard Book Number)] | Um código de barras identificador de livro comercial exclusivo de 10 ou 13 dígitos. O International Standard Book Number (ISBN) é um identificador de livro comercial exclusivo. Cada código ISBN identifica exclusivamente um livro. Um ISBN tem dez ou 13 dígitos. Todos os ISBN atribuídos após 1° de janeiro de 2007 têm 13 dígitos. |
| UPC (Universal Product Code) | Um código de barras de 12 dígitos. O Universal Product Code (UPC) é um código de barras de 12 dígitos usado extensivamente para embalagens de varejo nos Estados Unidos. |
| [!UICONTROL General Search] | Selecione um atributo. Este atributo é aquele que você pode selecionar para corresponder [!DNL Commerce] produtos para a lista apropriada do Amazon. A pesquisa geral usa pesquisas por palavras-chave do catálogo. Assim, recomenda-se a utilização de um [!DNL Commerce] atributo que contém palavras-chave relevantes, como SKU do produto ou nome do produto. A pesquisa geral pode retornar muitas correspondências possíveis e, nesses casos, você pode selecionar a lista apropriada do Amazon nas correspondências possíveis. Uma seleção comum para esse campo é `Product Name`. |

**Acesso rápido** - [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
