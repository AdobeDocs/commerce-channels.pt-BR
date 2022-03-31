---
title: Sobre [!DNL Channel Manager]
description: Saiba como instalar e usar o [!DNL Channel Manager] para integrar Adobe Commerce e Magento Open Source stores a mercados de terceiros e criar um canal de vendas para gerenciar listas de marketplace, preços, inventário e vendas de maneira simples do seu administrador de comércio.
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: ac084bf968a262dd4e7f6b6040aea2e6dc6197c2
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Visão geral

O Channel Manager for Adobe Commerce e Magento Open Source oferece um espaço de trabalho conveniente no Admin para gerenciar vendas de canais em mercados de terceiros, como Walmart, Amazon e eBay. Aumente as vendas e expanda-se para novos mercados enquanto gerencia as operações dos canais de vendas com facilidade do seu Administrador de comércio.

![[!DNL Channel Manager] visualização de administração de extensão](assets/channel-manager-admin-entry-page.png)

## Visão geral da versão beta

A versão Beta do Channel Manager oferece suporte a vendedores de Adobe Commerce ou Magento Open Source que desejam oferecer produtos no Walmart Marketplace.

Esta versão é compatível com os seguintes recursos para gerenciar operações de canal de vendas:

* Estabeleça uma conexão de API entre o Adobe Commerce ou o Magento Open Source e o Walmart Marketplace

* Publicar produtos do Gerenciador de canais no Walmart usando a correspondência de produtos

* Exibir o status da lista de produtos no Gerenciador de canais, por exemplo *projeto*, *processamento*, *correspondente*, *erro*.

* Sincronizar quantidades de inventário para produtos correspondentes do Commerce para o Walmart

* Sincronizar preços de catálogo para produtos correspondentes do Commerce para o Walmart

* Receba pedidos do Walmart Marketplace e visualize-os no [!DNL Commerce] painel de pedidos

### Latência esperada para operações do Gerenciador de canal

Os processos de sincronização de dados entre [!DNL Channel Manager] e um link [!DNL Walmart Marketplace] a loja requer algum tempo para ser concluída. Revise o tempo de processamento esperado para [!DNL Channel Manager] operações para ajudar a planejar o funcionamento das operações do canal de vendas.

**Latência estimada para operações do Gerenciador de canal**

| **Operação** | **Descrição** | **Atraso esperado** |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Adicionar produtos ao Gerenciador de canais | Selecione produtos do catálogo de produtos Commerce e importe-os para o Channel Manager. | **Até 5 minutos**-Se você selecionar muitos produtos, por exemplo, um catálogo de produtos inteiro, o processo de importação leva mais tempo. |
| Produtos correspondentes no Walmart Marketplace | Selecione listas de produtos no Gerenciador de canais e envie para o Walmart para correspondência. | **Até 30 minutos**-Se você selecionar muitos produtos, o processo correspondente demorará mais, dependendo da quantidade selecionada. |
| Atualizações de inventário | Quando a quantidade do inventário é alterada em Comércio. O Gerenciador de Canais sincroniza a atualização para o Walmart. | **Até 10 minutos** |
| Atualizações de preço | Quando um preço de produto muda, o Channel Manager sincroniza a atualização com o Walmart. | **Até 5 minutos** |
| Solicitar sincronizações do Walmart para o Commerce | O cliente solicita um produto comercial no Walmart Marketplace. O Walmart envia o pedido para o Gerenciador de Canais. A ordem é exibida no painel de ordem. | **Até 30 minutos** |
| Ordem criada no Commerce Order Management | O Gerenciador de Canais cria o pedido de Comércio a partir do pedido Walmart e atualiza o painel de pedidos para incluir o número do pedido de Comércio. | **Até 5 minutos** |

## Pré-requisitos Walmart

Você precisa das seguintes informações do Walmart para integrar o Commerce ao Walmart Marketplace:

* Aprovação para vender no Walmart e credenciais para iniciar sessão na conta registrada do vendedor do Marketplace

* Uma chave de API para conectar o Adobe Commerce ou o Magento Open Source ao Walmart Marketplace

   A chave de API do Walmart Marketplace permite a integração entre o Channel Manager para Adobe Commerce ou Magento Open Source e o Walmart Marketplace. Configure a chave da API no Seller Central antes de iniciar o processo de integração do Gerenciador de canais.

### Configurar uma conta do vendedor do Marketplace

1. [Envie seu aplicativo Walmart](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI)
2. Depois de obter a homologação da Walmart, [configurar sua conta do Walmart](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

### Gerar uma chave de API do Walmart Marketplace

1. Vá para o Walmart para gerar um [chave da API de produção do provedor de soluções para Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. Crie a chave e configure as permissões:

   * Selecione Adobe como o provedor de soluções.

   * Defina as permissões conforme mostrado na tabela a seguir. Para obter detalhes, consulte [Credenciais da API](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) no *Ajuda do vendedor do Walmart*.

   **Configuração de chave de API do Adobe para Walmart**

   | **Permissão** | **Configuração** |
   |----------------|-------------|
   | Conteúdo | Acesso completo |
   | Obter feeds | Exibir somente |
   | Inventário | Acesso completo |
   | Itens | Acesso completo |
   | Tempo de atraso | Acesso completo |
   | Pedido | Acesso completo |
   | Preço | Acesso completo |
   | Relatórios | Exibir somente |
   | Devoluções | Acesso completo |
   | Regras | Acesso completo |
   | Envio | Acesso completo |

## Status da loja no Walmart Marketplace

Ao publicar produtos no Walmart Marketplace, a listagem da disponibilidade depende do status das suas lojas do Walmart:

* Para lojas ao vivo, suas ofertas de produto são listadas e disponibilizadas para venda assim que a operação de correspondência for concluída.

* Para lojas que não estão ativas, suas ofertas de produto são preparadas e não ficam visíveis para os clientes. Assim que a loja entra em vigor, as listas preparadas são enviadas automaticamente para a loja ativa.


![[!DNL Walmart Seller Central] produtos preparados](assets/walmart-seller-central-staged.png)
