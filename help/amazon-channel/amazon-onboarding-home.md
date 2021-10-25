---
title: Sales Channel Amazon integrado
description: Saiba mais sobre as tarefas de pré-configuração, as etapas de integração e como o Amazon funciona com o Amazon Sales Channel no Adobe Commerce e no Magento Open Source.
redirect_from: /sales-channels/amazon/amazon-onboarding-home.html
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Canal de vendas integrado da Amazon

Esta seção descreve as tarefas de pré-configuração, as etapas de integração e alguns conceitos-chave de como o Amazon funciona com o canal de vendas da Amazon no Adobe Commerce e no Magento Open Source.

O [!DNL Amazon Sales Channel] A extensão oferece suporte a várias lojas Amazon. Para um único [!DNL Amazon Seller Central] Uma conta que opera na região Amazon EUA/Canadá/México, cria três lojas Amazon (uma para cada vendas dos EUA, vendas do México e vendas do Canadá). Cada uma das três lojas define o país do marketplace durante sua criação. Se você tiver mais de um [!DNL Amazon Seller Central] pode ter até três lojas Amazon para cada uma de suas [!DNL Amazon Seller Central] contas. Se você também vendesse no Reino Unido, você teria uma quarta loja da Amazon.

>[!TIP]
>
>A [Conta do vendedor profissional](https://sell.amazon.com/){target=&quot;_blank&quot;} em [!DNL Amazon Seller Central] na América do Norte ou na região europeia (Reino Unido). A Amazon cobra uma assinatura mensal e as tarifas de venda. Consulte [Amazon: Escolha seu plano de venda](https://sell.amazon.com/pricing.html){target=&quot;_blank&quot;}.<br><br>
>A integração é simples — crie sua loja e depois a conecte à sua [!DNL Amazon Seller Central] conta.
>Quando a loja está conectada, o canal Amazon tenta importar as listagens do Amazon e associá-las ao catálogo, com base em [mapeamento de atributo](./attributes-view.md).<br><br>
>As configurações de canal de vendas da Amazon afetam as listagens da Amazon. Sua listagem inicial, os preços e as configurações do produto são padronizados para você. Você pode modificar [configurações de armazenamento](./ob-store-review.md) (listagem, preços, pedido e relatórios) após a loja estar conectada a sua [!DNL Amazon Seller Central] conta.

| Etapas | O que acontece |
|--- |--- |
| [Tarefas de pré-configuração](./amazon-pre-setup-tasks.md) | Antes de integrar, você deve garantir que tem um ativo e aprovado [!DNL Amazon Seller Central] conta. Há também alguns [!DNL Commerce] requisitos e recomendações a serem concluídos antes da integração. |
| [Verifique a chave da API do Amazon](./amazon-verify-api-key.md) | Ao acessar o canal de vendas da Amazon, [!DNL Commerce] verifica e valida automaticamente a chave da API do Amazon adicionada na configuração da loja. Se a chave da API não tiver sido adicionada ou for inválida, você será solicitado a [adicionar ou atualizar sua chave de API do Amazon](./amazon-verify-api-key.md). |
| [Integração de loja](./store-integration.md) | Esta etapa inclui a criação de uma loja de canais de vendas da Amazon e a conexão com seu [!DNL Amazon Seller Central] conta. Você precisa das principais credenciais de logon para sua [!DNL Amazon Seller Central] conta (o email ou telefone usado para criar a conta do vendedor) para esta etapa. |
| [Criar Regra de Listagem](./ob-create-listing-rule.md) | Depois de conectar a loja de canais de vendas da Amazon, você será solicitado a criar uma regra de listagem. Essa etapa é incentivada, mas também é possível ignorá-la para iniciar o processo de importação da listagem. Você também pode acessar seu [configurações de armazenamento e listagem](./ob-store-review.md) na loja [painel](./amazon-store-dashboard.md). |
