---
title: Exibir detalhes da listagem do Amazon
description: Para entender as métricas competitivas em suas listagens do Amazon e em alterações individuais de SKU/produto, consulte a página Detalhes da listagem de produtos.
feature: Sales Channels, Products, Merchandising
exl-id: faece1b1-b4fb-4506-bf77-576ae445ed28
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Exibir detalhes da listagem do Amazon

A página _[!UICONTROL Product Listing Details]_mostra informações adicionais sobre suas listas de produtos ativas, incluindo o Log de Atividades de Listagem, que mostra as alterações em uma SKU/Produto individual. Essas informações podem ajudá-lo a entender as métricas competitivas em seus produtos e em alterações individuais de SKU/produto. As informações adicionais nesta página incluem:

- **[!UICONTROL Listing Details]** - Detalhes do produto, incluindo o Nome e o SKU do Vendedor da Amazon
- **[!UICONTROL Listing Activity Log]** - Registro histórico de todas as alterações ocorridas para esta lista, como alterações de preço e quantidade/estoque. Nenhuma outra ação é necessária. Este log é fornecido para análise para compreender o histórico de alterações.
- **[!UICONTROL Buy Box Competitor Pricing]** - Dados para o status [[!DNL Buy Box]](./buy-box-competitor-pricing.md) da Amazon e preços do concorrente
- **[!UICONTROL Lowest Competitor Pricing]** - Informações sobre preços e comentários dos concorrentes da Amazon mais baixos

As home pages dos canais de vendas do Amazon compartilham alguns [controles de espaço de trabalho](./workspace-controls.md) comuns que permitem personalizar os dados exibidos.

## Detalhes da listagem

As informações do produto exibidas incluem:

- _[!UICONTROL Amazon Name]_
- _[!UICONTROL Catalog (Magento) SKU]_
- _[!UICONTROL Amazon Seller SKU]_

![Detalhes da listagem](assets/amazon-product-listing-details.png){width="600" zoomable="yes"}

## Log de atividades de listagem {#listing-activity-log}

Mostra todas as atividades recentes da lista do Amazon. As informações mostradas incluem:

- SKU do vendedor da Amazon: identifica a unidade de manutenção de estoque (SKU) definida para a lista.
- ASIN: identifica o identificador de produto de 10 dígitos do Amazon.
- Ação de listagem: Identifica o tipo de ação que ocorreu para a listagem.
- Comentários: fornece detalhes adicionais relacionados ao tipo de ação de listagem que ocorreu.
- Executado às: identifica a data e a hora em que a ação ocorreu.

![Detalhes da listagem de produtos - Log de atividades da listagem](assets/amazon-listing-activity-log.png){width="600" zoomable="yes"}
__

## Preços do concorrente Buy Box {#buy-box-competitor-pricing}

Esta guia exibe informações sobre o comerciante do Amazon que detém a posição [[!DNL Buy Box]](./buy-box-competitor-pricing.md) para a lista. Essas informações podem ser usadas para entender o posicionamento de preços de seus concorrentes no Amazon. As informações mostradas incluem:

- ASIN: o identificador de produto de 10 dígitos do Amazon.
- É vendedor: identifica se você é o vendedor [!DNL Buy Box]. Opções Sim / Não.
- Condição: Identifica a condição definida para a lista.
- Preço da Lista: Identifica o preço no qual a lista foi publicada.
- Preço de Entrega: Identifica o preço de entrega adicionado à lista.
- Preço da Entrega: Identifica o preço da lista mais o preço da entrega para a lista.
- Última Atualização: Identifica a data e a hora em que as informações de precificação foram atualizadas no Amazon.

![Detalhes da lista de produtos: preço de Buy Box do concorrente](assets/amazon-listing-details-buy-box-2.png){width="600" zoomable="yes"}

## Menor preço para concorrentes {#lowest-competitor-pricing}

Esta guia exibe informações sobre os concorrentes da Amazon para a mesma lista. Essas informações podem ser usadas para entender o posicionamento de preços e o [preço mais baixo para o concorrente](./lowest-competitor-pricing.md). As informações mostradas incluem:

- ASIN: o identificador de produto de 10 dígitos do Amazon.
- Condição: Identifica a condição definida para a lista.
- Canal de Fulfillment: Identifica a parte responsável pelo fulfillment. Opções: Comerciante/Amazon.
- Preço da Lista: Identifica o preço no qual a lista foi publicada.
- Preço de Entrega: Identifica o preço de entrega adicionado à lista.
- Preço da Entrega: Identifica o preço da lista mais o preço da entrega para a lista.
- Classificação de feedback: Identifica a classificação de feedback do Amazon para o comerciante de preço mais baixo.
- Contagem de feedback: Identifica a contagem de feedback do Amazon para o comerciante de preço mais baixo.
- Última Atualização: Identifica a data e a hora em que as informações de precificação foram atualizadas no Amazon.

![Detalhes da lista de produtos - menor preço para o concorrente](assets/amazon-listing-details-lowest-comp.png){width="600" zoomable="yes"}
