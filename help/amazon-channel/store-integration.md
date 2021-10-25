---
title: Integração de loja
description: Antes de iniciar o processo de integração, você deve criar (adicionar) uma loja do Amazon Sales Channel e conectá-la à sua conta do vendedor do Amazon.
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# Integração de loja

Para começar a usar o canal de vendas da Amazon, você deve criar (adicionar) uma loja de canais de vendas da Amazon e conectá-la à sua conta de vendedor da Amazon. Essas duas etapas integram o [!DNL Commerce] e contas da Amazon para compartilhar dados, sincronizar produtos e muito mais.

_Você precisa das principais credenciais de logon para sua [!DNL Amazon Seller Central] conta (o email ou telefone usado para criar a conta do vendedor) para conectar sua loja._

>[!NOTE]
>
>Após a integração da primeira loja, você será solicitado anualmente a renovar a conexão do canal de vendas da Amazon com a Amazon, concedendo acesso novamente. Você pode renovar ou revogar esta autorização no _Autorizações atuais_ na tabela _Permissões do desenvolvedor do Amazon MWS_ da seção **Configurações** > **Permissões do usuário** página da sua conta do Seller Central.

## Adicionar uma loja da Amazon

1. No _Administrador_ barra lateral, vá para **Marketing** > _Canais_ > **Sales Channel Amazon**.

   Ao adicionar seu primeiro armazenamento de canal de vendas da Amazon, a variável _Tarefas de pré-configuração_ será exibido. Após a adição da primeira loja, as tarefas de pré-configuração podem ser acessadas na [Página inicial do canal de vendas da Amazon](./amazon-sales-channel-home.md) página abaixo _Aprendizagem e preparação_ no menu à esquerda.

1. Clique em **[!UICONTROL Add Amazon Store]**.

   O _[!UICONTROL Add Amazon sales channel]_será aberta.

   ![Adicionar a loja de canais de vendas da Amazon](assets/amazon-store-integration.png)

1. Para **[!UICONTROL Magento Website to use for Amazon Listing]** escolha qual das [!DNL Commerce] sites a serem conectados para esta loja de canais de vendas da Amazon.

   Essa configuração também define o padrão [!DNL Commerce] armazenar para [importar pedidos Amazon](./order-settings.md).

1. Para **[!UICONTROL Email Address]**, insira o endereço de email de contato preferencial.

1. Para **[!UICONTROL New Store Name]**, insira um nome descritivo para o novo armazenamento de canal de vendas da Amazon.

   >[!NOTE]
   >
   >Este nome é usado como um [!DNL Commerce] somente referência e identifica a loja na [Página inicial do canal de vendas da Amazon](./amazon-sales-channel-home.md) página. Você quer torná-lo algo que sua equipe possa identificar facilmente. Por exemplo, a loja da Amazon que vende na região dos Estados Unidos pode ter o nome `Amazon Store USA`.

1. Para **[!UICONTROL Amazon Marketplace Country]**, escolha a região/país em que o armazenamento de canal de vendas da Amazon vende produtos. Opções:

   - Estados Unidos
   - Canadá
   - México
   - Reino Unido

1. No _[!UICONTROL Map your Magento attributes to Amazon]_faça o seguinte:

   - Para **[!UICONTROL Product ID on the Amazon market]**, escolha o atributo do Amazon para mapear para a variável [!DNL Commerce] atributo selecionado abaixo.

      Essa ID ajuda a corresponder corretamente aos produtos correspondentes na sua [!DNL Commerce] catálogo.

   - Para **[!UICONTROL Map a Magento attribute]**, escolha o [!DNL Commerce] atributo do produto para mapear para o atributo do Amazon selecionado acima.

      [Mapeamento de atributos](./ob-creating-magento-attributes.md) ajuda a garantir que sua lista do Amazon corresponda corretamente ao produto correspondente em sua [!DNL Commerce] catálogo.

1. Clique em **[!UICONTROL Connect]**.

   A caixa de diálogo é fechada e a nova loja é exibida na [Página inicial do canal de vendas da Amazon](./amazon-sales-channel-home.md) com uma mensagem de confirmação.

## Conectar uma loja a [!DNL Amazon Seller Central]

1. No painel da loja, clique em **[!UICONTROL Connect store]** no cartão de loja para iniciar [!DNL Amazon Seller Central] em uma nova guia.

1. Insira seu [!DNL Amazon Seller Central] credenciais da conta e clique em **[!UICONTROL Sign in]**.

   Para concluir essa conexão, você deve fazer logon no [!DNL Amazon Seller Central] conta usando as credenciais de logon do usuário principal (o email ou telefone usado para criar a conta do vendedor).

1. Se solicitado, complete a Autorização de dois fatores do Amazon (2FA) inserindo o código que você recebe do Amazon e clique em **[!UICONTROL Sign in]**.

1. No _[!UICONTROL Amazon Marketplace Web Service]_na página de confirmação, selecione o &quot;[!UICONTROL I understand...]&quot; caixa de seleção e clique em **[!UICONTROL Next]**.

1. No _[!UICONTROL You are almost done]_mensagem, clique em **[!UICONTROL Continue]**.

   Você concedeu permissão de canal de vendas da Amazon para acessar e compartilhar dados com seu [!DNL Amazon Seller Central] conta. A página do Amazon é fechada e uma mensagem de confirmação é exibida.

   O [Página inicial do canal de vendas da Amazon](./amazon-sales-channel-home.md) é aberta mostrando os cartões da loja da Amazon.

   Para exibir o painel da loja, clique em **[!UICONTROL View Store]** no cartão da loja.

![Página inicial do canal de vendas da Amazon com o novo cartão de loja](assets/asc-dashboard-after-2fa.png)

Sua nova loja de canais de vendas da Amazon agora está conectada a seu [!DNL Amazon Seller Central] conta.

![Ícone Próximo](assets/btn-next.png) [**Continuar a criar uma regra de listagem**](./ob-create-listing-rule.md)
