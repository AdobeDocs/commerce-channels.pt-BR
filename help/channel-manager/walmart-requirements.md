---
title: '"[!DNL Walmart] Requisitos"'
description: '"Verifique se você tem o[!DNL Walmart Marketplace]informações e recursos para integrar com o Gerenciador de canais."'
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: fffbdac54443b7b9bed8854eba8341446e78cc80
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# [!DNL Walmart] requisitos

[!DNL Channel Manager] requer os seguintes recursos e informações para configurar um [!DNL Commerce] canal de vendas para [!DNL Walmart Marketplace.]

* Aprovação para venda [!DNL Walmart] e credenciais para fazer logon na conta do vendedor do Marketplace registrada

* Uma chave de API para conectar o Adobe Commerce ou o Magento Open Source ao [!DNL Walmart Marketplace]

   O [!DNL Walmart Marketplace] A chave de API habilita a integração entre [!DNL Channel Manager] para Adobe Commerce ou Magento Open Source e o Walmart Marketplace. Configure a chave da API no Seller Central antes de iniciar o processo de integração do Gerenciador de canais.

## Configurar uma conta do vendedor do Marketplace

1. [Envie seu aplicativo Walmart](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI).
1. Depois de obter a homologação de [!DNL Walmart], [configurar sua conta do Walmart](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

## Gerar um [!DNL Walmart Marketplace] Chave da API de produção

1. Ir para [!DNL Walmart Marketplace]para gerar um [chave da API de produção do provedor de soluções para Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

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

Ao publicar produtos no marketplace, a listagem da disponibilidade depende do status do seu [!DNL Walmart Marketplace] lojas:

* Para lojas ao vivo, suas ofertas de produto são listadas e disponibilizadas para venda quando a operação de correspondência for concluída.

* Para lojas que não estão ativas, suas ofertas de produto são preparadas e não ficam visíveis para os clientes. Quando a variável [!DNL Walmart Marketplace] a loja fica ativa, as listagens preparadas são enviadas automaticamente para a loja ativa.

![[!DNL Walmart Seller Central] produtos preparados](assets/walmart-seller-central-staged.png)