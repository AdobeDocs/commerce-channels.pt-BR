---
title: Editar uma ASIN atribuída
description: Altere o valor ASIN de um produto Commerce que correspondeu incorretamente a uma de suas listagens do Amazon.
feature: Sales Channels, Products, Configuration
exl-id: 2aaeb700-96ac-4a15-9379-f74728d2dcbe
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# Editar uma ASIN atribuída

Você pode editar o valor da Amazon ASIN atribuído a um produto no catálogo [!DNL Commerce]. Esse recurso é útil se um produto de catálogo foi correspondido incorretamente a uma de suas listagens do Amazon. Alterar o ASIN atribuído à lista não altera o ASIN atribuído a um produto pelo Amazon. Ela só altera a lista do Amazon à qual o produto de catálogo corresponde.

Quando uma ASIN atribuída é alterada:

- O [!DNL Commerce] encerra suas listas do Amazon anexadas à ASIN antiga
- Valida o ASIN com o Amazon
- Cria uma lista para o ASIN atualizado
- Atualiza informações de lista no canal de vendas do Amazon

**_Para editar uma ASIN atribuída:_**

1. Exiba a listagem na página _[!UICONTROL Product Listings]_(guia_[!UICONTROL Inactive]_, _[!UICONTROL Active]_ou_[!UICONTROL Ineligible]_).

1. Em _[!UICONTROL Actions]_, clique em **[!UICONTROL Edit Assigned ASIN]**.

   Esta ação abre a página _[!UICONTROL Product Listing Update]_.

1. Para **[!UICONTROL Assign ASIN]**, insira o novo valor ASIN.

1. Para salvar as alterações, clique em **[!UICONTROL Save Listing Update]**.

![Editar uma ASIN atribuída](assets/amazon-assigned-asin-edit.png){width="600" zoomable="yes"}
