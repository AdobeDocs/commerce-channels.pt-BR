---
title: "Integrado [!DNL Amazon Sales Channel]"
description: Saiba mais sobre as tarefas de pré-configuração, as etapas de integração e como o Amazon funciona com o Amazon Sales Channel no Adobe Commerce e no Magento Open Source.
redirect_from: /sales-channels/amazon/amazon-onboarding-home.html
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Integrado [!DNL Amazon Sales Channel]

Esta seção descreve as tarefas de pré-configuração, as etapas de integração e alguns conceitos-chave sobre como o Amazon funciona com o canal de vendas do Amazon no Adobe Commerce e no Magento Open Source.

A variável [!DNL Amazon Sales Channel] A extensão do suporta várias lojas Amazon. Por um único [!DNL Amazon Seller Central] conta que opera na região Amazon EUA/Canadá/México, crie três lojas Amazon (uma para vendas dos EUA, do México e do Canadá). Cada uma das três lojas define o país do marketplace durante sua criação. Se tiver mais de um [!DNL Amazon Seller Central] conta, você pode ter até três lojas Amazon para cada uma de suas [!DNL Amazon Seller Central] contas. Se você também vender no Reino Unido, você terá uma quarta loja da Amazon.

>[!TIP]
>
>A [Conta de vendedor profissional](https://sell.amazon.com/){target="_blank"} on [!DNL Amazon Seller Central] in the North America or European (UK) region is required. Amazon charges a monthly subscription and fees for selling. See [Amazon: Choose your selling plan](https://sell.amazon.com/pricing.html){target="_blank"}.<br><br>
>A integração é simples: crie sua loja e conecte-a à sua [!DNL Amazon Seller Central] conta.
>Quando sua loja está conectada, o canal do Amazon tenta importar suas listagens do Amazon e correspondê-las ao catálogo, com base nas [mapeamento de atributo](./attributes-view.md).<br><br>
>As configurações de canal de vendas do Amazon afetam suas listagens do Amazon. Sua lista inicial, preços e configurações do produto são padronizados para você. Você pode modificar o [configurações da loja](./ob-store-review.md) (listagem, preços, pedidos e relatórios) depois que sua loja estiver conectada à [!DNL Amazon Seller Central] conta.

| Etapas | O que acontece |
|--- |--- |
| [Tarefas de Pré-configuração](./amazon-pre-setup-tasks.md) | Antes de integrar, você deve garantir que tem um ativo e aprovado [!DNL Amazon Seller Central] conta. Há também alguns [!DNL Commerce] requisitos e recomendações a serem concluídos antes da integração. |
| [Verifique a chave da API do Amazon](./amazon-verify-api-key.md) | Ao acessar o canal de vendas do Amazon, [!DNL Commerce] O verifica e valida automaticamente a chave de API do Amazon que você adicionou à configuração da loja. Se sua chave de API não tiver sido adicionada ou for inválida, você será solicitado a [adicionar ou atualizar sua chave de API do Amazon](./amazon-verify-api-key.md). |
| [Integração da loja](./store-integration.md) | Essa etapa inclui criar uma loja de canais de vendas da Amazon e conectá-la à [!DNL Amazon Seller Central] conta. Você precisa das credenciais de login principais para seu [!DNL Amazon Seller Central] conta (o email ou telefone usado para criar a conta do vendedor) para essa etapa. |
| [Criar regra de listagem](./ob-create-listing-rule.md) | Depois de conectar sua loja de canais de vendas da Amazon, você será solicitado a criar uma regra de listagem. Essa etapa é recomendada, mas você também pode ignorá-la para iniciar o processo de importação da lista. Você também pode acessar seu [configurações de armazenamento e listagem](./ob-store-review.md) na loja [painel](./amazon-store-dashboard.md). |
