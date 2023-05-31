---
title: Integrado [!DNL Channel Manager]
description: "Conecte sua instância à [!DNL Channel Manager] concluindo algumas etapas de integração."
role: User
level: Intermediate
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---


# Integrado [!DNL Channel Manager]

Após concluir o processo de integração do Gerenciador de canais, você poderá acessar, configurar e gerenciar as operações de vendas de canais do Walmart Marketplace no Adobe Commerce. O Gerenciador de canais está disponível no [!UICONTROL Channel Manager] opção no [!UICONTROL Commerce Admin Marketing] menu.

![[!DNL Channel Manager] opção na exibição do Administrador](assets/channel-manager-admin-view.png){width="500"}

## Requisitos

Revise os requisitos para usar o Gerenciador de canais e colete as informações de conta e credenciais necessárias para baixar, instalar e configurar a extensão.

- **[Requisitos do Walmart Marketplace](walmart-requirements.md)**-Verificar se atende aos requisitos para integração com o Channel Manager, incluindo [configurar sua conta de vendedor](https://sellerhelp.walmart.com/seller/s/guide?article=000008219) e gerar a chave de API para habilitar a integração.

- **Informações da conta de comércio**-Download e instalação [!DNL Channel Manager] exige um [Conta do Commerce](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-create.html). Você precisa de uma ID de conta e credenciais com acesso de Proprietário ou Administrador à [!DNL Adobe Commerce] ou [!DNL Magento Open Source] instância.

   - **ID DA IMAGEM**-[Fazer logon](https://account.magento.com/customer/account/login/) para o [!DNL Commerce] conta da qual obter a ID **[!UICONTROL My Account - Magento settings]**.

      ![[!DNL MAGEID] em [!DNL Commerce] configurações da conta](assets/mageid-my-commerce-account.png){width="250"}

   - **Chaves de acesso-** Obter chaves de autenticação para baixar [!DNL Commerce] extensões do [!DNL Commerce] Repositório do Composer `([!DNL repo.magento.com]`).

      ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png){width="400"}

      Em projetos Adobe Commerce e Magento Open Source, o proprietário pode configurar [Acesso compartilhado](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html) para permitir que funcionários confiáveis e provedores de serviços baixem extensões usando credenciais da conta Proprietário ou titular da licença.

      Para [!DNL Adobe Commerce] em projetos de infraestrutura em nuvem, os instaladores de software devem ter o seguinte acesso à [!DNL Commerce] instância:

      - Acesso de superusuário ao projeto na nuvem
      - Acesso de administrador a um ambiente específico
      - um [!DNL Adobe Commerce] conta com permissões para acessar o repositório do Composer

      Consulte [Gerenciar acesso do usuário](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) no *Guia do Commerce na infraestrutura em nuvem*.


- **Experiência com o Composer e o[!DNL Commerce CLI]**-Consulte [Instalar uma extensão](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) no *Guia de instalação* para obter informações sobre como usar essas ferramentas para instalar e gerenciar extensões no [!DNL Adobe Commerce] ou [!DNL Magento Open Source] plataformas.

- **[[!DNL Amazon Sales Channel] versão 4.4.2 ou posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)**-Se você ativou [!DNL Amazon Sales Channel] para seu [!DNL Commerce] sites, verifique se [!DNL Commerce] A plataforma do tem a versão 4.4.2 ou posterior instalada antes da instalação [!DNL Channel Manager].

- **[!DNL Inventory Management]extensão para Adobe Commerce e Magento Open Source**

   Se você planeja usar o Gerenciador de canais para gerenciamento de inventário e pedidos, é necessário ter a extensão do Inventory management instalada e ativada em sua instância do Adobe Commerce e do Magento Open Source. Normalmente, essa extensão é instalada e ativada por padrão no Adobe Commerce e [!DNL Magento Open Source] 2.3.x e posterior.

   Se você atualizou o Commerce da versão 2.2.x ou se desativou o Inventory management, atualize a instalação para incluir os módulos necessários. Consulte [Instalar o Inventory management](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html) no *Guia do Inventory management*.

### Requisitos do sistema

- [Adobe Commerce 2.4.x](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html)
- [PHP 7.3 / 7.4](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html)
- [Composer 1.x ou posterior](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/overview.html)
- [[!DNL Amazon Sales Channel] versão 4.4.2 ou posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)-Se você ativou [!DNL Amazon Sales Channel] para seu [!DNL Commerce] sites, verifique se [!DNL Commerce] A plataforma do tem a versão 4.4.2 instalada antes da instalação [!DNL Channel Manager].
- [[!DNL Inventory Management]](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html)

### Plataformas compatíveis

- Adobe Commerce na nuvem (ECE): 2.4.x
- Adobe Commerce no local (EE): 2.4.x
- Magento Open Source 2.4.x

## Etapas de integração

1. [Configurar sua conta de vendedor do Walmart](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

1. [Instale o [!DNL Channel Manager] extensão](install.md).

1. [Conectar-se a Commerce Services](connect.md) para integrar o Gerenciador de canais à instância do Commerce e outros serviços de suporte.

1. [Conecte seu [!DNL Commerce] armazenar em [!DNL Walmart Marketplace]](connect-marketplace.md).

1. [Concluir configuração da loja](complete-sales-channel-store-setup.md).
