---
title: Mapear transportadoras
description: Mapear atributos para correspondência [DNL! Comércio] produtos para produtos existentes [!DNL Walmart Marketplace] listagens e sincronização de dados entre [!DNL Channel Manager] e [!DNL Walmart].
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: e8c3fdc912b1e7ee4960a9a6ff66a2c9968f34f0
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# Mapear transportadoras

Antes de [transferências de ordem de processo](process-orders.md#ship-an-order) para [!DNL Walmart Marketplace] encomendas, mapear as transportadoras marítimas preferenciais da Walmart para a transportadora correspondente em [!DNL Commerce] para que os dados de envio possam ser sincronizados entre [!DNL Walmart] e [!DNL Commerce].

Operadoras de comércio que não mapeiam para uma operadora preferencial são rotuladas como *[!UICONTROL Other Carrier]* na Walmart.

**Pré-requisitos**

Antes de mapear as transportadoras de envio, realize as seguintes tarefas:

1. Revise o [Métodos de operadora e práticas recomendadas de envio para entrega em tempo](https://sellerhelp.walmart.com/s/guide?article=000009473) para Walmart Marketplace.

1. Verifique o [[!UICONTROL Shipping Carrier]](https://docs.magento.com/user-guide/shipping/carriers.html) e [!UICONTROL Shipping Settings] na configuração do [!DNL Commerce] armazenar para garantir que você otimizou a configuração de [!DNL Walmart Marketplace sales].

## Mapear transportadoras

1. No [!UICONTROL Listings] para o armazenamento do canal de vendas, selecione **[!UICONTROL Settings]**.

1. De *[!UICONTROL Map Attributes], selecione **[!UICONTROL Shipping Carriers].

   ![Mapear transportadoras](assets/map-shipping-carriers.png)

1. Para cada [!DNL Walmart] a operadora preferida listada, selecione a [!DNL Commerce] nome da operadora na lista suspensa, se a operadora estiver disponível.

1. Selecionar **[!UICONTROL Save]** para aplicar a configuração.
