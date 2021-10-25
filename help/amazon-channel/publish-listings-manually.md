---
title: Publicar manualmente as listagens do Amazon
description: Quando necessário, você pode publicar manualmente as listagens do Amazon encerradas no seu administrador do Commerce.
exl-id: ca3f674e-d93a-44a6-8c06-b417694a0f1e
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# Publicar manualmente as listagens do Amazon

Você pode publicar manualmente uma ou mais listagens do Amazon que foram encerradas.

1. Exibir uma ou mais listagens na _[!UICONTROL Ended]_na guia [Listas de produtos](./managing-product-listings.md) página (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_ou_[!UICONTROL Ineligible]_ ).

1. Na coluna à esquerda, clique em para verificar cada uma das listagens que deseja republicar.

1. Em _[!UICONTROL Actions]_, clique em **[!UICONTROL Publish Product to Amazon]**.

1. Clique em **[!UICONTROL OK]** na mensagem de confirmação.

   Uma mensagem é exibida para confirmar que as listagens selecionadas estão sendo processadas para publicação no Amazon.

   As informações de listagem são publicadas no Amazon com base nas configurações de cron. As informações de listagem são enviadas ao Amazon na próxima sincronização de dados. Até que a Amazon responda com a confirmação da listagem, as listagens publicadas manualmente permanecem no _Pronto para listar_ com uma `List in Progress` status. Quando a confirmação da listagem é recebida do Amazon, as listagens são movidas para o _Ativo_ com uma `Active` status.
