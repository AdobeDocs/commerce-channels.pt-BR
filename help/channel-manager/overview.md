---
title: Sobre [!DNL Channel Manager]
description: Saiba como instalar e usar o [!DNL Channel Manager] para integrar a Adobe Commerce e as Magento Open Source stores aos mercados de terceiros e criar um canal de vendas para gerenciar as listas, os preços, o inventário e as vendas do Marketplace de forma simples do seu administrador comercial.
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 61d72e655a9f9eaefddd7561e0bc5fe36da69577
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Sobre [!DNL Channel Manager]

[!DNL Channel Manager] ajuda você a aumentar as vendas e alcançar novos clientes integrando seu catálogo de produtos Adobe Commerce ou Magento Open Source com o [!DNL Walmart US Marketplace].

![[!DNL Channel Manager] visualização de administração de extensão](assets/channel-manager-home.png)

Depois de instalar e configurar [!DNL Channel Manager], o [!DNL Commerce] O administrador é estendido para que você possa gerenciar [!DNL Walmart Marketplace] operações de vendas perfeitamente no seu ambiente de Comércio.

* **Gerenciamento de listagem**-Publique facilmente as listas de produtos combinando produtos do catálogo do Commerce com as listas existentes do Walmart Marketplace .

* **Inventory management**-Os itens na conta do vendedor do comerciante são sincronizados e atualizados automaticamente do Commerce para garantir níveis precisos de inventário.

* **Atualizações de preços**- Mantenha preços precisos para listagens de marketplace com sincronização automática de preços. Quando um preço muda no Adobe Commerce, as alterações são refletidas no mercado em 10 minutos.

* **Gerenciamento de pedidos**-Quando novos pedidos são criados em um marketplace, o Gerenciador de Canais sincroniza pedidos com a Adobe Commerce e envia confirmações de pedido ao marketplace para garantir que o inventário seja reservado para cada pedido.

* **Gerenciamento de remessa**-Quando os pedidos são marcados como entregues na Adobe Commerce, a atualização de remessa é enviada para a [!DNL Walmart Marketplace]. Essa notificação garante que os vendedores atendam aos requisitos de SLA de cumprimento e que os clientes recebam notificações de atualização de envio para seus pedidos atuais.

* **Cancelamentos**-Quando os pedidos são cancelados no Adobe Commerce, o Gerenciador de Canais envia informações atualizadas do pedido ao marketplace para replicar a ação do pedido do marketplace correspondente.

[!DNL Channel Manager] oferece suporte para Adobe Commerce ou Magento Open Source sellers que desejam vender [!DNL Walmart Marketplace].

## Latência esperada para operações do Gerenciador de canal

Os processos de sincronização de dados entre [!DNL Channel Manager] e um link [!DNL Walmart Marketplace] a loja requer algum tempo para ser concluída. Revise o tempo de processamento esperado para [!DNL Channel Manager] operações para ajudar a planejar o funcionamento das operações do canal de vendas.

**Latência estimada para operações do Gerenciador de canal**

| **Operação** | **Descrição** | **Atraso esperado** |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Adicionar produtos ao Gerenciador de canais | Selecione produtos do catálogo de produtos Commerce e importe-os para o Channel Manager. | **Até 5 minutos**-Se você selecionar muitos produtos, por exemplo, um catálogo de produtos inteiro, o processo de importação leva mais tempo. |
| Produtos correspondentes no Walmart Marketplace | Selecione listas de produtos no Gerenciador de canais e envie para o Walmart para correspondência. | **Até 30 minutos**-Se você selecionar muitos produtos, o processo correspondente demorará mais, dependendo da quantidade selecionada. |
| Atualizações de inventário | Quando a quantidade do estoque for alterada no Commerce, [!DNL Channel Manager] sincroniza a atualização para o Walmart. | **Até 10 minutos** |
| Atualizações de preço | Quando um preço de produto muda, o Channel Manager sincroniza a atualização com o Walmart. | **Até 5 minutos** |
| Solicitar sincronizações do Walmart para o Commerce | O cliente solicita um produto comercial no Walmart Marketplace. O Walmart envia o pedido para o Gerenciador de Canais. A ordem é exibida no painel de ordem. | **Até 30 minutos** |
| Ordem criada no Commerce Order Management | O Gerenciador de Canais cria o pedido de Comércio a partir do pedido Walmart e atualiza o painel de pedidos para incluir o número do pedido de Comércio. | **Até 5 minutos** |

## Pré-requisitos Walmart

Você precisa das seguintes informações do Walmart para integrar o Commerce ao Walmart Marketplace:

* Aprovação para vender no Walmart e credenciais para iniciar sessão na conta registrada do vendedor do Marketplace

* Uma chave de API para conectar o Adobe Commerce ou o Magento Open Source ao Walmart Marketplace

   A chave de API do Walmart Marketplace permite a integração entre o Channel Manager para Adobe Commerce ou Magento Open Source e o Walmart Marketplace. Configure a chave da API no Seller Central antes de iniciar o processo de integração do Gerenciador de canais.

### Configurar uma conta do vendedor do Marketplace

1. [Envie seu aplicativo Walmart](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI).
2. Depois de obter a homologação da Walmart, [configurar sua conta do Walmart](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

### Gerar uma chave de API do Walmart Marketplace

1. Vá para o Walmart para gerar um [chave da API de produção do provedor de soluções para Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. Crie a chave e configure as permissões:

   * Selecione Adobe como o provedor de soluções.

   * Defina as permissões conforme mostrado na tabela a seguir. Para obter detalhes, consulte [Credenciais da API](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) no *[!DNL Walmart Marketplace]Ajuda do vendedor*.

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

* Para lojas ao vivo, suas ofertas de produto são listadas e disponibilizadas para venda quando a operação de correspondência for concluída.

* Para lojas que não estão ativas, suas ofertas de produto são preparadas e não ficam visíveis para os clientes. Quando a loja entra em vigor, as listas preparadas são enviadas automaticamente para a loja ativa.


![[!DNL Walmart Seller Central] produtos preparados](assets/walmart-seller-central-staged.png)
