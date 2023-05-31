---
title: Mapear Transportadoras
description: "Mapear atributos para correspondência [DNL! Commerce] para produtos existentes [!DNL Walmart Marketplace] listagens e sincronização de dados entre [!DNL Channel Manager] e [!DNL Walmart]."
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# Mapear Transportadoras

Antes de você [processar entregas de ordem](process-orders.md#ship-an-order) para [!DNL Walmart Marketplace] transportadoras preferenciais Walmart para a transportadora correspondente em [!DNL Commerce] para que os dados de envio possam ser sincronizados entre [!DNL Walmart] e [!DNL Commerce].

As transportadoras comerciais que não mapeiam para uma transportadora preferencial são rotuladas como *[!UICONTROL Other Carrier]* em [!DNL Walmart].

**Pré-requisitos**

Antes de mapear transportadoras, conclua as seguintes tarefas:

1. Revise o [Métodos da operadora e práticas recomendadas de envio para entrega no prazo](https://sellerhelp.walmart.com/s/guide?article=000009473) para [!DNL Walmart Marketplace].

1. Verifique se [[!UICONTROL Shipping Carrier]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/delivery/shipping-carriers/carriers.html) e [[!UICONTROL Shipping Settings]](https://experienceleague.adobe.com/docs/commerce-admin/config/sales/shipping-settings.html) configuração no seu [!DNL Commerce] armazene para garantir que você otimizou a configuração para [!DNL Walmart Marketplace sales].

## Mapear transportadoras

1. No **[!UICONTROL Listings]** ou **[!UICONTROL Orders]** selecione **[!UICONTROL Channel Settings]**.

1. Ligado **[!UICONTROL Channel Settings]**, selecione **[!UICONTROL Shipping Carriers]**.

   ![Mapear transportadoras](assets/map-shipping-carriers.png){width="600" zoomable="yes"}

1. Para cada [!DNL Walmart] transportadora preferencial listada, selecione a [!DNL Commerce] nome da operadora na lista suspensa se a operadora estiver disponível.

1. Selecionar **[!UICONTROL Save]** para aplicar a configuração.

