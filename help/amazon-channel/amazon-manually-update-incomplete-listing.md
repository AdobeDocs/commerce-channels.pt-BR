---
title: Atualizar Informações Necessárias (Lista Incompleta)
description: O canal de vendas da Amazon fornece a guia Incompleto para monitorar produtos do catálogo de comércio que não têm informações exigidas pela Amazon.
exl-id: f278cd50-8f04-452e-b9c2-c87820f9faf2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---

# Atualizar informações obrigatórias (lista incompleta)

Listagens exibidas no _[!UICONTROL Incomplete]_inclua sua [!DNL Commerce] produtos do catálogo que atendem aos requisitos de qualificação do Amazon conforme definido nas regras de listagem, mas não têm informações exigidas pelo Amazon antes da listagem.

## Atualizar informações necessárias (não é possível atribuir à listagem do Amazon) {#update-required-info-unable-to-assign-to-amazon-listing}

1. Exibir as listagens na _[!UICONTROL Incomplete]_em [Gerenciar Listagens](./managing-product-listings.md).

1. No _[!UICONTROL Action]_coluna, clique em **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**para a listagem que deseja atualizar.

1. Revise as informações do produto do catálogo (SKU e Nome do produto) para o qual você está tentando corresponder a uma listagem do Amazon.

1. Para **[!UICONTROL Assign ASIN]**, insira o ASIN atribuído pela Amazon para a listagem que você deseja corresponder ao produto do catálogo.

1. Para salvar a correspondência do produto, clique em **[!UICONTROL Save Listing Update]**.

A listagem agora corresponde ao seu catálogo, e a listagem é atualizada e publicada no Amazon com base nas configurações de sua cron e listagem. Também é removido do _[!UICONTROL Incomplete]_guia .

![Atribuir manualmente o ASIN sem correspondência de listagem](assets/amazon-listing-update-assign-asin.png)

## Atualizar informações necessárias (Várias correspondências encontradas) {#update-required-info-multiple-matches-found}

1. Exibir as listagens na _[!UICONTROL Incomplete]_em [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. No _Ação_ coluna, clique em **Selecionar** > **Atualizar informações necessárias** para a listagem que deseja atualizar.

1. Revise as informações do produto do catálogo (SKU e Nome do produto) para o qual você está tentando corresponder a uma listagem do Amazon.

1. Para **[!UICONTROL Select Correct Amazon Listing]**, escolha o ASIN correto para a listagem que deseja corresponder a este produto.

   As opções listadas aqui incluem produtos de catálogo que são identificados como possíveis correspondências. Se nenhuma das opções estiver correta, você poderá escolher `Manually Enter Correct ASIN` e insira manualmente o ASIN do produto.

1. Se inserir o ASIN manualmente, insira o ASIN correto para **[!UICONTROL Manually Assign ASIN]**.

1. Para salvar a correspondência do produto, clique em **[!UICONTROL Save Listing Update]**.

![Selecionar manualmente o ASIN de várias correspondências possíveis](assets/amazon-listing-update-multiple-matches.png)

## Atualizar informações necessárias (tem variantes) {#update-required-info-has-variants}

1. Exibir as listagens na _[!UICONTROL Incomplete]_em [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. No _[!UICONTROL Action]_coluna, clique em **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**para a listagem que deseja atualizar.

1. Revise as informações do produto do catálogo (SKU e Nome do produto) para o qual você está tentando corresponder a uma listagem do Amazon.

1. Para **[!UICONTROL Select Correct Amazon Listing]**, escolha o ASIN correto para a listagem que deseja corresponder a este produto.

   As opções listadas aqui incluem produtos de catálogo que são identificados como possíveis correspondências. Se nenhuma das opções estiver correta, você poderá selecionar `Manually Enter Correct ASIN` e insira manualmente o ASIN do produto.

1. Se inserir o ASIN manualmente, insira o ASIN correto para **[!UICONTROL Manually Assign ASIN]**.

1. Para salvar a correspondência do produto, clique em **[!UICONTROL Save Listing Update]**.

![Selecionar manualmente o ASIN de possíveis correspondências de variante](assets/amazon-listing-update-multiple-matches.png)

## Atualizar informações necessárias (condição ausente) {#update-required-info-missing-condition}

1. Exibir as listagens na _[!UICONTROL Incomplete]_em [Gerenciar Listagens](./managing-product-listings.md).

1. No _[!UICONTROL Action]_coluna, clique em **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**para a listagem que deseja atualizar.

1. Revise as informações do produto do catálogo (SKU e Nome do produto) para o qual você está tentando corresponder a uma listagem do Amazon.

1. Para **[!UICONTROL Condition]**, escolha a condição apropriada.

   A lista de opções disponíveis depende do [Condição de listagem de produtos](./product-listing-condition.md) configurações.

1. Para salvar a correspondência do produto, clique em **[!UICONTROL Save Listing Update]** .

![Atualizar manualmente a condição ausente](assets/amazon-update-listing-missing-condition.png)
