---
title: Atualizar informações necessárias do Amazon
description: O canal de vendas da Amazon fornece a guia Incompleto para monitorar produtos de catálogo do Commerce sem as informações necessárias da Amazon.
exl-id: f278cd50-8f04-452e-b9c2-c87820f9faf2
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Atualizar informações necessárias (listagem incompleta)

Listagens exibidas na _[!UICONTROL Incomplete]_inclua seu [!DNL Commerce] produtos de catálogo que atendem aos requisitos de qualificação da Amazon, conforme definido nas regras de lista, mas que não têm as informações exigidas pela Amazon antes da lista.

## Atualizar informações necessárias (não é possível atribuir à lista do Amazon) {#update-required-info-unable-to-assign-to-amazon-listing}

1. Exibir as listagens no _[!UICONTROL Incomplete]_guia em [Gerenciar Listagens](./managing-product-listings.md).

1. No _[!UICONTROL Action]_clique em **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**para a lista que você deseja atualizar.

1. Revise as informações do produto do catálogo (SKU e Nome do produto) para as quais você está tentando corresponder a uma lista do Amazon.

1. Para **[!UICONTROL Assign ASIN]**, insira o ASIN atribuído pelo Amazon para a lista que você deseja corresponder ao produto de catálogo.

1. Para salvar a correspondência do produto, clique em **[!UICONTROL Save Listing Update]**.

A lista agora corresponde ao catálogo, e a lista é atualizada e publicada no Amazon com base nas configurações de cron e lista. Também é removido do _[!UICONTROL Incomplete]_guia.

![Atribuir ASIN manualmente para nenhuma correspondência de listagem](assets/amazon-listing-update-assign-asin.png){width="600" zoomable="yes"}

## Atualizar informações necessárias (várias correspondências encontradas) {#update-required-info-multiple-matches-found}

1. Exibir as listagens no _[!UICONTROL Incomplete]_guia em [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. No _Ação_ clique em **Selecionar** > **Atualização de informações necessárias** para a lista que você deseja atualizar.

1. Revise as informações do produto do catálogo (SKU e Nome do produto) para as quais você está tentando corresponder a uma lista do Amazon.

1. Para **[!UICONTROL Select Correct Amazon Listing]**, escolha a ASIN correta para a lista que você deseja corresponder a este produto.

   As opções listadas aqui incluem produtos de catálogo identificados como correspondências possíveis. Se nenhuma das opções estiver correta, você poderá escolher `Manually Enter Correct ASIN` e insira manualmente o ASIN do produto.

1. Se estiver inserindo o ASIN manualmente, insira o ASIN correto para **[!UICONTROL Manually Assign ASIN]**.

1. Para salvar a correspondência do produto, clique em **[!UICONTROL Save Listing Update]**.

![Selecionar manualmente ASIN entre várias correspondências possíveis](assets/amazon-listing-update-multiple-matches.png){width="600" zoomable="yes"}

## Atualizar informações necessárias (tem variantes) {#update-required-info-has-variants}

1. Exibir as listagens no _[!UICONTROL Incomplete]_guia em [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. No _[!UICONTROL Action]_clique em **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**para a lista que você deseja atualizar.

1. Revise as informações do produto do catálogo (SKU e Nome do produto) para as quais você está tentando corresponder a uma lista do Amazon.

1. Para **[!UICONTROL Select Correct Amazon Listing]**, escolha a ASIN correta para a lista que você deseja corresponder a este produto.

   As opções listadas aqui incluem produtos de catálogo identificados como correspondências possíveis. Se nenhuma das opções estiver correta, você poderá selecionar `Manually Enter Correct ASIN` e insira manualmente o ASIN do produto.

1. Se estiver inserindo o ASIN manualmente, insira o ASIN correto para **[!UICONTROL Manually Assign ASIN]**.

1. Para salvar a correspondência do produto, clique em **[!UICONTROL Save Listing Update]**.

## Atualizar informações necessárias (condição ausente) {#update-required-info-missing-condition}

1. Exibir as listagens no _[!UICONTROL Incomplete]_guia em [Gerenciar Listagens](./managing-product-listings.md).

1. No _[!UICONTROL Action]_clique em **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**para a lista que você deseja atualizar.

1. Revise as informações do produto do catálogo (SKU e Nome do produto) para as quais você está tentando corresponder a uma lista do Amazon.

1. Para **[!UICONTROL Condition]**, escolha a condição apropriada.

   A lista de opções disponíveis depende do seu [Condição de listagem de produtos](./product-listing-condition.md) configurações.

1. Para salvar a correspondência do produto, clique em **[!UICONTROL Save Listing Update]** .

![Atualizar manualmente a condição ausente](assets/amazon-update-listing-missing-condition.png){width="600" zoomable="yes"}
