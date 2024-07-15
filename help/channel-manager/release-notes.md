---
title: '[!DNL Channel Manager] Notas de Versão'
description: As informações da versão mais recente do  [!DNL Channel Manager] Adobe Commerce.
feature: Sales Channels, Release Notes
exl-id: 8f40ace1-6587-4185-955a-91bc16dee8ce
source-git-commit: 003efd3c1044284a7d2c86db5d3eb1abfb3898ea
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Notas de versão do [!DNL Channel Manager]

Estas notas de versão descrevem a versão inicial do [!DNL Channel Manager] e incluem:

![Novos](../assets/new.svg) Novos recursos
![Problema corrigido](../assets/fix.svg) Correções e melhorias
![Problema conhecido](../assets/bug.svg) Problemas conhecidos

Consulte [Versões futuras](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) para saber mais sobre os cronogramas de lançamento e o suporte.

Consulte [Disponibilidade do Produto](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) para saber quais versões do Adobe Commerce oferecem suporte a esta extensão.

## v2.1.0

*3 de outubro de 2023*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"}

O ![Novo](../assets/new.svg) Gerenciador de Canais agora é compatível com as versões [Adobe Commerce versão 2.4.7 beta](https://experienceleague.adobe.com/docs/commerce-operations/release/beta.html).

## v2.0.0

*20 de março de 2023*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"}

O ![Novo](../assets/new.svg)<!--CHAN-5893--> Gerenciador de Canais agora é compatível com o Adobe Commerce versão 2.4.6.

## v1.1.0

*23 de novembro de 2022*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"}

![Novo](../assets/new.svg)<!--CHAN-5204--> **Devoluções e Reembolsos**—Agora é possível processar devoluções e reembolsos do Walmart Marketplace para pedidos enviados por meio de uma loja do Adobe Commerce e do Magento Open Source Channel Manager. As informações e atualizações sobre devoluções e reembolsos são sincronizadas entre o Walmart e o Adobe Commerce para que os dados atuais estejam disponíveis na loja [!DNL Commerce] e no [!DNL Walmart Marketplace]. Consulte [Ordens de devolução e reembolso](return-refund-orders.md).

![Correção](../assets/fix.svg)<!--CHAN-5661--> Corrigido o erro `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` que ocorria ao ressincronizar dados de pedidos do Gerenciador de Canais usando o comando `bin/magento saas:resync --feed orders`. O erro foi resolvido atualizando as dependências do pacote do Gerenciador de Canais para o módulo Exportador de Dados de Vendas, que foi renomeado de `magento/module-sales-data-exporter` para `magento/module-sales-orders-data-exporter`.

## v1.0.0

*14 de janeiro de 2022*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"}

![Nova](../assets/new.svg) Versão inicial do Gerenciador de Canais para disponibilidade geral

