---
title: Sobre o Amazon e o catálogo de comércio
description: O canal de vendas da Amazon importa suas listagens do Amazon para o backend do Commerce e sincroniza continuamente com produtos e vendas.
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 0%

---

# Sobre a Amazon e a [!DNL Commerce] catálogo

O back-end do Adobe Commerce ou Magento Open Source inclui um catálogo com todos os produtos e configurações e informações associadas (imagens, opções, preços e muito mais) e configurações de pedido e envio. Seu [!DNL Amazon Seller Central] A conta também tem um catálogo e configurações de pedido, rastreando rigorosamente suas vendas por meio do [!DNL Amazon Marketplace].

Para gerenciar e revisar melhor seu catálogo de produtos e suas vendas por meio de um local, o canal de vendas da Amazon importa suas listagens de Amazon para seu [!DNL Commerce] back-end, sincroniza continuamente com produtos e vendas, além de relatar problemas e tendências. Ele suporta integrações com vários [!DNL Amazon Seller Central] , rastreando todos os dados na única interface para várias vitrines.

## Atributos do produto

Adobe Commerce e Magento Open Source gerenciam sincronizações de catálogo com o uso de produto [atributos](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} para definir configurações e dados do produto. O Amazon também usa atributos para serem mapeados por meio da integração. Durante [tarefas de pré-configuração](./amazon-pre-setup-tasks.md) para o canal de vendas do Amazon, você define atributos adicionais do Amazon (se necessário) para garantir mapeamentos de produto corretos ao importar suas listagens do Amazon para o [!DNL Commerce] catálogo. Esses atributos incluem UPC, EAN, ISBN e ASIN ([!DNL Amazon Standard Identification Number]). Por meio da integração, os produtos sincronizam entre o Amazon e o [!DNL Commerce] catálogos usando seus atributos. Mapeamento adequado de [!DNL Commerce] O e os produtos da Amazon garantem uma sincronização contínua das informações, pedidos e inventário do produto.

Se esses atributos não foram criados ou configurados para o catálogo, você deve adicionar um [!DNL Commerce] [atributo do produto](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} e valores para seus produtos antes da integração. Quando um atributo do Amazon é importado, ele pode ser usado para pesquisa, navegação, regras de preço e muito mais. Para obter mais informações sobre esses atributos, consulte [Amazon: O que são UPCs, EANs, ISBNs e ASINs?](https://www.amazon.com/gp/seller/asin-upc-isbn-info.html){target=&quot;_blank&quot;}

Após a integração, é possível gerenciar e atualizar os atributos de produto e os mapeamentos do Amazon a qualquer momento.

## Listas de produtos

Uma listagem da Amazon é uma página de produto para cada produto que você vende por meio da [!DNL Amazon Marketplace], exibindo descrições de produtos, preços, imagens e muito mais mapeado por meio de atributos. Durante a integração, você pode configurar [!DNL Commerce] Os produtos podem ser publicados automaticamente nas listas do Amazon. Você também pode importar suas listagens existentes do Amazon, mapeando-as para o seu [!DNL Commerce] produtos.

Quando você criou uma listagem [!DNL Commerce] são submetidos à Amazon para aprovação. A maioria das listagens bem-sucedidas são aprovadas em poucas horas. Se sua listagem for aprovada, ela aparecerá no [!DNL Amazon Marketplace] para pedidos imediatos de clientes. O [!DNL Amazon Sales Channel] A extensão fornece um conjunto de guias para revisar as listagens do Amazon. Dependendo do problema ou dos dados necessários, você deve revisar a [!DNL Amazon Seller Central] para obter detalhes específicos sobre essas listagens.

- [Ativo](./active-listings.md): Lista listas de produtos aprovados disponíveis no mercado.

- [Pronto para listar](./ready-to-list.md): Lista os produtos que atendem aos requisitos de regras de listagem e estão prontos para publicação no Amazon.

- [Inativo](./inactive-listings.md): Lista os produtos que não estão disponíveis no mercado devido ao bloqueio por um motivo específico (como um problema de marca), fechado e que requer nova listagem, e assim por diante.

- [Inelegível](./ineligible-listings.md): Devido às regras de listagem, o lista produtos que não podem ser listados ativamente no mercado (como `0` quantidade ou datas de venda).

- [Incompleto](./incomplete-listings.md): Lista produtos sem informações necessárias. Atualize os dados do produto para outra análise.

- [Encerrado](./ended-listings.md): Lista listas de produtos elegíveis para listagem, mas removidas manualmente do Amazon. Você pode confiar nesses produtos.

## Sincronização de dados

A Adobe Commerce e o Magento Open Source comunicam dados de produtos e pedidos entre seus [!DNL Amazon Seller Central] e a [!DNL Commerce] backend. As atualizações contínuas fornecem uma única fonte por meio de [!DNL Commerce] para gerenciar e manter seus inventários, atendendo pedidos, rastreando vendas e reduzindo os custos indiretos e a duplicação de trabalho. Os relatórios capturam os dados mais recentes para rastrear tendências e resolver problemas de comunicação entre os dois sistemas.

Todas as sincronizações são gerenciadas por um [trabalho cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}, defina como atualizar a cada cinco minutos em seu [Tarefas de pré-configuração](./amazon-pre-setup-tasks.md).
