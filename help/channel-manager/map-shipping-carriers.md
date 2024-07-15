---
title: Mapear Transportadoras
description: '"Mapear atributos para correspondência [DNL! Commerce] para  [!DNL Walmart Marketplace] listagens existentes e sincronização de dados entre  [!DNL Channel Manager] e [!DNL Walmart].'''
role: Admin
feature: Sales Channels, Configuration, Shipping/Delivery
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Mapear Transportadoras

Antes de [processar remessas de pedidos](process-orders.md#ship-an-order) para [!DNL Walmart Marketplace] pedidos, mapeie as transportadoras preferenciais do Walmart para a transportadora correspondente em [!DNL Commerce] para que os dados de remessa possam ser sincronizados entre [!DNL Walmart] e [!DNL Commerce].

As transportadoras da Commerce que não mapeiam para uma transportadora preferencial são rotuladas como *[!UICONTROL Other Carrier]* em [!DNL Walmart].

**Pré-requisitos**

Antes de mapear transportadoras, conclua as seguintes tarefas:

1. Revise os [Métodos de Transportadora e Práticas Recomendadas de Envio para Entrega no Prazo](https://sellerhelp.walmart.com/s/guide?article=000009473) para [!DNL Walmart Marketplace].

1. Verifique a configuração de [[!UICONTROL Shipping Carrier]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/delivery/shipping-carriers/carriers.html) e [[!UICONTROL Shipping Settings]](https://experienceleague.adobe.com/docs/commerce-admin/config/sales/shipping-settings.html) no armazenamento [!DNL Commerce] para garantir que você otimizou a configuração para [!DNL Walmart Marketplace sales].

## Mapear transportadoras

1. Na página **[!UICONTROL Listings]** ou **[!UICONTROL Orders]**, selecione **[!UICONTROL Channel Settings]**.

1. Em **[!UICONTROL Channel Settings]**, selecione **[!UICONTROL Shipping Carriers]**.

   ![Mapear transportadoras](assets/map-shipping-carriers.png){width="600" zoomable="yes"}

1. Para cada operadora preferencial [!DNL Walmart] listada, selecione o nome da operadora [!DNL Commerce] na lista suspensa se a operadora estiver disponível.

1. Selecione **[!UICONTROL Save]** para aplicar a configuração.

