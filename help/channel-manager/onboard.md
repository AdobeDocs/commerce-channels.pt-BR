---
title: Integrado [!DNL Channel Manager]
description: '"Conecte sua instância ao [!DNL Channel Manager] , completando algumas etapas de integração."'
role: User
level: Intermediate
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: 638ba8c595652e66aa5f15f5207855c6d2b872d7
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---


# Integrado [!DNL Channel Manager]

Após concluir a integração, configure e gerencie as operações dos canais de vendas da [!UICONTROL Channel Manager] na [!UICONTROL Commerce Admin Marketing] menu.

![[!DNL Channel Manager] opção na visualização Administração](assets/channel-manager-admin-view.png)

## Visão geral da integração

1. [Instale o [!DNL Channel Manager] extensão](install.md).

1. [Configure o [!DNL Commerce Services Connector]](connect.md) para integrar o Channel Manager à instância do Commerce e outros serviços de suporte.

1. [Conecte seu [!DNL Commerce] armazenar para [!DNL Walmart Marketplace]](connect.md).

1. [Configuração completa da loja](complete-store-setup.md).

## Requisitos

- Verifique se você atende à [Requisitos do Walmart Marketplace](walmart-requirements.md) para integrar com o Gerenciador de canais.

- **Informações da conta comercial**-Download e instalação [!DNL Channel Manager] exige um [Conta comercial](https://docs.magento.com/user-guide/magento/magento-account.html){target=&quot;_blank&quot;}. Você precisa de uma ID de conta e credenciais com acesso de Proprietário ou Administrador ao [!DNL Adobe Commerce] ou [!DNL Magento Open Source] instância.

   - **ID DA MAGEM**-[Fazer logon](https://account.magento.com/customer/account/login/) para [!DNL Commerce] conta para obter a ID do **[!UICONTROL My Account - Magento settings]**.

      ![[!DNL MAGEID] on [!DNL Commerce] configurações da conta](assets/mageid-my-commerce-account.png)

   - **Chaves de acesso -** Obter chaves de autenticação para transferência [!DNL Commerce] extensões do [!DNL Commerce] Repositório Composer `([!DNL repo.magento.com]`).

      ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png)

      Em projetos do Adobe Commerce e do Magento Open Source, o proprietário pode configurar [Acesso compartilhado](https://docs.magento.com/user-guide/magento/magento-account-share.html) para permitir que funcionários e prestadores de serviços confiáveis baixem extensões usando credenciais da conta do Proprietário ou do titular da licença.

      Para [!DNL Adobe Commerce] em projetos de infraestrutura em nuvem, os instaladores de software devem ter o seguinte acesso ao [!DNL Commerce] instância:

      - Acesso de superusuário ao projeto do Cloud
      - Acesso do administrador a um ambiente específico
      - um [!DNL Adobe Commerce] ou [!DNL Magento Open Source] conta com permissões para acessar o repositório do Composer

      Consulte [Gerenciar o acesso do usuário](https://devdocs.magento.com/cloud/project/user-admin.html).


- **Experiência usando o Composer e a[!DNL Commerce CLI]** -Consulte [Instalação geral da CLI](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;} para obter informações sobre o uso dessas ferramentas para instalar e gerenciar extensões no [!DNL Adobe Commerce] ou [!DNL Magento Open Source] plataformas.

- [[!DNL Amazon Sales Channel] versão 4.4.2 ou posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)-Se você ativou [!DNL Amazon Sales Channel] para seu [!DNL Commerce] sites, verifique se seu [!DNL Commerce] a plataforma tem a versão 4.4.2 instalada antes da instalação [!DNL Channel Manager].

- [!DNL Inventory Management] extensão para Adobe Commerce e Magento Open Source

   Se você planeja usar o Gerenciador de canais para inventário e gerenciamento de pedidos, é necessário ter a extensão Inventory management instalada e ativada na sua instância do Adobe Commerce e do Magento Open Source. Normalmente, essa extensão é instalada e ativada por padrão no Adobe Commerce e Magento Open Source 2.3.x e posterior.

   Se você atualizou o Commerce a partir da 2.2.x ou se desabilitou o Inventory management, será necessário atualizar sua instalação para incluir os módulos necessários. Para obter mais informações, consulte [Instalar o Inventory management](https://devdocs.magento.com/extensions/inventory-management/) na documentação do desenvolvedor do Adobe Commerce.

### Requisitos do sistema

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [PHP 7.3 / 7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [Composer 1.x ou posterior](https://devdocs.magento.com/cloud/reference/cloud-composer.html)
- [[!DNL Amazon Sales Channel] versão 4.4.2 ou posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)-Se você ativou [!DNL Amazon Sales Channel] para seu [!DNL Commerce] sites, verifique se seu [!DNL Commerce] a plataforma tem a versão 4.4.2 instalada antes da instalação [!DNL Channel Manager].
- [[!DNL Inventory Management]](https://devdocs.magento.com/extensions/inventory-management/)

### Plataformas compatíveis

- Adobe Commerce on Cloud (ECE) : 2.4.x
- Adobe Commerce nas instalações (EE) : 2.4.x
- Magento Open Source 2.4.x
