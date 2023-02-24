---
title: Visão geral das configurações
description: "Saiba mais sobre o [!DNL Channel Manager settings] para configurar a autenticação e mapear os atributos do catálogo de produtos e as operadoras de remessa necessárias para coordenar as operações de vendas entre [!DNL Commerce] e [!DNL Walmart Marketplace]."
exl-id: 305b3580-bfe2-4fc2-9dc8-fb41f5eaf959
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Visão geral das configurações

As configurações de canal de vendas permitem a comunicação e a sincronização de dados entre [!DNL Commerce] e [!DNL Walmart Marketplace] para que você possa gerenciar [!DNL Walmart Marketplace] operações de venda da [!DNL Commerce] Administrador

Em [!DNL Channel Manager], você configurará algumas configurações de canais de vendas durante o processo de integração. Após a integração, você pode exibir e gerenciar a configuração selecionando **[!UICONTROL Channel Settings]** do [!UICONTROL Listings] e [!UICONTROL Orders] painéis.

* **[Conexão Walmart](manage-wmt-connection.md)**-Durante o [!DNL Channel Manager] processo de integração, você fornece [Credenciais da API](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) do [!DNL Walmart Marketplace] Conta do vendedor para conexão [!DNL Commerce] para [!DNL Walmart Marketplace] para comunicação e sincronização de dados. Se necessário, você pode atualizar essas credenciais do *Configurações de canal* página.

* **[Mapear identificadores exclusivos](map-catalog-attributes.md)**-Antes de conectar as listagens de [!DNL Commerce] para [!DNL Walmart Marketplace]mapeie pelo menos um identificador exclusivo de [!DNL Commerce] catálogo para o identificador correspondente do Walmart. Esta etapa é necessária para corresponder a [!DNL Commerce] aos produtos existentes [!DNL Walmart] e para sincronizar os dados do produto entre [!DNL Commerce] e [!DNL Walmart].

* **[Mapear operadoras de transporte](map-shipping-carriers.md)**- Antes de processar [!DNL Walmart Marketplace] ordens de [!DNL Commerce], certifique-se de mapear as transportadoras da sua [!DNL Commerce] às transportadoras correspondentes em [!DNL Walmart Marketplace].
