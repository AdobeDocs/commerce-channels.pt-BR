---
title: 'Conectar [!DNL Channel Manager] a [!DNL Walmart Marketplace]'
description: "Conecte uma exibição da Commerce Store ao  [!DNL Walmart Marketplace] para criar o canal de vendas para gerenciar listas de produtos, estoque, preço e pedidos do Commerce para vendas do Walmart Marketplace."
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
role: Admin, Developer
feature: Sales Channels, Install, Integration
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Conectar [!DNL Channel Manager] a [!DNL Walmart Marketplace]

Depois de instalar o Gerenciador de Canais na sua instância do [!DNL Commerce], crie um canal de vendas no Gerenciador de Canais e configure as credenciais para conectar [!DNL Channel Manager] a [!DNL Walmart Marketplace].

1. [Crie o canal de vendas](#create-the-sales-channel) selecionando a loja [!DNL Commerce] para as listagens de produtos.

1. [Conectar o canal ao [!DNL Walmart Marketplace] adicionando [!UICONTROL Walmart API credentials]](#connect-the-channel-to-walmart-marketplace).

1. [Conclua a configuração do canal de vendas](#complete-sales-channel-store-setup) para gerenciar listas, estoque, preços e pedidos da sua variedade de produtos [!DNL Walmart Marketplace].

>[!NOTE]
>
>O Gerenciador de Canais requer uma conexão individualizada entre uma conta do Walmart e uma exibição de loja do [!DNL Commerce]. Não é possível conectar a mesma visualização de loja a várias contas do Walmart.

## Criar o canal de vendas

1. No Admin, abra [!DNL Channel Manager] selecionando **[!UICONTROL Marketing** > _Canais _> **Gerenciador de Canais]**.

1. Na seção **[!UICONTROL Marketplaces available to connect]**, selecione **[!UICONTROL Get Started]**.

   ![Conectar novo armazenamento [!DNL Walmart] a [!DNL Channel Manager]](assets/channel-manager-home.png){width="700" zoomable="yes"}

1. Se necessário, configure sua conta do [!DNL Walmart Marketplace Seller].

1. Configure o armazenamento e a conexão:

   - Selecione **[!UICONTROL Add Credentials]**.

   - Selecione a exibição da loja [!DNL Commerce] que oferece os produtos que você deseja vender no marketplace.

     ![Configurar conexão entre [!DNL Commerce] e [!DNL Walmart Marketplace] de [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png){width="500" zoomable="yes"}

   - Digite um **[!UICONTROL store name]** exclusivo.

   - Selecione o **[!UICONTROL Adobe [!DNL Commerce] site]** para listas de produtos e processamento de pedidos.

   - Para receber notificações relacionadas a [!DNL Channel Manager], adicione um **[!UICONTROL email address]**.

1. Conectar o canal a [!DNL Walmart Marketplace].

   - Adicione as credenciais para o [[!DNL Walmart Marketplace Adobe Production API key]](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) da sua conta [!DNL Walmart Marketplace Seller].

   - Se você não tiver as credenciais, obtenha-as de [!DNL Walmart Marketplace Developer Portal] selecionando **[!UICONTROL Get API credentials]**.

     No Portal do desenvolvedor, selecione sua região (EUA e Canadá) e faça logon.

     ![[!DNL Walmart Marketplace] logon da conta](assets/walmart-marketplace-login-page.png){width="600"}

   - No formulário da chave de API, copie e salve os valores **[!UICONTROL Client ID]** e **[!UICONTROL Client Secret]** de [!UICONTROL Adobe Inc Production API key] em um local seguro.

     ![[!DNL Walmart Marketplace API key] página de configuração](assets/walmart-api-key-management-form.png){width="600" zoomable="yes"}

     >[!NOTE]
     >
     >Se a chave [!DNL Adobe Inc] não estiver listada no Portal do Desenvolvedor, selecione **[!UICONTROL Add New Key for a Solution Provider]** para configurar permissões e gerar a chave. Para obter detalhes sobre a configuração, consulte [Gerar um [!DNL Walmart Marketplace API Key]](walmart-requirements.md#generate-a-walmart-marketplace-api-key).

   - Retorne a [!DNL Channel Manager] para adicionar as credenciais às informações de **[!UICONTROL Walmart Connection]**.

     Ao adicionar credenciais, o Adobe oculta o segredo do cliente e armazena o valor em um cofre seguro.

1. Selecione **[!UICONTROL Save Store]** para aplicar a configuração e conectar-se a [!DNL Walmart marketplace].

1. Após se conectar com êxito, [conclua a configuração do repositório](complete-sales-channel-store-setup.md) na página de repositório **[!UICONTROL Channel Manager]**.

![Configurar primeiro armazenamento](assets/channel-manager-setup-first-store.png){width="500" zoomable="yes"}

### Solução de problemas de conexão

Se a conexão com o [!DNL Walmart] falhar, consulte as [Perguntas frequentes sobre o Walmart Marketplace](https://developer.walmart.com/faq/us/faq-auth/){target="_blank"} para obter dicas de solução de problemas.

- Do [!DNL Walmart Developer Portal], verifique se você copiou as credenciais corretas da chave de API de produção para [!UICONTROL Adobe Inc.]

- Verifique se a configuração de acesso para [!UICONTROL Walmart Adobe API key] tem as permissões corretas. Consulte [[!DNL Walmart Requirements]](walmart-requirements.md##generate-a-walmart-marketplace-api-key).

- Confirme se o serviço [!DNL Walmart API] está disponível na [página de status da API do Walmart](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target="_blank"}.
