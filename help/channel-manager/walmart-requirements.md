---
title: '[!DNL Walmart] Requisitos'
description: 'Verifique se você tem as  [!DNL Walmart Marketplace]informações e os recursos necessários para integrar ao Gerenciador de Canais.'
role: Leader, Admin, Developer
feature: Sales Channels, Install, User Account, Tools and External Services
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# [!DNL Walmart] requisitos

O [!DNL Channel Manager] requer os seguintes recursos e informações para configurar um canal de vendas [!DNL Commerce] para [!DNL Walmart Marketplace.]

* Uma Conta De Vendedor [!DNL Walmart]

* Uma chave de API para conectar Adobe Commerce ou Magento Open Source a [!DNL Walmart Marketplace]

  A chave de API [!DNL Walmart Marketplace] habilita a integração entre o [!DNL Channel Manager] para o Adobe [!DNL Commerce] ou Magento Open Source e o Walmart Marketplace. Configure a chave de API na Central do vendedor antes de iniciar o processo de integração do Gerenciador de canal.

## Configurar uma conta do [!DNL Walmart Seller]

Vá para o [!DNL Walmart Seller Center] para configurar sua [conta Walmart Seller](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

## Gerar uma chave de API de produção [!DNL Walmart Marketplace]

1. Vá para [!DNL Walmart Marketplace] para gerar uma [chave da API de produção do provedor de soluções para o Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. Crie a chave e configure as permissões:

   * Selecione Adobe como o provedor de soluções.

   * Defina as permissões conforme mostrado na tabela a seguir. Para obter detalhes, consulte [Credenciais da API](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) na _Ajuda para Vendedores do Walmart Marketplace_.

   Configuração da chave de API **Adobe para o Walmart**

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

## Status do armazenamento [!DNL Walmart Marketplace]

Quando você conecta produtos ao marketplace, a disponibilidade da lista depende do status das suas lojas [!DNL Walmart Marketplace]:

* Para lojas ao vivo, suas ofertas de produtos são listadas e estão disponíveis para venda quando a operação de correspondência é concluída.

* Para lojas que não estão ativas, as ofertas de produtos são preparadas e não ficam visíveis para os clientes. Quando o armazenamento [!DNL Walmart Marketplace] é ativado, as listagens preparadas são enviadas automaticamente para o armazenamento ativo.

![[!DNL Walmart Seller Central] produtos preparados](assets/walmart-seller-central-staged.png){width="600" zoomable="yes"}

>[!IMPORTANT]
>
>Depois que o [!DNL Channel Manager] for instalado e configurado, todas as atualizações de inventário, preço e pedido serão sincronizadas automaticamente. Não conecte [!DNL Channel Manager] a uma loja ativa do Walmart Marketplace até desabilitar outras integrações que atualizem os dados do produto e do pedido. Se você tiver outras integrações configuradas, verifique se a quantidade e os preços do item em [!DNL Commerce] correspondem às quantidades em [!DNL Walmart Marketplace] antes de se conectar a uma loja em tempo real.

