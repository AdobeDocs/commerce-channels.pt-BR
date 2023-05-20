---
title: Integrado [!DNL Channel Manager]
description: "Conecte sua instância à [!DNL Channel Manager] concluindo algumas etapas de integração."
role: User
level: Intermediate
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# Integrado [!DNL Channel Manager]

Após concluir o processo de integração do Gerenciador de canais, você poderá acessar, configurar e gerenciar as operações de vendas de canais do Walmart Marketplace no Adobe Commerce. O Gerenciador de canais está disponível no [!UICONTROL Channel Manager] opção no [!UICONTROL Commerce Admin Marketing] menu.

![[!DNL Channel Manager] opção na exibição do Administrador](assets/channel-manager-admin-view.png)

## Requisitos

Revise os requisitos para usar o Gerenciador de canais e colete as informações de conta e credenciais necessárias para baixar, instalar e configurar a extensão.

- **[Requisitos do Walmart Marketplace](walmart-requirements.md)**-Verificar se atende aos requisitos para integração com o Channel Manager, incluindo [configurar sua conta de vendedor](https://sellerhelp.walmart.com/seller/s/guide?article=000008219) e gerar a chave de API para habilitar a integração.

- **Informações da conta de comércio**-Download e instalação [!DNL Channel Manager] exige um [Conta do Commerce](https://docs.magento.com/user-guide/magento/magento-account.html){target="_blank"}. Você precisa de uma ID de conta e credenciais com acesso de Proprietário ou Administrador à [!DNL Adobe Commerce] ou [!DNL Magento Open Source] instância.

   - **ID DA IMAGEM**-[Fazer logon](https://account.magento.com/customer/account/login/) para o [!DNL Commerce] conta da qual obter a ID **[!UICONTROL My Account - Magento settings]**.

      ![[!DNL MAGEID] em [!DNL Commerce] configurações da conta](assets/mageid-my-commerce-account.png)

   - **Chaves de acesso-** Obter chaves de autenticação para baixar [!DNL Commerce] extensões do [!DNL Commerce] Repositório do Composer `([!DNL repo.magento.com]`).

      ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png)

      Em projetos Adobe Commerce e Magento Open Source, o proprietário pode configurar [Acesso compartilhado](https://docs.magento.com/user-guide/magento/magento-account-share.html) para permitir que funcionários confiáveis e provedores de serviços baixem extensões usando credenciais da conta Proprietário ou titular da licença.

      Para [!DNL Adobe Commerce] em projetos de infraestrutura em nuvem, os instaladores de software devem ter o seguinte acesso à [!DNL Commerce] instância:

      - Acesso de superusuário ao projeto na nuvem
      - Acesso de administrador a um ambiente específico
      - um [!DNL Adobe Commerce] conta com permissões para acessar o repositório do Composer

      Consulte [Gerenciar acesso do usuário](https://devdocs.magento.com/cloud/project/user-admin.html).


- **Experiência com o Composer e o[!DNL Commerce CLI]**-Consulte [Instalação geral da CLI](https://devdocs.magento.com/extensions/install/){target="_blank"} para obter informações sobre como usar essas ferramentas para instalar e gerenciar extensões no [!DNL Adobe Commerce] ou [!DNL Magento Open Source] plataformas.

- **[[!DNL Amazon Sales Channel] versão 4.4.2 ou posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)**-Se você ativou [!DNL Amazon Sales Channel] para seu [!DNL Commerce] sites, verifique se [!DNL Commerce] A plataforma do tem a versão 4.4.2 ou posterior instalada antes da instalação [!DNL Channel Manager].

- **[!DNL Inventory Management]extensão para Adobe Commerce e Magento Open Source**

   Se você planeja usar o Gerenciador de canais para gerenciamento de inventário e pedidos, é necessário ter a extensão do Inventory management instalada e ativada em sua instância do Adobe Commerce e do Magento Open Source. Normalmente, essa extensão é instalada e ativada por padrão no Adobe Commerce e [!DNL Magento Open Source] 2.3.x e posterior.

   Se você atualizou o Commerce da versão 2.2.x ou se desativou o Inventory management, atualize a instalação para incluir os módulos necessários. Consulte [Instalar o Inventory management](https://devdocs.magento.com/extensions/inventory-management/) na documentação para desenvolvedores do Adobe Commerce.

### Requisitos do sistema

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [PHP 7.3 / 7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [Composer 1.x ou posterior](https://devdocs.magento.com/cloud/reference/cloud-composer.html)
- [[!DNL Amazon Sales Channel] versão 4.4.2 ou posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)-Se você ativou [!DNL Amazon Sales Channel] para seu [!DNL Commerce] sites, verifique se [!DNL Commerce] A plataforma do tem a versão 4.4.2 instalada antes da instalação [!DNL Channel Manager].
- [[!DNL Inventory Management]](https://devdocs.magento.com/extensions/inventory-management/)

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
