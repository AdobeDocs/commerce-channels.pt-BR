---
title: Conectar-se aos Commerce Services
description: Conecte a instância do Gerenciador de Canais a [!DNL Commerce services] para permitir a sincronização e a comunicação de dados entre a instância do Commerce, o Gerenciador de Canais e outros serviços de suporte.
role: User
level: Intermediate
source-git-commit: ec950579a9b2220f9ec106b616779fc3503f3add
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# Conectar-se aos Commerce Services

O Commerce Services Connector integra o serviço Channel Manager às instâncias do Adobe Commerce e do Magento Open Source. O conector permite a sincronização de dados e a comunicação entre a [!DNL Commerce] instância, [!DNL Channel Manager]e outros serviços de apoio.

A configuração do Commerce Services Connector é um processo único necessário para usar o Adobe [Serviços SaaS de comércio](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html){target=&quot;_blank&quot;} curtir [!DNL Channel Manager], [!DNL Live Search]e [!DNL Product Recommendations]. Se você já tiver configurado o conector para outro serviço, ignore esta etapa.

## Pré-requisitos

- **Conta comercial com [Acesso do administrador](https://docs.magento.com/user-guide/stores/admin.html){target=&quot;_blank&quot;}** à sua instância do Commerce**-Os proprietários da conta e usuários administradores podem configurar contas de usuário na instância do Commerce ou na linha de comando usando o [!DNL Commerce] comando CLI `admin:user:create`.

- **Adobe Commerce [Chaves da API de produção](https://docs.magento.com/user-guide/system/saas.html#apikey){target=&quot;_blank&quot;}**-Habilitar o acesso à API para os serviços exigidos pelo Gerenciador de canais

   Para fornecer as credenciais, um titular de licença do Commerce ou um proprietário de conta tem opções para
   [compartilhar acesso](https://docs.magento.com/user-guide/magento/magento-account-share.html){target=&quot;_blank&quot;}, ou dar a variável [Chave da API](https://docs.magento.com/user-guide/system/saas.html#apikey)Credenciais do {target=&quot;_blank&quot;} para um desenvolvedor confiável.

## Configurar o Conector de serviços do Commerce

1. Abra a Configuração de serviços de loja.

   - Em Admin, selecione [!UICONTROL Stores].

   - Em *Configurações*, selecione [!UICONTROL Configuration].

   - No [!UICONTROL Configuration] página, expandir [!UICONTROL Services] e selecione [!UICONTROL Commerce Services Connector].

1. Adicione chaves da API de produção em sua conta da Adobe Commerce.

   ![[!DNL Commerce Service Connector] no [!DNL Admin] exibir](assets/commerce-services-connector-admin-service-view.png)


   >[!NOTE]
   >
   > Se o seu [!DNL Commerce] instância tem outro [!DNL Adobe Commerce] serviços como [!DNL Live Search] ou [!DNL Product Recommendations] instalados, as informações da credencial são exibidas na interface e nenhuma configuração adicional é necessária.

1. Configure o projeto SaaS e o espaço de dados para que o Commerce Services possa enviar dados para o serviço Gerenciador de Canais.

   ![[!DNL Commerce Service Connector] Configuração do Identificador SaaS no [!DNL Admin] exibir](assets/commerce-services-connector-saas-config.png)

