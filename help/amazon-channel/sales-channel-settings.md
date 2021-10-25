---
title: Configurações do Sales Channel
description: Para gerenciar o registro, a fonte de cron e a sincronização das funções do canal de vendas do Amazon, atualize a configuração do Commerce.
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Configurações de Sales Channel

Quando a variável [!DNL Amazon Sales Channel] estiver instalada, os valores padrão serão definidos no canal Admin for Amazon de vendas . Essas configurações podem ser modificadas nas configurações da loja da Amazon. Essas configurações incluem:

- Intervalos para limpar o histórico do Log de atividades
- Seleção de fonte de cron
- Opções de sincronização de log

## Modificar as configurações dos canais do Commerce

1. No _Administrador_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales Channels]** e escolha **[!UICONTROL Global Settings]**.

1. Para **[!UICONTROL Clear Log History]**, escolha uma opção:

   - `Once Daily` - Escolha limpar o histórico de atividades da loja uma vez por dia.

   - `Once Weekly` - Escolha limpar o histórico de atividades da loja uma vez por semana.

   - `Once Monthly` - (Padrão) Escolha limpar o histórico de atividades da loja uma vez por mês.

1. Para **[!UICONTROL Background Tasks (CRON) Source]**, escolha `Magento CRON`.

   Essa opção permite que o canal de vendas da Amazon use seu [!DNL Commerce] [Cron](https://docs.magento.com/user-guide/system/cron.html) configurações para determinar a comunicação e os intervalos de sincronização de dados com [!DNL Amazon Seller Central].

1. Para **[!UICONTROL Enable Debug Logging]**, escolha `Enabled` para coletar dados de sincronização adicionais quando a solução de problemas for necessária.

   O registro do canal de vendas da Amazon é gravado no `{Commerce Root}/var/log/channel_amazon.log` e pode ser visualizado em [modo desenvolvedor](https://docs.magento.com/user-guide/magento/installation-modes.html){target=&quot;_blank&quot;}. O registro só deve ser `Enabled` durante a solução de problemas e deve ser `Disabled` quando a solução de problemas for concluída.

1. Clique em **[!UICONTROL Save Config]**.

![Definições de configuração do Sales Channel](assets/config-sales-channel-global-settings.png)
