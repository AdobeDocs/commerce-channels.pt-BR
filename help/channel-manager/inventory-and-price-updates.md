---
title: Atualizações de Estoque e Preço
description: '[!DNL Channel Manager] sincroniza atualizações de inventário e preço entre a [!DNL Commerce] armazenar e [!DNL Walmart Marketplace] para gerenciar suas operações de canal de vendas na [!DNL Commerce] Administrador'
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# Atualizar Estoque e Preços

[!DNL Channel Manager] rastreia o inventário e os preços dos produtos na [!DNL Commerce] catálogo de produtos e sincroniza atualizações para o canal de vendas conectado e [!DNL Walmart Marketplace]. A operação de sincronização garante que as listagens de produtos reflitam a quantidade e o preço de estoque atuais.


>[!IMPORTANT]
>
>Depois [!DNL Channel Manager] O está instalado e configurado, todas as atualizações de inventário, preço e pedido são sincronizadas automaticamente. Se você já vende no Walmart Marketplace, desative todas as outras integrações que atualizam os dados do produto e do pedido. Em seguida, verifique se os níveis de estoque e os preços no [!DNL Commerce] as vitrines são precisas e correspondem aos dados em [!DNL Walmart Marketplace] antes de se conectar [!DNL Channel Manager] à loja do live marketplace.


## Atualizações de inventário

Quando os níveis de estoque do produto mudam em [!DNL Commerce], [!DNL Channel Manager] sincroniza atualizações para o [!DNL Walmart Marketplace]. Pode levar até 10 minutos para que as atualizações de inventário sejam sincronizadas entre o canal de vendas e o [!DNL Walmart marketplace].

* **Atualizações da quantidade de estoque no catálogo de produtos**— When [!DNL Commerce] a quantidade em estoque mudou devido a [alterações manuais na quantidade de estoque](https://experienceleague.adobe.com/docs/commerce-admin/inventory/quantities/quantities-assign-per-product.html), reembolsos ou cancelamentos, [!DNL Channel Manager] sincroniza a alteração para canais conectados e [!DNL Walmart Marketplace].

* **Reduzir quantidade em estoque para refletir [!DNL Walmart Marketplace] pedidos**—Depois de um [!DNL Walmart Marketplace] ordenar sincronizações para [!DNL Channel Manager], [!DNL Channel Manager] envia a atualização para o [!DNL Commerce] sistema de pedidos. [!DNL Commerce] ajusta as quantidades de estoque com base na ordem. Em seguida, a quantidade atualizada é sincronizada com [!DNL Walmart Marketplace]. Até que as operações de sincronização sejam concluídas, você poderá ver quantidades diferentes nas listagens de canais de vendas e [!DNL Walmart].

>[!IMPORTANT]
>
>Depois de um [!DNL Walmart Marketplace] ordenar sincronizações para [!DNL Channel Manager], as quantidades de inventário e as informações de pedido são atualizadas apenas para restituições e cancelamentos iniciados em [!DNL Commerce]. Se um pedido for reembolsado ou cancelado na [!DNL Walmart marketplace], processar a alteração de [!DNL Commerce] para garantir a exatidão das [!DNL Commerce] quantidades de inventário e informações sobre a ordem.

## Atualizações de preços

Quando o preço do produto muda em [!DNL Commerce], [!DNL Channel Manager] sincroniza a atualização com o [!DNL Walmart Marketplace]. Pode levar até cinco minutos para que a alteração de preço seja exibida no [!DNL Walmart Marketplace] listagem.

### Gerenciar preços de um produto conectado

1. No [!UICONTROL Admin], selecione **[!UICONTROL Catalog > Products]**.
1. Na grade de produtos, encontre o produto a ser atualizado e selecione **[!UICONTROL Edit]**.
1. Revise e atualize o preço conforme necessário.
1. **[!UICONTROL Save]** a alteração.

Para obter ajuda com o gerenciamento da configuração de preço do produto no [!DNL Commerce], consulte [Gerenciar preços](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html).
