---
title: Canal de vendas da Amazon - Controles do Workspace
description: O Amazon Sales Channel fornece controles de espaço de trabalho que ajudam a localizar listagens, exibir informações e facilmente e aplicar ações.
feature: Sales Channels
exl-id: 4f76b1d0-ae58-435b-bd6d-50155a023421
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Controles do Workspace

A [página inicial](./amazon-sales-channel-home.md) do canal de vendas do Amazon tem alguns controles de espaço de trabalho comuns, incluindo Filtros, Exibição Padrão, Colunas e Exportar. Nem todas as páginas têm as mesmas opções de controle.

![exemplos de controle de espaço de trabalho do Amazon Sales Channel](assets/amazon-workspace-controls.png){width="600" zoomable="yes"}

## Ações

O seletor _[!UICONTROL Actions]_fornece uma lista de ações que estão disponíveis para um usuário para uma página. Quando escolhida, a ação é aplicada a todos os itens selecionados. Para aplicar uma ação a um item específico, marque a caixa de seleção na primeira coluna de cada item e escolha uma opção em_[!UICONTROL Actions]_.

Por exemplo, quando o seletor é exibido na página _[!UICONTROL Attributes]_, ele inclui a ação_[!UICONTROL Re-import Product Attribute Values]_. Escolher esta ação faz o ping da conta [!DNL Amazon Seller Central] correspondente e atualiza os dados [!DNL Commerce] de cada um dos itens de armazenamento do Amazon marcados na coluna do lado esquerdo.

![Exemplo de menu de ações](assets/amazon-sales-channel-home-actions-option.png){width="500"}

## Filtros

O controle _[!UICONTROL Filters]_mostra opções para restringir os dados mostrados na tabela. As opções de filtro se baseiam nas colunas selecionadas no controle Colunas. As opções de filtro são exibidas somente para colunas ativadas no controle Colunas.

Os controles de filtros podem incluir calendários dinâmicos para restringir dados de datas especificadas, menus suspensos para colunas que têm seleções predefinidas e campos de texto livre que podem conter dados personalizados.

O exemplo a seguir mostra as configurações para filtrar a lista de pedidos para mostrar apenas os pedidos que atendem aos seguintes critérios:

- Pedidos feitos entre 2/01/2019 e 2/07/2019, e
- Pedidos com um comprador chamado de `Smith` e
- Pedidos com status `Shipped`.

Quando tiver suas opções de filtragem definidas, clique em **[!UICONTROL Apply Filters]** para filtrar os dados listados. Clique em Cancelar para sair do controle Filtros sem aplicar.

![Exemplo de controle de filtros](assets/workspace-controls-filters.png){width="600" zoomable="yes"}

Depois de aplicar filtros aos seus dados, as informações de **[!UICONTROL Active Filters]** serão exibidas. Você pode clicar no ícone ![Limpar filtros](assets/x-icon-clear-filters.png) para limpar uma opção de filtro específica ou clicar em **[!UICONTROL Clear All]** para limpar todos os filtros aplicados.

![Exemplo de filtros ativos](assets/applied-filters-line.png){width="700"}

## Exibir

O controle Exibição é baseado nas colunas padrão da página, sendo assim chamado de Exibição padrão. É possível adicionar ou remover colunas disponíveis usando o controle Colunas. Ao personalizar suas colunas, você pode salvar a exibição como uma exibição personalizada no controle Exibição.

Quando você tiver suas colunas adicionadas ou removidas da exibição de página:

1. Clique em **[!UICONTROL Default View]** > **[!UICONTROL Save View As...]**.

1. Insira um nome para a exibição.

1. Para salvar a exibição personalizada, clique no ícone de seta.

![Exibir exemplo de controle](assets/workspace-controls-view.png)

Neste exemplo, a coluna _ID do Pedido_ é adicionada ao controle Coluna e salva como uma exibição personalizada. Observe que após o nome do modo de exibição personalizado ser salvo, o nome do Modo de Exibição mudou de _Modo de Exibição Padrão_ para o nome inserido.

Você pode alternar entre as exibições selecionando a exibição desejada no menu _[!UICONTROL View]_.

Para excluir ou alterar o nome da exibição personalizada, clique no ícone de lápis. Você pode digitar um nome diferente ou clicar no ícone da lixeira para excluir a exibição personalizada. A Exibição Padrão não pode ser excluída.

## Colunas

O controle Colunas permite adicionar ou remover colunas de dados da exibição da página. Cada página do canal de vendas do Amazon tem uma combinação predefinida de colunas de dados, mas a maioria das páginas tem colunas adicionais disponíveis. Se nenhuma coluna adicional estiver disponível, você ainda poderá remover as colunas padrão da exibição.

O exemplo a seguir mostra um controle Colunas. As opções marcadas correspondem aos cabeçalhos de coluna exibidos na página.

- Para adicionar uma coluna de dados à página, marque a caixa de seleção.
- Para remover uma coluna de dados da página, não marque a caixa de seleção.

![Exemplo de controle de colunas](assets/workspace-controls-columns.png){width="400"}

As alterações na caixa de seleção são exibidas imediatamente. Se você fizer alterações e sair da página, ela retornará à exibição de coluna padrão. Para alterações feitas regularmente, você pode salvar as alterações nas colunas como uma exibição personalizada no controle Exibição. Em seguida, você pode alternar no controle Exibição sem precisar adicionar ou remover colunas manualmente.

Você pode clicar em **[!UICONTROL Reset]** para definir as opções de volta às configurações padrão, ou pode clicar em **[!UICONTROL Cancel]** para sair sem suas alterações.

## Exportar

A opção Exportar permite exportar os dados para um arquivo de dados que podem ser importados para um software de terceiros ou banco de dados separado. Os dados exportados são limitados aos dados mostrados. Se necessário, adicione ou remova colunas antes de usar o controle Exportar.

Quando estiver pronto para exportar os dados, escolha uma opção de formato de exportação e clique em **[!UICONTROL Export]**.

- CSV - um arquivo de valor separado por vírgulas contendo dados de texto sem formatação
- XML do Excel - um formato de dados de planilha baseado em XML (normalmente usado para usuários do Excel)

O arquivo de dados gerado é salvo automaticamente na pasta designada para downloads.

![Controle de exportação](assets/workspace-controls-export.png){width="250"}
