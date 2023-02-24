---
title: '''Conectar-se a [!DNL Commerce] Serviços"'
description: '"Conecte o Gerenciador de Canais ao [!DNL Commerce] para permitir a sincronização e a comunicação de dados entre a [!DNL Commerce] instância, Gerenciador de canal e outros serviços de suporte.'''
role: User
level: Intermediate
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---


# Conectar-se a [!DNL Commerce] Serviços

O [!DNL Commerce Services Connector] integra o serviço Gerenciador de canais às instâncias do Adobe Commerce e do Magento Open Source. O conector permite a sincronização de dados e a comunicação entre a [!DNL Commerce] instância, [!DNL Channel Manager]e outros serviços de apoio.

[!DNL Commerce Services Connector] configuração é um processo único necessário para usar [Serviços SaaS da Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html){target="_blank"} como [!DNL Channel Manager], [!DNL Live Search]e [!DNL Product Recommendations]. Se você já tiver configurado o conector para outro serviço, pule esta etapa.

## Requisitos

- **Conta comercial**-Para instalar o software em [!DNL Commerce] Você deve ter uma conta com acesso de Proprietário ou Administrador ao [!DNL Commerce] plataforma.

   Proprietários da conta e Superusuários podem criar contas de administrador a partir do [!DNL Commerce] ou da linha de comando usando o [!DNL Commerce] comando CLI `admin:user:create`.

- **Chave da API de produção do Adobe Commerce**-Este [key](https://docs.magento.com/user-guide/system/saas.html#apikey){target="_blank"} habilita o acesso da API aos serviços exigidos pelo Gerenciador de canais. Você precisa das credenciais públicas e privadas para essa chave.

>[!TIP]
>
>Para fornecer as credenciais, uma [!DNL Commerce] o titular da licença ou o proprietário da conta tem opções para [compartilhar acesso](https://docs.magento.com/user-guide/magento/magento-account-share.html){target="_blank"}, or give the [API Key](https://docs.magento.com/user-guide/system/saas.html#apikey){target="_blank"} credenciais para um desenvolvedor confiável.

## Configure o [!DNL Commerce Services Connector]

1. Abra a Configuração de serviços de loja.

   - Em Admin, selecione **[!UICONTROL Stores]**.

   - Em *[!UICONTROL Settings]*, selecione **[!UICONTROL Configuration]**.

   - Expandir **[!UICONTROL Services]** e selecione **[!UICONTROL Commerce Services Connector]**.

1. Adicione credenciais da chave da API de produção em sua conta da Adobe Commerce.

   ![[!DNL Commerce Services Connector] no [!DNL Admin] exibir](assets/commerce-services-connector-admin-service-view.png)


   >[!NOTE]
   >
   > Se o seu [!DNL Commerce] instância tem outro [!DNL Adobe Commerce] serviços como [!DNL Live Search] ou [!DNL Product Recommendations] instalados, as informações da credencial são exibidas na interface e nenhuma configuração adicional é necessária.

1. Configure o projeto SaaS e o espaço de dados para que o Commerce Services possa enviar dados para o serviço Gerenciador de Canais.

   ![[!DNL Commerce Services Connector] Configuração do Identificador SaaS no [!DNL Admin] exibir](assets/commerce-services-connector-saas-config.png)

