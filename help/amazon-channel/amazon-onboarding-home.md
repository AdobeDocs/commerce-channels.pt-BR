---
title: "Integrar [!DNL Amazon Sales Channel]"
description: Saiba mais sobre as tarefas de pré-configuração, as etapas de integração e como o Amazon funciona com o Amazon Sales Channel no Adobe Commerce e no Magento Open Source.
role: Leader, Admin, User
feature: Sales Channels, Integration, Tools and External Services
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: 6321f17c0e6f9e86bb3f5755dc7710fa68d68b0d
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Integrar [!DNL Amazon Sales Channel]

Esta seção descreve as tarefas de pré-configuração, as etapas de integração e alguns conceitos-chave sobre como o Amazon funciona com o canal de vendas do Amazon no Adobe Commerce e no Magento Open Source.

A extensão [!DNL Amazon Sales Channel] dá suporte a vários armazenamentos Amazon. Para uma única conta do [!DNL Amazon Seller Central] que opera na região Amazon EUA/Canadá/México, crie três lojas Amazon (uma para vendas dos EUA, do México e do Canadá). Cada uma das três lojas define o país do marketplace durante sua criação. Se você tiver mais de uma conta [!DNL Amazon Seller Central], poderá ter até três lojas Amazon para cada uma de suas contas [!DNL Amazon Seller Central]. Se você também vender no Reino Unido, você terá uma quarta loja da Amazon.

>[!TIP]
>
>É necessária uma [Conta de vendedor profissional](https://sell.amazon.com/){target="_blank"} em [!DNL Amazon Seller Central] na América do Norte ou na região da Europa (Reino Unido). A Amazon cobra uma assinatura mensal e taxas de venda. Consulte [Amazon: escolha seu plano de vendas](https://sell.amazon.com/pricing.html){target="_blank"}.<br><br>
>A integração é simples: crie seu armazenamento e conecte-o à sua conta do [!DNL Amazon Seller Central].
>Quando seu armazenamento está conectado, o canal do Amazon tenta importar suas listas do Amazon e correspondê-las ao seu catálogo, com base no seu [mapeamento de atributos](./attributes-view.md).<br><br>
>As configurações de canal de vendas do Amazon afetam suas listagens do Amazon. Sua lista inicial, preços e configurações do produto são padronizados para você. Você pode modificar suas [configurações da loja](./ob-store-review.md) (listagem, preços, pedidos e relatórios) depois que a loja estiver conectada à sua conta do [!DNL Amazon Seller Central].

| Etapas | O que acontece |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tarefas de pré-configuração](./amazon-pre-setup-tasks.md) | Antes de integrar, verifique se você tem uma conta [!DNL Amazon Seller Central] ativa e aprovada. Também há alguns [!DNL Commerce] requisitos e recomendações a serem concluídos antes da integração. |
| [Verificar a Chave de API do Amazon](./amazon-verify-api-key.md) | Ao acessar o canal de vendas do Amazon, o [!DNL Commerce] verifica e valida automaticamente a chave de API do Amazon que você adicionou à configuração da loja. Se sua chave de API não tiver sido adicionada ou for inválida, você será solicitado a [adicionar ou atualizar sua Chave de API do Amazon](./amazon-verify-api-key.md). |
| [Integração de armazenamento](./store-integration.md) | Esta etapa inclui a criação de uma loja de canais de vendas da Amazon e a conexão à sua conta do [!DNL Amazon Seller Central]. Você precisa das credenciais de logon principais para sua conta do [!DNL Amazon Seller Central] (o email ou telefone usado para criar a conta do vendedor) para esta etapa. |
| [Criar Regra de Listagem](./ob-create-listing-rule.md) | Depois de conectar sua loja de canais de vendas da Amazon, você será solicitado a criar uma regra de listagem. Essa etapa é recomendada, mas você também pode ignorá-la para iniciar o processo de importação da lista. Você também pode acessar suas [configurações de armazenamento e listagem](./ob-store-review.md) no [painel](./amazon-store-dashboard.md) do armazenamento. |
