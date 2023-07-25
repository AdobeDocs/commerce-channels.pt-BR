---
title: Gerenciar Conexão do Walmart Marketplace
description: "Atualize as credenciais da API para autorizar a conexão entre um [DNL! Commerce] exibição de loja e o [!DNL Walmart Marketplace]. The connection is required to connect [!DNL Commerce] listas de produtos e sincronizar dados de estoque, preço, pedido e remessa entre [!DNL Commerce] e o Walmart."
role: Admin, Developer
feature: Sales Channels, Configuration, Shipping/Delivery, Integration
exl-id: 817b1b58-a57e-4c8d-b08f-1ce3bec15bc3
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Mapear Transportadoras

Antes de você [processar entregas de ordem](process-orders.md#ship-an-order) para [!DNL Walmart Marketplace] transportadoras preferenciais Walmart para a transportadora correspondente em [!DNL Commerce] para que os dados de envio possam ser sincronizados entre [!DNL Walmart] e [!DNL Commerce].

As transportadoras comerciais que não mapeiam para uma transportadora preferencial são rotuladas como *[!UICONTROL Other Carrier]* em [!DNL Walmart].

**Pré-requisitos**

Revisão [Requisitos do Walmart](walmart-requirements.md) para o [!DNL Marketplace Seller account].

## Atualizar credenciais de conexão

1. No [!UICONTROL Listings] para a loja de canal de vendas, selecione **[!UICONTROL Channel Settings]**.

1. Ligado **[!UICONTROL Channel Settings]**, selecione **[!UICONTROL Walmart Connection]**.

1. Para modificar as credenciais, selecione **[!UICONTROL Change Credentials]**

   ![Atualizar credenciais da API do Walmart para autorizar a conexão](assets/update-connection-credentials.png){width="700" zoomable="yes"}

1. Insira o **[!UICONTROL Walmart Client ID]** e **[!UICONTROL Walmart Client Secret]**.

1. Selecionar **[!UICONTROL Save]** para aplicar a configuração.
