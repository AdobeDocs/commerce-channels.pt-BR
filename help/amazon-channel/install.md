---
title: Instalar a extensão
description: Para integrar a [!DNL Commerce] catálogo com [!DNL Amazon Seller Accounts] e vender através do [!DNL Amazon Marketplace], baixe e instale a extensão Sales Channel do Amazon.
exl-id: ebf22e28-b6a2-420b-80ca-2d750839286c
source-git-commit: e20e377fdef565ca526e6f67cca126c36b450e75
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Instalar a extensão

>[!IMPORTANT]
>
>Somente [!DNL Amazon Sales Channel] as versões de extensão 4.0+ são compatíveis com as versões Adobe Commerce e Magento Open Source 2.4.x. Se você estiver executando uma versão 2.3.x, consulte a documentação do [versão compatível do canal de vendas da Amazon](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html){target=&quot;_blank&quot;}. Para obter mais informações sobre compatibilidade de versões, consulte o [Disponibilidade](https://devdocs.magento.com/release/availability.html)página {target=&quot;_blank&quot;} na documentação do desenvolvedor.

O [!UICONTROL Amazon Sales Channel] A extensão instala e adiciona recursos para integrar seu catálogo do Commerce com o [!DNL Amazon Seller Accounts] para vender através da [!DNL Amazon Marketplace]. Para revisar informações adicionais, consulte o [Sales Channel Amazon](https://marketplace.magento.com/magento-module-amazon.html) em [!DNL Commerce Marketplace] e [notas de versão](release-notes.md).

## Requisitos

- **Instância de comércio**: O [!DNL Amazon Sales Channel] A extensão pode ser instalada em instâncias com o Magento Open Source, Adobe Commerce e Adobe Commerce nas versões 2.3.x ou posterior da infraestrutura em nuvem. Não é mais compatível com versões 2.1, 2.2 ou 1.x.
- **Conta Web de comércio**: Você deve ter uma conta da Web do Commerce, usada para criar e rastrear uma chave de API.
- **Chave da API**: Crie uma chave de API do canal de vendas da Amazon por meio de sua conta da Web do Commerce. As instruções a seguir incluem essas etapas.

## Instalar

Para obter informações mais detalhadas sobre o uso do Composer nesse processo, consulte o [instalação de extensão](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;} instruções na documentação do desenvolvedor.

1. Faça logon no [Commerce Marketplace](https://marketplace.magento.com/customer/account/){target=&quot;_blank&quot;}.

1. Clique no botão **[!UICONTROL Marketplace]** e clique em **[!UICONTROL My Purchases]**.

1. Localize e selecione **[!UICONTROL Amazon Sales Channel]**.

1. Na página de extensão, selecione a versão .

1. Para o nome e a versão do componente, clique em **[!UICONTROL Technical Details]**.

1. Use as informações de nome e versão para atualizar a entrada do conector de serviços em seu `composer.json` arquivo.

   - Adicione o nome e a versão da extensão ao `composer.json` arquivo.

   - Navegue até seu [!DNL Commerce] diretório do projeto e atualize seu `composer.json` arquivo.

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - Insira seu [chaves de autenticação](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target=&quot;_blank&quot;}. Sua chave pública é seu nome de usuário; sua chave privada é sua senha.

   - Aguarde até que o Composer conclua a atualização das dependências do projeto e verifique se não há erros.


1. [Verificar a extensão](https://devdocs.magento.com/extensions/install/#verify-the-extension){target=&quot;_blank&quot;}.

## Adicionar a chave da API do canal de vendas do Amazon

Depois de instalar, insira um [Chave da API](./amazon-verify-api-key.md) para concluir a configuração.

## Definir as opções de configuração do canal Amazon

Você tem as seguintes opções para configurar o canal de vendas da Amazon. Não é necessário modificar essas configurações para começar a integrar e vender no Amazon. Recomenda-se que os administradores avançados considerem essas opções.

1. Faça logon em Admin.

1. No _Administrador_ barra lateral, vá para **Lojas** > _Configurações_ > **Configuração**.

1. Clique em **Sales Channel**, em seguida **Configurações globais**.

1. Para **Limpar Histórico de Log**, defina o intervalo para limpar os logs coletados.

   As opções incluem `Once Daily`, `Once Weekly`e `Once Monthly` (padrão).

1. (Opcional) Para **Origem das Tarefas em Segundo Plano (CRON)**, altere a configuração para `Command Line (CLI) CRON`.

   Esta configuração é recomendada para **_usuários/administradores avançados_**.

1. Clique em **[!UICONTROL Save Config]**.

## Atualizar a extensão

1. Faça logon no [Commerce Marketplace](https://marketplace.magento.com/customer/account/){target=&quot;_blank&quot;}.

1. Clique no botão **[!UICONTROL Marketplace]** e clique em **[!UICONTROL My Purchases]**.

1. Localize e selecione **[!UICONTROL Amazon Sales Channel]**.

1. Na página de extensão, selecione a versão .

1. Para o nome e a versão do componente, clique em **[!UICONTROL Technical Details]**.

1. Complete o [instruções de atualização de extensão](https://devdocs.magento.com/extensions/install/#upgrade-an-extension){target=&quot;_blank&quot;} na documentação do desenvolvedor.
