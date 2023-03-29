---
title: '[!DNL Channel Manager] Notas de versão'
description: As últimas informações da versão para [!DNL Channel Manager] do Adobe Commerce.
exl-id: 8f40ace1-6587-4185-955a-91bc16dee8ce
source-git-commit: d3acde7aa297ba33dffa7854aa7578985ad12c9b
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---

# [!DNL Channel Manager] Notas de versão

Essas notas de versão descrevem a versão inicial do [!DNL Channel Manager] e incluem:

![Novo](../assets/new.svg) Novos recursos
![Problema corrigido](../assets/fix.svg) Correções e melhorias
![Problema conhecido](../assets/bug.svg) Problemas conhecidos


## v2.0.0

*20 de março de 2023*

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"}

![Novo](../assets/new.svg)<!--CHAN-5893--> O Gerenciador de canais agora é compatível com a versão 2.4.6 do Adobe Commerce.

## v1.1.0

*23 de novembro de 2022*

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"}

![Novo](../assets/new.svg)<!--CHAN-5204--> **Devoluções e reembolsos**—Agora você pode processar o processo de devoluções e reembolsos do Walmart para pedidos enviados por meio de uma loja Adobe Commerce e Magento Open Source Channel Manager. As informações e atualizações sobre devoluções e reembolsos são sincronizadas entre o Walmart e o Adobe Commerce para que os dados atuais estejam disponíveis no [!DNL Commerce] vitrine e [!DNL Walmart Marketplace]. Consulte [Devoluções e pedidos de reembolso](return-refund-orders.md).

![Fixo](../assets/fix.svg)<!--CHAN-5661--> Correção do `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` erro que ocorreu ao ressincronizar o Gerenciador de Canais solicita dados usando o `bin/magento saas:resync --feed orders` comando. O erro foi resolvido atualizando as dependências do pacote do Gerenciador de Canais para o módulo Exportador de Dados de Vendas, que foi renomeado de `magento/module-sales-data-exporter` para `magento/module-sales-orders-data-exporter`.

## v1.0.0

*14 de janeiro de 2022*

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"}

![Novo](../assets/new.svg) Versão inicial do Gerenciador de canais para disponibilidade geral

