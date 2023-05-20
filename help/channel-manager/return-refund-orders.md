---
title: Ordens de Devolução e de Reembolso
description: Instruções para a emissão de reembolsos totais ou parciais para pedidos de devolução recebidos do [!DNL Walmart Marketplace] de [!DNL Channel Manager] para Adobe Commerce e Magento Open Source.
exl-id: 45617011-4add-444c-819b-6bb4164d03e4
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '1180'
ht-degree: 0%

---

# Ordens de Devolução e de Reembolso

Quando um comprador solicitar uma devolução para itens de ordem comprados por meio do [!DNL Walmart Marketplace], o Walmart cria uma solicitação de retorno. [!DNL Channel Manager] monitora o canal do marketplace para essas solicitações e sincroniza automaticamente as informações da solicitação de retorno com o Gerenciador de canais.

No lado do Comércio, a solicitação de retorno inicia o seguinte fluxo de trabalho:

1. O Gerenciador de canais cria uma solicitação de retorno correspondente com um status recebido e adiciona o número de ID de retorno ([!UICONTROL RMA #]) para o [!UICONTROL Returns] painel. No [!DNL Orders] painel de controle, os detalhes do status do pedido associado à devolução são atualizados para incluir uma [!UICONTROL Return requested] link para exibir e processar a devolução.

1. Os comerciantes processam a restituição associada à devolução criando um Aviso de Crédito após a [Fluxo de trabalho de reembolso do Adobe Commerce](https://docs.magento.com/user-guide/sales/credit-memos.html#refund-workflow). Todos os reembolsos são processados usando o método offline.

1. [!DNL Channel Manager] envia uma atualização de reembolso ao Walmart marketplace para que o status da devolução possa ser atualizado para refletir o reembolso concluído da Adobe Commerce.

No Administrador da loja, é possível visualizar e processar os retornos do Gerenciador de canais abrindo a loja de canais de vendas e selecionando **[!UICONTROL Returns]**.

![Gerenciador de canal Retorna o painel para processar reembolsos de solicitações de retorno recebidas do [!DNL Walmart Marketplace]](assets/returns-dashboard-view.png)

>[!NOTE]
>
>Você só pode processar reembolsos para ordens entregues. Entrada [!DNL Channel Manager], o status do pedido deve ser [!UICONTROL Shipped]. Entrada [!DNL Walmart Marketplace] Conta do vendedor, a ordem deve ser [!UICONTROL Delivered].

## Retorna Controles e Descrições de Coluna

As tabelas a seguir descrevem os controles e colunas disponíveis para [!DNL Channel Manager] retorna.

**Controles para[!UICONTROL Returns]**

<table>
<tr>
<td><strong>Controle</strong></td>
<td><strong>Descrição</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter returns]</td>
<td>Filtre a exibição selecionando uma das opções [!UICONTROL Return Status] cartões.</td>
</tr>
<tr>
<td>Detalhes do status</td>
<td>Para entradas de retorno com o [!UICONTROL Received] ou [!UICONTROL Refunded] status, você pode criar ou exibir o aviso de crédito para a restituição selecionando o texto vinculado na coluna Detalhes do Status.</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>Para exibir detalhes do pedido, selecione o [!DNL Commerce] número do pedido no [!UICONTROL Order] tabela para abrir a ordem do Commerce.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>Para modificar a configuração do canal, selecione as credenciais de conexão do canal Walmart, os atributos mapeados ou os identificadores de envio e as configurações selecionam o [!DNL Commerce] número do pedido no [!UICONTROL Order] tabela. Em seguida, use [!DNL Commerce] opções de ordem para processar a ordem.</td>
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
<td>O número de Autorização para Devolução de Mercadoria associado à solicitação de devolução recebida do [!DNL Walmart Marketplace]. Este número é gerado pelo Walmart Marketplace [!UICONTROL Returns] quando o processo de devolução é iniciado.</td>
</tr>
<tr>
<td>[!DNL Commerce] Nº do pedido</td>
<td>A variável [!DNL Commerce] número do pedido associado aos itens incluídos na solicitação de devolução do Walmart Marketplace. Exibir detalhes do pedido selecionando o número do pedido.</td>
</tr>
<tr>
<td>Solicitado</td>
<td>A data em que a devolução foi solicitada no [!DNL Walmart Marketplace]
convertido para a hora local.</td>
</tr>
<tr>
<td>[!UICONTROL Return By]</td>
<td>A data em que a devolução deve ser reembolsada por para atender [!DNL Walmart Marketplace] [requisitos](https://sellerhelp.walmart.com/seller/s/guide?language=en_US&amp;article=000007176f) convertido para a hora local.</td>
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
<td>Indica o status de retorno atual na [!DNL Commerce] workflow de retorno-<i>Recebido</i>, <i>Reembolsado</i>ou <i>Erro</i>.</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>Para entradas de devolução recebidas e reembolsadas, os detalhes do status fornecem um link para acessar o aviso de crédito para processamento de restituição. Se ocorrer um erro durante o [!DNL Channel Manager] processo de sincronização entre o Adobe Commerce e o [!DNL Walmart marketplace], esse campo fornece a descrição do erro.</td>
</tr>
</table>

## Status de retorno

[!UICONTROL Return Status] fornece informações sobre o estado atual do [!DNL Walmart Marketplace] solicitações de retorno gerenciadas do Adobe Commerce ou Magento Open Source.

As atualizações de status de retorno ocorrem quando [!DNL Channel Manager] recebe uma solicitação de retorno do [!DNL Walmart Marketplace] ou quando a variável [!DNL Commerce] o aviso de crédito é criado para processar a restituição dos itens devolvidos.

Os retornos podem ter os seguintes status:

* **[!UICONTROL Received]**-Este é o status inicial da solicitação de retorno recebida do [!DNL Walmart Marketplace] armazenamento. O comerciante pode processar a restituição para a devolução selecionando **[!UICONTROL Create credit memo]** no [!UICONTROL Status details].

* **[!UICONTROL Refunded]**— Indica que um aviso de crédito foi criado para emitir uma restituição para os itens devolvidos. Os comerciantes podem exibir informações de reembolso selecionando **[!UICONTROL View credit memo]** no [!UICONTROL Status details].

* **[!UICONTROL Error]**—Retorna solicitações com erros. Podem ocorrer erros quando a solicitação de retorno do Walmart tiver dados ausentes ou incorretos. Ou, se [!DNL Channel Manager] O não pode enviar a notificação de atualização de reembolso para o Walmart.

## Cenários de retorno

Os cenários a seguir descrevem como emitir reembolsos para diferentes tipos de solicitações de devolução de [!DNL Channel Manager].

* **Retorno completo**—Se a solicitação de devolução do Walmart Marketplace for para todos os itens na ordem, atualize a quantidade do aviso de crédito para reembolsar todos os itens.

* **Retorno parcial**-Se a solicitação de devolução do Walmart Marketplace for somente para alguns itens de pedido, atualize a quantidade do aviso de crédito somente para os itens a serem reembolsados.

* **Devolução já reembolsada através do Walmart Marketplace**-Em alguns casos, um reembolso é processado em [!DNL Walmart Marketplace] antes de processar o retorno no Gerenciador de Canais. Por exemplo, se uma ordem do Commerce não for reembolsada dentro da janela de processamento de reembolso de 48 horas exigida pelo Walmart, o Walmart reembolsará automaticamente a ordem. Quando isso acontece, o Gerenciador de canais ainda sincroniza a solicitação de retorno com o Adobe Commerce para que você possa processar o retorno e emitir o aviso de crédito. Esse fluxo de trabalho garante que os detalhes do pedido em [!DNL Commerce] corresponde às informações de pedido no Walmart Marketplace.

>[!NOTE]
>
> Pode levar até cinco minutos para que as atualizações de reembolso sejam sincronizadas com o [!DNL Walmart Marketplace]. Você pode verificar o status de retorno atual na [!DNL Channel Manager] [!UICONTROL Returns] painel.

## Processar uma solicitação de reembolso

1. Abra o [!UICONTROL Returns] painel da sua loja de canal de vendas.

   * Em Admin, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * Abra a exibição de loja selecionando o ícone de olho de uma loja de canal de vendas.

   * É possível revisar os retornos selecionando o **[!UICONTROL Returns]** guia.

      Você também pode acessar as informações de devolução na [!UICONTROL Orders] página. Procure [!UICONTROL Shipped] ordens que têm uma solicitação de devolução. Em seguida, selecione o `Return requested` no [!UICONTROL Status Details] para exibir e processar a solicitação.

1. Na tabela Devoluções, localize um retorno com a variável *[!UICONTROL Received]* status.

1. Na coluna itens, revise a lista de itens da ordem e a quantidade a ser reembolsada.

1. Processe a restituição emitindo um aviso de crédito.

   * No [!UICONTROL Status Details] coluna, selecione **[!UICONTROL Create credit memo]** para abrir a página Detalhes do pedido em [!DNL Commerce].

      Se o pedido não tiver sido faturado, a página Detalhes do pedido exibirá uma mensagem de erro solicitando a criação de um. Selecionar **[!UICONTROL Create invoice]**. Em seguida, [criar e salvar a fatura](https://docs.magento.com/user-guide/sales/invoices.html).

   * Na página Detalhes do pedido, selecione **[!UICONTROL Credit Memo]**.

   * Entrada [!UICONTROL Items to Refund] seção do [!UICONTROL Credit Memo], atualize o **[!UICONTROL Qty to refund]** e **[!UICONTROL Return to Stock]** informações sobre os itens incluídos na solicitação de devolução.

      Certifique-se de retornar apenas os itens listados na solicitação de devolução.

   * Para adicionar um comentário, insira o texto no campo **[!UICONTROL Credit Memo Comments]**

   * Selecionar **[!UICONTROL Refund Offline]**.

Após concluir o reembolso, [!DNL Channel Manager] atualiza o status de retorno no [!UICONTROL Returns] painel para [!UICONTROL Refunded] e sincroniza a atualização para o Walmart para atualizar o status de retorno no marketplace.


## Exibir informações de reembolso para uma devolução

Você pode exibir informações sobre solicitações de devolução e processamento de reembolso no [!UICONTROL Returns] painel.

1. Abra o painel Devoluções da sua loja de canal de vendas.

   * Em Admin, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * Abra a exibição de loja selecionando o ícone de olho de uma loja de canal de vendas.

   * Selecionar **[!UICONTROL Returns]**.

1. Exibir ordens reembolsadas selecionando o **[!UICONTROL Refunded]** Cartão de status.

1. Exibir detalhes de reembolso para uma devolução selecionando **[!UICONTROL View credit memo]**.

   ![Aviso de crédito para reembolso de itens devolvidos de um [!DNL Walmart Marketplace] pedido](assets/refund-credit-memo-for-marketplace-order.png)

>[!NOTE]
>
>Após o reembolso de uma injunção, a [!UICONTROL Orders] o painel não mostra informações de retorno. Para exibir informações de devolução, use o [!DNL Channel Manager] Retorna o painel. Informações mais detalhadas sobre devoluções e reembolsos também estão disponíveis na página Detalhes do pedido.

## Corrigir erros de retorno

Podem ocorrer erros quando as informações de retorno são recebidas do [!DNL Walmart Marketplace]ou quando [!DNL Channel Manager] sincroniza atualizações de status de [!DNL Commerce] para [!DNL Walmart Marketplace].

Se a operação de sincronização de uma atualização de retorno falhar, a variável [!DNL Channel Manager] Retorna o painel que mostra uma *[!UICONTROL Error]* status da entrada de devolução. Para garantir que as informações de devolução e reembolso sejam refletidas com precisão na conta do Walmart Marketplace, atualize manualmente o pedido em seu [!DNL Walmart Marketplace] armazenamento.
