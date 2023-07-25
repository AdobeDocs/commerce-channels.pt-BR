---
title: Visão geral das configurações
description: '''Saiba mais sobre o [!DNL Channel Manager settings] para configurar a autenticação e mapear atributos de catálogo de produtos e transportadoras necessárias para coordenar operações de vendas entre [!DNL Commerce] e a variável [!DNL Walmart Marketplace]."'
role: Admin
feature: Sales Channels, Configuration, Merchandising, Shipping/Delivery
exl-id: 305b3580-bfe2-4fc2-9dc8-fb41f5eaf959
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Visão geral das configurações

As configurações do canal de vendas permitem a comunicação e a sincronização de dados entre [!DNL Commerce] e [!DNL Walmart Marketplace] para gerenciar [!DNL Walmart Marketplace] operações de vendas do [!DNL Commerce] Admin.

Entrada [!DNL Channel Manager], você define algumas configurações de canais de vendas durante o processo de integração. Após a integração, você pode visualizar e gerenciar a configuração selecionando **[!UICONTROL Channel Settings]** do [!UICONTROL Listings] e [!UICONTROL Orders] painéis.

* **[Conexão do Walmart](manage-wmt-connection.md)**-Durante o [!DNL Channel Manager] processo de integração, você fornece [Credenciais da API](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) do seu [!DNL Walmart Marketplace] Conta do vendedor a conectar [!DNL Commerce] para [!DNL Walmart Marketplace] para comunicação e sincronização de dados. Se necessário, você pode atualizar essas credenciais no *Configurações do canal* página.

* **[Identificadores exclusivos do mapa](map-catalog-attributes.md)**-Antes de conectar as listagens de [!DNL Commerce] para [!DNL Walmart Marketplace], mapeie pelo menos um identificador exclusivo do [!DNL Commerce] ao identificador correspondente do Walmart. Esta etapa é necessária para corresponder a [!DNL Commerce] produtos para os existentes [!DNL Walmart] listagens e para sincronizar dados de produtos entre [!DNL Commerce] e [!DNL Walmart].

* **[Mapear Transportadoras](map-shipping-carriers.md)**-Antes do processamento [!DNL Walmart Marketplace] pedidos de [!DNL Commerce], certifique-se de mapear as transportadoras de seu [!DNL Commerce] aos transportadores correspondentes em [!DNL Walmart Marketplace].
