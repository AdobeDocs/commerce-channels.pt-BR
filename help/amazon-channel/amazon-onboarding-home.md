---
title: Sales Channel Amazon integrado
description: Saiba mais sobre as tarefas de pré-configuração, as etapas de integração e como o Amazon funciona com o Amazon Sales Channel no Adobe Commerce e Magento Open Source.
redirect_from: /sales-channels/amazon/amazon-onboarding-home.html
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Canal de vendas integrado da Amazon

Esta seção descreve as tarefas de pré-configuração, as etapas de integração e alguns conceitos-chave de como o Amazon funciona com o canal de vendas da Amazon no Adobe Commerce e Magento Open Source.

A extensão [!DNL Amazon Sales Channel] oferece suporte a várias lojas Amazon. Para uma única conta [!DNL Amazon Seller Central] que opera na região Amazon EUA/Canadá/México, crie três lojas Amazon (uma para vendas dos EUA, vendas do México e vendas do Canadá). Cada uma das três lojas define o país do marketplace durante sua criação. Se você tiver mais de uma conta [!DNL Amazon Seller Central], poderá ter até três lojas Amazon para cada uma de suas contas [!DNL Amazon Seller Central]. Se você também vendesse no Reino Unido, você teria uma quarta loja da Amazon.

>[!TIP]
>
>É necessária uma [Conta de Vendedor Profissional](https://sell.amazon.com/){target=&quot;_blank&quot;} em [!DNL Amazon Seller Central] na região da América do Norte ou da Europa (UK). A Amazon cobra uma assinatura mensal e as tarifas de venda. Consulte [Amazon: Escolha seu plano de venda](https://sell.amazon.com/pricing.html){target=&quot;_blank&quot;}.<br><br>
>A integração é simples — crie sua loja e conecte-a à sua conta [!DNL Amazon Seller Central].
>Quando sua loja está conectada, o canal Amazon tenta importar suas listagens do Amazon e associá-las ao catálogo, com base no [mapeamento de atributo](./attributes-view.md).<br><br>
>As configurações de canal de vendas da Amazon afetam as listagens da Amazon. Sua listagem inicial, os preços e as configurações do produto são padronizados para você. Você pode modificar suas [configurações de armazenamento](./ob-store-review.md) (listagem, preço, pedido e relatórios) depois que sua loja estiver conectada à sua conta [!DNL Amazon Seller Central].

| Etapas | O que acontece |
|--- |--- |
| [Tarefas de pré-configuração](./amazon-pre-setup-tasks.md) | Antes de integrar, você deve garantir que tenha uma conta ativa e aprovada [!DNL Amazon Seller Central]. Também há alguns [!DNL Commerce] requisitos e recomendações a serem concluídos antes da integração. |
| [Verifique a chave da API do Amazon](./amazon-verify-api-key.md) | Ao acessar o canal de vendas da Amazon, [!DNL Commerce] verifica e valida automaticamente a chave de API do Amazon adicionada na configuração da loja. Se a chave da API não tiver sido adicionada ou for inválida, você será solicitado a [adicionar ou atualizar a chave de API do Amazon](./amazon-verify-api-key.md). |
| [Integração de loja](./store-integration.md) | Esta etapa inclui a criação de um armazenamento de canal de vendas da Amazon e a conexão com sua conta [!DNL Amazon Seller Central]. Você precisa das principais credenciais de logon para sua conta [!DNL Amazon Seller Central] (o email ou telefone usado para criar a conta do vendedor) para esta etapa. |
| [Criar Regra de Listagem](./ob-create-listing-rule.md) | Depois de conectar a loja de canais de vendas da Amazon, você será solicitado a criar uma regra de listagem. Essa etapa é incentivada, mas também é possível ignorá-la para iniciar o processo de importação da listagem. Você também pode acessar seu [armazenamento e listar configurações](./ob-store-review.md) no armazenamento [painel](./amazon-store-dashboard.md). |
