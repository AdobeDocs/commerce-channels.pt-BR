---
title: '"Integrado [!DNL Channel Manager]"'
description: Conecte sua instância ao [!DNL Channel Manager] concluindo algumas etapas de integração.
role: User
level: Intermediate
source-git-commit: ff87f31fec7a689385a93b8cab260fd93ff15f90
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Integrado [!DNL Channel Manager]

Gerenciador de canal integrado instalando a extensão do Gerenciador de canais em seu [!DNL Commerce] e configurar conexões de API para permitir a comunicação e a sincronização de dados entre sua instância do Commerce e o Walmart Marketplace.

Após concluir a integração, você pode configurar e gerenciar as operações dos canais de vendas da [!UICONTROL Channel Manager] na [!UICONTROL Commerce Admin Marketing] menu.

![[!DNL Channel Manager] opção na visualização Administração](assets/channel-manager-admin-view.png)

## Visão geral da integração

1. [Instale o [!DNL Channel Manager] extensão](install.md).

1. [Configure o [!DNL Commerce Services Connector]](connect.md) para integrar o Channel Manager à instância do Commerce e outros serviços de suporte.

1. [Conecte seu [!DNL Commerce] armazenar para [!DNL Walmart Marketplace]](connect.md).

## Pré-requisitos

- Verifique se você tem os requisitos do Walmart Marketplace Seller AccountWalmart para vender no Walmart Marketplace

- **Informações da conta comercial**-Download e instalação [!DNL Channel Manager] exige uma ID e credenciais de um [Conta comercial](https://docs.magento.com/user-guide/magento/magento-account.html){target=&quot;_blank&quot;} com acesso do proprietário ao [!DNL Adobe Commerce] ou [!DNL Magento Open Source] instância.

   - **ID DA MAGEM**-[Fazer logon](https://account.magento.com/customer/account/login/) para a conta comercial do para obter a ID do [!UICONTROL My Account - Magento settings]. Você precisa dessa ID para se registrar na [!DNL Channel Manager] programa beta de serviço.

      ![[!DNL MAGEID] nas configurações da conta do Commerce](assets/mageid-my-commerce-account.png)

   - **Chaves de acesso -** Obter chaves de autenticação para baixar extensões do Commerce do repositório do Commerce Composer ([!DNL repo.magento.com]).

      ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png)

      Em projetos Adobe Commerce e Magento Open Source, o Proprietário pode configurar [Acesso compartilhado](https://docs.magento.com/user-guide/magento/magento-account-share.html) para permitir que funcionários e prestadores de serviços confiáveis baixem extensões usando credenciais da conta do Proprietário ou do titular da licença.

      Ligado [!DNL Adobe Commerce] em projetos de infraestrutura em nuvem, os usuários devem ter as seguintes permissões para instalar o software no [!DNL Commerce] instância:

      - Acesso de superusuário ao projeto do Cloud
      - Acesso do administrador a um ambiente específico
      - um [!DNL Adobe Commerce] ou [!DNL Magento Open Source] conta com permissões para acessar o repositório do Composer. Consulte [Gerenciar o acesso do usuário](https://devdocs.magento.com/cloud/project/user-admin.html).

- **Autorização para baixar o pacote do Channel Manager Composer**-Forneça a MAGE ID da conta comercial usada para gerenciar o serviço ao representante do Adobe que coordena o programa Beta para sua organização.
- **Experiência usando o Composer e a[!DNL Commerce CLI]** -Consulte [Instalação geral da CLI](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;} para obter informações sobre o uso dessas ferramentas para instalar e gerenciar extensões em A[!DNL Adobe Commerce] ou [!DNL Magento Open Source] plataformas.
- Para instâncias do Commerce que têm o Amazon Sales Channel instalado, verifique se [Amazon Sales Channel versão 4.4.2 ou posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html) é instalado antes de instalar o Gerenciador de canais.


### Requisitos

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [PHP 7.3 / 7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [Composer 1.x ou posterior](https://devdocs.magento.com/cloud/reference/cloud-composer.html)


### Plataformas compatíveis

- Adobe Commerce on Cloud (ECE) : 2.4.x
- Adobe Commerce nas instalações (EE) : 2.4.x
- Magento Open Source 2.4.x
