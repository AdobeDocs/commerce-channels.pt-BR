---
title: '"Sobre [!DNL Channel Manager]"'
description: '"Saiba como instalar e usar o [!DNL Channel Manager] para integrar a Adobe Commerce e as Magento Open Source stores aos mercados de terceiros e criar um canal de vendas para gerenciar as listas, os preços, o inventário e as vendas do Marketplace de forma simples do seu administrador comercial."'
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: ae3d95fd0da6ee5013a19d7ac7ed5ef87e4a1325
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---


# Sobre [!DNL Channel Manager]

[!DNL Channel Manager] ajuda você a aumentar as vendas e alcançar novos clientes integrando seu catálogo de produtos Adobe Commerce ou Magento Open Source com o [!DNL Walmart US Marketplace].

![[!DNL Channel Manager] visualização de administração de extensão](assets/channel-manager-home.png)

O Channel Manager oferece suporte para Adobe Commerce ou Magento Open Source seletores que desejam vender no [!DNL Walmart Marketplace].

Depois de instalar e configurar [!DNL Channel Manager], o [!DNL Commerce] O administrador é estendido para que você possa gerenciar [!DNL Walmart Marketplace] operações de vendas perfeitamente no seu ambiente de Comércio.

* **Gerenciamento de listagem**-Publique facilmente as listas de produtos ao combinar produtos de seu [!DNL Commerce] catálogo para existente [!DNL Walmart Marketplace] listagens.

* **Inventory management**-Os itens na conta do vendedor do comerciante são sincronizados e atualizados automaticamente do Commerce para garantir níveis precisos de inventário.

* **Atualizações de preços**- Mantenha preços precisos para listagens de marketplace com sincronização automática de preços. Quando um preço muda no Adobe Commerce, as alterações são refletidas no mercado em 10 minutos.

* **Gerenciamento de pedidos**-Quando novos pedidos são criados em um marketplace, o Gerenciador de Canais sincroniza pedidos com a Adobe Commerce e envia confirmações de pedido ao marketplace para garantir que o inventário seja reservado para cada pedido.

* **Gestão de remessa**-Quando os pedidos são marcados como entregues na Adobe Commerce, a atualização de remessa é enviada para a [!DNL Walmart Marketplace]. Essa notificação garante que os vendedores atendam aos requisitos de SLA de cumprimento e que os clientes recebam notificações de atualização de envio para seus pedidos atuais.

* **Cancelamentos**-Quando os pedidos são cancelados no Adobe Commerce, o Gerenciador de Canais envia informações atualizadas do pedido ao marketplace para replicar a ação do pedido do marketplace correspondente.

## Latência esperada para operações do Gerenciador de canal

Os processos de sincronização de dados entre [!DNL Channel Manager] e um link [!DNL Walmart Marketplace] a loja requer algum tempo para ser concluída. Revise o tempo de processamento esperado para [!DNL Channel Manager] operações para ajudar a planejar o funcionamento das operações do canal de vendas.

**Latência estimada para operações do Gerenciador de canal**

| **Operação** | **Descrição** | **Atraso esperado** |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Adicionar produtos ao Gerenciador de canais | Selecione produtos do catálogo de produtos Commerce e importe-os para o Channel Manager. | **Até cinco minutos**-Se você selecionar muitos produtos, por exemplo, um catálogo de produtos inteiro, o processo de importação leva mais tempo. |
| Corresponder produtos em[!DNL Walmart Marketplace] | Selecione listas de produtos no Gerenciador de canais e envie para o Walmart para correspondência. | **Até 30 minutos**-Se você selecionar muitos produtos, o processo correspondente demorará mais, dependendo da quantidade selecionada. |
| Atualizações de inventário | Quando a quantidade do estoque for alterada no Commerce, [!DNL Channel Manager] sincroniza a atualização para o Walmart. | **Até 10 minutos** |
| Atualizações de preço | Quando um preço de produto muda, o Channel Manager sincroniza a atualização com o Walmart. | **Até cinco minutos** |
| Solicitar sincronizações do Walmart para o Commerce | O cliente solicita um produto comercial no Walmart Marketplace. O Walmart envia o pedido para o Gerenciador de Canais. A ordem é exibida no painel de ordem. | **Até 30 minutos** |
| Ordem criada no Commerce Order Management | O Gerenciador de Canais cria o pedido de Comércio a partir do pedido Walmart e atualiza o painel de pedidos para incluir o número do pedido de Comércio. | **Até cinco minutos** |

