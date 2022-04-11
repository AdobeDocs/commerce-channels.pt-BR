---
title: Conectar canal de vendas ao [!DNL Walmart Marketplace]
description: Configure o canal de vendas e conecte-se ao Walmart Marketplace.
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
source-git-commit: e6368d30e16ccffcb1dfc64bdd56561116934b54
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---


# Conectar canal de vendas ao [!DNL Walmart Marketplace]

Depois de instalar o Gerenciador de canais em seu [!DNL Commerce] conecte uma loja do Commerce ao Walmart Marketplace.

1. [Criar o canal de vendas](#create-the-sales-channel) selecionando a loja Comércio para ver as listas de produtos.

1. [Conecte o canal ao [!DNL Walmart Marketplace] adicionando credenciais da API do Walmart](#connect-the-channel-to-walmart-marketplace).

1. [Configuração completa do canal de vendas](#complete-store-setup) para gerenciar listas, inventário, preços e pedidos para o seu sortimento de produto do Walmart Marketplace.

## Criar o canal de vendas

1. Abrir [!DNL Channel Manager].

   - Em Admin, selecione **[!UICONTROL Marketing** > _Canais _> **Gerenciador de canal]**.

   - Selecionar **[!UICONTROL Connect New Store]**.

      ![Conexão da loja do Commerce ao [!DNL Walmart Marketplace] from [!DNL Channel Manager]](assets/connect-commerce-store-to-marketplace.png)


1. Configure a loja e a conexão:

   - Insira um **[!UICONTROL store name]**.

   - Selecione o **[!UICONTROL Adobe Commerce site]** para listas de produtos.

   - Adicione um **[!UICONTROL email address]** para receber notificações de serviço relacionadas a [!DNL Channel Manager].

      ![Configurar a conexão entre o Commerce e o [!DNL Walmart Marketplace] from [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png)

## Conecte o canal ao Walmart Marketplace

1. Adicione as credenciais para a [[!DNL Walmart Marketplace Adobe Production API key]](connect-marketplace.md#generate-a-walmart-marketplace-production-api-key) do [!DNL Walmart Marketplace Seller] conta.

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

1. Selecionar [!UICONTROL Save] para aplicar a configuração e conectar-se ao [!DNL Walmart marketplace].

Depois de se conectar com êxito, gerencie o canal de **[!UICONTROL Channel Manager > Marketplace Stores]**.

![[!DNL Walmart Marketplace API key] página de configuração](assets/manage-connected-stores.png)


### Solução de problemas de conexão

Se a conexão com o Walmart falhar, consulte o [Perguntas frequentes sobre o Walmart Marketplace](https://developer.walmart.com/faq/us/faq-auth/){target=&quot;_blank&quot;} para dicas de solução de problemas.

- No [!DNL Walmart Developer Portal], verifique se você copiou as credenciais corretas para a chave da API de produção do para o [!UICONTROL Adobe Inc.]

- Verifique se a configuração de acesso da chave de API do Adobe Walmart tem as permissões corretas. Consulte [Pré-requisitos do Walmart](walmart-prerequisites.md##generate-a-walmart-marketplace-api-key).

- Confirme se a variável [!DNL Walmart API] está disponível no [Página de status da API Walmart](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target=&quot;_blank&quot;}.

## Configuração completa da loja

Depois de conectar uma loja do Commerce a [!DNL Walmart Marketplace], você pode concluir a configuração de armazenamento no [!DNL Channel Manager Stores] exibir.

Para concluir a configuração da loja:

1. Em Admin, selecione **[!UICONTROL Marketing** > **Gerenciador de canais**].

   ![[!DNL Walmart Marketplace API key] página de configuração](assets/connect-commerce-store-config.png)

1. Abra um canal de vendas conectado selecionando o ícone de lápis na linha de entrada da loja.

1. Iniciar operações de canal de vendas.

   - [Adicionar produtos do seu Catálogo de Comércio ao Gerenciador de Canais](add-products-to-connected-channel.md)

   - [Publicar produtos no Walmart usando a correspondência de produtos](publish-listings-to-marketplace.md)

   - [Exibir e gerenciar inventário e preços](inventory-and-price-updates.md)

   - Exibir e gerenciar pedidos do Walmart pelo Administrador do Commerce
