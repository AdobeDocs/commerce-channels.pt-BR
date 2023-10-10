---
title: '[!DNL Channel Manager] Notas de versão'
description: As informações mais recentes da versão do [!DNL Channel Manager] do Adobe Commerce.
feature: Sales Channels, Release Notes
exl-id: 8f40ace1-6587-4185-955a-91bc16dee8ce
source-git-commit: 003efd3c1044284a7d2c86db5d3eb1abfb3898ea
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 3%

---

# [!DNL Channel Manager] Notas de versão

Estas notas de versão descrevem a versão inicial do [!DNL Channel Manager] e incluem:

![Novo](../assets/new.svg) Novos recursos
![Problema corrigido](../assets/fix.svg) Correções e aprimoramentos
![Problema conhecido](../assets/bug.svg) Problemas conhecidos

Consulte [Versões futuras](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) para saber mais sobre as programações de lançamento e o suporte.

Consulte [Disponibilidade do produto](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) para saber quais versões do Adobe Commerce são compatíveis com essa extensão.

## v2.1.0

*3 de outubro de 2023*

[!BADGE Compatível]{type=Informative tooltip="Compatível"}

![Novo](../assets/new.svg) O Gerenciador de canais agora é compatível com o [Versão 2.4.7 beta do Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-operations/release/beta.html) versões.

## v2.0.0

*20 de março de 2023*

[!BADGE Compatível]{type=Informative tooltip="Compatível"}

![Novo](../assets/new.svg)<!--CHAN-5893--> O Channel Manager agora é compatível com o Adobe Commerce versão 2.4.6.

## v1.1.0

*23 de novembro de 2022*

[!BADGE Compatível]{type=Informative tooltip="Compatível"}

![Novo](../assets/new.svg)<!--CHAN-5204--> **Devoluções e Reembolsos**—Agora é possível processar devoluções e reembolsos do Walmart Marketplace para pedidos enviados por meio de uma loja do Adobe Commerce e do Magento Open Source Channel Manager. As informações e atualizações sobre devoluções e reembolsos são sincronizadas entre o Walmart e o Adobe Commerce para que os dados atuais estejam disponíveis no [!DNL Commerce] vitrine e [!DNL Walmart Marketplace]. Consulte [Ordens de devolução e de reembolso](return-refund-orders.md).

![Fixo](../assets/fix.svg)<!--CHAN-5661--> Corrigido o `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` erro que ocorreu ao ressincronizar dados de pedidos do Gerenciador de canal usando o `bin/magento saas:resync --feed orders` comando. O erro foi resolvido atualizando as dependências do pacote do Gerenciador de canais para o módulo Exportador de dados de vendas, que foi renomeado de `magento/module-sales-data-exporter` para `magento/module-sales-orders-data-exporter`.

## v1.0.0

*14 de janeiro de 2022*

[!BADGE Compatível]{type=Informative tooltip="Compatível"}

![Novo](../assets/new.svg) Versão inicial do Channel Manager para disponibilidade geral

