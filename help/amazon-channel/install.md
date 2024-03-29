---
title: "Instale o [!DNL Amazon Sales Channel] extensão"
description: Para integrar sua [!DNL Commerce] catálogo com [!DNL Amazon Seller Accounts] e vender por meio da [!DNL Amazon Marketplace], baixe e instale a extensão Amazon Sales Channel.
role: Admin, Developer
feature: Sales Channels, Install, Integration, Tools and External Services
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# Instale o [!DNL Amazon Sales Channel] extensão

>[!IMPORTANT]
>
>Somente [!DNL Amazon Sales Channel] as versões da extensão 4.0+ são compatíveis com as versões do Adobe Commerce e Magento Open Source 2.4.x. Se estiver executando uma versão 2.3.x, consulte a documentação do [versão compatível do canal de vendas do Amazon](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html). Para obter mais informações sobre compatibilidade de versões, consulte a [Disponibilidade](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) página na documentação do desenvolvedor.

A variável [!UICONTROL Amazon Sales Channel] A extensão do instala e adiciona recursos para integrar seu catálogo do Commerce ao [!DNL Amazon Seller Accounts] para vender através da [!DNL Amazon Marketplace]. Para revisar informações adicionais, consulte a [Sales Channel Amazon](https://marketplace.magento.com/magento-module-amazon.html) página em [!DNL Commerce Marketplace] e a variável [notas de versão](release-notes.md).

## Requisitos

- **Instância do Commerce**: A variável [!DNL Amazon Sales Channel] A extensão do pode ser instalada em instâncias com o Magento Open Source, Adobe Commerce e Adobe Commerce nas versões 2.3.x ou posteriores da infraestrutura em nuvem. Não é mais compatível com as versões 2.1, 2.2 ou 1.x.
- **Conta da Web do Commerce**: você deve ter uma conta da Web do Commerce, usada para criar e rastrear uma chave de API.
- **Chave de API**: crie uma chave de API do canal de vendas do Amazon por meio da conta da Web do Commerce. As instruções a seguir incluem essas etapas.

## Instalar

Para obter informações mais detalhadas sobre como usar o Composer para esse processo, consulte [instalação de extensão](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) instruções na documentação do desenvolvedor.

1. Faça logon no [Commerce Marketplace](https://marketplace.magento.com/customer/account/).

1. Clique em **[!UICONTROL Marketplace]** e clique em **[!UICONTROL My Purchases]**.

1. Localizar e selecionar **[!UICONTROL Amazon Sales Channel]**.

1. Na página da extensão, selecione a versão.

1. Para o nome e a versão do componente, clique em **[!UICONTROL Technical Details]**.

1. Use o nome e as informações de versão para atualizar a entrada do conector de serviços no `composer.json` arquivo.

   - Adicione o nome e a versão da extensão à `composer.json` arquivo.

   - Navegue até o [!DNL Commerce] diretório do projeto e atualize seu `composer.json` arquivo.

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - Insira seu [chaves de autenticação](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html). Sua chave pública é seu nome de usuário; sua chave privada é sua senha.

   - Espere o Composer terminar de atualizar as dependências do projeto e garantir que não haja erros.

1. [Verificar a extensão](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

## Adicionar a chave da API do canal de vendas do Amazon

Após a instalação, insira um [Chave de API](./amazon-verify-api-key.md) para concluir a configuração.

## Definir as opções de configuração de canal do Amazon

Você tem as seguintes opções para configurar o canal de vendas do Amazon. Não é necessário modificar essas configurações para iniciar a integração e a venda no Amazon. É recomendável que administradores avançados considerem essas opções.

1. Faça logon no Admin.

1. No _Admin_ barra lateral, vá para **Lojas** > _Configurações_ > **Configuração**.

1. Clique em **Sales Channel**, depois **Configurações globais**.

1. Para **Limpar histórico do log**, defina o intervalo para limpar os logs coletados.

   As opções incluem `Once Daily`, `Once Weekly`, e `Once Monthly` (padrão).

1. (Opcional) Para **Origem de Tarefas em Segundo Plano (CRON)**, altere a configuração para `Command Line (CLI) CRON`.

   Esta configuração é recomendada para **_usuários/administradores avançados_**.

1. Clique em **[!UICONTROL Save Config]**.

## Atualizar a extensão

1. Faça logon no [Commerce Marketplace](https://marketplace.magento.com/customer/account/).

1. Clique em **[!UICONTROL Marketplace]** e clique em **[!UICONTROL My Purchases]**.

1. Localizar e selecionar **[!UICONTROL Amazon Sales Channel]**.

1. Na página da extensão, selecione a versão.

1. Para o nome e a versão do componente, clique em **[!UICONTROL Technical Details]**.

1. Conclua o [instruções de atualização da extensão](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) no _Guia de instalação_.
