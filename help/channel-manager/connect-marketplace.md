---
title: Conectar Sales Channel a [!DNL Walmart Marketplace]
description: Configure o canal de vendas e conecte-se ao Walmart Marketplace.
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
source-git-commit: 8f07b215c20cc28aa9a6862bcb2b00da30a1ed84
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# Conectar-se a [!DNL Walmart Marketplace]

Depois de instalar o Gerenciador de canais em seu [!DNL Commerce] conecte uma loja do Commerce ao Walmart Marketplace.

1. Crie o canal de vendas por [selecionar a loja Comércio para listagens de produtos](#select-the-commerce-store-for-the-sales-channel).

1. [Conecte o canal ao [!DNL Walmart Marketplace] adicionando credenciais da API do Walmart](#connect-the-channel-to-walmart-marketplace).

1. [Configuração completa do canal de vendas](#complete-store-setup) para gerenciar listas, inventário, preços e vendas do Channel Manager.

## Criar o canal de vendas

1. Abra o Gerenciador de canais.

   - Em Admin, selecione **[!UICONTROL Marketing** > _Canais _> **Gerenciador de canal]**.

   - Selecionar **[!UICONTROL Connect New Store]**.

      ![Conexão da loja do Commerce ao [!DNL Walmart Marketplace] from [!DNL Channel Manager]](assets/connect-commerce-store-to-marketplace.png)


1. Configure a loja e a conexão:

   - Insira um **[!UICONTROL store name]**.

   - Selecione o **[!UICONTROL Adobe Commerce site]** para listas de produtos.

   - Adicione um **[!UICONTROL email address]** para receber notificações de serviço relacionadas a [!DNL Channel Manager].

      ![Configurar a conexão entre o Commerce e o [!DNL Walmart Marketplace] from [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png)


## Conecte o canal ao Walmart Marketplace

1. Adicione as credenciais para a [!DNL Walmart Marketplace Adobe Production API key] do [!DNL Walmart Marketplace Seller] conta.

   - Se não tiver as credenciais, selecione **[!UICONTROL Get API credentials]** para obtê-los do [!DNL Walmart Marketplace Developer Portal].

      Se solicitado, selecione sua região (EUA e Canadá) e faça logon.

      ![[!DNL Walmart Marketplace] logon da conta](assets/walmart-marketplace-login-page.png)

   - No formulário da chave API, copie e salve a variável **[!UICONTROL Client ID]** e **[!UICONTROL Client Secret]** para [!UICONTROL Adobe Inc Production API key] para um local seguro.

      ![[!DNL Walmart Marketplace API key] página de configuração](assets/walmart-api-key-management-form.png)

      >[!NOTE]
      >
      >Se a variável [!DNL Adobe Inc] A chave não está listada no Portal do desenvolvedor, selecione **[!UICONTROL Add New Key for a Solution Provider]** para configurar permissões e gerar a chave. Para obter detalhes de configuração, consulte [Gerar um [!DNL Walmart Marketplace API Key]](walmart-prerequisites.md#generate-a-walmart-marketplace-api-key).

   - Retornar para [!DNL Channel Manager] para adicionar as credenciais ao **[!UICONTROL Walmart Connection]** informações.

      Ao adicionar credenciais ao [!DNL Channel Manager], o Adobe oculta o segredo do cliente e armazena o valor em um cofre seguro.

1. [!UICONTROL Save] a configuração para estabelecer a conexão.

   Depois de se conectar com êxito, gerencie o canal de **[!UICONTROL Channel Manager > Marketplace Stores]**.

   ![[!DNL Walmart Marketplace API key] página de configuração](assets/manage-connected-stores.png)


### Solução de problemas de conexão

Se a conexão com o Walmart falhar, consulte o [Perguntas frequentes sobre o Walmart Marketplace](https://developer.walmart.com/faq/us/faq-auth/){target=&quot;_blank&quot;} para dicas de solução de problemas.

- No [!DNL Walmart Developer Portal], verifique se você copiou as credenciais corretas para a chave da API de produção do para o [!UICONTROL Adobe Inc.]

- Verifique se a configuração de acesso da chave de API do Adobe Walmart tem as permissões corretas. Consulte [Pré-requisitos do Walmart](walmart-prerequisites.md##generate-a-walmart-marketplace-api-key).

- Confirme se o serviço de API do Walmart está disponível no [Página de status da API Walmart](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target=&quot;_blank&quot;}.
