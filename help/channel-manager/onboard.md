---
title: Integrado [!DNL Channel Manager]
description: Conecte sua instância ao [!DNL Channel Manager] concluindo algumas etapas de integração.
role: User
level: Intermediate
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: f57c6db4c0314272d10bb5483d2c8a0ae396a9fc
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# Integrado [!DNL Channel Manager]

Gerenciador de canal integrado instalando a extensão do Gerenciador de canais em seu [!DNL Commerce] instância e configuração de conexões de API. Essas conexões permitem a comunicação e a sincronização de dados entre a sua instância do Commerce e o Walmart Marketplace.

Após concluir a integração, configure e gerencie as operações dos canais de vendas da [!UICONTROL Channel Manager] na [!UICONTROL Commerce Admin Marketing] menu.

![[!DNL Channel Manager] opção na visualização Administração](assets/channel-manager-admin-view.png)

## Visão geral da integração

1. [Instale o [!DNL Channel Manager] extensão](install.md).

1. [Configure o [!DNL Commerce Services Connector]](connect.md) para integrar o Channel Manager à instância do Commerce e outros serviços de suporte.

1. [Conecte seu [!DNL Commerce] armazenar para [!DNL Walmart Marketplace]](connect.md).

1. [Configuração completa da loja](complete-store-setup.md).

## Pré-requisitos

- Verifique se você tem o [Pré-requisitos do Walmart Marketplace](walmart-prerequisites.md) para integrar com o Gerenciador de canais.

- **Informações da conta comercial**-Download e instalação [!DNL Channel Manager] exige um [Conta comercial](https://docs.magento.com/user-guide/magento/magento-account.html){target=&quot;_blank&quot;}. Você precisa de uma ID de conta e credenciais com acesso de Proprietário ou Administrador ao [!DNL Adobe Commerce] ou [!DNL Magento Open Source] instância.

   - **ID DA MAGEM**-[Fazer logon](https://account.magento.com/customer/account/login/) para a conta comercial do para obter a ID do **[!UICONTROL My Account - Magento settings]**. Você precisa dessa ID para se registrar na [!DNL Channel Manager] programa beta de serviço.

      ![[!DNL MAGEID] nas configurações da conta do Commerce](assets/mageid-my-commerce-account.png)

   - **Chaves de acesso -** Obter chaves de autenticação para baixar extensões do Commerce do repositório do Commerce Composer `([!DNL repo.magento.com]`).

      ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png)

      Em projetos do Adobe Commerce e do Magento Open Source, o proprietário pode configurar [Acesso compartilhado](https://docs.magento.com/user-guide/magento/magento-account-share.html) para permitir que funcionários e prestadores de serviços confiáveis baixem extensões usando credenciais da conta do Proprietário ou do titular da licença.

      Ligado [!DNL Adobe Commerce] em projetos de infraestrutura em nuvem, os instaladores de software devem ter o seguinte acesso: [!DNL Commerce] instância:

      - Acesso de superusuário ao projeto do Cloud
      - Acesso do administrador a um ambiente específico
      - um [!DNL Adobe Commerce] ou [!DNL Magento Open Source] conta com permissões para acessar o repositório do Composer.

      Consulte [Gerenciar o acesso do usuário](https://devdocs.magento.com/cloud/project/user-admin.html).


- **Autorização para baixar o pacote do Channel Manager Composer**-Forneça a MAGE ID da conta comercial usada para gerenciar o serviço ao representante do Adobe que coordena o programa Beta para sua organização.
- **Experiência usando o Composer e a[!DNL Commerce CLI]** -Consulte [Instalação geral da CLI](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;} para obter informações sobre o uso dessas ferramentas para instalar e gerenciar extensões no [!DNL Adobe Commerce] ou [!DNL Magento Open Source] plataformas.
- **[Amazon Sales Channel versão 4.4.2 ou posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)-Se você ativou o Amazon Sales Channel para seus sites de Comércio, verifique se sua plataforma de Comércio tem a versão 4.42 instalada antes de instalar o Channel Manager.


### Requisitos

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [PHP 7.3 / 7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [Composer 1.x ou posterior](https://devdocs.magento.com/cloud/reference/cloud-composer.html)


### Plataformas compatíveis

- Adobe Commerce on Cloud (ECE) : 2.4.x
- Adobe Commerce nas instalações (EE) : 2.4.x
- Magento Open Source 2.4.x