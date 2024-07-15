---
title: Instalar a extensão  [!DNL Amazon Sales Channel]
description: Para integrar seu catálogo do  [!DNL Commerce] ao [!DNL Amazon Seller Accounts] e vender por meio do [!DNL Amazon Marketplace], baixe e instale a extensão Amazon Sales Channel.
role: Admin, Developer
feature: Sales Channels, Install, Integration, Tools and External Services
exl-id: ebf22e28-b6a2-420b-80ca-2d750839286c
source-git-commit: 010a95d7be29354515cf4dcbf5d557eebaa40ed6
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# Instalar a extensão [!DNL Amazon Sales Channel]

>[!IMPORTANT]
>
>Somente [!DNL Amazon Sales Channel] versões de extensão 4.0+ têm suporte para as versões Adobe Commerce e Magento Open Source 2.4.x. Se você estiver executando uma versão 2.3.x, consulte a documentação da [versão compatível do canal de vendas da Amazon](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html). Para obter mais informações sobre compatibilidade de versões, consulte a página [Disponibilidade](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) na documentação do desenvolvedor.

A extensão do [!UICONTROL Amazon Sales Channel] instala e adiciona recursos para integrar seu catálogo do Commerce ao [!DNL Amazon Seller Accounts] para vender por meio do [!DNL Amazon Marketplace]. Para ver mais informações, consulte a página [Sales Channel do Amazon](https://marketplace.magento.com/magento-module-amazon.html) em [!DNL Commerce Marketplace] e as [notas de versão](release-notes.md).

## Requisitos

- **Instância do Commerce**: a extensão [!DNL Amazon Sales Channel] pode ser instalada em instâncias com o Magento Open Source, o Adobe Commerce e o Adobe Commerce nas versões 2.3.x ou posteriores da infraestrutura na nuvem. Não é mais compatível com as versões 2.1, 2.2 ou 1.x.
- **Conta da Web do Commerce**: você deve ter uma conta da Web do Commerce, que é usada para criar e rastrear uma chave de API.
- **Chave de API**: crie uma chave de API de canal de vendas do Amazon por meio da sua conta da Web do Commerce. As instruções a seguir incluem essas etapas.

## Instalar

Para obter informações mais detalhadas sobre como usar o Composer para esse processo, consulte as instruções de [instalação de extensão](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) na documentação do desenvolvedor.

1. Faça logon no [Commerce Marketplace](https://marketplace.magento.com/customer/account/).

1. Clique na guia **[!UICONTROL Marketplace]** e em **[!UICONTROL My Purchases]**.

1. Localize e selecione **[!UICONTROL Amazon Sales Channel]**.

1. Na página da extensão, selecione a versão.

1. Para o nome e a versão do componente, clique em **[!UICONTROL Technical Details]**.

1. Use as informações de nome e versão para atualizar a entrada do conector de serviços no arquivo `composer.json`.

   - Adicione o nome e a versão da extensão ao arquivo `composer.json`.

   - Navegue até o diretório de projeto [!DNL Commerce] e atualize o arquivo `composer.json`.

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - Insira suas [chaves de autenticação](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html). Sua chave pública é seu nome de usuário; sua chave privada é sua senha.

   - Espere o Composer terminar de atualizar as dependências do projeto e garantir que não haja erros.

1. [Verifique a extensão](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

## Adicionar a chave da API do canal de vendas do Amazon

Após a instalação, insira uma [Chave de API](./amazon-verify-api-key.md) para concluir a configuração.

## Definir as opções de configuração de canal do Amazon

Você tem as seguintes opções para configurar o canal de vendas do Amazon. Não é necessário modificar essas configurações para iniciar a integração e a venda no Amazon. É recomendável que administradores avançados considerem essas opções.

1. Faça logon no Admin.

1. Na barra lateral _Admin_, vá para **Lojas** > _Configurações_ > **Configuração**.

1. Clique em **Sales Channel** e depois em **Configurações Globais**.

1. Para **Limpar Histórico de Log**, defina o intervalo para limpar os logs coletados.

   As opções incluem `Once Daily`, `Once Weekly` e `Once Monthly` (padrão).

1. (Opcional) Para **Tarefas em Segundo Plano (CRON) Source**, altere a configuração para `Command Line (CLI) CRON`.

   Esta configuração é recomendada para **_usuários/administradores avançados_**.

1. Clique em **[!UICONTROL Save Config]**.

## Atualizar a extensão

1. Faça logon no [Commerce Marketplace](https://marketplace.magento.com/customer/account/).

1. Clique na guia **[!UICONTROL Marketplace]** e em **[!UICONTROL My Purchases]**.

1. Localize e selecione **[!UICONTROL Amazon Sales Channel]**.

1. Na página da extensão, selecione a versão.

1. Para o nome e a versão do componente, clique em **[!UICONTROL Technical Details]**.

1. Conclua as [instruções de atualização de extensão](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) no _Guia de Instalação_.
