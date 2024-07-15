---
title: Integração de armazenamento com um  [!DNL Amazon Seller Account]
description: Antes de iniciar o processo de integração, você deve criar (adicionar) um armazenamento de Sales Channel da Amazon e conectá-lo à sua conta de vendedor da Amazon.
role: Admin, Developer
feature: Sales Channels, Configuration, Integration, Tools and External Services
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# Integração de armazenamento com um [!DNL Amazon Seller Account]

Para começar a usar o canal de vendas da Amazon, você deve criar (adicionar) uma loja de canais de vendas da Amazon e conectá-la ao seu [!DNL Amazon Seller Account]. Essas duas etapas integram suas contas do [!DNL Commerce] e do Amazon para compartilhar dados, sincronizar produtos e muito mais.

_Você precisa das credenciais de logon principais da sua conta do [!DNL Amazon Seller Central] (o email ou o telefone usado para criar a conta do vendedor) para conectar sua loja._

>[!NOTE]
>
>Após a primeira integração da loja, você será solicitado anualmente a renovar sua conexão do canal de vendas da Amazon com o Amazon, concedendo o acesso novamente. Você pode renovar ou revogar esta autorização na tabela _Autorizações Atuais_ da seção _Permissões para Desenvolvedores do Amazon MWS_ da página **Configurações** > **Permissões de Usuário** da sua conta da Central de Vendas.

## Adicionar uma loja da Amazon

1. Na barra lateral _Admin_, vá para **Marketing** > _Canais_ > **Sales Channel Amazon**.

   Ao adicionar seu primeiro armazenamento de canal de vendas do Amazon, o modal _Tarefas de pré-configuração_ é exibido. Após adicionar sua primeira loja, as tarefas de pré-configuração podem ser acessadas na [página inicial do canal de vendas do Amazon](./amazon-sales-channel-home.md) em _Aprendizado e preparação_ no menu à esquerda.

1. Clique em **[!UICONTROL Add Amazon Store]**.

   A página _[!UICONTROL Add Amazon sales channel]_é aberta.

   ![Adicionar o armazenamento do canal de vendas da Amazon](assets/amazon-store-integration.png){width="500" zoomable="yes"}

1. Para **[!UICONTROL Magento Website to use for Amazon Listing]**, escolha qual dos sites do [!DNL Commerce] você quer conectar para esta loja de canais de vendas da Amazon.

   Essa configuração também define o armazenamento [!DNL Commerce] padrão para [importar pedidos do Amazon](./order-settings.md).

1. Para **[!UICONTROL Email Address]**, insira seu endereço de email de contato preferido.

1. Para **[!UICONTROL New Store Name]**, insira um nome descritivo para sua nova loja de canais de vendas da Amazon.

   >[!NOTE]
   >
   >Esse nome é usado como uma referência somente para [!DNL Commerce] e identifica a loja na página inicial do [canal de vendas do Amazon](./amazon-sales-channel-home.md). Você quer fazer disso algo que sua equipe possa identificar facilmente. Por exemplo, sua loja Amazon que vende na região dos Estados Unidos pode se chamar `Amazon Store USA`.

1. Para **[!UICONTROL Amazon Marketplace Country]**, escolha a região/país em que esta loja de canais de vendas da Amazon vende produtos. Opções:

   - Estados Unidos
   - Canadá
   - México
   - Reino Unido

1. Na seção _[!UICONTROL Map your Magento attributes to Amazon]_, faça o seguinte:

   - Para **[!UICONTROL Product ID on the Amazon market]**, escolha o atributo Amazon a ser mapeado para o atributo [!DNL Commerce] selecionado abaixo.

     Esta ID ajuda a corresponder corretamente os produtos correspondentes no catálogo [!DNL Commerce].

   - Para **[!UICONTROL Map a Magento attribute]**, escolha o atributo de produto [!DNL Commerce] a ser mapeado para o atributo de Amazon selecionado acima.

     [Os atributos de mapeamento](./ob-creating-magento-attributes.md) ajudam a garantir que sua lista do Amazon corresponda corretamente ao produto correspondente no catálogo [!DNL Commerce].

1. Clique em **[!UICONTROL Connect]**.

   A caixa de diálogo é fechada e a nova loja aparece na [página inicial do canal de vendas do Amazon](./amazon-sales-channel-home.md) com uma mensagem de confirmação.

## Conectar um armazenamento a [!DNL Amazon Seller Central]

1. No painel da loja, clique em **[!UICONTROL Connect store]** no cartão da loja para iniciar [!DNL Amazon Seller Central] em uma nova guia.

1. Insira suas credenciais de conta do [!DNL Amazon Seller Central] e clique em **[!UICONTROL Sign in]**.

   Para concluir esta conexão, você deve entrar em sua conta do [!DNL Amazon Seller Central] usando as credenciais de logon do usuário principal (o email ou o telefone usado para criar a conta do vendedor).

1. Se solicitado, complete o Amazon Two-Fator Authorization (2FA) inserindo o código recebido do Amazon e clique em **[!UICONTROL Sign in]**.

1. Na página de confirmação _[!UICONTROL Amazon Marketplace Web Service]_, marque a caixa de seleção &quot;[!UICONTROL I understand...]&quot; e clique em **[!UICONTROL Next]**.

1. Na mensagem _[!UICONTROL You are almost done]_, clique em **[!UICONTROL Continue]**.

   Você concedeu ao canal de vendas da Amazon permissão para acessar e compartilhar dados com sua conta [!DNL Amazon Seller Central]. A página do Amazon é fechada e uma mensagem de confirmação é exibida.

   A página inicial do [canal de vendas do Amazon](./amazon-sales-channel-home.md) é aberta, mostrando seus cartões de loja da Amazon.

   Para exibir o painel da loja, clique em **[!UICONTROL View Store]** no cartão da loja.

![página inicial do canal de vendas da Amazon com novo cartão de loja](assets/asc-dashboard-after-2fa.png){width="600" zoomable="yes"}

Sua nova loja de canais de vendas da Amazon agora está conectada à sua conta [!DNL Amazon Seller Central].

![Próximo ícone](assets/btn-next.png) [**Continuar para Criar uma Regra de Listagem**](./ob-create-listing-rule.md)
