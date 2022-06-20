---
title: Gerenciar Conexão Walmart Marketplace
description: Atualize as credenciais da API para autorizar a conexão entre um [DNL! Comércio] exibição de loja e o [!DNL Walmart Marketplace]. A conexão é necessária para conectar as listas de produtos do Commerce e sincronizar dados de inventário, preço, pedido e remessa entre o Commerce e o Walmart.
source-git-commit: 97128dcf45d7672e958c771f88389aba40c6e39e
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# Mapear transportadoras

Antes de [transferências de ordem de processo](process-orders.md#ship-an-order) para [!DNL Walmart Marketplace] encomendas, mapear as transportadoras marítimas preferenciais da Walmart para a transportadora correspondente em [!DNL Commerce] para que os dados de envio possam ser sincronizados entre [!DNL Walmart] e [!DNL Commerce].

Operadoras de comércio que não mapeiam para uma operadora preferencial são rotuladas como *[!UICONTROL Other Carrier]* on [!DNL Walmart].

**Pré-requisitos**

Revisão [Requisitos do Walmart](walmart-requirements.md) para [!DNL Marketplace Seller account].

## Atualizar credenciais de conexão

1. No [!UICONTROL Listings] para o armazenamento do canal de vendas, selecione **[!UICONTROL Channel Settings]**.

1. Ligado **[!UICONTROL Channel Settings]**, selecione **[!UICONTROL Walmart Connection]**.

1. Para modificar as credenciais, selecione **[!UICONTROL Change Credentials]**

   ![Atualize as credenciais da API do Walmart para autorizar a conexão](assets/update-connection-credentials.png)

1. Insira o **[!UICONTROL Walmart Client ID]** e **[!UICONTROL Walmart Client Secret]**.

1. Selecionar **[!UICONTROL Save]** para aplicar a configuração.
