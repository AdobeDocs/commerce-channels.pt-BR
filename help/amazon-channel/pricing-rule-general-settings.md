---
title: Configurações gerais da regra de preços
description: Use as configurações gerais da regra de preço para definir as características principais de uma regra de preço de listagem.
redirect_from: /sales-channels/asc/ob-pricing-rules-general-settings.html: 
exl-id: 915b3eed-997e-4f94-a23f-0553a9dfe30c
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 0
ht-degree: 0%

---

# Configurações gerais da regra de preços

Defina o nome, a descrição, as datas ativas e a prioridade da regra.

## Preencha a seção Configurações Gerais da Regra de Preço

1. Para **[!UICONTROL Rule Name]** (obrigatório), insira o nome da regra.

   Esse nome é somente para fins de identificação interna. Quanto mais descritivo o nome da regra, melhor.

1. Para **[!UICONTROL Description]**, insira uma descrição detalhada da regra.

   Essa descrição pode incluir informações sobre os produtos que se qualificam, as datas ativas, a fórmula para calcular o preço ajustado ou qualquer outra informação que você ache útil se quiser modificar a regra.

1. Para **[!UICONTROL Status]**, escolha uma opção:

   - `Active` - Escolha essa opção quando desejar que a regra de preço se aplique aos produtos qualificados e ajuste o preço da listagem antes de publicar no Amazon.

   - `Inactive` - Escolha essa opção quando não quiser que a regra de preços se aplique aos seus produtos qualificados. Essa opção provavelmente será usada ao modificar uma regra de precificação ou ao desativá-la após uma promoção limitada.

1. Para **[!UICONTROL From]** e **[!UICONTROL To]**, insira uma data de início e de término para a regra de precificação.

   Você também pode clicar no ícone de calendário para selecionar uma data no calendário dinâmico. Essa opção automática de início e parada é benéfica ao configurar promoções sazonais ou de tempo limitado com datas de início e término definidas.

1. Para **[!UICONTROL Priority]**, insira um valor numérico para a prioridade da regra.

   O valor de prioridade igual a `1` é a prioridade mais alta. Quando você tem várias regras de preços ativas, pode usar esse valor de prioridade para determinar qual regra é aplicada primeiro. Este campo é necessário para usar o recurso _[!UICONTROL Discard Subsequent Rules]_.

1. Para **[!UICONTROL Discard Subsequent Rules]**, escolha uma opção:

   - `Yes` - Escolha essa opção quando não quiser que outras regras de preços que possam se aplicar a um produto sejam aplicadas. Descartar regras subsequentes significa que, se várias regras de preços se aplicarem ao mesmo produto, somente a regra de preços com o valor de prioridade definido mais alto será aplicada ao produto. Essa opção impede que várias regras de preços sejam empilhadas e oferece descontos adicionais e não intencionais.

   - `No` - Escolha essa opção quando quiser permitir que várias regras de preços sejam aplicadas ao mesmo produto. Essa opção pode resultar no empilhamento e no fornecimento de vários descontos a serem aplicados.

>[!NOTE]
>
>Para descartar regras subsequentes, uma regra de preço deve ter um valor definido **Priority**.

![Configurações gerais da regra de preços](assets/amazon-pricing-rule-general.png)

| Campo | Descrição |
|---|---|
| [!UICONTROL Rule Name] | (Obrigatório) Digite um nome para a regra, usado para fins de identificação interna. Quanto mais descritivo o nome da regra, melhor. Por exemplo, &quot;25% da venda de livros no final do ano&quot;. |
| [!UICONTROL Description] | Insira uma descrição detalhada que explica a regra (também usada para fins internos). Por exemplo, &quot;Venda de fim de ano, 25% de todos os itens na Categoria de Livros.&quot; |
| [!UICONTROL Status] | Opções:<ul><li>**[!UICONTROL Inactive]** - A regra de preço não se aplica às suas listagens. Essa opção pode ser usada ao modificar uma regra de precificação ou ao desativá-la após uma promoção limitada.</li><li>**[!UICONTROL Active]** - A regra de preço se aplica às suas listas e ajusta o preço da listagem antes de publicar no Amazon.</li></ul> |
| [!UICONTROL From] | Informe a data inicial em que a regra de precificação começa. Por exemplo, para ter uma venda durante o último mês do ano, você definiria a data `From` como 1º de dezembro para que a regra de preços fosse aplicada automaticamente às suas listagens do Amazon a partir de 1º de dezembro. |
| [!UICONTROL To] | Informe a data final quando a regra de precificação terminar. Continuando com o exemplo anterior, para limitar a venda ao último mês do ano, você definiria a data `To` como 31 de dezembro, de modo que a regra de preços expiraria em 31 de dezembro. |
| [!UICONTROL Priority] | Insira um valor para a prioridade da regra de precificação. Um valor de prioridade igual a `1` é a prioridade mais alta. Quando você tem várias regras de preços, pode usar o valor de prioridade para determinar qual regra é aplicada primeiro. Este campo é necessário para usar o recurso **Descartar regras subsequentes**. |
| [!UICONTROL Discard Subsequent Rules] | Usado para permitir ou impedir o empilhamento de várias regras de preço e fornecer descontos adicionais. Para descartar regras subsequentes, uma regra de precificação deve ter um valor definido para **[!UICONTROL Priority]**. Opções:<ul><li>**[!UICONTROL Yes]** - Escolha quando você não deseja que outras regras de preços que possam se aplicar a um produto sejam aplicadas. Descartar regras subsequentes significa que, quando várias regras de preços se aplicam ao mesmo produto, somente a regra de preços com o valor de prioridade definido mais alto é aplicada.</li><li>**[!UICONTROL No]** - Escolha quando você deseja permitir que várias regras de preços sejam aplicadas ao mesmo produto. Essa opção pode resultar no empilhamento e em vários descontos aplicados ao preço da listagem.</li></ul> |
