---
title: Visão geral das configurações
description: 'Saiba mais sobre [!DNL Channel Manager settings] a fim de configurar a autenticação e mapear os atributos do catálogo de produtos e as transportadoras necessárias para coordenar as operações de vendas entre [!DNL Commerce] e [!DNL Walmart Marketplace].'
role: Admin
feature: Sales Channels, Configuration, Merchandising, Shipping/Delivery
exl-id: 305b3580-bfe2-4fc2-9dc8-fb41f5eaf959
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Visão geral das configurações

As configurações do canal de vendas habilitam a comunicação e a sincronização de dados entre [!DNL Commerce] e [!DNL Walmart Marketplace] para que você possa gerenciar [!DNL Walmart Marketplace] operações de vendas do Administrador [!DNL Commerce].

No [!DNL Channel Manager], você define algumas configurações de canais de vendas durante o processo de integração. Após a integração, você pode visualizar e gerenciar a configuração selecionando **[!UICONTROL Channel Settings]** nos painéis [!UICONTROL Listings] e [!UICONTROL Orders].

* **[Conexão Walmart](manage-wmt-connection.md)** - Durante o processo de integração do [!DNL Channel Manager], você fornece [credenciais de API](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) da sua conta de vendedor do [!DNL Walmart Marketplace] para conectar o [!DNL Commerce] ao [!DNL Walmart Marketplace] para comunicação e sincronização de dados. Se necessário, você pode atualizar essas credenciais na página *Configurações do canal*.

* **[Mapear identificadores exclusivos](map-catalog-attributes.md)**-Antes de conectar as listagens de [!DNL Commerce] a [!DNL Walmart Marketplace], mapeie pelo menos um identificador exclusivo do catálogo [!DNL Commerce] para o identificador correspondente do Walmart. Esta etapa é necessária para corresponder produtos do [!DNL Commerce] às listagens existentes do [!DNL Walmart] e para sincronizar dados de produtos entre [!DNL Commerce] e [!DNL Walmart].

* **[Mapear transportadoras](map-shipping-carriers.md)**-Antes de processar [!DNL Walmart Marketplace] pedidos de [!DNL Commerce], certifique-se de mapear transportadoras da sua instância [!DNL Commerce] para as transportadoras correspondentes em [!DNL Walmart Marketplace].
