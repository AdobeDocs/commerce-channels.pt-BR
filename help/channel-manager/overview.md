---
title: 'Introdução a  [!DNL Channel Manager]'
description: "Saiba como instalar e usar o  [!DNL Channel Manager] para integrar lojas Adobe Commerce e Magento Open Source com o Walmart Marketplace e criar um canal de vendas para gerenciar listas, preços, estoque e vendas do marketplace de forma contínua com o Administrador do Commerce."
role: Leader, Admin, User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 850aece134084e108b324a964d7d834042c7ddfd
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---


# Introdução ao [!DNL Channel Manager]

O [!DNL Channel Manager] ajuda os comerciantes a aumentar as vendas, alcançar novos clientes, otimizar as operações de vendas e economizar tempo, integrando um catálogo de produtos Adobe Commerce ou Magento Open Source ao [!DNL Walmart Marketplace].

![[!DNL Channel Manager] exibição de administrador da extensão](assets/channel-manager-home.png){width="700" zoomable="yes"}

O [!DNL Channel Manager] oferece suporte a comerciantes de Adobe Commerce ou Magento Open Source que desejam vender em [!DNL Walmart Marketplace] estendendo o Administrador [!DNL Commerce]. Com o [!DNL Channel Manager] instalado, os administradores de loja e a equipe de operações podem gerenciar vendas, estoque e preços de produtos do [!DNL Walmart Marketplace] perfeitamente no ambiente do Commerce.

O Administrador estendido simplifica as operações porque os comerciantes podem usar os mesmos fluxos de trabalho e processos para gerenciar vendas de [!DNL Commerce] vitrines e do Walmart Marketplace.

Depois de instalar e configurar o [!DNL Channel Manager], você poderá usar os seguintes recursos para gerenciar ordens de venda do Walmart Marketplace:

* **Gerenciamento de listas** - Conecte facilmente listas de produtos, associando produtos do seu catálogo [!DNL Commerce] a listas [!DNL Walmart Marketplace] existentes.

* **Inventory management**-Os itens na conta de vendedor do marketplace do comerciante são sincronizados e atualizados automaticamente de [!DNL Commerce] para garantir níveis de estoque precisos.

* **Atualizações de preços**—Mantenha preços precisos para as listagens de marketplace com sincronização automática de preços. Quando um preço muda no Adobe Commerce, as alterações são refletidas no mercado.

* **Gerenciamento de pedidos** — Quando novos pedidos são criados no marketplace, [!DNL Channel Manager] sincroniza pedidos com o Adobe Commerce e envia confirmações de pedidos para o marketplace. Essa confirmação garante que o inventário seja reservado para cada pedido. A etapa final é criar os pedidos correspondentes no sistema Order Management [!DNL Commerce] para processamento.

* **Gerenciamento de remessa**—Quando os pedidos são marcados como remetidos na Adobe Commerce, a atualização da remessa é enviada para [!DNL Walmart Marketplace]. Essa notificação garante que os vendedores atendam aos requisitos de SLA de atendimento e que os clientes recebam notificações de atualização de envio para seus pedidos atuais.

* **Cancelamentos** — Quando os pedidos são cancelados no Adobe Commerce, [!DNL Channel Manager] envia informações atualizadas sobre o pedido ao marketplace para replicar a ação para o pedido do marketplace correspondente. Após a conclusão do cancelamento do pedido, as [!DNL Commerce] atualizações de quantidade em estoque para refletir os itens devolvidos e as atualizações de estoque são sincronizadas automaticamente para [!DNL Walmart Marketplace].

* **Devoluções e Reembolsos**—Quando o Walmart Marketplace solicita uma devolução de itens solicitados através do canal de vendas Adobe Commerce ou Magento Open Source, o [!DNL Channel Manager] envia as informações da solicitação de devolução ao armazenamento do canal de vendas Commerce para replicar a solicitação de devolução. Em seguida, o reembolso pode ser processado usando o [!DNL Commerce] [fluxo de trabalho de reembolso](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html#refund-workflow), método offline. Após a conclusão do reembolso, [!DNL Channel Manager] sincroniza a atualização para o Walmart para que o status do retorno na conta de vendedor do marketplace possa ser atualizado para refletir o reembolso.

## Latência esperada para [!DNL Channel Manager] operações

Os processos de sincronização de dados entre [!DNL Channel Manager] e um repositório [!DNL Walmart Marketplace] vinculado exigem algum tempo para serem concluídos. Revise o tempo de processamento esperado para [!DNL Channel Manager] operações para ajudar a planejar o trabalho das operações do canal de vendas.

**Latência estimada para [!DNL Channel Manager] operações**

| **Operação** | **Descrição** | **Atraso esperado** |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Adicionar produtos a [!DNL Channel Manager] | Selecione produtos do catálogo de produtos [!DNL Commerce] e importe-os para [!DNL Channel Manager]. | **Até cinco minutos**-Se você selecionar muitos produtos, por exemplo, um catálogo de produtos inteiro, o processo de importação levará mais tempo. |
| Combinar produtos em [!DNL Walmart Marketplace] | Selecione as listas de produtos em [!DNL Channel Manager] e envie para o Walmart para correspondência. | **Até 30 minutos**-Se você selecionar muitos produtos, o processo de correspondência levará mais tempo, dependendo da quantidade selecionada. |
| Atualizações de inventário | Quando a quantidade do estoque é alterada no Commerce, o [!DNL Channel Manager] sincroniza a atualização com o Walmart. | **Até 10 minutos** |
| Atualizações de preços | Quando o preço de um produto muda, o [!DNL Channel Manager] sincroniza a atualização com o Walmart. | **Até cinco minutos** |
| Solicitar sincronizações do Walmart para [!DNL Commerce] | O cliente solicita um produto [!DNL Commerce] no Walmart Marketplace. O Walmart envia o pedido para [!DNL Channel Manager]. A ordem é exibida no painel de ordens. | **Até 30 minutos** |
| Pedido criado em [!DNL Commerce] Order Management | [!DNL Channel Manager] cria o pedido [!DNL Commerce] a partir do pedido do Walmart e atualiza o painel de pedidos para incluir o número do pedido [!DNL Commerce]. | **Até cinco minutos** |
| Atualização do status de envio no Order Management [!DNL Commerce] | Quando um pedido é enviado pela Commerce, o [!DNL Channel Manager] atualiza o status do Envio no painel de pedidos e envia a atualização para o Walmart Marketplace para que o cliente possa ser notificado. | **Até cinco minutos** |
| Atualização do cancelamento de pedido no Commerce Order Management | Quando um pedido é cancelado no Commerce, [!DNL Channel Manager] atualiza o status do pedido no painel de pedidos e envia a atualização para o Walmart Marketplace para que o cliente possa ser notificado. Após a conclusão do cancelamento do pedido, a quantidade em estoque de [!DNL Commerce] é atualizada para refletir os itens devolvidos. Em seguida, [!DNL Channel Manager] sincroniza a atualização para o [!DNL Walmart Marketplace]. | **Até cinco minutos** |


