---
title: Atualizações de Estoque e Preço
description: '[!DNL Channel Manager] sincroniza atualizações de preço e estoque entre a [!DNL Commerce] loja e a [!DNL Walmart Marketplace] loja para que você possa gerenciar suas operações de canal de vendas pelo [!DNL Commerce] Administrador'
feature: Sales Channels, Merchandising, Inventory, Tools and External Services
role: Leader, Admin, User
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Atualizar Estoque e Preços

O [!DNL Channel Manager] controla o estoque e os preços dos produtos no catálogo de produtos [!DNL Commerce] e sincroniza as atualizações para o canal de vendas conectado e o [!DNL Walmart Marketplace]. A operação de sincronização garante que as listagens de produtos reflitam a quantidade e o preço de estoque atuais.


>[!IMPORTANT]
>
>Depois que o [!DNL Channel Manager] for instalado e configurado, todas as atualizações de inventário, preço e pedido serão sincronizadas automaticamente. Se você já vende no Walmart Marketplace, desative todas as outras integrações que atualizam os dados do produto e do pedido. Em seguida, verifique se os níveis de estoque e os preços na loja [!DNL Commerce] estão precisos e se correspondem aos dados em [!DNL Walmart Marketplace] antes de conectar [!DNL Channel Manager] à loja do marketplace live.


## Atualizações de inventário

Quando os níveis de estoque do produto mudam no [!DNL Commerce], o [!DNL Channel Manager] sincroniza atualizações para o [!DNL Walmart Marketplace]. Pode levar até 10 minutos para que as atualizações de estoque sejam sincronizadas entre o canal de vendas e o [!DNL Walmart marketplace].

* **Atualizações na quantidade em estoque no catálogo de produtos**—Quando [!DNL Commerce] a quantidade em estoque é alterada devido a [alterações manuais na quantidade em estoque](https://experienceleague.adobe.com/docs/commerce-admin/inventory/quantities/quantities-assign-per-product.html), reembolsos ou cancelamentos, o [!DNL Channel Manager] sincroniza a alteração com os canais conectados e o [!DNL Walmart Marketplace].

* **Reduzir quantidade de estoque para refletir [!DNL Walmart Marketplace] pedidos**—Depois que um pedido de [!DNL Walmart Marketplace] é sincronizado com [!DNL Channel Manager], [!DNL Channel Manager] envia a atualização para o sistema de pedidos [!DNL Commerce]. [!DNL Commerce] ajusta as quantidades de estoque com base no pedido. Em seguida, a quantidade atualizada é sincronizada com [!DNL Walmart Marketplace]. Até que as operações de sincronização sejam concluídas, você poderá ver quantidades diferentes nas listagens de canais de vendas e [!DNL Walmart].

>[!IMPORTANT]
>
>Depois que um pedido de [!DNL Walmart Marketplace] é sincronizado com [!DNL Channel Manager], quantidades de estoque e informações de pedido são atualizadas apenas para reembolsos e cancelamentos iniciados a partir de [!DNL Commerce]. Se um pedido for reembolsado ou cancelado em [!DNL Walmart marketplace], processe a alteração de [!DNL Commerce] para garantir a precisão de [!DNL Commerce] quantidades de estoque e informações do pedido.

## Atualizações de preços

Quando o preço do produto muda em [!DNL Commerce], o [!DNL Channel Manager] sincroniza a atualização para o [!DNL Walmart Marketplace]. Pode levar até cinco minutos para que a alteração de preço seja exibida na lista [!DNL Walmart Marketplace].

### Gerenciar preços de um produto conectado

1. Em [!UICONTROL Admin], selecione **[!UICONTROL Catalog > Products]**.
1. Na grade de produtos, encontre o produto a ser atualizado e selecione **[!UICONTROL Edit]**.
1. Revise e atualize o preço conforme necessário.
1. **[!UICONTROL Save]** a alteração.

Para obter ajuda sobre como gerenciar a configuração de preço do produto em [!DNL Commerce], consulte [Gerenciar Preços](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html).
