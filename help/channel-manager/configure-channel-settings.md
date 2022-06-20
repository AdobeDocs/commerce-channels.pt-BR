---
title: Definir configurações de canal
description: Configure o Gerenciador de Canais e as configurações do canal de vendas para autenticação, mapeie os atributos do catálogo e as transportadoras de remessa necessárias para coordenar as operações de vendas entre [!DNL Commerce] e [!DNL Walmart Marketplace].
source-git-commit: 5c478813af442a4e54cb5c64045698f04d710c9a
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Definir configurações de canal de vendas

As configurações de canal de vendas permitem a comunicação e a sincronização de dados entre [!DNL Commerce] e [!DNL Walmart Marketplace] para que você possa gerenciar [!DNL Walmart Marketplace] operações de venda da [!DNL Commerce] Administrador:

Em [!DNL Channel Manager], você configurará algumas configurações de canais de vendas durante o processo de integração. Após a integração, você pode exibir e gerenciar a configuração do canal na *[!UICONTROL Channel Settings]* página.

- **[Mapear identificadores exclusivos](map-catalog-attributes.md)**-Antes de conectar as listagens de [!DNL Commerce] para [!DNL Walmart Marketplace]mapeie pelo menos um identificador exclusivo de [!DNL Commerce] catálogo para o identificador correspondente de [!DNL Walmart]. Esta etapa é necessária para corresponder a [!DNL Commerce] aos produtos existentes [!DNL Walmart] e para sincronizar os dados do produto entre [!DNL Commerce] e [!DNL Walmart].

- **[Mapear operadoras de transporte](map-shipping-carriers.md)**- Antes de processar [!DNL Walmart Marketplace] ordens de [!DNL Commerce], certifique-se de mapear as transportadoras da sua [!DNL Commerce] às transportadoras correspondentes em [!DNL Walmart Marketplace].

- **Credenciais da API do Walmart**-Durante o [!DNL Channel Manager] processo de integração, você fornece a variável [Credenciais da API do Walmart](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) do [!DNL Walmart Marketplace Seller] conta para conexão [!DNL Commerce] para [!DNL Walmart Marketplace] para comunicação e sincronização de dados. Se necessário, você pode [atualizar estas credenciais](manage-wmt-connection.md) do _[!UICONTROL Channel Settings]_página.
