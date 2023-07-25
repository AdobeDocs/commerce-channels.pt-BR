---
title: Publicar listas do Amazon manualmente
description: Quando necessário, você pode publicar manualmente suas listagens encerradas do Amazon com o administrador do Commerce.
feature: Sales Channels, Products, Merchandising
exl-id: ca3f674e-d93a-44a6-8c06-b417694a0f1e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# Publicar listas do Amazon manualmente

Você pode publicar manualmente uma ou mais listagens do Amazon que foram encerradas.

1. Exibir uma ou mais listagens no _[!UICONTROL Ended]_na guia [Listagens de produtos](./managing-product-listings.md) página (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_ou_[!UICONTROL Ineligible]_ guia ).

1. Na coluna à esquerda, clique em para marcar cada uma das listagens que deseja republicar.

1. Em _[!UICONTROL Actions]_, clique em **[!UICONTROL Publish Product to Amazon]**.

1. Clique em **[!UICONTROL OK]** na mensagem de confirmação.

   Uma mensagem é exibida para confirmar que as listagens selecionadas estão sendo processadas para publicação no Amazon.

   As informações de listagem são publicadas no Amazon com base nas configurações cron. As informações da listagem são enviadas para a Amazon na próxima sincronização de dados. Até que o Amazon responda com a confirmação da listagem, as listagens publicadas manualmente permanecerão no _Pronto para Listar_ com uma `List in Progress` status. Quando a confirmação da listagem é recebida do Amazon, as listagens são movidas para a _Ativo_ com um `Active` status.
