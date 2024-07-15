---
title: Configurações do canal de vendas
description: Para gerenciar o registro, a origem do cron e a sincronização das funções de canal de vendas do Amazon, atualize a configuração do Commerce.
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
role: Admin, Developer
feature: Sales Channels, Configuration, Logs
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# Configurações do canal de vendas

Quando a extensão [!DNL Amazon Sales Channel] é instalada, os valores padrão são definidos no Admin para o canal de vendas do Amazon. Essas configurações podem ser modificadas nas configurações da loja da Amazon. Essas configurações incluem:

- Intervalos para limpar o histórico do log de atividades
- Seleção da origem do Cron
- Opções de sincronização de log

## Modificar as configurações de canais do Commerce

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales Channels]** e escolha **[!UICONTROL Global Settings]**.

1. Para **[!UICONTROL Clear Log History]**, escolha uma opção:

   - `Once Daily` - Opte por limpar o histórico de atividades da loja uma vez por dia.

   - `Once Weekly` - Opte por limpar o histórico de atividades da loja uma vez por semana.

   - `Once Monthly` - (Padrão) Escolha limpar o histórico de atividades da loja uma vez por mês.

1. Para **[!UICONTROL Background Tasks (CRON) Source]**, escolha `Magento CRON`.

   Esta opção permite que o canal de vendas da Amazon use suas configurações do [!DNL Commerce] [Cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html) para determinar os intervalos de comunicação e sincronização de dados com o [!DNL Amazon Seller Central].

1. Para **[!UICONTROL Enable Debug Logging]**, escolha `Enabled` para coletar dados de sincronização adicionais quando a solução de problemas for necessária.

   O log do canal de vendas da Amazon é gravado no arquivo `{Commerce Root}/var/log/channel_amazon.log` e pode ser exibido no [modo de desenvolvedor](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/developer-tools.html#operation-modes). O registro em log deve ser `Enabled` apenas durante a solução de problemas e deve ser `Disabled` quando a solução de problemas estiver concluída.

1. Para **[!UICONTROL Read-Only Mode]**, selecione `Enabled` para bloquear todas as solicitações de API que mudam de estado de saída.

   Com esta configuração, as alterações potenciais são salvas, mas não enviadas, até que [!UICONTROL Read-Only Mode] seja desabilitado. O cache de configuração deve ser limpo para que o Modo Somente Leitura seja habilitado. Para iniciar as transferências de dados novamente, selecione `Disabled`.

   >[!IMPORTANT]
   >
   >[!UICONTROL Read-Only Mode] foi criado para cópias da Instância de produção, como preparo ou controle de qualidade, e não deve ser usado na instância de produção.
   >
   >Quando um banco de dados é migrado para uma nova cópia da instância (detectada quando a URL de um armazenamento muda na configuração), o [!UICONTROL Read-Only Mode] é automaticamente habilitado.

1. Clique em **[!UICONTROL Save Config]**.

![configurações do Sales Channel](assets/config-sales-channel-global-settings.png){width="600" zoomable="yes"}
