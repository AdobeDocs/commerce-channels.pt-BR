---
title: Exibir detalhes da listagem
description: Para entender métricas competitivas em suas listas do Amazon e em alterações de SKU/produto individuais, consulte a página Detalhes da lista de produtos .
exl-id: faece1b1-b4fb-4506-bf77-576ae445ed28
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# Exibir detalhes da listagem

A página _[!UICONTROL Product Listing Details]_mostra informações adicionais sobre suas listas de produtos ativas, incluindo o Log de atividades de listagem , que mostra as alterações em um SKU/Produto individual. Essas informações podem ajudá-lo a entender métricas competitivas em seus produtos e sobre alterações de SKU/produto. Informações adicionais nesta página incluem:

- **[!UICONTROL Listing Details]** - Detalhes do produto, incluindo o SKU Nome e o vendedor da Amazon
- **[!UICONTROL Listing Activity Log]** - Registro histórico de todas as alterações verificadas para esta listagem, tais como preços e alterações de quantidade/existências. Não são necessárias mais ações. Esse log é fornecido para análise para entender o histórico de alterações.
- **[!UICONTROL Buy Box Competitor Pricing]** - Dados sobre o  [[!DNL Buy Box]](./buy-box-competitor-pricing.md) status da Amazon e os preços dos concorrentes
- **[!UICONTROL Lowest Competitor Pricing]** - Informações sobre os preços e as informações de feedback do menor concorrente da Amazon

As home pages do canal de vendas do Amazon compartilham alguns [controles do espaço de trabalho](./workspace-controls.md) comuns que permitem personalizar os dados exibidos.

## Detalhes da listagem

As informações do produto exibidas incluem:

- _[!UICONTROL Amazon Name]_
- _[!UICONTROL Catalog (Magento) SKU]_
- _[!UICONTROL Amazon Seller SKU]_

![Detalhes da listagem](assets/amazon-product-listing-details.png)

## Listando log de atividades {#listing-activity-log}

Mostra todas as atividades recentes para a listagem do Amazon. As informações mostradas incluem:

- SKU do vendedor de Amazon: Identifica a Unidade de manutenção de estoque (SKU) definida para a listagem.
- ASIN: Identifica o identificador de produto Amazon de 10 dígitos.
- Ação de listagem: Identifica o tipo de ação que ocorreu para a listagem.
- Comentários: Fornece detalhes adicionais relacionados ao tipo de ação de listagem que ocorreu.
- Executado em: Identifica a data e a hora em que a ação ocorreu.

![Detalhes da lista de produtos - Listando o log de atividades](assets/amazon-listing-activity-log.png)
__

## Preços do concorrente do Buy Box {#buy-box-competitor-pricing}

Esta guia exibe informações sobre o comerciante do Amazon que mantém a posição [[!DNL Buy Box]](./buy-box-competitor-pricing.md) para a listagem. Essas informações podem ser usadas para entender o posicionamento de preços de seus concorrentes no Amazon. As informações mostradas incluem:

- ASIN: O identificador de produto Amazon de 10 dígitos.
- É Vendedor: Identifica se você é o vendedor [!DNL Buy Box]. Opções Sim / Não.
- Condição: Identifica a condição definida para a listagem.
- Preço de Listagem: Identifica o preço a que a lista foi publicada.
- Preço de Remessa: Identifica o preço de envio adicionado à lista.
- Preço Lançado: Identifica o preço de listagem mais o preço de frete da listagem.
- Última atualização: Identifica a data e a hora em que as informações de preços foram atualizadas na Amazon.

![Detalhes da lista de produtos: Preços da concorrência Buy Box](assets/amazon-listing-details-buy-box-2.png)

## Preços dos Concorrentes Mais Baixos {#lowest-competitor-pricing}

Esta guia exibe informações sobre concorrentes do Amazon para a mesma listagem. Essas informações podem ser usadas para entender o posicionamento de preços e [os preços mais baixos do concorrente](./lowest-competitor-pricing.md). As informações mostradas incluem:

- ASIN: O identificador de produto Amazon de 10 dígitos.
- Condição: Identifica a condição definida para a listagem.
- Canal de Cumprimento: Identifica a parte responsável pelo cumprimento. Opções: Merchant/Amazon.
- Preço de Listagem: Identifica o preço a que a lista foi publicada.
- Preço de Remessa: Identifica o preço de envio adicionado à lista.
- Preço Lançado: Identifica o preço de listagem mais o preço de frete da listagem.
- Classificação de feedback: Identifica a classificação de feedback da Amazon para o comerciante de menor preço.
- Contagem de comentários: Identifica a contagem de comentários da Amazon para o comerciante de preço mais baixo.
- Última atualização: Identifica a data e a hora em que as informações de preços foram atualizadas na Amazon.

![Detalhes da lista de produtos - menor preço do concorrente](assets/amazon-listing-details-lowest-comp.png)
