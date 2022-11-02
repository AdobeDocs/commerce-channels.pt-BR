---
title: '[!DNLChannel Manager] Notas de versão'
description: "As informações mais recentes da versão para [!DNL Channel Manager] do Adobe Commerce."
source-git-commit: 501a76a126f090805f95e64078ec2c73de003aa4
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---

# [!DNL Channel Manager] Notas de versão

Essas notas de versão descrevem a versão inicial do [!DNL Channel Manager] e incluem:

![Novo](../assets/new.svg) Novos recursos
![Problema corrigido](../assets/fix.svg) Correções e melhorias
![Problema conhecido](../assets/bug.svg) Problemas conhecidos


## v1.1.0

![Novo](../assets/new.svg)<!--CHAN-5204--> **Devoluções e reembolsos**—Agora você pode processar o processo de devoluções e reembolsos do Walmart para pedidos enviados por meio de uma loja Adobe Commerce e Magento Open Source Channel Manager. As informações e atualizações sobre devoluções e reembolsos são sincronizadas entre o Walmart e o Adobe Commerce para que os dados atuais estejam disponíveis no [!DNL Commerce] vitrine e [!DNL Walmart Marketplace]. Consulte [Devoluções e pedidos de reembolso](return-refund-orders.md).

![Fixo](../assets/fix.svg)<!--CHAN-5661--> Correção do `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` erro que ocorreu ao ressincronizar o Gerenciador de Canais solicita dados usando o `bin/magento saas:resync --feed orders` comando. O erro foi resolvido atualizando as dependências do pacote do Gerenciador de Canais para o módulo Exportador de Dados de Vendas, que foi renomeado de `magento/module-sales-data-exporter` para `magento/module-sales-orders-data-exporter`.

## v1.0.0

Versão inicial, compatível com as seguintes versões do Commerce:

* Fonte aberta (CE): 2.4.x
* Adobe Commerce (EE): 2.4.x
* Adobe Commerce para nuvem (ECE): 2.4.x
* Estabilidade: Estável
