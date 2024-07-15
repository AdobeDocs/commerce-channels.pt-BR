---
title: 'Conectar-se a  [!DNL Commerce] Serviços'
description: 'Conecte o Gerenciador de Canais a  [!DNL Commerce] serviços para habilitar a sincronização de dados e a comunicação entre a instância  [!DNL Commerce] , o Gerenciador de Canais e outros serviços de suporte.'
role: Admin, Developer
level: Intermediate
feature: Sales Channels, Install, Integration
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---


# Conectar-se aos Serviços do [!DNL Commerce]

O [!DNL Commerce Services Connector] integra o serviço Gerenciador de Canais às instâncias Adobe Commerce e Magento Open Source. O conector habilita a sincronização de dados e a comunicação entre a instância [!DNL Commerce], [!DNL Channel Manager] e outros serviços de suporte.

A instalação do [!DNL Commerce Services Connector] é um processo único necessário para usar os [serviços SaaS do Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html), como [!DNL Channel Manager], [!DNL Live Search] e [!DNL Product Recommendations]. Se você já tiver configurado o conector para outro serviço, ignore esta etapa.

## Requisitos

- **Conta do Commerce** - Para instalar o software em [!DNL Commerce] instâncias, é necessário ter uma conta com acesso de Proprietário ou de Administrador à plataforma [!DNL Commerce].

  Os proprietários de contas e Superusuários podem criar contas de Administrador na instância [!DNL Commerce] ou na linha de comando usando o comando `admin:user:create` da CLI [!DNL Commerce].

- **Chave da API de Produção do Adobe Commerce**-Esta [chave](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#genapikey) habilita o acesso da API aos serviços exigidos pelo Gerenciador de Canais. Você precisa das credenciais públicas e privadas para esta chave.

>[!TIP]
>
>Para fornecer as credenciais, um titular de licença ou proprietário de conta [!DNL Commerce] tem opções para [compartilhar acesso](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html) ou fornecer as credenciais da [Chave de API](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html) a um desenvolvedor confiável.

## Configurar o [!DNL Commerce Services Connector]

1. Abra a Configuração dos serviços de armazenamento.

   - Em Admin, selecione **[!UICONTROL Stores]**.

   - Em *[!UICONTROL Settings]*, selecione **[!UICONTROL Configuration]**.

   - Expanda **[!UICONTROL Services]** e selecione **[!UICONTROL Commerce Services Connector]**.

1. Adicione as credenciais da chave da API de produção da sua conta do Adobe Commerce.

   Serviço ![[!DNL Commerce Services Connector] no modo de exibição [!DNL Admin]](assets/commerce-services-connector-admin-service-view.png){width="600" zoomable="yes"}


   >[!NOTE]
   >
   > Se sua instância do [!DNL Commerce] tiver outros serviços do [!DNL Adobe Commerce], como o [!DNL Live Search] ou o [!DNL Product Recommendations] instalados, as informações de credencial serão exibidas na interface, e nenhuma configuração adicional será necessária.

1. Configure o projeto SaaS e o espaço de dados para que os Serviços da Commerce possam enviar dados para o serviço Gerenciador de canais.

   ![[!DNL Commerce Services Connector] Configuração do identificador SaaS na [!DNL Admin] visualização](assets/commerce-services-connector-saas-config.png){width="600" zoomable="yes"}

