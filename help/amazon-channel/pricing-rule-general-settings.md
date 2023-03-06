---
title: Configurações Gerais da Regra de Precificação
description: Use as configurações gerais da regra de preço para definir as características principais de uma regra de preço de lista.
redirect_from: /sales-channels/asc/ob-pricing-rules-general-settings.html
exl-id: 915b3eed-997e-4f94-a23f-0553a9dfe30c
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---

# Configurações Gerais da Regra de Precificação

Defina o nome, a descrição, as datas ativas e a prioridade da regra.

## Conclua a seção Configurações Gerais da Regra de Preço

1. Para **[!UICONTROL Rule Name]** (obrigatório), digite o nome da regra.

   Esse nome é somente para fins de identificação interna. Quanto mais descritivo for o nome da regra, melhor.

1. Para **[!UICONTROL Description]**, insira uma descrição detalhada da regra.

   Essa descrição pode incluir informações sobre os produtos qualificados, as datas de ativação, a fórmula para calcular o preço ajustado ou qualquer outra informação que você considere útil se quiser modificar a regra.

1. Para **[!UICONTROL Status]**, escolha uma opção:

   - `Active` - Escolha essa opção quando quiser que a regra de precificação seja aplicada aos seus produtos qualificados e ajuste os preços da lista antes de publicar no Amazon.

   - `Inactive` - Escolha essa opção quando não quiser que a regra de preço seja aplicada aos seus produtos qualificados. Essa opção provavelmente será usada ao modificar uma regra de precificação ou desativá-la após uma promoção limitada.

1. Para **[!UICONTROL From]** e **[!UICONTROL To]**, informe uma data inicial e final para a regra de precificação.

   Você também pode clicar no ícone do calendário para selecionar uma data no calendário dinâmico. Essa opção automática de início e interrupção é benéfica ao configurar promoções sazonais ou por tempo limitado com datas de início e término definidas.

1. Para **[!UICONTROL Priority]**, insira um valor numérico para a prioridade da regra.

   Valor de prioridade igual a `1` é a prioridade mais alta. Quando você tiver várias regras de precificação ativas, poderá usar esse valor de prioridade para determinar qual regra será aplicada primeiro. Este campo é obrigatório para usar a variável _[!UICONTROL Discard Subsequent Rules]_recurso.

1. Para **[!UICONTROL Discard Subsequent Rules]**, escolha uma opção:

   - `Yes` - Escolha essa opção quando não quiser que outras regras de preços que possam se aplicar a um produto sejam aplicadas. Descartar regras subsequentes significa que, se várias regras de precificação forem aplicadas ao mesmo produto, somente a regra de precificação com o valor de prioridade definido mais alto será aplicada ao produto. Essa opção impede que várias regras de preço sejam empilhadas e ofereçam descontos adicionais não intencionais.

   - `No` - Escolha essa opção quando quiser permitir que várias regras de preços sejam aplicadas ao mesmo produto. Essa opção pode resultar no empilhamento e no fornecimento de vários descontos a serem aplicados.

>[!NOTE]
>
>Para descartar regras subsequentes, uma regra de precificação deve ter uma definição **Prioridade** valor.

![Configurações gerais da regra de preço](assets/amazon-pricing-rule-general.png)

| Campo | Descrição |
|---|---|
| [!UICONTROL Rule Name] | (Obrigatório) Informe um nome para a regra, usado para fins de identificação interna. Quanto mais descritivo for o nome da regra, melhor. Por exemplo, &quot;25% de desconto na venda de livros no final do ano&quot;. |
| [!UICONTROL Description] | Informe uma descrição detalhada que explique a regra (também usada para fins internos). Por exemplo, &quot;Fim de ano de venda, 25% de desconto em todos os itens na Categoria Livros&quot;. |
| [!UICONTROL Status] | Opções:<ul><li>**[!UICONTROL Inactive]** - A regra de preço não se aplica às suas listas. Essa opção pode ser usada ao modificar uma regra de precificação ou desativá-la após uma promoção limitada.</li><li>**[!UICONTROL Active]** - A regra de preço se aplica às suas listas e ajusta o preço da lista antes de publicar no Amazon.</li></ul> |
| [!UICONTROL From] | Informe a data inicial de início da regra de precificação. Por exemplo, para ter uma venda durante o último mês do ano, você definiria a variável `From` de 1° de dezembro para que a regra de preços seja aplicada automaticamente às suas listagens do Amazon a partir de 1° de dezembro. |
| [!UICONTROL To] | Informe a data final em que a regra de precificação termina. Continuando o exemplo anterior, para limitar a venda ao último mês do ano, você definiria a variável `To` data como 31 de dezembro, portanto, a regra de preço expira em 31 de dezembro. |
| [!UICONTROL Priority] | Informe um valor para a prioridade da regra de precificação. Um valor de prioridade igual a `1` é a prioridade mais alta. Quando você tem várias regras de precificação, pode usar o valor de prioridade para determinar qual regra é aplicada primeiro. Este campo é obrigatório para usar a variável **Descartar Regras Subsequentes** recurso. |
| [!UICONTROL Discard Subsequent Rules] | Usado para permitir ou impedir que várias regras de preço sejam empilhadas e forneçam descontos adicionais. Para descartar regras subsequentes, uma regra de preço deve ter um valor definido para **[!UICONTROL Priority]**. Opções:<ul><li>**[!UICONTROL Yes]** - Escolha quando não deseja que nenhuma outra regra de precificação que possa ser aplicada a um produto. Descartar regras subsequentes significa que, quando várias regras de precificação são aplicadas ao mesmo produto, somente a regra de precificação com o maior valor de prioridade definido é aplicada.</li><li>**[!UICONTROL No]** - Escolha quando deseja permitir que várias regras de preços sejam aplicadas ao mesmo produto. Essa opção pode resultar em empilhamento e vários descontos aplicados ao preço da lista.</li></ul> |
