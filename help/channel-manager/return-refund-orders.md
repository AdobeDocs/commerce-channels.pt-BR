---
title: Ordens de Devolução e de Reembolso
description: Instruções para emitir reembolsos totais ou parciais para solicitações de devolução recebidas de [!DNL Walmart Marketplace] de [!DNL Channel Manager] para Adobe Commerce e Magento Open Source.
feature: Sales Channels, Orders, Shipping/Delivery, Customer Service
exl-id: 45617011-4add-444c-819b-6bb4164d03e4
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 0%

---

# Ordens de Devolução e de Reembolso

Quando um comprador solicita uma devolução para itens de pedido comprados através do [!DNL Walmart Marketplace], o Walmart cria uma solicitação de devolução. [!DNL Channel Manager] monitora o canal do marketplace para essas solicitações e sincroniza automaticamente as informações da solicitação de retorno com o Gerenciador de Canais.

No Commerce, a solicitação de retorno inicia o seguinte fluxo de trabalho:

1. O Gerenciador de Canais cria uma solicitação de retorno correspondente com um status recebido e adiciona o número de ID de retorno ([!UICONTROL RMA #]) ao painel [!UICONTROL Returns]. No painel [!DNL Orders], os detalhes do status do pedido associado à devolução são atualizados para incluir um link [!UICONTROL Return requested] para exibir e processar a devolução.

1. Os comerciantes processam o reembolso associado ao retorno criando um Aviso de Crédito após o [fluxo de trabalho de reembolso do Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html). Todos os reembolsos são processados usando o método offline.

1. [!DNL Channel Manager] envia uma atualização de reembolso ao Walmart Marketplace para que o status da devolução possa ser atualizado para refletir o reembolso concluído da Adobe Commerce.

No Administrador da loja, você pode exibir e processar retornos do Gerenciador de Canais abrindo a loja de canais de vendas e selecionando **[!UICONTROL Returns]**.

![Gerenciador de canais Retorna o painel para processar reembolsos de solicitações de retorno recebidas de [!DNL Walmart Marketplace]](assets/returns-dashboard-view.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Você só pode processar reembolsos para ordens entregues. Em [!DNL Channel Manager], o status do pedido deve ser [!UICONTROL Shipped]. Na conta de Vendedor [!DNL Walmart Marketplace], a ordem deve ser [!UICONTROL Delivered].

## Retorna Controles e Descrições de Coluna

As tabelas a seguir descrevem os controles e colunas disponíveis para [!DNL Channel Manager] retornos.

**Controles para[!UICONTROL Returns]**

<table>
<tr>
<td><strong>Controle</strong></td>
<td><strong>Descrição</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter returns]</td>
<td>Filtre a exibição selecionando um dos cartões [!UICONTROL Return Status].</td>
</tr>
<tr>
<td>Detalhes do status</td>
<td>Para entradas de retorno com o status [!UICONTROL Received] ou [!UICONTROL Refunded], você pode criar ou exibir o memorando de crédito do reembolso selecionando o texto vinculado na coluna Detalhes do Status.</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>Para exibir detalhes do pedido, selecione o número do pedido [!DNL Commerce] na tabela [!UICONTROL Order] para abrir o pedido do Commerce.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>Para modificar a configuração do canal, selecione credenciais de conexão Walmart do canal, atributos mapeados ou identificadores de envio. As configurações selecionam o número de pedido [!DNL Commerce] na tabela [!UICONTROL Order]. Em seguida, use as opções de pedido [!DNL Commerce] para processar o pedido.</td>
</tr>
</table>

**Descrições da coluna**

<table>
<tr>
<td><strong>Campo</strong></td>
<td><strong>Descrição</strong></td>
</tr>
<tr>
<td>[!UICONTROL RMA #]</td>
<td>O número de Autorização para Devolução de Mercadoria associado à solicitação de devolução recebida de [!DNL Walmart Marketplace]. Este número é gerado pelo Walmart Marketplace [!UICONTROL Returns] quando o processo de retorno é iniciado.</td>
</tr>
<tr>
<td>[!DNL Commerce] Nº do pedido</td>
<td>O número do pedido [!DNL Commerce] associado aos itens incluídos na solicitação de devolução do Walmart Marketplace. Exibir detalhes do pedido selecionando o número do pedido.</td>
</tr>
<tr>
<td>Solicitado</td>
<td>A data em que a devolução foi solicitada no [!DNL Walmart Marketplace]
convertido para a hora local.</td>
</tr>
<tr>
<td>[!UICONTROL Return By]</td>
<td>A data em que o retorno deve ser reembolsado por para atender a [!DNL Walmart Marketplace] [requisitos](https://sellerhelp.walmart.com/seller/s/guide?language=en_US&amp;article=000007176f) convertido para a hora local.</td>
</tr>
<tr>
<td>[!UICONTROL Items]</td>
<td>Lista o SKU e a quantidade de cada item listado na devolução.</td>
</tr>
<tr>
<td>[!UICONTROL Refund amount]</td>
<td>O valor total a ser reembolsado para os itens devolvidos.</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>Indica o status de retorno atual no fluxo de trabalho de retorno [!DNL Commerce]-<i>Recebido</i>, <i>Reembolsado</i> ou <i>Erro</i>.</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>Para entradas de devolução recebidas e reembolsadas, os detalhes do status fornecem um link para acessar o aviso de crédito para processamento de restituição. Se ocorrer um erro durante o processo de sincronização [!DNL Channel Manager] entre o Adobe Commerce e o [!DNL Walmart marketplace], este campo fornecerá a descrição do erro.</td>
</tr>
</table>

## Status de retorno

[!UICONTROL Return Status] fornece informações sobre o estado atual de [!DNL Walmart Marketplace] solicitações de retorno gerenciadas de Adobe Commerce ou Magento Open Source.

As atualizações de status de retorno ocorrem quando [!DNL Channel Manager] recebe uma solicitação de retorno do [!DNL Walmart Marketplace] ou quando o memorando de crédito [!DNL Commerce] é criado para processar o reembolso dos itens retornados.

Os retornos podem ter os seguintes status:

* **[!UICONTROL Received]**-Este é o status inicial da solicitação de retorno recebida do armazenamento [!DNL Walmart Marketplace]. O comerciante pode processar o reembolso da devolução selecionando **[!UICONTROL Create credit memo]** no [!UICONTROL Status details].

* **[!UICONTROL Refunded]** — Indica que um aviso de crédito foi criado para emitir um reembolso para os itens devolvidos. Os comerciantes podem exibir informações de reembolso selecionando **[!UICONTROL View credit memo]** no [!UICONTROL Status details].

* **[!UICONTROL Error]** — Retorna solicitações com erros. Podem ocorrer erros quando a solicitação de retorno do Walmart tiver dados ausentes ou incorretos. Ou, se [!DNL Channel Manager] não puder enviar a notificação de atualização de reembolso para o Walmart.

## Cenários de retorno

Os cenários a seguir descrevem como emitir reembolsos para diferentes tipos de solicitações de retorno de [!DNL Channel Manager].

* **Retorno completo**—Se a solicitação de devolução do Walmart Marketplace for para todos os itens no pedido, atualize a quantidade do aviso de crédito para reembolsar todos os itens.

* **Retorno parcial** - Se a solicitação de retorno do Walmart Marketplace se referir apenas a alguns itens de pedido, atualize a quantidade do aviso de crédito apenas para os itens a serem reembolsados.

* **O retorno já foi reembolsado pelo Walmart Marketplace**. Em alguns casos, um reembolso é processado em [!DNL Walmart Marketplace] antes que você processe o retorno no Gerenciador de Canais. Por exemplo, se um pedido do Commerce não for reembolsado dentro da janela de processamento de reembolso de 48 horas exigida pelo Walmart, o Walmart reembolsará automaticamente o pedido. Quando isso acontece, o Gerenciador de canais ainda sincroniza a solicitação de retorno com o Adobe Commerce para que você possa processar o retorno e emitir o aviso de crédito. Esse fluxo de trabalho garante que os detalhes do pedido em [!DNL Commerce] correspondam às informações do pedido no Walmart Marketplace.

>[!NOTE]
>
> Pode levar até cinco minutos para que as atualizações de reembolso sejam sincronizadas com o [!DNL Walmart Marketplace]. Você pode verificar o status de retorno atual no painel [!DNL Channel Manager] [!UICONTROL Returns].

## Processar uma solicitação de reembolso

1. Abra o painel [!UICONTROL Returns] da sua loja de canais de vendas.

   * No Administrador, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * Abra a exibição de loja selecionando o ícone de olho de uma loja de canal de vendas.

   * Você pode revisar os retornos selecionando a guia **[!UICONTROL Returns]**.

     Você também pode acessar informações de retorno na página [!UICONTROL Orders]. Procure [!UICONTROL Shipped] pedidos que tenham uma solicitação de devolução. Em seguida, selecione o link `Return requested` na coluna [!UICONTROL Status Details] para exibir e processar a solicitação.

1. Na tabela Retornos, encontre um retorno com o status *[!UICONTROL Received]*.

1. Na coluna itens, revise a lista de itens da ordem e a quantidade a ser reembolsada.

1. Processe a restituição emitindo um aviso de crédito.

   * Na coluna [!UICONTROL Status Details], selecione **[!UICONTROL Create credit memo]** para abrir a página Detalhes do pedido em [!DNL Commerce].

     Se o pedido não tiver sido faturado, a página Detalhes do pedido exibirá uma mensagem de erro solicitando a criação de um. Selecione **[!UICONTROL Create invoice]**. Em seguida, [crie e salve a fatura](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html).

   * Na página Detalhes do pedido, selecione **[!UICONTROL Credit Memo]**.

   * Na seção [!UICONTROL Items to Refund] de [!UICONTROL Credit Memo], atualize as informações de **[!UICONTROL Qty to refund]** e **[!UICONTROL Return to Stock]** dos itens incluídos na solicitação de devolução.

     Certifique-se de retornar apenas os itens listados na solicitação de devolução.

   * Para adicionar um comentário, insira o texto no **[!UICONTROL Credit Memo Comments]**

   * Selecione **[!UICONTROL Refund Offline]**.

Após concluir o reembolso, [!DNL Channel Manager] atualiza o status do retorno no painel [!UICONTROL Returns] para [!UICONTROL Refunded] e sincroniza a atualização para o Walmart para atualizar o status do retorno no marketplace.


## Exibir informações de reembolso para uma devolução

Você pode exibir informações sobre solicitações de devolução e processamento de reembolso no painel [!UICONTROL Returns].

1. Abra o painel Devoluções da sua loja de canal de vendas.

   * No Administrador, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * Abra a exibição de loja selecionando o ícone de olho de uma loja de canal de vendas.

   * Selecione **[!UICONTROL Returns]**.

1. Exiba pedidos reembolsados selecionando o cartão de status **[!UICONTROL Refunded]**.

1. Exibir detalhes do reembolso de uma devolução selecionando **[!UICONTROL View credit memo]**.

   ![Aviso de crédito para reembolsar itens devolvidos de um pedido [!DNL Walmart Marketplace]](assets/refund-credit-memo-for-marketplace-order.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Depois que um pedido é reembolsado, o painel [!UICONTROL Orders] não mostra informações de devolução. Para exibir informações de devolução, use o painel de [!DNL Channel Manager] Devoluções. Informações mais detalhadas sobre devoluções e reembolsos também estão disponíveis na página Detalhes do pedido.

## Corrigir erros de retorno

Podem ocorrer erros quando as informações de retorno forem recebidas de [!DNL Walmart Marketplace], ou quando [!DNL Channel Manager] sincroniza atualizações de status de [!DNL Commerce] para [!DNL Walmart Marketplace].

Se a operação de sincronização para uma atualização de retorno falhar, o painel de [!DNL Channel Manager] Retornos mostrará um status *[!UICONTROL Error]* para a entrada de retorno. Para garantir que as informações de devolução e reembolso sejam refletidas com precisão na conta do Walmart Marketplace, atualize manualmente o pedido em sua loja [!DNL Walmart Marketplace].
