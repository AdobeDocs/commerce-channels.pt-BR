---
title: Atualizações de inventário e preço
description: '''[!DNL Channel Manager] sincroniza atualizações de inventário e preço entre a loja do Commerce e [!DNL Walmart Marketplace] para que você possa gerenciar suas operações de canal de vendas com o administrador de comércio'''
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: a1944052f02968c36495275cd5ddfb2ca43ce967
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Atualizações de inventário e preço

[!DNL Channel Manager] rastreia inventário e preços de produtos na loja de canais. Quando o inventário ou o preço são alterados, as atualizações são sincronizadas com ambos [!DNL Channel Manager] e [!DNL Walmart Marketplace] para refletir a quantidade de estoque atual e o preço nas listas de produtos.

## Atualizações de inventário

Quando os níveis de inventário mudam, o Gerenciador de Canais sincroniza atualizações entre o Commerce e o Walmart Marketplace para garantir que o Gerenciador de Canais e o Walmart Marketplace tenham a quantidade de estoque correta.

Pode levar até 10 minutos para que as atualizações de inventário sejam sincronizadas no Gerenciador de canais e no mercado.

* **Atualizações da quantidade de estoque no catálogo de produtos**-Quando a quantidade de estoque do Commerce for alterada por causa de [alterações manuais na quantidade de estoque](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html), reembolsos ou cancelamentos, o Gerenciador de Canais sincroniza a alteração em canais conectados e [!DNL Walmart Marketplace].

* **Reduza a quantidade de estoque para refletir os pedidos do Walmart Marketplace**-Depois que um pedido do Walmart é sincronizado com o Gerenciador de canais, o Gerenciador de canais envia a atualização para o sistema de pedidos do Commerce. O Commerce ajusta as quantidades de estoque com base no pedido. Em seguida, a quantidade atualizada é sincronizada com o Walmart Marketplace. Até que as operações de sincronização sejam concluídas, você poderá ver diferenças de quantidade entre o Gerenciador de canais e o Marketplace.

>[!IMPORTANT]
>
> Depois que um pedido do Walmart é sincronizado com o Gerenciador de Canais, as quantidades de inventário e as informações do pedido são atualizadas somente para reembolsos e cancelamentos iniciados do Commerce. Se um pedido for reembolsado ou cancelado do Walmart Marketplace, processe a alteração do Commerce para garantir a precisão das quantidades de inventário e informações do pedido do Commerce.

## Atualizações de preço

Quando o preço do produto muda no Commerce, o Channel Manager sincroniza a atualização do [!DNL Commerce] catálogo de produtos para [!DNL Walmart Marketplace]. Pode levar até cinco minutos para que o mercado exiba as alterações de preço.

### Gerenciar preços de um produto publicado

1. No [!UICONTROL Admin], selecione **[!UICONTROL Catalog > Products]**.
1. Na grade do produto, localize o produto a ser atualizado e selecione **[!UICONTROL Edit]**.
1. Revise e atualize o preço conforme necessário.
1. **[!UICONTROL Save]** a mudança.

Para obter detalhes sobre como gerenciar a configuração de preço do produto no Commerce, consulte [Gerenciar Preços](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}.
