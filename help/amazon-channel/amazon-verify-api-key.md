---
title: Adicionar ou verificar a chave da API do Amazon
description: Na configuração do Commerce, a chave validada da API do Amazon permite integrar suas lojas à conta do Amazon Seller.
exl-id: 2257b64d-309d-4efd-ba79-6e0cdeed63cb
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Adicionar ou verificar a chave de API do Amazon

Ao acessar o canal de vendas da Amazon, [!DNL Commerce] verifica e valida automaticamente a chave da API do Amazon adicionada na configuração da loja. Se validado, você pode seguir para a próxima etapa, [Integração de loja](./store-integration.md).

Se a chave da API do Amazon estiver ausente, inválida ou expirada, você deverá atualizar a chave. Uma mensagem é exibida solicitando que você obtenha uma chave de API e adicione-a à configuração do canal de vendas do Amazon.

## Obtenha e adicione a chave de API do Amazon, conforme solicitado

A chave da API é validada sempre que você acessa o canal de vendas da Amazon.

1. Faça logon no [!DNL Commerce] Administrador

1. No _[!UICONTROL Admin]_barra lateral, vá para **[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Se for a primeira vez que você acessa o canal de vendas da Amazon ou se a chave de API exigir atualização, o sistema solicitará a atualização durante o processo.

   ![Obter e adicionar o prompt de chave da API do Amazon](assets/amazon-api-verification-prompt.png)

1. Clique em **[!UICONTROL Sign in]** para acessar seu [!DNL Commerce] conta da Web.

   A página Contas comerciais é aberta em uma nova guia do navegador.

   - Se você estiver conectado ao [!DNL Commerce] , a _[!UICONTROL API Portal]_da seção_[!UICONTROL My Account]_ será exibida automaticamente.

   - Se você não estiver conectado, será solicitado a digitar o [!DNL Commerce] nome de usuário e senha da conta antes da _[!UICONTROL API Portal]_será exibida.

   - Se você não tiver uma conta, visite [o [!DNL Commerce] página da conta](https://account.magento.com/customer/account/login/){target=&quot;_blank&quot;} e registro. Essa conta deve fazer parte de sua empresa ou empresa.

1. Se necessário, é possível exibir e gerar chaves de API no _[!UICONTROL API Portal]_na guia [!DNL Commerce] conta.

   Para criar uma chave de API, insira uma descrição como `Amazon Sales Channel` e clique em **[!UICONTROL Add New]**. A nova chave é gerada e mostrada com o nome inserido. Clique em **[!UICONTROL Copy]** para copiar a nova chave.

   ![Gerar ou copiar uma chave de API](assets/amazon-add-api-key.png)

1. Com a nova chave gerada e copiada, retorne ao _[!UICONTROL Amazon Sales Channel]_no navegador.

1. No _[!UICONTROL Welcome to Amazon Sales Channel]_página, clique em **[!UICONTROL Add the key]**.

   O navegador sai do canal de vendas do Amazon e uma página de configuração de loja abre o _[!UICONTROL Api Keys]_na página [!DNL Commerce] Administrador Você pode abrir esta página manualmente ao acessar **[!UICONTROL Stores]**>_[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**, expandir **[!UICONTROL Services]** no painel esquerdo e escolha **[!UICONTROL Magento Services]**.

1. Cole a chave copiada para o **[!UICONTROL Production Api key]**.

1. Clique em **[!UICONTROL Save Config]**. Agora você pode retornar ao canal de vendas da Amazon.

   ![Adicionar sua chave de API na configuração da loja](assets/config-magento-services-api-screen.png)

1. No _[!UICONTROL Admin]_barra lateral, vá para **[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Acessar novamente acionadores de canal de vendas da Amazon [!DNL Commerce] verifique e valide sua chave de API e permita continuar.

   Se for solicitado que você verifique a chave novamente, repita essa etapa _Adicionar e verificar_ processo.

![Ícone Próximo](assets/btn-next.png) [**Continuar para armazenar a integração**](./store-integration.md)
