---
title: Integração de loja
description: Antes de iniciar o processo de integração, você deve criar (adicionar) uma loja do Amazon Sales Channel e conectá-la à sua conta do vendedor do Amazon.
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Integração de loja

Para começar a usar o canal de vendas da Amazon, você deve criar (adicionar) uma loja de canais de vendas da Amazon e conectá-la à sua conta de vendedor da Amazon. Essas duas etapas integram suas contas [!DNL Commerce] e Amazon para compartilhar dados, sincronizar produtos e muito mais.

_Você precisa das principais credenciais de logon para sua  [!DNL Amazon Seller Central] conta (o email ou telefone usado para criar a conta do vendedor) para conectar sua loja._

>[!NOTE]
>
>Após a integração da primeira loja, você será solicitado anualmente a renovar a conexão do canal de vendas da Amazon com a Amazon, concedendo acesso novamente. Você pode renovar ou revogar essa autorização na tabela _Autorizações atuais_ na seção _Permissões do desenvolvedor do Amazon MWS_ da **Configurações** > **Permissões do usuário** da sua conta do Vendedor Central.

## Adicionar uma loja da Amazon

1. Na barra lateral _Admin_, vá para **Marketing** > _Canais_ > **Amazon Sales Channel**.

   Ao adicionar seu primeiro armazenamento de canal de vendas do Amazon, o modal _Tarefas de pré-configuração_ é exibido. Após a adição da primeira loja, as tarefas de pré-configuração podem ser acessadas na página inicial do canal de vendas do Amazon](./amazon-sales-channel-home.md) em _Aprendizagem e preparação_ no menu do lado esquerdo.[

1. Clique em **[!UICONTROL Add Amazon Store]**.

   A página _[!UICONTROL Add Amazon sales channel]_é aberta.

   ![Adicionar a loja de canais de vendas da Amazon](assets/amazon-store-integration.png)

1. Para **[!UICONTROL Magento Website to use for Amazon Listing]**, escolha qual dos seus sites [!DNL Commerce] se conectará a este armazenamento de canal de vendas do Amazon.

   Essa configuração também define o armazenamento padrão [!DNL Commerce] para [importar pedidos Amazon](./order-settings.md).

1. Para **[!UICONTROL Email Address]**, insira o endereço de email de contato preferencial.

1. Para **[!UICONTROL New Store Name]**, insira um nome descritivo para o novo armazenamento de canal de vendas da Amazon.

   >[!NOTE]
   >
   >Esse nome é usado somente como uma referência [!DNL Commerce] e identifica a loja na página [inicial do canal de vendas do Amazon](./amazon-sales-channel-home.md). Você quer torná-lo algo que sua equipe possa identificar facilmente. Por exemplo, sua loja Amazon que vende na região dos Estados Unidos pode ser chamada de `Amazon Store USA`.

1. Para **[!UICONTROL Amazon Marketplace Country]**, escolha a região/país na qual esse armazenamento de canal de vendas da Amazon vende produtos. Opções:

   - Estados Unidos
   - Canadá
   - México
   - Reino Unido

1. Na seção _[!UICONTROL Map your Magento attributes to Amazon]_, faça o seguinte:

   - Para **[!UICONTROL Product ID on the Amazon market]**, escolha o atributo Amazon a ser mapeado para o atributo [!DNL Commerce] selecionado abaixo.

      Essa ID ajuda a corresponder corretamente os produtos correspondentes no catálogo [!DNL Commerce].

   - Para **[!UICONTROL Map a Magento attribute]**, escolha o atributo do produto [!DNL Commerce] a ser mapeado para o atributo do Amazon selecionado acima.

      [Mapear ](./ob-creating-magento-attributes.md) atributos ajuda a garantir que sua lista do Amazon corresponda corretamente ao produto correspondente em seu  [!DNL Commerce] catálogo.

1. Clique em **[!UICONTROL Connect]**.

   A caixa de diálogo é fechada e a nova loja é exibida na página inicial do canal de vendas do Amazon](./amazon-sales-channel-home.md) com uma mensagem de confirmação.[

## Conectar um armazenamento a [!DNL Amazon Seller Central]

1. No painel da loja, clique em **[!UICONTROL Connect store]** no cartão da loja para iniciar [!DNL Amazon Seller Central] em uma nova guia.

1. Insira suas credenciais de conta [!DNL Amazon Seller Central] e clique em **[!UICONTROL Sign in]**.

   Para concluir essa conexão, você deve fazer logon em sua conta [!DNL Amazon Seller Central] usando as credenciais de logon do usuário principal (o email ou telefone usado para criar a conta do vendedor).

1. Se solicitado, complete a Autorização de dois fatores do Amazon (2FA) inserindo o código que você recebe do Amazon e clique em **[!UICONTROL Sign in]**.

1. Na página de confirmação _[!UICONTROL Amazon Marketplace Web Service]_, marque a caixa de seleção &quot;[!UICONTROL I understand...]&quot; e clique em **[!UICONTROL Next]**.

1. Na mensagem _[!UICONTROL You are almost done]_, clique em **[!UICONTROL Continue]**.

   Você concedeu permissão de canal de vendas da Amazon para acessar e compartilhar dados com sua conta [!DNL Amazon Seller Central]. A página do Amazon é fechada e uma mensagem de confirmação é exibida.

   A página inicial [do canal de vendas do Amazon](./amazon-sales-channel-home.md) é aberta mostrando seus cartões de loja da Amazon.

   Para exibir o painel da loja, clique em **[!UICONTROL View Store]** no cartão da loja.

![Página inicial do canal de vendas da Amazon com o novo cartão de loja](assets/asc-dashboard-after-2fa.png)

A nova loja de canais de vendas da Amazon agora está conectada à sua conta [!DNL Amazon Seller Central].

![Próximo ](assets/btn-next.png) [**íconeContinuar a criar uma regra de listagem**](./ob-create-listing-rule.md)
