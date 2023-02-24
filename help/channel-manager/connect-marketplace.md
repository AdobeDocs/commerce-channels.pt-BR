---
title: 'Conectar [!DNL Channel Manager] para [!DNL Walmart Marketplace]'
description: "Conectar uma exibição de loja do Commerce a [!DNL Walmart Marketplace] para criar o canal de vendas para gerenciar listas de produtos, inventário, preço e pedidos do Commerce para vendas do Walmart Marketplace."
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Connect [!DNL Channel Manager] para [!DNL Walmart Marketplace]

Depois de instalar o Gerenciador de canais em seu [!DNL Commerce] criar um canal de vendas no Gerenciador de canais e configurar as credenciais para se conectar [!DNL Channel Manager] para [!DNL Walmart Marketplace].

1. [Criar o canal de vendas](#create-the-sales-channel) selecionando o [!DNL Commerce] armazenar para listagens de produtos.

1. [Conecte o canal ao [!DNL Walmart Marketplace] adicionando [!UICONTROL Walmart API credentials]](#connect-the-channel-to-walmart-marketplace).

1. [Configuração completa do canal de vendas](#complete-sales-channel-store-setup) para gerenciar listas, inventário, preços e pedidos de sua [!DNL Walmart Marketplace] sortimento de produto.

>[!NOTE]
>
>O Gerenciador de Canais requer uma conexão um para um entre uma conta Walmart e uma [!DNL Commerce] exibição de loja. Não é possível conectar a mesma exibição de loja a várias contas do Walmart.

## Criar o canal de vendas

1. Em Admin, abra [!DNL Channel Manager] selecionando **[!UICONTROL Marketing** > _Canais _> **Gerenciador de canal]**.

1. No **[!UICONTROL Marketplaces available to connect]** seção , selecione **[!UICONTROL Get Started]**.

   ![Conectar novo [!DNL Walmart] armazenar para [!DNL Channel Manager]](assets/channel-manager-home.png)

1. Se necessário, configure as [!DNL Walmart Marketplace Seller] conta.

1. Configure a loja e a conexão:

   - Selecionar **[!UICONTROL Add Credentials]**.

   - Selecione o [!DNL Commerce] exibição de loja que oferece os produtos que você deseja vender no mercado.

      ![Configurar conexão entre [!DNL Commerce] e [!DNL Walmart Marketplace] from [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png)

   - Insira um **[!UICONTROL store name]**.

   - Selecione o **[!UICONTROL Adobe [!DNL Commerce] site]** para listagens de produtos e processamento de pedidos.

   - Para receber notificações relacionadas a [!DNL Channel Manager], adicione um **[!UICONTROL email address]**.

1. Conecte o canal ao [!DNL Walmart Marketplace].

   - Adicione as credenciais para a [[!DNL Walmart Marketplace Adobe Production API key]](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) do [!DNL Walmart Marketplace Seller] conta.

   - Se você não tiver as credenciais, obtenha-as do [!DNL Walmart Marketplace Developer Portal] selecionando **[!UICONTROL Get API credentials]**.

      No Portal do desenvolvedor, selecione sua região (EUA e Canadá) e faça logon.

      ![[!DNL Walmart Marketplace] logon da conta](assets/walmart-marketplace-login-page.png)

   - No formulário da chave API, copie e salve a variável **[!UICONTROL Client ID]** e **[!UICONTROL Client Secret]** para [!UICONTROL Adobe Inc Production API key] para um local seguro.

      ![[!DNL Walmart Marketplace API key] página de configuração](assets/walmart-api-key-management-form.png)

      >[!NOTE]
      >
      >Se a variável [!DNL Adobe Inc] A chave não está listada no Portal do desenvolvedor, selecione **[!UICONTROL Add New Key for a Solution Provider]** para configurar permissões e gerar a chave. Para obter detalhes de configuração, consulte [Gerar um [!DNL Walmart Marketplace API Key]](walmart-requirements.md#generate-a-walmart-marketplace-api-key).

   - Retornar para [!DNL Channel Manager] para adicionar as credenciais ao **[!UICONTROL Walmart Connection]** informações.

      Ao adicionar credenciais, o Adobe oculta o segredo do cliente e armazena o valor em um cofre seguro.

1. Selecionar **[!UICONTROL Save Store]** para aplicar a configuração e conectar-se ao [!DNL Walmart marketplace].

1. Após a conexão bem-sucedida, [configuração completa do armazenamento](complete-sales-channel-store-setup.md) do **[!UICONTROL Channel Manager]** página de armazenamento.

![Configurar primeira loja](assets/channel-manager-setup-first-store.png)

### Solução de problemas de conexão

Se a conexão com [!DNL Walmart] falha, consulte o [Perguntas frequentes sobre o Walmart Marketplace](https://developer.walmart.com/faq/us/faq-auth/){target="_blank"} para obter dicas sobre solução de problemas.

- No [!DNL Walmart Developer Portal], verifique se você copiou as credenciais corretas para a chave da API de produção do para o [!UICONTROL Adobe Inc.]

- Verifique se a configuração de acesso para a variável [!UICONTROL Walmart Adobe API key] O tem as permissões corretas. Consulte [[!DNL Walmart Requirements]](walmart-requirements.md##generate-a-walmart-marketplace-api-key).

- Confirme se a variável [!DNL Walmart API] está disponível no [Página de status da API Walmart](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target="_blank"}.
