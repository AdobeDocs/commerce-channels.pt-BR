---
title: 'Conectar [!DNL Channel Manager] para [!DNL Walmart Marketplace]'
description: "Conectar uma exibição de loja do Commerce a [!DNL Walmart Marketplace] criar o canal de vendas para gerenciar listas de produtos, estoque, preço e pedidos do Commerce para vendas do Walmart Marketplace."
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Conectar [!DNL Channel Manager] para [!DNL Walmart Marketplace]

Depois de instalar o Channel Manager no seu [!DNL Commerce] crie um canal de vendas no Gerenciador de Canais e configure as credenciais para se conectar [!DNL Channel Manager] para [!DNL Walmart Marketplace].

1. [Criar o canal de vendas](#create-the-sales-channel) selecionando o [!DNL Commerce] loja para listagens de produtos.

1. [Conectar o canal a [!DNL Walmart Marketplace] adicionando [!UICONTROL Walmart API credentials]](#connect-the-channel-to-walmart-marketplace).

1. [Concluir configuração do canal de vendas](#complete-sales-channel-store-setup) para gerenciar listas, inventário, preços e pedidos para o seu [!DNL Walmart Marketplace] variedade de produtos.

>[!NOTE]
>
>O Gerenciador de canais exige uma conexão individualizada entre uma conta do Walmart e um [!DNL Commerce] exibição de loja. Não é possível conectar a mesma visualização de loja a várias contas do Walmart.

## Criar o canal de vendas

1. No Administrador, abra [!DNL Channel Manager] selecionando **[!UICONTROL Marketing** > _Canais _> **Gerenciador de canal]**.

1. No **[!UICONTROL Marketplaces available to connect]** , selecione **[!UICONTROL Get Started]**.

   ![Conectar novo [!DNL Walmart] armazenar em [!DNL Channel Manager]](assets/channel-manager-home.png){width="700" zoomable="yes"}

1. Se necessário, configure [!DNL Walmart Marketplace Seller] conta.

1. Configure o armazenamento e a conexão:

   - Selecionar **[!UICONTROL Add Credentials]**.

   - Selecione o [!DNL Commerce] exibição de loja que oferece os produtos que você deseja vender no marketplace.

      ![Configurar conexão entre [!DNL Commerce] e [!DNL Walmart Marketplace] de [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png){width="500" zoomable="yes"}

   - Insira um único **[!UICONTROL store name]**.

   - Selecione o **[!UICONTROL Adobe [!DNL Commerce] site]** para obter listas de produtos e processamento de pedidos.

   - Para receber notificações relacionadas a [!DNL Channel Manager], adicionar um **[!UICONTROL email address]**.

1. Conectar o canal a [!DNL Walmart Marketplace].

   - Adicione as credenciais para o [[!DNL Walmart Marketplace Adobe Production API key]](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) do seu [!DNL Walmart Marketplace Seller] conta.

   - Se você não tiver as credenciais do, obtenha-as do [!DNL Walmart Marketplace Developer Portal] selecionando **[!UICONTROL Get API credentials]**.

      No Portal do desenvolvedor, selecione sua região (EUA e Canadá) e faça logon.

      ![[!DNL Walmart Marketplace] logon da conta](assets/walmart-marketplace-login-page.png){width="600"}

   - No formulário da chave de API, copie e salve a variável **[!UICONTROL Client ID]** e **[!UICONTROL Client Secret]** valores para o [!UICONTROL Adobe Inc Production API key] para um local seguro.

      ![[!DNL Walmart Marketplace API key] página de configuração](assets/walmart-api-key-management-form.png){width="600" zoomable="yes"}

      >[!NOTE]
      >
      >Se a variável [!DNL Adobe Inc] não estiver listada no Portal do desenvolvedor, selecione **[!UICONTROL Add New Key for a Solution Provider]** para configurar permissões e gerar a chave. Para obter detalhes sobre a configuração, consulte [Gerar um [!DNL Walmart Marketplace API Key]](walmart-requirements.md#generate-a-walmart-marketplace-api-key).

   - Retornar para [!DNL Channel Manager] para adicionar as credenciais à **[!UICONTROL Walmart Connection]** informações.

      Ao adicionar credenciais, o Adobe oculta o segredo do cliente e armazena o valor em um cofre seguro.

1. Selecionar **[!UICONTROL Save Store]** para aplicar a configuração e conectar-se à [!DNL Walmart marketplace].

1. Depois de se conectar com êxito, [concluir configuração da loja](complete-sales-channel-store-setup.md) do **[!UICONTROL Channel Manager]** página de armazenamento.

![Configurar primeira loja](assets/channel-manager-setup-first-store.png){width="500" zoomable="yes"}

### Solução de problemas de conexão

Se a conexão com o [!DNL Walmart] falha, consulte a [Perguntas frequentes sobre o Walmart Marketplace](https://developer.walmart.com/faq/us/faq-auth/){target="_blank"} para obter dicas de solução de problemas.

- No [!DNL Walmart Developer Portal], verifique se você copiou as credenciais corretas da chave de API de produção para [!UICONTROL Adobe Inc.]

- Verifique se a configuração de acesso do [!UICONTROL Walmart Adobe API key] O tem as permissões corretas. Consulte [[!DNL Walmart Requirements]](walmart-requirements.md##generate-a-walmart-marketplace-api-key).

- Confirme se o [!DNL Walmart API] serviço está disponível no [Página de status da API do Walmart](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target="_blank"}.
