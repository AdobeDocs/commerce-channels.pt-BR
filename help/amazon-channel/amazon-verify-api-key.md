---
title: Adicionar ou verificar a chave da API do Amazon
description: Na configuração do Commerce, a chave validada da API do Amazon permite integrar suas lojas à conta do Amazon Seller.
exl-id: 2257b64d-309d-4efd-ba79-6e0cdeed63cb
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Adicionar ou verificar a chave de API do Amazon

Ao acessar o canal de vendas da Amazon, [!DNL Commerce] verifica e valida automaticamente a chave de API do Amazon adicionada na configuração da loja. Se validado, você pode seguir para a próxima etapa, [Armazenar integração](./store-integration.md).

Se a chave da API do Amazon estiver ausente, inválida ou expirada, você deverá atualizar a chave. Uma mensagem é exibida solicitando que você obtenha uma chave de API e adicione-a à configuração do canal de vendas do Amazon.

## Obtenha e adicione a chave de API do Amazon, conforme solicitado

A chave da API é validada sempre que você acessa o canal de vendas da Amazon.

1. Faça logon no Administrador [!DNL Commerce].

1. Na barra lateral _[!UICONTROL Admin]_, vá para **[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Se for a primeira vez que você acessa o canal de vendas da Amazon ou se a chave de API exigir atualização, o sistema solicitará a atualização durante o processo.

   ![Obter e adicionar o prompt de chave da API do Amazon](assets/amazon-api-verification-prompt.png)

1. Clique em **[!UICONTROL Sign in]** para acessar sua conta da Web [!DNL Commerce].

   A página Contas comerciais é aberta em uma nova guia do navegador.

   - Se você estiver conectado na conta [!DNL Commerce], a seção _[!UICONTROL API Portal]_da página_[!UICONTROL My Account]_ aparece automaticamente.

   - Se você não estiver conectado, será solicitado a inserir seu nome de usuário e senha da conta [!DNL Commerce] antes que a guia _[!UICONTROL API Portal]_seja exibida.

   - Se você não tiver uma conta, visite [a [!DNL Commerce] página da conta](https://account.magento.com/customer/account/login/){target=&quot;_blank&quot;} e registre-se. Essa conta deve fazer parte de sua empresa ou empresa.

1. Se necessário, você pode exibir e gerar chaves de API na guia _[!UICONTROL API Portal]_em sua conta [!DNL Commerce].

   Para criar uma chave de API, insira uma descrição como `Amazon Sales Channel` e clique em **[!UICONTROL Add New]**. A nova chave é gerada e mostrada com o nome inserido. Clique em **[!UICONTROL Copy]** para copiar a nova chave.

   ![Gerar ou copiar uma chave de API](assets/amazon-add-api-key.png)

1. Com a nova chave gerada e copiada, retorne à guia _[!UICONTROL Amazon Sales Channel]_no navegador.

1. Na página _[!UICONTROL Welcome to Amazon Sales Channel]_, clique em **[!UICONTROL Add the key]**.

   O navegador sai do canal de vendas do Amazon e uma página de configuração de loja abre a página _[!UICONTROL Api Keys]_no Administrador [!DNL Commerce]. Você pode abrir esta página manualmente quando ir para **[!UICONTROL Stores]**>_[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**, expandir **[!UICONTROL Services]** no painel esquerdo e escolher **[!UICONTROL Magento Services]**.

1. Cole a chave copiada para **[!UICONTROL Production Api key]**.

1. Clique em **[!UICONTROL Save Config]**. Agora você pode retornar ao canal de vendas da Amazon.

   ![Adicionar sua chave de API na configuração da loja](assets/config-magento-services-api-screen.png)

1. Na barra lateral _[!UICONTROL Admin]_, vá para **[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Acessar novamente os acionadores do canal de vendas da Amazon [!DNL Commerce] verificar e validar sua chave de API e permitir que você continue.

   Se for solicitado a verificar a chave novamente, repita esse processo _Add and Verify_.

![Próximo ](assets/btn-next.png) [**íconeContinuar para armazenar a integração**](./store-integration.md)
