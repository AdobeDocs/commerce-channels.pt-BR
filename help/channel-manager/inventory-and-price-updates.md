---
title: Atualizações de inventário e preço
description: '[!DNL Channel Manager] sincroniza atualizações de inventário e preço entre o [!DNL Commerce] armazenar e [!DNL Walmart Marketplace] para que você possa gerenciar suas operações de canal de vendas na [!DNL Commerce] Admin'
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Atualizar inventário e preços

[!DNL Channel Manager] acompanha o inventário e os preços de produtos na [!DNL Commerce] catálogo de produtos e sincroniza atualizações ao canal de vendas conectado e [!DNL Walmart Marketplace]. A operação de sincronização garante que as listas de produtos reflitam a quantidade e o preço atuais do estoque.


>[!IMPORTANT]
>
>Depois [!DNL Channel Manager] estiver instalado e configurado, todas as atualizações de inventário, preço e pedido serão sincronizadas automaticamente. Se você já vende no Walmart Marketplace, desative quaisquer outras integrações que atualizem o produto e solicitem os dados. Em seguida, verifique se os níveis de estoque de inventário e os preços no [!DNL Commerce] a loja é precisa e corresponde aos dados em [!DNL Walmart Marketplace] antes de se conectar [!DNL Channel Manager] para a loja de mercados em tempo real.


## Atualizações de inventário

Quando os níveis de estoque do produto mudam em [!DNL Commerce], [!DNL Channel Manager] sincroniza atualizações no [!DNL Walmart Marketplace]. Pode levar até 10 minutos para que as atualizações de inventário sejam sincronizadas no canal de vendas com a [!DNL Walmart marketplace].

* **Atualizações da quantidade de estoque no catálogo de produtos**—Quando [!DNL Commerce] a quantidade de estoque é alterada devido a [alterações manuais na quantidade de estoque](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html), reembolsos ou anulações, [!DNL Channel Manager] sincroniza a alteração em canais conectados e [!DNL Walmart Marketplace].

* **Reduza a quantidade de estoque para refletir [!DNL Walmart Marketplace] ordens**—Após uma [!DNL Walmart Marketplace] ordenar sincronizações para [!DNL Channel Manager], [!DNL Channel Manager] envia a atualização para o [!DNL Commerce] sistema de pedido. [!DNL Commerce] ajusta as quantidades de estoque com base no pedido. Em seguida, a quantidade atualizada é sincronizada com [!DNL Walmart Marketplace]. Até que as operações de sincronização sejam concluídas, você poderá ver quantidades diferentes nas listas de canais de vendas e [!DNL Walmart].

>[!IMPORTANT]
>
>Depois de um [!DNL Walmart Marketplace] ordenar sincronizações para [!DNL Channel Manager], as quantidades de inventário e as informações sobre a encomenda são atualizadas apenas para as restituições e anulações iniciadas a partir de [!DNL Commerce]. Se uma ordem for reembolsada ou cancelada da [!DNL Walmart marketplace], processe a alteração de [!DNL Commerce] para garantir a exatidão [!DNL Commerce] quantidades de inventário e informações do pedido.

## Atualizações de preço

Quando o preço do produto muda em [!DNL Commerce], [!DNL Channel Manager] sincroniza a atualização com o [!DNL Walmart Marketplace]. Pode levar até cinco minutos para que a alteração de preço seja exibida na variável [!DNL Walmart Marketplace] listagem.

### Gerenciar preços de um produto conectado

1. No [!UICONTROL Admin], selecione **[!UICONTROL Catalog > Products]**.
1. Na grade do produto, localize o produto a ser atualizado e selecione **[!UICONTROL Edit]**.
1. Revise e atualize o preço conforme necessário.
1. **[!UICONTROL Save]** a mudança.

Para obter ajuda com o gerenciamento da configuração de preço do produto em [!DNL Commerce], consulte [Gerenciar Preços](https://docs.magento.com/user-guide/catalog/pricing.html){target="_blank"}.
