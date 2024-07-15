---
title: Adicionar ou verificar a chave de API do Amazon
description: Na configuração do Commerce, a chave de API validada do Amazon permite integrar suas lojas à sua conta de vendedor do Amazon.
role: Admin, Developer
feature: Sales Channels, Integration, Tools and External Services
exl-id: 2257b64d-309d-4efd-ba79-6e0cdeed63cb
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# Adicionar ou verificar a chave de API do Amazon

Ao acessar o canal de vendas do Amazon, o [!DNL Commerce] verifica e valida automaticamente a chave de API do Amazon que você adicionou à configuração da loja. Se for validado, você poderá seguir para a próxima etapa, [Integração da Loja](./store-integration.md).

Se a chave de API do Amazon estiver ausente, inválida ou expirada, será necessário atualizar a chave. Será exibida uma mensagem solicitando que você obtenha uma chave de API e adicione-a à configuração do canal de vendas da Amazon.

## Obtenha e adicione a chave de API do Amazon conforme solicitado

A chave de API é validada sempre que você acessa o canal de vendas da Amazon.

1. Faça logon no [!DNL Commerce] Administrador.

1. Na barra lateral _[!UICONTROL Admin]_, vá para **[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Se for a primeira vez que você acessa o canal de vendas da Amazon ou se sua chave de API exigir atualização, o sistema o orientará durante o processo.

   ![Obter e adicionar o Prompt de Chave de API do Amazon](assets/amazon-api-verification-prompt.png){width="500"}

1. Clique em **[!UICONTROL Sign in]** para acessar sua conta da web [!DNL Commerce].

   A página Contas do Commerce é aberta em uma nova guia do navegador.

   - Se você estiver conectado à sua conta [!DNL Commerce], a seção _[!UICONTROL API Portal]_da página_[!UICONTROL My Account]_ será exibida automaticamente.

   - Se você não estiver conectado, será solicitado a digitar seu nome de usuário e senha da conta [!DNL Commerce] antes que a guia _[!UICONTROL API Portal]_apareça.

   - Se você não tiver uma conta, visite [a [!DNL Commerce] página da conta](https://account.magento.com/customer/account/login/){target="_blank"} e registre-se. Essa conta deve fazer parte de sua empresa ou negócio.

1. Se necessário, você pode exibir e gerar chaves de API na guia _[!UICONTROL API Portal]_da sua conta [!DNL Commerce].

   Para criar uma chave de API, insira uma descrição como `Amazon Sales Channel` e clique em **[!UICONTROL Add New]**. A nova chave é gerada e mostrada com o nome inserido. Clique em **[!UICONTROL Copy]** para copiar a nova chave.

   ![Gerar ou copiar uma chave de API](assets/amazon-add-api-key.png){width="500" zoomable="yes"}

1. Com a nova chave gerada e copiada, retorne à guia _[!UICONTROL Amazon Sales Channel]_no navegador.

1. Na página _[!UICONTROL Welcome to Amazon Sales Channel]_, clique em **[!UICONTROL Add the key]**.

   O navegador sai do canal de vendas da Amazon e uma página de configuração da loja abre a página _[!UICONTROL Api Keys]_no Administrador [!DNL Commerce]. Você pode abrir esta página manualmente ao acessar **[!UICONTROL Stores]**>_[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**, expandir **[!UICONTROL Services]** no painel esquerdo e escolher **[!UICONTROL Magento Services]**.

1. Cole a chave copiada para **[!UICONTROL Production Api key]**.

1. Clique em **[!UICONTROL Save Config]**. Agora você pode retornar ao canal de vendas da Amazon.

   ![Adicionando a chave de API à configuração do armazenamento](assets/config-magento-services-api-screen.png){width="600" zoomable="yes"}

1. Na barra lateral _[!UICONTROL Admin]_, vá para **[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Acessar novamente os gatilhos de canal de vendas do Amazon [!DNL Commerce] verifica e valida sua chave de API e permite que você continue.

   Se for solicitado que você verifique a chave novamente, repita este processo de _Adicionar e Verificar_.

![Próximo ícone](assets/btn-next.png) [**Continuar para a Integração de Armazenamento**](./store-integration.md)
