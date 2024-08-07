---
title: Registra e armazena relatórios para listagens do Amazon
description: Use os registros e relatórios da loja para ver o que está acontecendo em sua loja Adobe Commerce ou Magento Open Source e suas listagens do Amazon Marketplace.
feature: Sales Channels, Logs
exl-id: 4654f718-d15f-4c3b-b984-ac7b9c29e6c4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Registra e armazena relatórios para listagens do Amazon

A extensão de canal de vendas da Amazon inclui alguns logs valiosos e relatórios de loja que permitem visualizar as alterações que afetam suas listagens e pedidos da Amazon. Você pode usar esses relatórios para ver o que está acontecendo em sua loja e entender vários status da lista.

Nenhuma ação está disponível para os logs ou relatórios de armazenamento, pois eles são recursos somente de revisão.

Os seguintes logs podem ser acessados do [painel de repositório](./amazon-store-dashboard.md).

- O [Log de Alterações de Listagem](./listing-changes-log.md) mostra as alterações que ocorreram em sua Conta de Vendedor da Amazon como um reflexo das configurações do canal de vendas da Amazon.

- O [Log de Erros de Comunicação](./communication-errors-log.md) mostra todos os erros de comunicação relatados com o Amazon.

Os seguintes relatórios específicos de armazenamento podem ser acessados no [painel de armazenamento](./amazon-store-dashboard.md).

- O relatório [Análise de Preço Competitiva](./competitive-price-analysis.md) mostra que o _preço no destino_ da sua Amazon (preço de listagem mais preço de envio) está relacionado ao preço [Buy Box](./buy-box-competitor-pricing.md) e ao preço [mais baixo concorrente](./lowest-competitor-pricing.md).

- O relatório [Melhorias de Listagem](./listing-improvements.md) mostra todas as melhorias de listagem sugeridas fornecidas pela Amazon para a loja selecionada.

>[!TIP]
>
>Você também pode verificar o arquivo de log para obter informações adicionais quando a solução de problemas for necessária. Consulte [Configurações de administração do canal de vendas](./sales-channel-settings.md). O log de sincronização do canal de vendas do Amazon é gravado no arquivo `{Commerce Root}/var/log/channel_amazon.log` e pode ser exibido no [modo de desenvolvedor](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/developer-tools.html#operation-modes).
