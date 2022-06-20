---
title: '"Sobre [!DNL Channel Manager]"'
description: '"Saiba como instalar e usar o [!DNL Channel Manager] para integrar a Adobe Commerce e as Magento Open Source stores aos mercados de terceiros e criar um canal de vendas para gerenciar as listas, os preços, o inventário e as vendas do Marketplace de forma simples do seu administrador comercial."'
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 690eeb5d03b23cac11f3c14b04601c514c76e0bd
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Sobre [!DNL Channel Manager]

[!DNL Channel Manager] ajuda os comerciantes a aumentar as vendas, alcançar novos clientes, simplificar as operações de vendas e economizar tempo integrando um catálogo de produtos Adobe Commerce ou Magento Open Source com a [!DNL Walmart Marketplace].

![[!DNL Channel Manager] visualização de administração de extensão](assets/channel-manager-home.png)

[!DNL Channel Manager] O suporta comerciantes Adobe Commerce ou Magento Open Source que desejam vender [!DNL Walmart Marketplace] alargando a [!DNL Commerce] Administrador com recursos para gerenciar [!DNL Walmart Marketplace] vendas, inventário e preços do produto perfeitamente no ambiente de Comércio.

O Administrador estendido simplifica as operações, pois os comerciantes podem usar os mesmos fluxos de trabalho e processos para gerenciar as vendas tanto das vitrines do Commerce quanto do Walmart Marketplace.

Depois de instalar e configurar [!DNL Channel Manager], você pode usar os seguintes recursos para gerenciar os pedidos de vendas do Walmart Marketplace:

* **Gerenciamento de listagem**-Conecte facilmente as listas de produtos ao combinar produtos da sua [!DNL Commerce] catálogo para existente [!DNL Walmart Marketplace] listagens.

* **Inventory management**-Os itens na conta do vendedor do comerciante são sincronizados e atualizados automaticamente do Commerce para garantir níveis precisos de inventário.

* **Atualizações de preços**- Mantenha preços precisos para listagens de marketplace com sincronização automática de preços. Quando um preço muda no Adobe Commerce, as alterações são refletidas no mercado.

* **Gerenciamento de pedidos**- Quando novos pedidos são criados em um mercado, [!DNL Channel Manager] sincroniza pedidos com o Adobe Commerce, envia confirmações de pedido ao marketplace para garantir que o inventário seja reservado para cada pedido e cria uma ordem correspondente no sistema de gerenciamento de pedidos de comércio para processamento.

* **Gestão de remessa**-Quando os pedidos são marcados como entregues na Adobe Commerce, a atualização de remessa é enviada para a [!DNL Walmart Marketplace]. Essa notificação garante que os vendedores atendam aos requisitos de SLA de cumprimento e que os clientes recebam notificações de atualização de envio para seus pedidos atuais.

* **Cancelamentos**- Quando os pedidos são cancelados no Adobe Commerce, [!DNL Channel Manager] envia informações atualizadas do pedido para o marketplace para replicar a ação da ordem do marketplace correspondente.  Depois que o cancelamento do pedido for concluído, a variável [!DNL Commerce] as atualizações de quantidade de estoque para refletir os itens retornados e as atualizações de inventário são sincronizadas automaticamente para [!DNL Walmart Marketplace].

## Latência esperada para [!DNL Channel Manager] operações

Os processos de sincronização de dados entre [!DNL Channel Manager] e um link [!DNL Walmart Marketplace] a loja requer algum tempo para ser concluída. Revise o tempo de processamento esperado para [!DNL Channel Manager] operações para ajudar a planejar o funcionamento das operações do canal de vendas.

**Latência estimada para [!DNL Channel Manager] operações**

| **Operação** | **Descrição** | **Atraso esperado** |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Adicionar produtos ao [!DNL Channel Manager] | Selecione produtos do catálogo de produtos do Commerce e importe-os para [!DNL Channel Manager]. | **Até cinco minutos**-Se você selecionar muitos produtos, por exemplo, um catálogo de produtos inteiro, o processo de importação leva mais tempo. |
| Corresponder produtos em [!DNL Walmart Marketplace] | Selecione listas de produtos em [!DNL Channel Manager] e envie para Walmart para correspondência. | **Até 30 minutos**-Se você selecionar muitos produtos, o processo correspondente demorará mais, dependendo da quantidade selecionada. |
| Atualizações de inventário | Quando a quantidade do estoque for alterada no Commerce, [!DNL Channel Manager] sincroniza a atualização para o Walmart. | **Até 10 minutos** |
| Atualizações de preço | Quando o preço de um produto muda, [!DNL Channel Manager] sincroniza a atualização para o Walmart. | **Até cinco minutos** |
| Solicitar sincronizações do Walmart para o Commerce | O cliente solicita um produto comercial no Walmart Marketplace. O Walmart envia o pedido para [!DNL Channel Manager]. A ordem é exibida no painel de ordem. | **Até 30 minutos** |
| Ordem criada no Commerce Order Management | [!DNL Channel Manager] O cria a ordem de comércio a partir do pedido Walmart e atualiza o painel de pedidos para incluir o número de pedido de comércio. | **Até cinco minutos** |
| Atualização do status da remessa no Commerce Order Management | Quando um pedido é enviado do Commerce, [!DNL Channel Manager] atualiza o status Shipping no painel de pedidos e envia a atualização para o Walmart para que o cliente possa ser notificado. | **Até cinco minutos** |
| Atualização de cancelamento de pedido no Commerce Order Management | Quando um pedido é cancelado do Commerce, [!DNL Channel Manager] atualiza o status do pedido no painel de pedidos e envia a atualização para o supermercado Walmart para que o cliente possa ser notificado. Depois que o cancelamento do pedido for concluído, a variável [!DNL Commerce] atualizações de quantidade de estoque para refletir os itens retornados. Então, [!DNL Channel Manager] sincroniza a atualização com o [!DNL Walmart Marketplace]. | **Até cinco minutos** |


