---
title: Definir configurações de canal
description: Configure o Gerenciador de Canais e as configurações do canal de vendas para autenticação, mapeie os atributos do catálogo e as transportadoras de remessa necessárias para coordenar as operações de vendas entre [!DNL Commerce] e [!DNL Walmart Marketplace].
source-git-commit: e3b12c9ce1ad4b5be17284e98956a773d7ccca24
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---


# Definir configurações de canal de vendas

As configurações de canal de vendas permitem a comunicação e a sincronização de dados entre [!DNL Commerce] e [!DNL Walmart Marketplace] para que você possa gerenciar [!DNL Walmart Marketplace] operações de venda da [!DNL Commerce] Administrador:

Em [!DNL Channel Manager], você configurará algumas configurações de canais de vendas durante o processo de integração. Após a integração, você pode exibir e gerenciar a configuração das Configurações na *Configurações* página.

* **[Mapear identificadores exclusivos](map-catalog-attributes.md)**- Antes de publicar listagens de [!DNL Commerce] para [!DNL Walmart Marketplace]mapeie pelo menos um identificador exclusivo de [!DNL Commerce] catálogo para o identificador correspondente de [!DNL Walmart]. Esta etapa é necessária para corresponder a [!DNL Commerce] aos produtos existentes [!DNL Walmart] e para sincronizar os dados do produto entre [!DNL Commerce] e [!DNL Walmart].

* **[Mapear operadoras de transporte](map-shipping-carriers.md)**- Antes de processar [!DNL Walmart Marketplace] ordens de [!DNL Commerce], certifique-se de mapear as transportadoras da sua [!DNL Commerce] às transportadoras correspondentes em [!DNL Walmart Marketplace].

* **Credenciais da API do Walmart**-Durante o [!DNL Channel Manager] processo de integração, você fornece a variável [Credenciais da API do Walmart](walmart-prerequisites.md#generate-a-walmart-marketplace-production-api-key) do [!DNL Walmart Marketplace Seller] conta para conexão [!DNL Commerce] para [!DNL Walmart Marketplace] para comunicação e sincronização de dados. Se necessário, você pode atualizar essas credenciais do *Configurações* página.
