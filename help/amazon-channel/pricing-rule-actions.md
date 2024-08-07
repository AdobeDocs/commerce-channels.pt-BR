---
title: Canal de vendas do Amazon - Ações de regra de preço
description: Use as ações de regra de preço para definir os cálculos de ajuste aplicados à origem do preço para determinar o preço de listagem do Amazon.
feature: Sales Channels, Price Rules
exl-id: c46bd5c2-7994-45b4-ae0c-9e473372c73a
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Ações de regra de preço

As Ações de Regra de Preço definem os cálculos de ajuste aplicados à origem do preço para determinar o preço da lista.

## Regra de preço padrão

Uma [regra de preço padrão](./standard-price-rules.md) permite aumentar ou diminuir um preço de listagem do Amazon por uma porcentagem específica ou valor fixo em dólar relativo ao preço de catálogo [!DNL Commerce] (ou fonte de preço).

| Seção | Descrição |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Select Rule Type]](./standard-price-rules.md) | Defina o tipo de regra para `Standard price rule`. |
| [[!UICONTROL Price Adjustment]](./standard-price-rules.md) | Definir os cálculos de ajuste aplicados à origem do preço para determinar o preço de listagem |

## Regra inteligente de reavaliação de preços

Uma [regra inteligente de reavaliação de preços](./intelligent-repricing-rules.md) usa os preços dos concorrentes da Amazon para determinar seu preço de lista. Os concorrentes são outros vendedores que estão listando os mesmos produtos que você está listando no Amazon.

| Seção | Descrição |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md) | Defina o tipo de regra como `Intelligent repricing rule` junto com seus requisitos de Preço de Concorrente do Source e Feedback. |
| [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md) | Definir variações para condições do mesmo produto vendido por concorrentes. |
| [[!UICONTROL Price Adjustment]](./price-adjustment.md) | Definir os cálculos de ajuste aplicados à origem do preço para determinar o preço de listagem |
| [[!UICONTROL Floor Price]](./floor-price.md) | Defina o menor preço para um produto para evitar que várias regras de precificação definam um preço de lista muito baixo. |
| [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md) | Defina o preço mais alto de um produto para garantir que seu preço permaneça competitivo. |
