---
title: "Introdução a  [!DNL Amazon Sales Channel]"
description: "[!DNL Amazon Sales Channel] permite que comerciantes vendam produtos facilmente no [!DNL Amazon Marketplace]."
redirect_from: /sales-channels/amazon/amazon-sales-channel.html
role: Admin, User, Leader
exl-id: a4a6f446-7029-4c92-bce3-5b857cc33056
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# Introdução ao [!DNL Amazon Sales Channel]

Como comerciante de Adobe Commerce ou Magento Open Source, você pode usar a extensão [!DNL Amazon Sales Channel] para integrar suas lojas ao maior destino global de compras na Internet do mundo. Essa extensão habilita as vendas do Amazon conectando o [!DNL Commerce] à sua conta do [!DNL Amazon Seller Central] e fornecendo automação e sincronização de dados de catálogo e pedido. Gerencie completamente todas as listagens do Amazon, implemente regras de preços simples ou inteligentes e mantenha seus pedidos e estoque por meio de um único painel do [!DNL Commerce].

Após a [integração](./amazon-onboarding-home.md), o [!DNL Commerce] se torna um &quot;centro de comando central&quot; para gerenciar e controlar suas listas, seus pedidos, seu estoque e os preços da Amazon para sua loja da Amazon. A [integração de armazenamento](./store-integration.md) conecta a instância do [!DNL Commerce] e o Amazon para sincronizar dados entre as duas plataformas. O canal de vendas da Amazon permite:

- [Integrar](./amazon-onboarding-home.md) e integrar uma ou mais contas do [!DNL Amazon Seller Central] com o Adobe Commerce ou o Magento Open Source.

- Importe e sincronize suas listas existentes do Amazon e corresponda aos produtos no catálogo [!DNL Commerce], criando um catálogo de produtos centralizado.

- Crie e gerencie listagens do Amazon para produtos no catálogo do [!DNL Commerce].

- Exibir e atender (enviar) pedidos no [!DNL Commerce] e no Amazon, sincronizando status de pedido, pagamento e informações de reembolso.

- Exiba logs para análise e erros para [preços competitivos](./competitive-price-analysis.md), [alterações na lista](./listing-changes-log.md) e [problemas de comunicação](./communication-errors-log.md).

Acesse suas lojas do Amazon para exibir e gerenciar todos esses recursos, informações de conta, listas, pedidos e muito mais na [home page](./amazon-sales-channel-home.md) do canal de vendas do Amazon.

## Promoções e preços

Com a extensão [!DNL Amazon Sales Channel], você pode:

- Sincronizar os preços da listagem do Amazon com o preço de catálogo [!DNL Commerce] (ou atributo de preço alternativo).

- Habilite o MSRP [preço tachado](./listing-price.md#configure-listing-price-settings) nas suas listagens do Amazon para aumentar a proposta de valor do cliente.

- Habilite e gerencie o [Preço Mínimo Anunciado (MAP)](./listing-price.md#configure-listing-price-settings) nas suas listagens do Amazon.

- Configure o [Imposto de IVA](./listing-price.md#configure-listing-price-settings) adicional em seu preço do Amazon.

- Defina um valor personalizado para &quot;quantidade disponível&quot; nas [configurações de estoque/quantidade](./stock-quantity.md#configure-stock--quantity-settings) a serem mostradas nas listagens do Amazon para aumentar a urgência da compradora.

## Regras de preços

Com a extensão [!DNL Amazon Sales Channel], você pode:

- Crie [regras de preços](./pricing-products.md) empilháveis, flexíveis e complexas para gerenciar os preços do Amazon para vendas diárias ou promoções sazonais.

- Crie preços de [andar](./floor-price.md) e [teto](./optional-ceiling-price.md) para proteger seus preços mais baixos e mais altos.

- Crie e gerencie as [regras inteligentes de reavaliação de preços](./intelligent-repricing-rules.md) que ajustam automaticamente os preços do seu produto em relação a outros concorrentes da Amazon (preço do [concorrente mais baixo](./lowest-competitor-pricing.md) e do [Buy Box](./buy-box-competitor-pricing.md)).

## Gerenciamento de feed de catálogo

Com a extensão [!DNL Amazon Sales Channel], você pode:

- Importe suas listagens existentes do Amazon (produtos) e corresponda a produtos existentes ou crie produtos no catálogo [!DNL Commerce].

- Publish seus produtos do [!DNL Commerce] na Amazon para criar listagens do Amazon.

- Criar [substituições](./creating-editing-overrides.md) para definir um preço individual, lidar com tempo, condição e mensagem de notas do vendedor.

- Importe e mapeie [atributos](./attributes-view.md) do produto das suas listas do Amazon para corresponder automaticamente aos produtos do catálogo [!DNL Commerce].

- Defina vários parâmetros de pesquisa para corresponder às listagens do Amazon do catálogo [!DNL Commerce].

- Defina as [regras de listagem](./listing-rules.md) para determinar quais dos seus [!DNL Commerce] produtos estão qualificados para serem listados no Amazon.

- Defina um [tempo de manipulação](./product-listing-actions.md) padrão para suas novas listagens do Amazon.

- Corresponder condições de listagem com base em um atributo [!DNL Commerce].

- Adicione notas do vendedor para cada tipo de condição (opcional).

- Implemente limites de quantidade ao importar listas do Amazon para o catálogo [!DNL Commerce].

- Exibir [melhorias na listagem](./listing-improvements.md) recomendadas.

## Gerenciamento de pedidos e atendimento ao cliente

Com a extensão [!DNL Amazon Sales Channel], você pode:

- Suporte e processamento de pedidos no Amazon e [!DNL Commerce].

- [Importe](./order-settings.md#configure-order-settings) seus pedidos da Amazon para [!DNL Commerce] ou deixe-os na Amazon.

- Defina qual dos seus sites do [!DNL Commerce] armazena pedidos para associar aos seus pedidos da Amazon para importar e gerenciar pedidos.

- Exiba, cancele e envie ordens de [!DNL Commerce] e/ou Amazon dependendo de suas [configurações de preenchimento](./fulfilled-by.md).

- Mapeie seu status de pedido do Amazon para um status personalizado dentro de [!DNL Commerce] (opcional).

- Exiba e gerencie erros de pedidos para resolver problemas e conectar-se com clientes.

- Envie dados de acompanhamento de pedidos para sua conta [!DNL Amazon Seller Central].

- [Cancelar pedidos](./cancel-unshipped-order.md) e selecionar uma resposta de motivo.

- Exiba as informações de [pedido recente](./amazon-store-dashboard.md) para seus pedidos do Amazon.

## Relatórios

Com a extensão [!DNL Amazon Sales Channel], você pode revisar informações de relatório sobre:

- Listas por status de ativo, inativo, elegível e incompleto.

- Pedidos aguardando remessa.

- Pedidos mais recentes.

- Amazon [log de alterações de listagem](./listing-changes-log.md) para examinar alterações de feed de produto/listagem (como preço e quantidade).

- Dados de Preços do Concorrente do Produto [Buy Box](./buy-box-competitor-pricing.md).

- Dados de [Preço mais baixo do concorrente](./lowest-competitor-pricing.md) do produto.

## Suporte para vendas globais

Com a extensão [!DNL Amazon Sales Channel], você pode:

- Gerenciar várias regiões (países) do [!DNL Amazon Marketplace].

- Suporte a várias moedas usando a [ferramenta de configuração de moeda do Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html).

- Gerencie remessas de seus locais de produtos e centros de atendimento da Amazon.

## Gerenciamento de clientes

Crie o banco de dados do cliente [!DNL Commerce] importando os dados do cliente ](./order-settings.md#configure-order-settings) associados aos seus pedidos da Amazon. [ Aumente seu potencial de marketing com essa lista expandida de clientes com suas listas do [!DNL Amazon Marketplace] e loja do [!DNL Commerce].


Começar é fácil. Um pequeno processo de integração o orienta na criação de uma conta do [!DNL Amazon Seller Central] e na integração com seu armazenamento de canal de vendas da Amazon e seu catálogo [!DNL Commerce] para gerenciar listas, pedidos, estoque e atendimento do Amazon. Um painel central mostra atualizações de status para todas as integrações da loja de canais de vendas da Amazon e listagens do Amazon. Alcance novos clientes no [!DNL Amazon Marketplace] global com processos simplificados e automatizados - tudo com pouco ou nenhum custo e mão de obra para configurar um novo sistema.

Depois de integrar sua conta do [!DNL Amazon Seller Central], a extensão do [!DNL Amazon Sales Channel] permite que você gerencie suas contas e sincronize dados entre o [!DNL Commerce] e a Amazon. Ele permite criar listas, gerenciar promoções, definir preços e gerenciar o estoque e a execução diretamente por meio do Administrador do [!DNL Commerce]. Essas opções incluem regras de precificação que monitoram a precificação do Amazon para o mesmo item e ajustam automaticamente seus preços para serem mais competitivos.

