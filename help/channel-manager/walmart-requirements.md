---
title: '[!DNL Walmart] Requisitos'
description: '''Verifique se você tem a [!DNL Walmart Marketplace]informações e recursos para integrar com o Channel Manager."'
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# [!DNL Walmart] Requisitos

[!DNL Channel Manager] O requer os seguintes recursos e informações para configurar um [!DNL Commerce] canal de vendas para [!DNL Walmart Marketplace.]

* A [!DNL Walmart] Conta do Vendedor

* Uma chave de API para conectar o Adobe Commerce ou o Magento Open Source a [!DNL Walmart Marketplace]

   A variável [!DNL Walmart Marketplace] A chave de API permite a integração entre [!DNL Channel Manager] para Adobe [!DNL Commerce] ou o Magento Open Source e o Walmart Marketplace. Configure a chave de API na Central do vendedor antes de iniciar o processo de integração do Gerenciador de canal.

## Configurar um [!DNL Walmart Seller] account

Vá para a [!DNL Walmart Seller Center] para configurar o seu [Conta do vendedor do Walmart](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

## Gerar um [!DNL Walmart Marketplace] Chave da API de produção

1. Ir para [!DNL Walmart Marketplace] para gerar um [Chave da API de produção do provedor de soluções para o Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. Crie a chave e configure as permissões:

   * Selecione Adobe como o provedor de soluções.

   * Defina as permissões conforme mostrado na tabela a seguir. Para obter detalhes, consulte [Credenciais da API](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) no _Ajuda para Vendedores do Walmart Marketplace_.

   **Configuração da chave de API do Adobe para o Walmart**

   | **Permissão** | **Configuração** |
   |----------------|-------------|
   | Conteúdo | Acesso completo |
   | Obter Feeds | Exibir apenas |
   | Inventário | Acesso completo |
   | Itens | Acesso completo |
   | Tempo de retardo | Acesso completo |
   | Pedido | Acesso completo |
   | Preço | Acesso completo |
   | Relatórios | Exibir apenas |
   | Devoluções | Acesso completo |
   | Regras | Acesso completo |
   | Envio | Acesso completo |

## [!DNL Walmart Marketplace] Status da loja

Quando você conecta produtos ao marketplace, a disponibilidade da lista depende do status do seu [!DNL Walmart Marketplace] lojas:

* Para lojas ao vivo, suas ofertas de produtos são listadas e estão disponíveis para venda quando a operação de correspondência é concluída.

* Para lojas que não estão ativas, as ofertas de produtos são preparadas e não ficam visíveis para os clientes. Quando a variável [!DNL Walmart Marketplace] a loja fica ativa, as listagens preparadas são enviadas para a loja ativa automaticamente.

![[!DNL Walmart Seller Central] produtos preparados](assets/walmart-seller-central-staged.png)

>[!IMPORTANT]
>
>Depois [!DNL Channel Manager] O está instalado e configurado, todas as atualizações de inventário, preço e pedido são sincronizadas automaticamente. Não conectar [!DNL Channel Manager] para uma loja ativa do Walmart Marketplace até que você tenha desativado quaisquer outras integrações que atualizem os dados do produto e do pedido. Se você tiver outras integrações configuradas, verifique se a quantidade do item e os preços em [!DNL Commerce] corresponder às quantidades em [!DNL Walmart Marketplace] antes de se conectar a uma loja online.

