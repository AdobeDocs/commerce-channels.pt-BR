---
title: Atualizações de inventário e preço
description: '"[!DNL Channel Manager] sincroniza atualizações de inventário e preço entre a loja do Commerce e [!DNL Walmart Marketplace] para gerenciar suas operações de canal de vendas com o administrador de comércio"'
source-git-commit: 2a9bd2f8f91e672786c36f5e132f99bcab59dd00
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---


# Atualizações de inventário e preço

O Channel Manager rastreia o inventário e os preços de produtos publicados e sincroniza as alterações no Channel Manager e no Walmart Marketplace para refletir a quantidade atual de estoque e os preços nas listas de produtos.**

## Atualizações de inventário

Quando os níveis de inventário mudam, o Gerenciador de Canais sincroniza atualizações entre o catálogo de produtos do Commerce e o Walmart Marketplace para que o Gerenciador de Canais e o Walmart Marketplace exibam a quantidade de estoque atual.

Pode levar até 5 minutos para que as alterações de inventário sejam exibidas no Gerenciador de canais e no Walmart Marketplace.

* **Atualizações da quantidade de estoque no catálogo de produtos**- Se a quantidade de estoque do Commerce for alterada para um produto vendido no Walmart por causa de um [alteração manual da quantidade de estoque](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html) Para reembolso ou cancelamento de pedidos, o Gerenciador de Canais sincroniza a alteração no canal de vendas conectado e na variável [!DNL Walmart Marketplace].

* **Reduza a quantidade de estoque para refletir os pedidos do Walmart Marketplace**-Depois que um pedido do Walmart é sincronizado com o Gerenciador de canais, o Gerenciador de canais envia a atualização para o sistema de pedidos do Commerce. O Commerce ajusta as quantidades de estoque com base no pedido. Em seguida, a quantidade atualizada é sincronizada com o Walmart Marketplace. pode haver algumas diferenças na quantidade de estoque mostradas no Gerenciador de canais e no Marketplace até que as operações de sincronização sejam concluídas.

>[!IMPORTANT]
>
> Depois que um pedido do Walmart é sincronizado com o Gerenciador de Canais, as quantidades de inventário e outras informações de processamento de pedidos são atualizadas somente para reembolsos e cancelamentos iniciados do Commerce. Se um pedido for reembolsado ou cancelado do Walmart Marketplace, processe a alteração do Commerce para garantir que as quantidades do inventário do Commerce e as informações do pedido sejam precisas.

## Atualizações de preço

Quando o preço do produto muda no Commerce, o Channel Manager sincroniza a atualização do catálogo de produtos do Commerce para o Walmart Marketplace. Pode levar até 5 minutos para que as alterações de inventário sejam exibidas.

### Gerenciar preços de um produto publicado

1. No [!UICONTROL Admin], selecione **[!UICONTROL Catalog > Products]**.
1. Na grade do produto, localize o produto a ser atualizado e selecione **[!UICONTROL Edit]**.
1. Revise e atualize o preço conforme necessário.
1. **[!UICONTROL Save]** a mudança.

O Gerenciador de Canais sincroniza todas as atualizações de preço no armazenamento de canais e [!DNL Walmart Marketplace]. Essa operação pode levar até 5 minutos.

Para obter detalhes sobre como gerenciar a configuração de preço do produto no Commerce, consulte [Gerenciar Preços](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}.
