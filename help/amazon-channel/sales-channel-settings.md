---
title: Configurações do Sales Channel
description: Para gerenciar o registro, a fonte de cron e a sincronização das funções do canal de vendas do Amazon, atualize a configuração do Commerce.
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Configurações de Sales Channel

Quando a extensão [!DNL Amazon Sales Channel] é instalada, os valores padrão são definidos no canal Admin for Amazon sales . Essas configurações podem ser modificadas nas configurações da loja da Amazon. Essas configurações incluem:

- Intervalos para limpar o histórico do Log de atividades
- Seleção de fonte de cron
- Opções de sincronização de log

## Modificar as configurações dos canais do Commerce

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales Channels]** e escolha **[!UICONTROL Global Settings]**.

1. Para **[!UICONTROL Clear Log History]**, escolha uma opção:

   - `Once Daily` - Escolha limpar o histórico de atividades da loja uma vez por dia.

   - `Once Weekly` - Escolha limpar o histórico de atividades da loja uma vez por semana.

   - `Once Monthly` - (Padrão) Escolha limpar o histórico de atividades da loja uma vez por mês.

1. Para **[!UICONTROL Background Tasks (CRON) Source]**, escolha `Magento CRON`.

   Essa opção permite que o canal de vendas da Amazon use suas configurações [!DNL Commerce] [Cron](https://docs.magento.com/user-guide/system/cron.html) para determinar a comunicação e os intervalos de sincronização de dados com [!DNL Amazon Seller Central].

1. Para **[!UICONTROL Enable Debug Logging]**, escolha `Enabled` para coletar dados de sincronização adicionais quando a solução de problemas for necessária.

   O registro do canal de vendas do Amazon é gravado no arquivo `{Commerce Root}/var/log/channel_amazon.log` e pode ser visualizado no [modo desenvolvedor](https://docs.magento.com/user-guide/magento/installation-modes.html){:target=&quot;_blank&quot;}. O registro só deve ser `Enabled` durante a solução de problemas e deve ser `Disabled` quando a solução de problemas estiver concluída.

1. Clique em **[!UICONTROL Save Config]**.

![Definições de configuração do Sales Channel](assets/config-sales-channel-global-settings.png)
