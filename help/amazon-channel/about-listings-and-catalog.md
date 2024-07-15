---
title: Amazon e o catálogo do Commerce
description: O canal de vendas da Amazon importa suas listas do Amazon para o back-end da Commerce e sincroniza continuamente com produtos e vendas.
role: Leader, Admin, User
feature: Sales Channels, Integration, Tools and External Services, Merchandising, Catalog Management
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# Amazon e o catálogo [!DNL Commerce]

Seu back-end Adobe Commerce ou Magento Open Source inclui um catálogo com todos os produtos e configurações e informações associadas (imagens, opções, preços e muito mais) e configurações de pedido e envio. Sua conta do [!DNL Amazon Seller Central] também tem configurações de catálogo e pedido, controlando estritamente suas vendas pelo [!DNL Amazon Marketplace].

Para gerenciar e revisar melhor o catálogo de produtos e as vendas por meio de um único local, o canal de vendas da Amazon importa suas listas do Amazon para o back-end do [!DNL Commerce], sincroniza continuamente com produtos e vendas e relata problemas e tendências. Ele oferece suporte a integrações com várias contas do [!DNL Amazon Seller Central], rastreando todos os dados através de uma única interface para várias vitrines.

## Atributos do produto

O Adobe Commerce e o Magento Open Source gerenciam sincronizações de catálogo com o uso dos [atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) do produto para definir configurações e dados do produto. O Amazon também usa atributos, a serem mapeados por meio de integração. Durante as [tarefas de pré-configuração](./amazon-pre-setup-tasks.md) do canal de vendas da Amazon, você define atributos Amazon adicionais (se necessário) para garantir mapeamentos corretos de produtos ao importar suas listagens do Amazon para o catálogo [!DNL Commerce]. Esses atributos incluem UPC, EAN, ISBN e ASIN ([!DNL Amazon Standard Identification Number]). Por meio da integração, os produtos são sincronizados entre o Amazon e os catálogos do [!DNL Commerce] usando seus atributos. O mapeamento adequado do [!DNL Commerce] e dos produtos da Amazon garante uma sincronização contínua das informações do produto, dos pedidos e do inventário.

Se você não tiver esses atributos criados ou configurados para o catálogo, adicione um [!DNL Commerce] [atributo de produto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) e valores aos seus produtos antes da integração. Quando um atributo do Amazon é importado, ele pode ser usado para pesquisa, navegação, regras de preço e muito mais. Consulte [O que significam ASIN, UPC, EAN, ISBN, SKU e outros códigos de barras?](https://sellerskills.com/multi-channel-operations/what-asin-upc-ean-isbn-sku-and-other-barcodes-mean/#what-is-isbn-number){target="_blank"}

Após a integração, você pode gerenciar e atualizar os atributos do produto e os mapeamentos do Amazon a qualquer momento.

## Listagens de produtos

Uma lista do Amazon é uma página de produto para cada produto vendido pelo [!DNL Amazon Marketplace], exibindo descrições de produtos, preços, imagens e muito mais, mapeados por meio de atributos. Durante a integração, você pode configurar os produtos do [!DNL Commerce] para serem publicados automaticamente nas listagens do Amazon. Você também pode importar suas listagens existentes do Amazon mapeando-as para seus produtos do [!DNL Commerce].

Quando você cria uma lista de produtos [!DNL Commerce], eles são enviados à Amazon para aprovação. A maioria das listagens bem-sucedidas é aprovada em poucas horas. Se sua lista for aprovada, ela aparecerá no [!DNL Amazon Marketplace] para pedidos imediatos por clientes. A extensão [!DNL Amazon Sales Channel] fornece um conjunto de guias para revisar as listagens do Amazon. Dependendo do problema ou dos dados necessários, você deve consultar a conta do [!DNL Amazon Seller Central] para obter detalhes específicos sobre essas listagens.

- [Ativo](./active-listings.md): lista as listas de produtos aprovados disponíveis no marketplace.

- [Pronto para Listar](./ready-to-list.md): lista produtos que atendem aos requisitos de regras de listagem e estão prontos para publicar no Amazon.

- [Inativo](./inactive-listings.md): lista produtos que não estão disponíveis no marketplace devido ao bloqueio por um motivo específico (como problemas de marca), fechamento e exigência de lista de produtos, entre outros.

- [Inelegível](./ineligible-listings.md): devido às regras de listagem, lista produtos que não podem ser listados ativamente no marketplace (como `0` quantidade ou datas de venda).

- [Incompleto](./incomplete-listings.md): lista os produtos sem as informações necessárias. Atualize os dados do produto para outra revisão.

- [Encerrado](./ended-listings.md): Lista as listas de produtos qualificados para listagem, mas removidas manualmente do Amazon. Você pode listar esses produtos.

## Sincronização de dados

O Adobe Commerce e o Magento Open Source comunicam dados de produto e pedido entre sua conta do [!DNL Amazon Seller Central] e o back-end do [!DNL Commerce]. As atualizações contínuas fornecem uma única fonte por meio do [!DNL Commerce] para gerenciar e manter seus estoques, atender pedidos, controlar vendas e reduzir as despesas gerais e a duplicação de trabalho. Os relatórios capturam os dados mais recentes para rastrear tendências e resolver problemas de comunicação capturados entre os dois sistemas.

Toda a sincronização é gerenciada por um [trabalho do cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html), definido para atualização a cada cinco minutos em suas [Tarefas de Pré-Configuração](./amazon-pre-setup-tasks.md).
