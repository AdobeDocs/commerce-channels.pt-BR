---
title: Atualizar informações necessárias do Amazon
description: O canal de vendas da Amazon fornece a guia Incompleto para monitorar os produtos de catálogo da Commerce que não têm as informações exigidas pela Amazon.
feature: Sales Channels, Merchandising, Catalog Management, Products
exl-id: f278cd50-8f04-452e-b9c2-c87820f9faf2
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Atualizar informações necessárias (listagem incompleta)

As listas exibidas na guia _[!UICONTROL Incomplete]_incluem seus produtos de catálogo [!DNL Commerce] que atendem aos requisitos de qualificação da Amazon, conforme definido em suas regras de lista, mas não têm as informações exigidas pela Amazon antes da lista.

## Atualizar informações necessárias (não é possível atribuir à lista do Amazon) {#update-required-info-unable-to-assign-to-amazon-listing}

1. Exibir as listagens na guia _[!UICONTROL Incomplete]_em [Gerenciar Listagens](./managing-product-listings.md).

1. Na coluna _[!UICONTROL Action]_, clique em **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**para a lista que você deseja atualizar.

1. Revise as informações do produto do catálogo (SKU e Nome do produto) para as quais você está tentando corresponder a uma lista do Amazon.

1. Para **[!UICONTROL Assign ASIN]**, insira o ASIN atribuído pela Amazon para a lista que você deseja corresponder ao produto de catálogo.

1. Para salvar a correspondência do produto, clique em **[!UICONTROL Save Listing Update]**.

A lista agora corresponde ao catálogo, e a lista é atualizada e publicada no Amazon com base nas configurações de cron e lista. Ele também é removido da guia _[!UICONTROL Incomplete]_.

![Atribuir ASIN manualmente para nenhuma correspondência de listagem](assets/amazon-listing-update-assign-asin.png){width="600" zoomable="yes"}

## Atualizar informações necessárias (várias correspondências encontradas) {#update-required-info-multiple-matches-found}

1. Exibir as listagens na guia _[!UICONTROL Incomplete]_em [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. Na coluna _Ação_, clique em **Selecionar** > **Atualizar informações necessárias** para a lista que você deseja atualizar.

1. Revise as informações do produto do catálogo (SKU e Nome do produto) para as quais você está tentando corresponder a uma lista do Amazon.

1. Para **[!UICONTROL Select Correct Amazon Listing]**, escolha a ASIN correta para a lista que você deseja corresponder a este produto.

   As opções listadas aqui incluem produtos de catálogo identificados como correspondências possíveis. Se nenhuma das opções estiver correta, você poderá escolher `Manually Enter Correct ASIN` e inserir manualmente o ASIN do produto.

1. Se estiver inserindo o ASIN manualmente, insira o ASIN correto para **[!UICONTROL Manually Assign ASIN]**.

1. Para salvar a correspondência do produto, clique em **[!UICONTROL Save Listing Update]**.

![Selecionar manualmente ASIN entre várias correspondências possíveis](assets/amazon-listing-update-multiple-matches.png){width="600" zoomable="yes"}

## Atualizar informações necessárias (tem variantes) {#update-required-info-has-variants}

1. Exibir as listagens na guia _[!UICONTROL Incomplete]_em [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. Na coluna _[!UICONTROL Action]_, clique em **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**para a lista que você deseja atualizar.

1. Revise as informações do produto do catálogo (SKU e Nome do produto) para as quais você está tentando corresponder a uma lista do Amazon.

1. Para **[!UICONTROL Select Correct Amazon Listing]**, escolha a ASIN correta para a lista que você deseja corresponder a este produto.

   As opções listadas aqui incluem produtos de catálogo identificados como correspondências possíveis. Se nenhuma das opções estiver correta, você poderá selecionar `Manually Enter Correct ASIN` e inserir manualmente o ASIN do produto.

1. Se estiver inserindo o ASIN manualmente, insira o ASIN correto para **[!UICONTROL Manually Assign ASIN]**.

1. Para salvar a correspondência do produto, clique em **[!UICONTROL Save Listing Update]**.

## Atualizar informações necessárias (condição ausente) {#update-required-info-missing-condition}

1. Exibir as listagens na guia _[!UICONTROL Incomplete]_em [Gerenciar Listagens](./managing-product-listings.md).

1. Na coluna _[!UICONTROL Action]_, clique em **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**para a lista que você deseja atualizar.

1. Revise as informações do produto do catálogo (SKU e Nome do produto) para as quais você está tentando corresponder a uma lista do Amazon.

1. Para **[!UICONTROL Condition]**, escolha a condição apropriada.

   A lista de opções disponíveis depende das configurações de [Condição de listagem de produtos](./product-listing-condition.md).

1. Para salvar a correspondência do produto, clique em **[!UICONTROL Save Listing Update]**.

![Atualizar manualmente a condição ausente](assets/amazon-update-listing-missing-condition.png){width="600" zoomable="yes"}
