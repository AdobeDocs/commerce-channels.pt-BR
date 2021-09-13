---
title: Sobre o Amazon e o catálogo de comércio
description: O canal de vendas da Amazon importa suas listagens do Amazon para o backend do Commerce e sincroniza continuamente com produtos e vendas.
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Sobre o Amazon e o catálogo [!DNL Commerce]

Seu Adobe Commerce ou Magento Open Source backend inclui um catálogo com todos os produtos e configurações e informações associadas (imagens, opções, preços e muito mais) e configurações de pedido e envio. Sua conta [!DNL Amazon Seller Central] também tem um catálogo e configurações de pedido, rastreando rigorosamente suas vendas por meio do [!DNL Amazon Marketplace].

Para gerenciar e revisar melhor seu catálogo de produtos e suas vendas por meio de um local, o canal de vendas da Amazon importa suas listagens do Amazon para o [!DNL Commerce] backend, sincroniza continuamente com produtos e vendas e relata problemas e tendências. Ele suporta integrações com várias [!DNL Amazon Seller Central] contas, rastreando todos os dados por meio da única interface para várias vitrines.

## Atributos do produto

O Adobe Commerce e o Magento Open Source gerenciam sincronizações de catálogo com o uso do produto [attributes](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} para definir configurações e dados do produto. O Amazon também usa atributos para serem mapeados por meio da integração. Durante [tarefas de pré-configuração](./amazon-pre-setup-tasks.md) para o canal de vendas do Amazon, você define atributos adicionais do Amazon (se necessário) para garantir mapeamentos de produto corretos ao importar suas listagens do Amazon no catálogo [!DNL Commerce]. Esses atributos incluem UPC, EAN, ISBN e ASIN ([!DNL Amazon Standard Identification Number]). Por meio da integração, os produtos sincronizam entre o Amazon e os catálogos [!DNL Commerce] usando seus atributos. O mapeamento adequado dos produtos [!DNL Commerce] e da Amazon garante uma sincronização contínua das informações, pedidos e inventário do produto.

Se esses atributos não foram criados ou configurados para o catálogo, você deve adicionar um [!DNL Commerce] [atributo do produto](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} e valores aos seus produtos antes de integrar. Quando um atributo do Amazon é importado, ele pode ser usado para pesquisa, navegação, regras de preço e muito mais. Para obter mais informações sobre esses atributos, consulte [Amazon: O que são UPCs, EANs, ISBNs e ASINs?](https://www.amazon.com/gp/seller/asin-upc-isbn-info.html){target=&quot;_blank&quot;}

Após a integração, é possível gerenciar e atualizar os atributos de produto e os mapeamentos do Amazon a qualquer momento.

## Listas de produtos

Uma listagem do Amazon é uma página de produto para cada produto que você vende por meio do [!DNL Amazon Marketplace], exibindo descrições de produto, preços, imagens e muito mais mapeado por meio de atributos. Durante a integração, você pode configurar seus produtos [!DNL Commerce] que podem ser publicados automaticamente nas listas do Amazon. Você também pode importar suas listagens existentes do Amazon, mapeando-as para seus produtos [!DNL Commerce].

Quando você cria uma listagem de [!DNL Commerce] produtos, eles são submetidos à Amazon para aprovação. A maioria das listagens bem-sucedidas são aprovadas em poucas horas. Se sua listagem for aprovada, ela aparecerá no [!DNL Amazon Marketplace] para pedidos imediatos de clientes. A extensão [!DNL Amazon Sales Channel] fornece um conjunto de guias para revisar as listagens do Amazon. Dependendo do problema ou dos dados necessários, você deve revisar sua conta [!DNL Amazon Seller Central] para obter detalhes específicos sobre essas listagens.

- [Ativo](./active-listings.md): Lista listas de produtos aprovados disponíveis no mercado.

- [Pronto para listar](./ready-to-list.md): Lista os produtos que atendem aos requisitos de regras de listagem e estão prontos para publicação no Amazon.

- [Inativo](./inactive-listings.md): Lista os produtos que não estão disponíveis no mercado devido ao bloqueio por um motivo específico (como um problema de marca), fechado e que requer nova listagem, e assim por diante.

- [Inelegível](./ineligible-listings.md): Devido às regras de listagem, o lista produtos que não podem ser listados ativamente no mercado (como  `0` quantidade ou datas de venda).

- [Incompleto](./incomplete-listings.md): Lista produtos sem informações necessárias. Atualize os dados do produto para outra análise.

- [Encerrado](./ended-listings.md): Lista listas de produtos elegíveis para listagem, mas removidas manualmente do Amazon. Você pode confiar nesses produtos.

## Sincronização de dados

O Adobe Commerce e o Magento Open Source comunicam dados de produto e pedido entre a sua conta [!DNL Amazon Seller Central] e o [!DNL Commerce] back-end. As atualizações contínuas fornecem uma única fonte por meio de [!DNL Commerce] para gerenciar e manter seus inventários, atendendo aos pedidos, rastreando vendas e reduzindo a sobrecarga e a duplicação de trabalho. Os relatórios capturam os dados mais recentes para rastrear tendências e resolver problemas de comunicação entre os dois sistemas.

Toda sincronização é gerenciada por um [trabalho cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}, definido para atualizar a cada cinco minutos em suas [Tarefas de pré-configuração](./amazon-pre-setup-tasks.md).
