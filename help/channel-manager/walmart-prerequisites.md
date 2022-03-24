---
title: Pré-requisitos do Walmart
description: Verifique se você tem as informações e os recursos necessários do Walmart para integrar-se ao Channel Manager.
source-git-commit: 2a9bd2f8f91e672786c36f5e132f99bcab59dd00
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---


# Pré-requisitos Walmart

O Channel Manager requer os seguintes recursos e informações para configurar um canal de vendas do Commerce para o Walmart Marketplace.

* Aprovação para vender no Walmart e credenciais para iniciar sessão na conta registrada do vendedor do Marketplace

* Uma chave de API para conectar o Adobe Commerce ou o Magento Open Source ao Walmart Marketplace

   A chave de API do Walmart Marketplace permite a integração entre o Channel Manager para Adobe Commerce ou Magento Open Source e o Walmart Marketplace. Configure a chave da API no Seller Central antes de iniciar o processo de integração do Gerenciador de canais.

## Configurar uma conta do vendedor do Marketplace

1. [Envie seu aplicativo Walmart](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI)
1. Depois de obter a homologação da Walmart, [configurar sua conta do Walmart](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

## Gerar uma chave de API do Walmart Marketplace

1. Vá para o Walmart para gerar um [chave da API de produção do provedor de soluções para Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. Crie a chave e configure as permissões:

   * Selecione Adobe como o provedor de soluções.

   * Defina as permissões conforme mostrado na tabela a seguir. Para obter detalhes, consulte [Credenciais da API](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) no _Ajuda do vendedor do Walmart_.

|    **Configuração de chave de API do Adobe para Walmart**
| **Permissão** | **Configuração** | |—|—| | Conteúdo | Acesso total | | Obter feeds | Somente visualização | | Inventário | Acesso total | | Rubricas | Acesso total | | Atraso | Acesso total | | Ordem | Acesso total | | Preço | Acesso total | | Relatórios | Somente visualização | | Devoluções | Acesso total | | Regras | Acesso total | | Transporte | Acesso total |

## Status da loja no Walmart Marketplace

Ao publicar produtos no Walmart Marketplace, a listagem da disponibilidade depende do status das suas lojas do Walmart:

* Para lojas ao vivo, suas ofertas de produto são listadas e disponibilizadas para venda quando a operação de correspondência for concluída.

* Para lojas que não estão ativas, suas ofertas de produto são preparadas e não ficam visíveis para os clientes. Quando a loja entra em vigor, as listas preparadas são enviadas automaticamente para a loja ativa.

![[!DNL Walmart Seller Central] produtos preparados](assets/walmart-seller-central-staged.png)
