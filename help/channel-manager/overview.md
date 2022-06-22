---
title: '''Sobre [!DNL Channel Manager]'''
description: '"Saiba como instalar e usar [!DNL Channel Manager] para integrar a Adobe Commerce e as Magento Open Source stores aos mercados de terceiros e criar um canal de vendas para gerenciar as listas, os preços, o inventário e as vendas do Marketplace de forma simples do seu administrador comercial.'
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 8146be1c94ffb1c8abd0d28e53d3476fd78f2c62
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---


# Sobre [!DNL Channel Manager]

[!DNL Channel Manager] ajuda os comerciantes a aumentar as vendas, alcançar novos clientes, simplificar as operações de vendas e economizar tempo integrando um catálogo de produtos Adobe Commerce ou Magento Open Source com a [!DNL Walmart Marketplace].

![[!DNL Channel Manager] visualização de administração de extensão](assets/channel-manager-home.png)

[!DNL Channel Manager] O suporta comerciantes Adobe Commerce ou Magento Open Source que desejam vender [!DNL Walmart Marketplace] alargando a [!DNL Commerce] Administrador Com [!DNL Channel Manager] instalado, os administradores de armazenamento e a equipe de operações podem gerenciar [!DNL Walmart Marketplace] vendas, inventário e preços do produto perfeitamente no ambiente de Comércio.

O Administrador estendido simplifica as operações, pois os comerciantes podem usar os mesmos fluxos de trabalho e processos para gerenciar as vendas de ambos [!DNL Commerce] loja e o Walmart.

Depois de instalar e configurar [!DNL Channel Manager], você pode usar os seguintes recursos para gerenciar os pedidos de vendas do Walmart Marketplace:

* **Gerenciamento de listagem**-Conecte facilmente as listas de produtos ao combinar produtos da sua [!DNL Commerce] catálogo para existente [!DNL Walmart Marketplace] listagens.

* **Inventory management**-Os itens na conta do vendedor do marketplace do comerciante são sincronizados e atualizados automaticamente de [!DNL Commerce] para assegurar níveis exatos de inventário.

* **Atualizações de preços**- Mantenha preços precisos para listagens de marketplace com sincronização automática de preços. Quando um preço muda no Adobe Commerce, as alterações são refletidas no mercado.

* **Gerenciamento de pedidos**- Quando novos pedidos são criados em um mercado, [!DNL Channel Manager] sincroniza pedidos com o Adobe Commerce e envia confirmações de pedido ao marketplace. Este reconhecimento garante que o inventário seja reservado para cada pedido. A etapa final é criar os pedidos correspondentes na [!DNL Commerce] Sistema de gerenciamento de pedidos para processamento.

* **Gestão de remessa**-Quando os pedidos são marcados como entregues na Adobe Commerce, a atualização de remessa é enviada para a [!DNL Walmart Marketplace]. Essa notificação garante que os vendedores atendam aos requisitos de SLA de cumprimento e que os clientes recebam notificações de atualização de envio para seus pedidos atuais.

* **Cancelamentos**- Quando os pedidos são cancelados no Adobe Commerce, [!DNL Channel Manager] envia informações atualizadas do pedido para o marketplace para replicar a ação da ordem do marketplace correspondente. Depois que o cancelamento do pedido for concluído, a variável [!DNL Commerce] as atualizações de quantidade de estoque para refletir os itens retornados e as atualizações de inventário são sincronizadas automaticamente para [!DNL Walmart Marketplace].

## Latência esperada para [!DNL Channel Manager] operações

Os processos de sincronização de dados entre [!DNL Channel Manager] e um link [!DNL Walmart Marketplace] a loja requer algum tempo para ser concluída. Revise o tempo de processamento esperado para [!DNL Channel Manager] operações para ajudar a planejar o funcionamento das operações do canal de vendas.

**Latência estimada para [!DNL Channel Manager] operações**

| **Operação** | **Descrição** | **Atraso esperado** |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Adicionar produtos ao [!DNL Channel Manager] | Selecione produtos da [!DNL Commerce] catálogo de produtos e importá-los para [!DNL Channel Manager]. | **Até cinco minutos**-Se você selecionar muitos produtos, por exemplo, um catálogo de produtos inteiro, o processo de importação leva mais tempo. |
| Corresponder produtos em [!DNL Walmart Marketplace] | Selecione listas de produtos em [!DNL Channel Manager] e envie para Walmart para correspondência. | **Até 30 minutos**-Se você selecionar muitos produtos, o processo correspondente demorará mais, dependendo da quantidade selecionada. |
| Atualizações de inventário | Quando a quantidade do estoque for alterada no Commerce, [!DNL Channel Manager] sincroniza a atualização para o Walmart. | **Até 10 minutos** |
| Atualizações de preço | Quando o preço de um produto muda, [!DNL Channel Manager] sincroniza a atualização para o Walmart. | **Até cinco minutos** |
| Solicitar sincronizações do Walmart para o [!DNL Commerce] | Ordens de cliente a [!DNL Commerce] produto no Walmart Marketplace. O Walmart envia o pedido para [!DNL Channel Manager]. A ordem é exibida no painel de ordem. | **Até 30 minutos** |
| Ordem criada em [!DNL Commerce] Gerenciamento de pedidos | [!DNL Channel Manager] cria o [!DNL Commerce] solicitar a partir do pedido Walmart e atualizar o painel de pedidos para incluir o [!DNL Commerce] número do pedido. | **Até cinco minutos** |
| Atualização do status da remessa em [!DNL Commerce] Gerenciamento de pedidos | Quando um pedido é enviado do Commerce, [!DNL Channel Manager] atualiza o status Shipping no painel de pedidos e envia a atualização para o Walmart para que o cliente possa ser notificado. | **Até cinco minutos** |
| Atualização de cancelamento de pedido no Commerce Order Management | Quando um pedido é cancelado do Commerce, [!DNL Channel Manager] atualiza o status do pedido no painel de pedidos e envia a atualização para o supermercado Walmart para que o cliente possa ser notificado. Depois que o cancelamento do pedido for concluído, a variável [!DNL Commerce] atualizações de quantidade de estoque para refletir os itens retornados. Então, [!DNL Channel Manager] sincroniza a atualização com o [!DNL Walmart Marketplace]. | **Até cinco minutos** |


