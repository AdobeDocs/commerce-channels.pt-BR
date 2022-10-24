---
title: Devoluções e pedidos de reembolso
description: "Instruções para a concessão de restituições totais ou parciais para os pedidos de regresso recebidos de [!DNL Walmart Marketplace] from [!DNL Channel Manager] para Adobe Commerce e Magento Open Source."
source-git-commit: e9d2f53a955956a2b5086649d9ac18cc982ef4e3
workflow-type: tm+mt
source-wordcount: '1180'
ht-degree: 0%

---

# Devoluções e pedidos de reembolso

Quando um comprador solicita um retorno para itens de ordem comprados por [!DNL Walmart Marketplace], o Walmart cria uma solicitação de retorno. [!DNL Channel Manager] monitora o canal do marketplace para essas solicitações e sincroniza automaticamente as informações da solicitação de retorno ao Gerenciador de canais.

No lado do Commerce, a solicitação de retorno inicia o seguinte fluxo de trabalho:

1. O Gerenciador de canais cria uma solicitação de retorno correspondente com um status recebido e adiciona o número da ID de retorno ([!UICONTROL RMA #]) à [!UICONTROL Returns] painel. No [!DNL Orders] painel, os detalhes do status da ordem associada com as atualizações de retorno para incluir uma [!UICONTROL Return requested] para exibir e processar o retorno.

1. Os comerciantes processam o reembolso associado ao retorno criando um Aviso de Crédito após a [Fluxo de trabalho de reembolso do Adobe Commerce](https://docs.magento.com/user-guide/sales/credit-memos.html#refund-workflow). Todos os reembolsos são processados usando o método offline.

1. [!DNL Channel Manager] envia uma atualização de reembolso para o Walmart, para que o status de retorno possa ser atualizado para refletir o reembolso concluído da Adobe Commerce.

No Administrador da loja, você pode visualizar e processar retornos do Gerenciador de canais abrindo a loja de canais de vendas e selecionando **[!UICONTROL Returns]**.

![O Gerenciador de Canais Retorna o painel para processar reembolsos de solicitações de retorno recebidas do [!DNL Walmart Marketplace]](assets/returns-dashboard-view.png)

>[!NOTE]
>
>Você só pode processar reembolsos para ordens enviadas. Em [!DNL Channel Manager], o status do pedido deve ser [!UICONTROL Shipped]. Em [!DNL Walmart Marketplace] Conta do vendedor, a ordem deve ser [!UICONTROL Delivered].

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
<td>Filtre a exibição selecionando uma das [!UICONTROL Return Status] cartões.</td>
</tr>
<tr>
<td>Detalhes do status</td>
<td>Para entradas de retorno com o [!UICONTROL Received] ou [!UICONTROL Refunded] , é possível criar ou exibir o aviso de crédito para o reembolso selecionando o texto vinculado na coluna Detalhes do Status .</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>Para exibir detalhes do pedido, selecione a [!DNL Commerce] número do pedido na [!UICONTROL Order] tabela para abrir o pedido de comércio.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>Para modificar a configuração do canal, selecione as credenciais do canal Walmart Connection, os atributos mapeados ou os identificadores de envio, as configurações selecionam a variável [!DNL Commerce] número do pedido na [!UICONTROL Order] tabela. Em seguida, use [!DNL Commerce] opções de pedido para processar o pedido.</td>
</tr>
</table>

**Descrições das colunas**

<table>
<tr>
<td><strong>Campo</strong></td>
<td><strong>Descrição</strong></td>
</tr>
<tr>
<td>[!UICONTROL RMA #]</td>
<td>O número da Autorização de Devolução de Produto associado à solicitação de retorno recebida do [!DNL Walmart Marketplace]. Esse número é gerado pelo Walmart Marketplace [!UICONTROL Returns] quando o processo de devolução for iniciado.</td>
</tr>
<tr>
<td>[!DNL Commerce] Nº do pedido</td>
<td>O [!DNL Commerce] número do pedido associado aos itens incluídos na solicitação de retorno do Walmart Marketplace. Visualize os detalhes do pedido selecionando o número do pedido.</td>
</tr>
<tr>
<td>Solicitado</td>
<td>A data em que o retorno foi solicitado na [!DNL Walmart Marketplace]
convertido em horário local.</td>
</tr>
<tr>
<td>[!UICONTROL Return By]</td>
<td>A data em que a devolução deve ser reembolsada por [!DNL Walmart Marketplace] [requirements](https://sellerhelp.walmart.com/seller/s/guide?language=en_US&amp;article=000007176f) convertido em horário local.</td>
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
<td>Indica o status de retorno atual no [!DNL Commerce] fluxo de trabalho de retorno-<i>Recebido</i>, <i>Refundado</i>ou <i>Erro</i>.</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>Para entradas de devolução recebidas e reembolsadas, os detalhes do status fornecem um link para acessar o aviso de crédito para o processamento do reembolso. Se ocorrer um erro durante a [!DNL Channel Manager] processo de sincronização entre o Adobe Commerce e o [!DNL Walmart marketplace], este campo fornece a descrição do erro.</td>
</tr>
</table>

## Status da devolução

[!UICONTROL Return Status] fornece informações sobre o estado atual de [!DNL Walmart Marketplace] retornam solicitações gerenciadas do Adobe Commerce ou Magento Open Source.

As atualizações de status de retorno ocorrem quando [!DNL Channel Manager] recebe uma solicitação de retorno da [!DNL Walmart Marketplace] ou quando a [!DNL Commerce] o aviso de crédito é criado para processar o reembolso dos itens retornados.

Os retornos podem ter os seguintes status:

* **[!UICONTROL Received]**-Este é o status inicial da solicitação de retorno recebida do [!DNL Walmart Marketplace] armazenar. O comerciante pode processar o reembolso do retorno selecionando **[!UICONTROL Create credit memo]** no [!UICONTROL Status details].

* **[!UICONTROL Refunded]**—Indica que um aviso de crédito foi criado para emitir um reembolso para os itens devolvidos. Os comerciantes podem visualizar as informações de reembolso selecionando **[!UICONTROL View credit memo]** no [!UICONTROL Status details].

* **[!UICONTROL Error]**—Retorna solicitações com erros. Erros podem ocorrer quando a solicitação de retorno do Walmart tem dados ausentes ou incorretos. Ou, se [!DNL Channel Manager] O não pode enviar a notificação de atualização de reembolso para o Walmart.

## Cenários de retorno

Os cenários a seguir descrevem como emitir reembolsos para diferentes tipos de solicitações de retorno de [!DNL Channel Manager].

* **Retorno completo**—Se a solicitação de retorno do Walmart Marketplace for para todos os itens no pedido, atualize a quantidade do aviso de crédito para reembolsar todos os itens.

* **Retorno parcial**-Se a solicitação de retorno do Walmart Marketplace for apenas para alguns itens de pedido, atualize a quantidade do aviso de crédito somente para os itens a serem reembolsados.

* **Retorno já reembolsado através do Walmart Marketplace**-Em alguns casos, uma restituição é processada em [!DNL Walmart Marketplace] antes de processar o retorno no Gerenciador de canais. Por exemplo, se um pedido comercial não for reembolsado dentro da janela de processamento de reembolso de 48 horas exigida pelo Walmart, o Walmart reembolsará automaticamente o pedido. Quando isso acontece, o Gerenciador de canais ainda sincroniza a solicitação de retorno ao Adobe Commerce, para que você possa processar a devolução e emitir o aviso de crédito. Esse workflow garante que os detalhes do pedido em [!DNL Commerce] corresponde às informações de pedido no Walmart Marketplace.

>[!NOTE]
>
> Pode levar até cinco minutos para que as atualizações de reembolso sejam sincronizadas com o [!DNL Walmart Marketplace]. Você pode verificar o status de retorno atual do [!DNL Channel Manager] [!UICONTROL Returns] painel.

## Processar uma solicitação de reembolso

1. Abra o [!UICONTROL Returns] painel para a loja de canais de vendas.

   * Em Admin, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * Abra a visualização da loja selecionando o ícone de olho de uma loja de canais de vendas.

   * Você pode revisar os retornos selecionando o **[!UICONTROL Returns]** guia .

      Você também pode acessar informações de retorno do [!UICONTROL Orders] página. Procure por [!UICONTROL Shipped] pedidos que têm uma solicitação de retorno. Em seguida, selecione a `Return requested` no [!UICONTROL Status Details] para exibir e processar a solicitação.

1. Na tabela Retornos , encontre um retorno com a variável *[!UICONTROL Received]* status.

1. Na coluna items , revise a lista de itens de pedido e a quantidade para reembolso.

1. Processar o reembolso através da emissão de um aviso de crédito.

   * No [!UICONTROL Status Details] coluna, selecione **[!UICONTROL Create credit memo]** para abrir a página Detalhes do pedido em [!DNL Commerce].

      Se o pedido não tiver sido faturado, a página Detalhes do pedido exibirá uma mensagem de erro solicitando que você crie uma. Selecionar **[!UICONTROL Create invoice]**. Então, [criar e salvar a fatura](https://docs.magento.com/user-guide/sales/invoices.html).

   * Na página Detalhes do pedido , selecione **[!UICONTROL Credit Memo]**.

   * Em [!UICONTROL Items to Refund] da seção [!UICONTROL Credit Memo], atualize o **[!UICONTROL Qty to refund]** e **[!UICONTROL Return to Stock]** informações para os itens incluídos na solicitação de retorno.

      Certifique-se de retornar somente os itens listados na solicitação de retorno.

   * Para adicionar um comentário, insira o texto na **[!UICONTROL Credit Memo Comments]**

   * Selecionar **[!UICONTROL Refund Offline]**.

Após o pagamento da restituição, [!DNL Channel Manager] atualiza o status de retorno no [!UICONTROL Returns] painel para [!UICONTROL Refunded] e sincroniza a atualização para o Walmart para atualizar o status de retorno no marketplace.


## Exibir informações de reembolso para um retorno

Você pode visualizar informações sobre solicitações de retorno e processamento de reembolso do [!UICONTROL Returns] painel.

1. Abra o painel Devoluções para a loja de canais de vendas.

   * Em Admin, selecione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * Abra a visualização da loja selecionando o ícone de olho de uma loja de canais de vendas.

   * Selecionar **[!UICONTROL Returns]**.

1. Exibir ordens reembolsadas selecionando **[!UICONTROL Refunded]** cartão de status.

1. Exibir detalhes de reembolso de um retorno selecionando **[!UICONTROL View credit memo]**.

   ![Aviso de crédito para reembolso de itens devolvidos para um [!DNL Walmart Marketplace] pedido](assets/refund-credit-memo-for-marketplace-order.png)

>[!NOTE]
>
>Após o reembolso de um pedido, a variável [!UICONTROL Orders] o painel não mostra informações de retorno. Para exibir informações de retorno, use o [!DNL Channel Manager] Retorna o painel. Informações mais detalhadas sobre devolução e reembolso também estão disponíveis na página Detalhes do pedido .

## Corrigir erros de retorno

Erros podem ocorrer quando as informações de retorno são recebidas de [!DNL Walmart Marketplace]ou quando [!DNL Channel Manager] sincroniza atualizações de status de [!DNL Commerce] para [!DNL Walmart Marketplace].

Se a operação de sincronização de uma atualização de retorno falhar, a variável [!DNL Channel Manager] O painel de retornos mostra um *[!UICONTROL Error]* status da entrada de retorno. Para garantir que as informações de devolução e reembolso sejam refletidas com precisão na conta do Walmart Marketplace, atualize manualmente o pedido em seu [!DNL Walmart Marketplace] armazenar.


