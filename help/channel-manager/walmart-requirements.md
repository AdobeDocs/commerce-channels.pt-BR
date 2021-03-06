---
title: '''[!DNL Walmart] Requisitos"'
description: '"Verifique se você tem o [!DNL Walmart Marketplace]informações e recursos para integrar com o Gerenciador de Canais."'
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: 4f0c40d7bcd05f7c8708d0d339cc29d920d646d5
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# [!DNL Walmart] requisitos

[!DNL Channel Manager] requer os seguintes recursos e informações para configurar um [!DNL Commerce] canal de vendas para [!DNL Walmart Marketplace.]

* Aprovação para venda [!DNL Walmart] e credenciais para fazer logon na conta do vendedor do Marketplace registrada

* Uma chave de API para conectar o Adobe Commerce ou o Magento Open Source ao [!DNL Walmart Marketplace]

   O [!DNL Walmart Marketplace] A chave de API habilita a integração entre [!DNL Channel Manager] para Adobe [!DNL Commerce] ou o Magento Open Source e o Walmart Marketplace. Configure a chave da API no Seller Central antes de iniciar o processo de integração do Gerenciador de canais.

## Configure um [!DNL Walmart Seller] account

1. [Envie seu aplicativo Walmart](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI).
1. Depois de obter a homologação de [!DNL Walmart], [configurar sua conta do Walmart](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

## Gerar um [!DNL Walmart Marketplace] Chave da API de produção

1. Ir para [!DNL Walmart Marketplace] para gerar um [chave da API de produção do provedor de soluções para Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. Crie a chave e configure as permissões:

   * Selecione Adobe como o provedor de soluções.

   * Defina as permissões conforme mostrado na tabela a seguir. Para obter detalhes, consulte [Credenciais da API](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) no _Ajuda do vendedor do Walmart_.

   **Configuração de chave de API do Adobe para Walmart**

   | **Permissão** | **Configuração** |
   |----------------|-------------|
   | Conteúdo | Acesso completo |
   | Obter feeds | Exibir somente |
   | Inventário | Acesso completo |
   | Itens | Acesso completo |
   | Tempo de atraso | Acesso completo |
   | Pedido | Acesso completo |
   | Preço | Acesso completo |
   | Relatórios | Exibir somente |
   | Devoluções | Acesso completo |
   | Regras | Acesso completo |
   | Envio | Acesso completo |

## [!DNL Walmart Marketplace] Status da loja

Quando você conecta produtos ao mercado, a listagem da disponibilidade depende do status de seu [!DNL Walmart Marketplace] lojas:

* Para lojas ao vivo, suas ofertas de produto são listadas e disponibilizadas para venda quando a operação de correspondência for concluída.

* Para lojas que não estão ativas, suas ofertas de produto são preparadas e não ficam visíveis para os clientes. Quando a variável [!DNL Walmart Marketplace] a loja fica ativa, as listagens preparadas são enviadas automaticamente para a loja ativa.

![[!DNL Walmart Seller Central] produtos preparados](assets/walmart-seller-central-staged.png)

>[!IMPORTANT]
>
>Depois [!DNL Channel Manager] estiver instalado e configurado, todas as atualizações de inventário, preço e pedido serão sincronizadas automaticamente. Não conectar [!DNL Channel Manager] para uma loja Walmart ao vivo no Marketplace até você ter desativado quaisquer outras integrações que atualizam o produto e dados do pedido. Se você tiver outras integrações configuradas, verifique se a quantidade e os preços do item em [!DNL Commerce] corresponda às quantidades em [!DNL Walmart Marketplace] antes de se conectar a uma loja ao vivo.

