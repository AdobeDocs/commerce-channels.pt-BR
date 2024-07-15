---
title: Integrar [!DNL Channel Manager]
description: 'Conecte sua instância ao serviço  [!DNL Channel Manager]  concluindo algumas etapas de integração.'
level: Intermediate
role: Leader, Admin, Developer
feature: Sales Channels, Install
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---


# Integrar [!DNL Channel Manager]

Após concluir o processo de integração do Gerenciador de canais, você poderá acessar, configurar e gerenciar as operações de vendas de canais do Walmart Marketplace no Adobe Commerce. O Gerenciador de Canais está disponível na opção [!UICONTROL Channel Manager] do menu [!UICONTROL Commerce Admin Marketing].

Opção ![[!DNL Channel Manager] no modo de exibição de Administrador](assets/channel-manager-admin-view.png){width="500"}

## Requisitos

Revise os requisitos para usar o Gerenciador de canais e colete as informações de conta e credenciais necessárias para baixar, instalar e configurar a extensão.

- **[Requisitos do Walmart Marketplace](walmart-requirements.md)**-Verifique se você atende aos requisitos para integração com o Gerenciador de Canais, incluindo [configurar sua conta de Vendedor](https://sellerhelp.walmart.com/seller/s/guide?article=000008219) e gerar a chave de API para habilitar a integração.

- **Informações da conta da Commerce**. O download e a instalação de [!DNL Channel Manager] exigem uma [conta da Commerce](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-create.html). Você precisa de uma ID de conta e credenciais com acesso de Proprietário ou Administrador à instância [!DNL Adobe Commerce] ou [!DNL Magento Open Source].

   - **ID da MAGE**-[Faça logon](https://account.magento.com/customer/account/login/) na conta [!DNL Commerce] para obter a ID de **[!UICONTROL My Account - Magento settings]**.

     ![[!DNL MAGEID] em [!DNL Commerce] configurações da conta](assets/mageid-my-commerce-account.png){width="250"}

   - **Chaves de acesso-** Obtenha chaves de autenticação para baixar [!DNL Commerce] extensões do [!DNL Commerce] Repositório do Composer `([!DNL repo.magento.com]`).

     ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png){width="400"}

     Em projetos Adobe Commerce e Magento Open Source, o proprietário pode configurar o [Acesso Compartilhado](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html) para permitir que funcionários e provedores de serviços confiáveis baixem extensões usando credenciais da conta de Proprietário ou titular da licença.

     Para [!DNL Adobe Commerce] em projetos de infraestrutura em nuvem, os instaladores de software devem ter o seguinte acesso à instância [!DNL Commerce]:

      - Acesso de superusuário ao projeto na nuvem
      - Acesso de administrador a um ambiente específico
      - uma conta [!DNL Adobe Commerce] com permissões para acessar o repositório do Composer

     Consulte [Gerenciar acesso do usuário](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) no *Guia do Commerce on Cloud Infrastructure*.

- **Experiência usando o Composer e o[!DNL Commerce CLI]**-Consulte [Instalar uma extensão](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) no *Guia de Instalação* para obter informações sobre como usar essas ferramentas para instalar e gerenciar extensões nas plataformas [!DNL Adobe Commerce] ou [!DNL Magento Open Source].

- **[[!DNL Amazon Sales Channel] versão 4.4.2 ou posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)**-Se você ativou o [!DNL Amazon Sales Channel] para seus sites [!DNL Commerce], verifique se a sua plataforma [!DNL Commerce] tem a versão 4.4.2 ou posterior instalada antes de instalar o [!DNL Channel Manager].

- Extensão **[!DNL Inventory Management]para Adobe Commerce e Magento Open Source**

  Se você planeja usar o Gerenciador de canais para gerenciamento de inventário e pedidos, é necessário ter a extensão do Inventory management instalada e ativada em sua instância do Adobe Commerce e do Magento Open Source. Normalmente, essa extensão é instalada e habilitada por padrão no Adobe Commerce e [!DNL Magento Open Source] 2.3.x e posterior.

  Se você atualizou o Commerce da versão 2.2.x ou se desativou o Inventory management, atualize a instalação para incluir os módulos necessários. Consulte [Instalar o Inventory management](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html) no *Guia do Inventory management*.

### Requisitos do sistema

- [Adobe Commerce 2.4.x](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html)
- [PHP 7.3 / 7.4](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html)
- [Composer 1.x ou posterior](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/overview.html)
- [[!DNL Amazon Sales Channel] versão 4.4.2 ou posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)-Se você ativou o [!DNL Amazon Sales Channel] para seus sites do [!DNL Commerce], verifique se a sua plataforma [!DNL Commerce] tem a versão 4.4.2 instalada antes de instalar o [!DNL Channel Manager].
- [[!DNL Inventory Management]](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html)

### Plataformas compatíveis

- Adobe Commerce na nuvem (ECE): 2.4.x
- Adobe Commerce no local (EE): 2.4.x
- Magento Open Source 2.4.x

## Etapas de integração

1. [Configure sua conta de vendedor do Walmart](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

1. [Instalar a [!DNL Channel Manager] extensão](install.md).

1. [Conecte-se aos Serviços da Commerce](connect.md) para integrar o Gerenciador de Canais com a instância do Commerce e outros serviços de suporte.

1. [Conecte seu [!DNL Commerce] armazenamento a [!DNL Walmart Marketplace]](connect-marketplace.md).

1. [Concluir configuração de armazenamento](complete-sales-channel-store-setup.md).
