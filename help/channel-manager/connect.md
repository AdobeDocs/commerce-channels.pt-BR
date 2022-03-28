---
title: Conectar-se aos Commerce Services
description: Conecte a instância do Gerenciador de Canais a [!DNL Commerce services] para permitir a sincronização e a comunicação de dados entre a instância do Commerce, o Gerenciador de Canais e outros serviços de suporte.
role: User
level: Intermediate
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: 8f07b215c20cc28aa9a6862bcb2b00da30a1ed84
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# Conectar-se aos Commerce Services

O Commerce Services Connector integra o serviço Channel Manager às instâncias do Adobe Commerce e do Magento Open Source. O conector permite a sincronização de dados e a comunicação entre a [!DNL Commerce] instância, [!DNL Channel Manager]e outros serviços de apoio.

A configuração do Commerce Services Connector é um processo único necessário para usar o Adobe [Serviços SaaS de comércio](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html){target=&quot;_blank&quot;} curtir [!DNL Channel Manager], [!DNL Live Search]e [!DNL Product Recommendations]. Se você já tiver configurado o conector para outro serviço, pule esta etapa.

## Pré-requisitos

- **Conta comercial**-Para instalar o software nas instâncias do Commerce, você deve ter uma conta com acesso de Proprietário ou Administrador à plataforma do Commerce.

   Os proprietários da conta e os usuários administradores podem criar novas contas de administrador a partir da instância de Comércio ou da linha de comando usando a [!DNL Commerce] comando CLI `admin:user:create`.

- **Chave da API de produção do Adobe Commerce**-Este [key](https://docs.magento.com/user-guide/system/saas.html#apikey){target=&quot;_blank&quot;} habilita o acesso da API a serviços exigidos pelo Gerenciador de canais. Você precisa das credenciais públicas e privadas para essa chave.

   Para fornecer as credenciais, um titular de licença do Commerce ou um proprietário de conta tem opções para
   [compartilhar acesso](https://docs.magento.com/user-guide/magento/magento-account-share.html){target=&quot;_blank&quot;}, ou dar a variável [Chave da API](https://docs.magento.com/user-guide/system/saas.html#apikey)Credenciais do {target=&quot;_blank&quot;} para um desenvolvedor confiável.

## Configurar o Conector de serviços do Commerce

1. Abra a Configuração de serviços de loja.

   - Em Admin, selecione **[!UICONTROL Stores]**.

   - Em *Configurações*, selecione **[!UICONTROL Configuration]**.

   - Expandir **[!UICONTROL Services]** e selecione **[!UICONTROL Commerce Services Connector]**.

1. Adicione credenciais da chave da API de produção em sua conta da Adobe Commerce.

   ![[!DNL Commerce Service Connector] no [!DNL Admin] exibir](assets/commerce-services-connector-admin-service-view.png)


   >[!NOTE]
   >
   > Se o seu [!DNL Commerce] instância tem outro [!DNL Adobe Commerce] serviços como [!DNL Live Search] ou [!DNL Product Recommendations] instalados, as informações da credencial são exibidas na interface e nenhuma configuração adicional é necessária.

1. Configure o projeto SaaS e o espaço de dados para que o Commerce Services possa enviar dados para o serviço Gerenciador de Canais.

   ![[!DNL Commerce Service Connector] Configuração do Identificador SaaS no [!DNL Admin] exibir](assets/commerce-services-connector-saas-config.png)
