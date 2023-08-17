---
title: '[!DNL Channel Manager] Notas de versão'
description: As informações mais recentes da versão do [!DNL Channel Manager] do Adobe Commerce.
feature: Sales Channels, Release Notes
exl-id: 8f40ace1-6587-4185-955a-91bc16dee8ce
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 4%

---

# [!DNL Channel Manager] Notas de versão

Estas notas de versão descrevem a versão inicial do [!DNL Channel Manager] e incluem:

![Novo](../assets/new.svg) Novos recursos
![Problema corrigido](../assets/fix.svg) Correções e aprimoramentos
![Problema conhecido](../assets/bug.svg) Problemas conhecidos


## v2.0.0

*20 de março de 2023*

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"}

![Novo](../assets/new.svg)<!--CHAN-5893--> O Channel Manager agora é compatível com o Adobe Commerce versão 2.4.6.

## v1.1.0

*23 de novembro de 2022*

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"}

![Novo](../assets/new.svg)<!--CHAN-5204--> **Devoluções e Reembolsos**—Agora é possível processar devoluções e reembolsos do Walmart Marketplace para pedidos enviados por meio de uma loja do Adobe Commerce e do Magento Open Source Channel Manager. As informações e atualizações sobre devoluções e reembolsos são sincronizadas entre o Walmart e o Adobe Commerce para que os dados atuais estejam disponíveis no [!DNL Commerce] vitrine e [!DNL Walmart Marketplace]. Consulte [Ordens de devolução e de reembolso](return-refund-orders.md).

![Fixo](../assets/fix.svg)<!--CHAN-5661--> Corrigido o `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` erro que ocorreu ao ressincronizar dados de pedidos do Gerenciador de canal usando o `bin/magento saas:resync --feed orders` comando. O erro foi resolvido atualizando as dependências do pacote do Gerenciador de canais para o módulo Exportador de dados de vendas, que foi renomeado de `magento/module-sales-data-exporter` para `magento/module-sales-orders-data-exporter`.

## v1.0.0

*14 de janeiro de 2022*

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"}

![Novo](../assets/new.svg) Versão inicial do Channel Manager para disponibilidade geral

