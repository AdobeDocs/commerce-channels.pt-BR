---
title: '"Introdução ao [!DNL Channel Manager]'''
description: "Saiba como instalar e usar o [!DNL Channel Manager] integrar as lojas Adobe Commerce e Magento Open Source ao Walmart Marketplace e criar um canal de vendas para gerenciar as listagens, os preços, o inventário e as vendas do marketplace com facilidade através do Administrador de comércio."
role: Leader, Admin, User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 850aece134084e108b324a964d7d834042c7ddfd
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---


# Introdução ao [!DNL Channel Manager]

[!DNL Channel Manager] ajuda os comerciantes a aumentar as vendas, alcançar novos clientes, simplificar as operações de vendas e economizar tempo, integrando um catálogo de produtos Adobe Commerce ou Magento Open Source com o [!DNL Walmart Marketplace].

![[!DNL Channel Manager] exibição do administrador da extensão](assets/channel-manager-home.png){width="700" zoomable="yes"}

[!DNL Channel Manager] oferece suporte a comerciantes de Adobe Commerce ou Magento Open Source que desejam vender no [!DNL Walmart Marketplace] estendendo o [!DNL Commerce] Admin. Com [!DNL Channel Manager] instalados, os administradores de armazenamento e a equipe de operações podem gerenciar [!DNL Walmart Marketplace] vendas, inventário e preços de produtos perfeitamente no ambiente do Commerce.

O administrador estendido simplifica as operações, pois os comerciantes podem usar os mesmos fluxos de trabalho e processos para gerenciar vendas de ambos [!DNL Commerce] lojas e o Walmart Marketplace.

Depois de instalar e configurar [!DNL Channel Manager], você pode usar os seguintes recursos para gerenciar ordens de venda do Walmart Marketplace:

* **Gerenciamento de listas**-Conecte facilmente listas de produtos, combinando produtos de sua [!DNL Commerce] catálogo para existente [!DNL Walmart Marketplace] listagens.

* **Inventory management**-Os itens na conta de vendedor do marketplace do comerciante são sincronizados e atualizados automaticamente em [!DNL Commerce] para garantir níveis precisos de inventário.

* **Atualizações de preços**—Mantenha preços precisos para listagens de marketplace com sincronização automática de preços. Quando um preço muda no Adobe Commerce, as alterações são refletidas no mercado.

* **Gerenciamento de pedidos**—Quando novas ordens são criadas no marketplace, [!DNL Channel Manager] sincroniza pedidos com o Adobe Commerce e envia confirmações de pedidos para o marketplace. Essa confirmação garante que o inventário seja reservado para cada pedido. A etapa final é criar os pedidos correspondentes no [!DNL Commerce] Sistema do Order Management para processamento.

* **Gerenciamento de remessa**—Quando os pedidos são marcados como entregues no Adobe Commerce, a atualização da entrega é enviada para o [!DNL Walmart Marketplace]. Essa notificação garante que os vendedores atendam aos requisitos de SLA de atendimento e que os clientes recebam notificações de atualização de envio para seus pedidos atuais.

* **Cancelamentos**—Quando os pedidos são cancelados no Adobe Commerce, [!DNL Channel Manager] envia informações de ordem atualizadas para o marketplace para replicar a ação para a ordem de marketplace correspondente. Depois que o cancelamento do pedido for concluído, a [!DNL Commerce] as atualizações de quantidade de estoque para refletir os itens devolvidos e as atualizações de estoque são sincronizadas automaticamente para [!DNL Walmart Marketplace].

* **Devoluções e Reembolsos**—Quando o Walmart Marketplace solicita uma devolução de itens solicitados por meio do canal de vendas Adobe Commerce ou Magento Open Source, [!DNL Channel Manager] envia as informações da solicitação de devolução à loja do canal de vendas do Commerce para replicar a solicitação de devolução. Em seguida, o reembolso pode ser processado usando o [!DNL Commerce] [workflow de reembolso](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html#refund-workflow), método offline. Após a conclusão do reembolso, [!DNL Channel Manager] sincroniza a atualização para o Walmart para que o status de retorno na conta do vendedor do marketplace possa ser atualizado para refletir o reembolso.

## Latência esperada para [!DNL Channel Manager] operações

A sincronização de dados entre [!DNL Channel Manager] e um link [!DNL Walmart Marketplace] o armazenamento requer algum tempo para ser concluído. Revise o tempo de processamento esperado para [!DNL Channel Manager] operações para ajudar a planejar o trabalho das operações do canal de vendas.

**Latência estimada para [!DNL Channel Manager] operações**

| **Operação** | **Descrição** | **Atraso esperado** |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Adicionar produtos a [!DNL Channel Manager] | Selecione produtos da [!DNL Commerce] catálogo de produtos e importá-los para [!DNL Channel Manager]. | **Até cinco minutos**- Se você selecionar muitos produtos, por exemplo, um catálogo de produtos inteiro, o processo de importação levará mais tempo. |
| Combinar produtos em [!DNL Walmart Marketplace] | Selecionar listas de produtos em [!DNL Channel Manager] e enviar para o Walmart para correspondência. | **Até 30 minutos**-Se você selecionar muitos produtos, o processo de correspondência levará mais tempo, dependendo da quantidade selecionada. |
| Atualizações de inventário | Quando a quantidade do estoque for alterada no Commerce, [!DNL Channel Manager] sincroniza a atualização com o Walmart. | **Até 10 minutos** |
| Atualizações de preços | Quando o preço de um produto muda, [!DNL Channel Manager] sincroniza a atualização com o Walmart. | **Até cinco minutos** |
| Solicitar sincronizações de Walmart para [!DNL Commerce] | O cliente solicita uma [!DNL Commerce] produto no Walmart Marketplace. O Walmart envia o pedido para [!DNL Channel Manager]. A ordem é exibida no painel de ordens. | **Até 30 minutos** |
| Pedido criado em [!DNL Commerce] Order Management | [!DNL Channel Manager] cria o [!DNL Commerce] pedido do pedido do Walmart e atualiza o painel de pedidos para incluir o [!DNL Commerce] número do pedido. | **Até cinco minutos** |
| Atualização do status da remessa em [!DNL Commerce] Order Management | Quando um pedido é enviado do Commerce, [!DNL Channel Manager] atualiza o status do Envio no painel de pedidos e envia a atualização para o Walmart Marketplace para que o cliente possa ser notificado. | **Até cinco minutos** |
| Atualização de cancelamento de pedido no Commerce Order Management | Quando um pedido é cancelado no Commerce, [!DNL Channel Manager] atualiza o status do pedido no painel de pedidos e envia a atualização para o Walmart marketplace para que o cliente possa ser notificado. Depois que o cancelamento do pedido for concluído, a [!DNL Commerce] atualizações de quantidade de estoque para refletir os itens devolvidos. Em seguida, [!DNL Channel Manager] sincroniza a atualização com o [!DNL Walmart Marketplace]. | **Até cinco minutos** |


