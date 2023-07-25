---
title: "Introdução ao [!DNL Amazon Sales Channel]"
description: "[!DNL Amazon Sales Channel] permite que os comerciantes vendam produtos sem problemas na [!DNL Amazon Marketplace]."
redirect_from: /sales-channels/amazon/amazon-sales-channel.html
role: Admin, User, Leader
exl-id: a4a6f446-7029-4c92-bce3-5b857cc33056
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# Introdução ao [!DNL Amazon Sales Channel]

Como comerciante de Adobe Commerce ou Magento Open Source, você pode usar o [!DNL Amazon Sales Channel] extensão para integrar suas lojas ao maior destino global de compras na internet do mundo. Essa extensão habilita as vendas do Amazon conectando-se [!DNL Commerce] com o seu [!DNL Amazon Seller Central] conta e fornecendo automação e sincronização de dados de catálogo e pedido. Gerencie completamente todas as listagens do Amazon, implemente regras de preços simples ou inteligentes e mantenha seus pedidos e inventário por meio de uma única [!DNL Commerce] painel.

Depois [integração](./amazon-onboarding-home.md), [!DNL Commerce] O se torna um &quot;centro de comando central&quot; para gerenciar e controlar suas listas, pedidos e inventário da Amazon, além de preços para sua loja da Amazon. [Integração da loja](./store-integration.md) conecta seu [!DNL Commerce] instância e o Amazon para sincronizar dados entre ambas as plataformas. O canal de vendas da Amazon permite:

- [Integrado](./amazon-onboarding-home.md) e integrar um ou mais [!DNL Amazon Seller Central] contas com Adobe Commerce ou Magento Open Source.

- Importe e sincronize suas listas existentes do Amazon e corresponda aos produtos em seu [!DNL Commerce] catálogo, criando um catálogo de produtos centralizado.

- Crie e gerencie listagens do Amazon para produtos em seu [!DNL Commerce] catálogo.

- Exibir e atender (remessa) ordens em [!DNL Commerce] e Amazon, sincronizando status de pedido, pagamento e informações de reembolso.

- Exibir logs para análise e erros para [preços competitivos](./competitive-price-analysis.md), [listando alterações](./listing-changes-log.md), e [problemas de comunicação](./communication-errors-log.md).

Acesse suas lojas Amazon para visualizar e gerenciar todos esses recursos, informações de conta, listas, pedidos e muito mais no canal de vendas da Amazon [home page](./amazon-sales-channel-home.md).

## Promoções e preços

Com o [!DNL Amazon Sales Channel] você pode:

- Sincronizar preços de listagem do Amazon com [!DNL Commerce] preço de catálogo (ou atributo de preço alternativo).

- Habilitar MSRP [preço tachado](./listing-price.md#configure-listing-price-settings) em suas listagens do Amazon para aumentar a proposta de valor do cliente.

- Ativar e gerenciar [Preço Mínimo Anunciado (MAP)](./listing-price.md#configure-listing-price-settings) em suas listagens do Amazon.

- Configurar adicional [Imposto IVA](./listing-price.md#configure-listing-price-settings) em seus preços do Amazon.

- Defina um valor personalizado para &quot;quantidade disponível&quot; no [configurações de estoque/quantidade](./stock-quantity.md#configure-stock--quantity-settings) para mostrar com suas listas do Amazon para aumentar a urgência do comprador.

## Regras de preços

Com o [!DNL Amazon Sales Channel] você pode:

- Criar empilháveis, flexíveis e complexos [regras de preços](./pricing-products.md) para gerenciar os preços do Amazon para vendas diárias ou promoções sazonais.

- Criar [andar](./floor-price.md) e [teto](./optional-ceiling-price.md) para proteger os preços mais baixos e mais altos.

- Criar e gerenciar [regras inteligentes de reavaliação de preços](./intelligent-repricing-rules.md) que ajustam automaticamente os preços do seu produto em relação aos outros concorrentes da Amazon ([concorrente mais baixo](./lowest-competitor-pricing.md) e [Buy Box](./buy-box-competitor-pricing.md) preço).

## Gerenciamento de feed de catálogo

Com o [!DNL Amazon Sales Channel] você pode:

- Importe suas listas existentes do Amazon (produtos) e corresponda aos produtos existentes ou crie produtos em seu [!DNL Commerce] catálogo.

- Publicar seu [!DNL Commerce] produtos ao Amazon para criar listagens do Amazon.

- Criar [sobreposições](./creating-editing-overrides.md) para definir um preço individual, tempo de manuseio, condição e mensagem de notas do vendedor.

- Importar e mapear produto [atributos](./attributes-view.md) em suas listagens do Amazon para corresponder automaticamente aos produtos em sua [!DNL Commerce] catálogo.

- Defina vários parâmetros de pesquisa para corresponder às listagens do Amazon [!DNL Commerce] catálogo.

- Definir [regras de listagem](./listing-rules.md) para determinar qual dos seus [!DNL Commerce] os produtos estão qualificados para serem listados no Amazon.

- Definir um padrão [tempo de manuseio](./product-listing-actions.md) para suas novas listagens do Amazon.

- Corresponder às condições da lista com base em um [!DNL Commerce] atributo.

- Adicione notas do vendedor para cada tipo de condição (opcional).

- Implementar limites de quantidade ao importar listas do Amazon para sua [!DNL Commerce] catálogo.

- Exibir recomendado [melhorias na lista](./listing-improvements.md).

## Gerenciamento de pedidos e atendimento ao cliente

Com o [!DNL Amazon Sales Channel] você pode:

- Suporte e processamento de pedidos no Amazon e [!DNL Commerce].

- [Importar](./order-settings.md#configure-order-settings) seus pedidos da Amazon para [!DNL Commerce] ou deixe-os no Amazon.

- Defina qual dos seus [!DNL Commerce] lojas de site para associar a seus pedidos da Amazon para importar e gerenciar pedidos.

- Exibir, cancelar e entregar ordens de [!DNL Commerce] e/ou Amazon dependendo do seu [configurações de preenchimento](./fulfilled-by.md).

- Mapear o status do pedido do Amazon para um status personalizado no [!DNL Commerce] (opcional).

- Exiba e gerencie erros de pedidos para resolver problemas e conectar-se com clientes.

- Envie dados de rastreamento de pedidos para o seu [!DNL Amazon Seller Central] conta.

- [Cancelar pedidos](./cancel-unshipped-order.md) e selecione uma resposta de motivo.

- Exibir o [pedido recente](./amazon-store-dashboard.md) informações para seus pedidos do Amazon.

## Relatórios

Com o [!DNL Amazon Sales Channel] extensão, é possível revisar as informações do relatório sobre:

- Listas por status de ativo, inativo, elegível e incompleto.

- Pedidos aguardando remessa.

- Pedidos mais recentes.

- Amazon [log de alterações da lista](./listing-changes-log.md) para revisar alterações no feed de produtos/listagens (como preço e quantidade).

- Produto [Buy Box](./buy-box-competitor-pricing.md) Dados de preços da concorrência.

- Produto [Menor preço para concorrentes](./lowest-competitor-pricing.md) dados.

## Suporte para vendas globais

Com o [!DNL Amazon Sales Channel] você pode:

- Gerenciar vários [!DNL Amazon Marketplace] regiões (países).

- Suporte a várias moedas usando o [Ferramenta de configuração de moeda de comércio](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html).

- Gerencie remessas de seus locais de produtos e centros de atendimento da Amazon.

## Gerenciamento de clientes

Crie seu [!DNL Commerce] banco de dados do cliente por [importação de dados do cliente](./order-settings.md#configure-order-settings) associados aos seus pedidos da Amazon. Aumente seu potencial de marketing com essa lista expandida de clientes com suas [!DNL Amazon Marketplace] listagens e [!DNL Commerce] vitrine eletrônica.


Começar é fácil. Um curto processo de integração orienta você na criação de um [!DNL Amazon Seller Central] conta e integração com sua loja de canais de vendas da Amazon e sua [!DNL Commerce] catálogo para gerenciar listagens, ordens, inventário e fulfillment do Amazon. Um painel central mostra atualizações de status para todas as integrações da loja de canais de vendas da Amazon e listagens do Amazon. Alcance novos clientes no mundo [!DNL Amazon Marketplace] com processos simplificados e automatizados - tudo com pouco ou nenhum custo e mão de obra para a configuração de um novo sistema.

Depois de integrar o [!DNL Amazon Seller Central] conta, a variável [!DNL Amazon Sales Channel] A extensão do permite gerenciar as contas e sincroniza os dados entre [!DNL Commerce] e Amazon. Ela permite criar listas, gerenciar promoções, definir preços e gerenciar o inventário e o fulfillment diretamente por meio da [!DNL Commerce] Admin. Essas opções incluem regras de precificação que monitoram a precificação do Amazon para o mesmo item e ajustam automaticamente seus preços para serem mais competitivos.

