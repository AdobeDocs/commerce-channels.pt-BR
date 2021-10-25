---
title: Logs e relatórios de armazenamento
description: Use os registros e relatórios de loja para ver o que está acontecendo em sua Adobe Commerce ou Magento Open Source Store e nas listagens do Amazon Marketplace .
exl-id: 4654f718-d15f-4c3b-b984-ac7b9c29e6c4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Registra e armazena relatórios

A extensão de canal de vendas do Amazon inclui alguns logs valiosos e relatórios de loja que permitem visualizar as alterações que estão afetando suas listas e pedidos do Amazon. Você pode usar esses relatórios para ver o que está acontecendo em sua loja e compreender vários status de listagem.

Nenhuma ação está disponível para os logs ou relatórios de loja, pois são recursos somente para revisão.

Os seguintes logs podem ser acessados do [painel de loja](./amazon-store-dashboard.md).

- O [Log de alterações de listagem](./listing-changes-log.md) mostra as alterações que ocorreram em sua conta de vendedor do Amazon como reflexo das configurações de canal de vendas do Amazon.

- O [Log de erros de comunicação](./communication-errors-log.md) mostra quaisquer erros de comunicação relatados com o Amazon.

Os relatórios específicos da loja a seguir podem ser acessados no [painel de loja](./amazon-store-dashboard.md).

- O [Análise de preços competitiva](./competitive-price-analysis.md) mostra que sua Amazon _preço de desembarque_ (preço de cotação mais preço de expedição) em relação ao [Buy Box](./buy-box-competitor-pricing.md) preço e [concorrente mais baixo](./lowest-competitor-pricing.md) preço.

- O [Melhorias na listagem](./listing-improvements.md) mostra todas as melhorias sugeridas de listagem fornecidas pela Amazon para a loja selecionada.

>[!TIP]
>
>Você também pode verificar o arquivo de log para obter informações adicionais quando a solução de problemas for necessária. Consulte [configurações de administrador do canal de vendas](./sales-channel-settings.md). O registro de sincronização do canal de vendas da Amazon é gravado no `{Commerce Root}/var/log/channel_amazon.log` e pode ser visualizado em [modo desenvolvedor](https://docs.magento.com/user-guide/magento/installation-modes.html){target=&quot;_blank&quot;}.
