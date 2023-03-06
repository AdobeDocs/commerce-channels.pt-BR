---
title: Sobre o Amazon e o catálogo do Commerce
description: O canal de vendas do Amazon importa suas listas do Amazon para o back-end do Commerce e sincroniza continuamente com produtos e vendas.
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# Sobre o Amazon e o [!DNL Commerce] Catálogo

Seu back-end Adobe Commerce ou Magento Open Source inclui um catálogo com todos os produtos e configurações e informações associadas (imagens, opções, preços e muito mais) e configurações de pedido e envio. Seu [!DNL Amazon Seller Central] conta também tem um catálogo e configurações de pedido, rastreando estritamente suas vendas através do [!DNL Amazon Marketplace].

Para gerenciar e revisar melhor o catálogo de produtos e as vendas por meio de um único local, o canal de vendas da Amazon importa suas listas do Amazon para o [!DNL Commerce] back-end do, sincroniza continuamente com produtos e vendas, além de relatar problemas e tendências. Oferece suporte a integrações com vários [!DNL Amazon Seller Central] contas do, rastreando todos os dados por meio da única interface para várias lojas.

## Atributos do produto

O Adobe Commerce e o Magento Open Source gerenciam sincronizações de catálogo com o uso do produto [atributos](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"} para definir configurações e dados do produto. O Amazon também usa atributos, a serem mapeados por meio de integração. Durante [tarefas de pré-configuração](./amazon-pre-setup-tasks.md) para o canal de vendas do Amazon, você define atributos Amazon adicionais (se necessário) para garantir mapeamentos corretos do produto ao importar suas listagens do Amazon para o [!DNL Commerce] catálogo. Esses atributos incluem UPC, EAN, ISBN e ASIN ([!DNL Amazon Standard Identification Number]). Por meio da integração, os produtos são sincronizados entre o Amazon e o [!DNL Commerce] catálogos usando seus atributos. Mapeamento adequado do seu [!DNL Commerce] O e os produtos da Amazon garantem uma sincronização contínua de informações sobre produtos, pedidos e inventário.

Se você não tiver esses atributos criados ou configurados para o catálogo, adicione um [!DNL Commerce] [atributo de produto](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"} and values to your products before onboarding. When an Amazon attribute is imported, it can be used for search, navigation, price rules, and much more. See [What Do ASIN, UPC, EAN, ISBN, SKU and Other Barcodes Mean?](https://sellerskills.com/multi-channel-operations/what-asin-upc-ean-isbn-sku-and-other-barcodes-mean/#what-is-isbn-number){target="_blank"}

Após a integração, você pode gerenciar e atualizar os atributos do produto e os mapeamentos do Amazon a qualquer momento.

## Listagens de produtos

Uma lista do Amazon é uma página de produto para cada produto vendido pelo [!DNL Amazon Marketplace], exibindo descrições de produtos, preços, imagens e muito mais, mapeados por meio de atributos. Durante a integração, é possível configurar as [!DNL Commerce] os produtos podem ser publicados automaticamente nas listagens do Amazon. Você também pode importar suas listagens existentes do Amazon mapeando-as para o seu [!DNL Commerce] produtos.

Quando tiver criado uma lista [!DNL Commerce] são enviados à Amazon para aprovação. A maioria das listagens bem-sucedidas é aprovada em poucas horas. Se a lista for aprovada, ela aparecerá no [!DNL Amazon Marketplace] para pedidos imediatos por clientes. A variável [!DNL Amazon Sales Channel] A extensão fornece um conjunto de guias para revisar as listagens do Amazon. Dependendo do problema ou dos dados necessários, você deve revisar [!DNL Amazon Seller Central] para obter detalhes específicos sobre essas listagens.

- [Ativo](./active-listings.md): lista as listas de produtos aprovados disponíveis no marketplace.

- [Pronto para Listar](./ready-to-list.md): lista os produtos que atendem aos requisitos das regras de lista e estão prontos para publicação no Amazon.

- [Inativo](./inactive-listings.md): lista produtos que não estão disponíveis no marketplace devido ao bloqueio por um motivo específico (como problema de marca), fechamento e exigência de lista de produtos e assim por diante.

- [Inelegível](./ineligible-listings.md): devido às regras de listagem, o lista produtos que não podem ser listados ativamente no marketplace (como `0` quantidade ou datas de venda).

- [Incompleto](./incomplete-listings.md): lista os produtos que não têm as informações necessárias. Atualize os dados do produto para outra revisão.

- [Terminado](./ended-listings.md): lista as listagens de produtos qualificados para listagem, mas removidos manualmente do Amazon. Você pode listar esses produtos.

## Sincronização de dados

O Adobe Commerce e o Magento Open Source comunicam dados de produtos e pedidos entre o [!DNL Amazon Seller Central] e a [!DNL Commerce] back-end. As atualizações contínuas fornecem uma única fonte através do [!DNL Commerce] para gerenciar e manter seus inventários, atender ordens, rastrear vendas e reduzir os custos indiretos e a duplicação de trabalho. Os relatórios capturam os dados mais recentes para rastrear tendências e resolver problemas de comunicação capturados entre os dois sistemas.

Toda a sincronização é gerenciada por um [trabalho cron](https://docs.magento.com/user-guide/system/cron.html){target="_blank"}, defina para atualizar a cada cinco minutos no [Tarefas de Pré-configuração](./amazon-pre-setup-tasks.md).
