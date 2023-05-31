---
title: Integração da loja com um [!DNL Amazon Seller Account]
description: Antes de iniciar o processo de integração, você deve criar (adicionar) um armazenamento de Sales Channel da Amazon e conectá-lo à sua conta de vendedor da Amazon.
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# Integração da loja com um [!DNL Amazon Seller Account]

Para começar a usar o canal de vendas da Amazon, você deve criar (adicionar) uma loja de canais de vendas da Amazon e conectá-la à [!DNL Amazon Seller Account]. Essas duas etapas integram o seu [!DNL Commerce] e contas do Amazon para compartilhar dados, sincronizar produtos e muito mais.

_Você precisa das credenciais de login principais para seu [!DNL Amazon Seller Central] conta (o email ou telefone usado para criar a conta do vendedor) para conectar sua loja._

>[!NOTE]
>
>Após a primeira integração da loja, você será solicitado anualmente a renovar sua conexão do canal de vendas da Amazon com o Amazon, concedendo o acesso novamente. Você pode renovar ou revogar essa autorização na _Autorizações atuais_ tabela no _Permissões de desenvolvedor do Amazon MWS_ seção do **Configurações** > **Permissões de usuário** página da sua conta da Central de Vendedores.

## Adicionar uma loja da Amazon

1. No _Admin_ barra lateral, vá para **Marketing** > _Canais_ > **Sales Channel Amazon**.

   Ao adicionar sua primeira loja de canais de vendas da Amazon, a variável _Tarefas de Pré-configuração_ será exibida. Após adicionar sua primeira loja, as tarefas de pré-configuração podem ser acessadas no [Página inicial do canal de vendas do Amazon](./amazon-sales-channel-home.md) página abaixo _Aprendizagem e preparação_ no menu do lado esquerdo.

1. Clique em **[!UICONTROL Add Amazon Store]**.

   A variável _[!UICONTROL Add Amazon sales channel]_é aberta.

   ![Adicionar a loja de canal de vendas da Amazon](assets/amazon-store-integration.png){width="500" zoomable="yes"}

1. Para **[!UICONTROL Magento Website to use for Amazon Listing]**, escolha qual dos seus [!DNL Commerce] sites a serem conectados nesta loja de canais de vendas da Amazon.

   Essa configuração também define o padrão [!DNL Commerce] armazenar para [importação de ordens do Amazon](./order-settings.md).

1. Para **[!UICONTROL Email Address]**, digite seu endereço de email de contato preferido.

1. Para **[!UICONTROL New Store Name]**, digite um nome descritivo para sua nova loja de canais de vendas da Amazon.

   >[!NOTE]
   >
   >Este nome é usado como um [!DNL Commerce] somente referência e identifica o armazenamento no [Página inicial do canal de vendas do Amazon](./amazon-sales-channel-home.md) página. Você quer fazer disso algo que sua equipe possa identificar facilmente. Por exemplo, sua loja da Amazon que vende na região dos Estados Unidos pode ter o nome `Amazon Store USA`.

1. Para **[!UICONTROL Amazon Marketplace Country]**, escolha a região/país em que esta loja do Amazon sales channel vende os produtos. Opções:

   - Estados Unidos
   - Canadá
   - México
   - Reino Unido

1. No _[!UICONTROL Map your Magento attributes to Amazon]_faça o seguinte:

   - Para **[!UICONTROL Product ID on the Amazon market]**, escolha o atributo do Amazon a ser mapeado para a variável [!DNL Commerce] atributo selecionado abaixo.

      Essa ID ajuda a corresponder corretamente os produtos correspondentes em seu [!DNL Commerce] catálogo.

   - Para **[!UICONTROL Map a Magento attribute]**, escolha o [!DNL Commerce] atributo de produto a ser mapeado para o atributo Amazon selecionado acima.

      [Mapeamento de atributos](./ob-creating-magento-attributes.md) ajuda a garantir que sua lista do Amazon corresponda corretamente ao produto correspondente em sua [!DNL Commerce] catálogo.

1. Clique em **[!UICONTROL Connect]**.

   A caixa de diálogo é fechada e o novo armazenamento é exibido no [Página inicial do canal de vendas do Amazon](./amazon-sales-channel-home.md) com uma mensagem de confirmação.

## Conectar uma loja a [!DNL Amazon Seller Central]

1. No painel da loja, clique em **[!UICONTROL Connect store]** no cartão de loja a ser iniciado [!DNL Amazon Seller Central] em uma nova guia.

1. Insira seu [!DNL Amazon Seller Central] credenciais da conta e clique em **[!UICONTROL Sign in]**.

   Para concluir esta conexão, você deve entrar no seu [!DNL Amazon Seller Central] usando as credenciais de logon do usuário principal (o email ou telefone usado para criar a conta do vendedor).

1. Se solicitado, complete a Amazon Two-Fator Authorization (2FA) inserindo o código recebido da Amazon e clique em **[!UICONTROL Sign in]**.

1. No _[!UICONTROL Amazon Marketplace Web Service]_confirmação, selecione a opção &quot;[!UICONTROL I understand...]&quot; e clique em **[!UICONTROL Next]**.

1. No _[!UICONTROL You are almost done]_clique em **[!UICONTROL Continue]**.

   Você concedeu ao canal de vendas da Amazon permissão para acessar e compartilhar dados com a [!DNL Amazon Seller Central] conta. A página do Amazon é fechada e uma mensagem de confirmação é exibida.

   A variável [Página inicial do canal de vendas do Amazon](./amazon-sales-channel-home.md) será aberta mostrando seus cartões de loja da Amazon.

   Para exibir o painel da loja, clique em **[!UICONTROL View Store]** no cartão de loja.

![Página inicial do canal de vendas da Amazon com o novo cartão de loja](assets/asc-dashboard-after-2fa.png){width="600" zoomable="yes"}

Sua nova loja de canais de vendas da Amazon agora está conectada ao seu [!DNL Amazon Seller Central] conta.

![Ícone Avançar](assets/btn-next.png) [**Continuar para criar uma regra de listagem**](./ob-create-listing-rule.md)
