---
title: Substituições
description: O Amazon Sales Channel fornece a guia Substituições para ajudar a identificar e gerenciar a forma como você está aplicando substituições nas listas do Amazon.
exl-id: e31bbbf9-b20d-42fd-a419-93d596e40be2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%

---

# Substituições

A guia _[!UICONTROL Overrides]_mostra as listagens do Amazon às quais você aplicou uma substituição. Uma substituição é uma configuração específica da listagem que pode ser usada para definir um valor definido como uma listagem. Uma substituição aplicada a uma listagem define a configuração da listagem, independentemente de outras configurações de listagem definidas ou regras para as quais a listagem é elegível. Quando uma substituição é aplicada a uma listagem, a listagem é exibida na guia_[!UICONTROL Overrides]_. O valor definido na substituição aparece na coluna apropriada para a listagem. Há quatro tipos de substituições que podem ser aplicadas: Preço, Tempo de Manuseio, Condição e Notas do Vendedor.

## Tipos de substituições

| Tipo | Descrição |
|---|---|
| Preço | Uma substituição que define o preço da listagem, ignorando todas as outras configurações de preço da listagem. <br><br>**Exemplo**: Você definiu uma regra de preço de desconto de 20% que se aplica a todos os produtos de uma categoria específica do catálogo. Você tem um produto novo no mercado e a demanda é alta, então você não quer o preço com desconto aplicado à listagem, mesmo que o produto esteja nessa categoria. Você pode selecionar a listagem, [criar uma sobreposição de preço](./creating-editing-overrides.md#edit-override-single-listing), e definir o preço da listagem em uma sobreposição de preço. |
| Tempo de manipulação | Uma substituição que define o tempo de manuseio de uma listagem, ignorando o tempo padrão de manuseio definido nas configurações de listagem.<br><br>**Exemplo**: O tempo de manipulação padrão das listagens é definido como 2 dias. Você tem um produto frágil e requer um dia extra para garantir sua embalagem especial para envio. Você pode exibir a listagem, [criar uma substituição de tempo de manuseio](./creating-editing-overrides.md#edit-override-single-listing), e definir o tempo de manuseio em três dias.<br><br>**Observação:** não está disponível para produtos definidos como  `Fulfilled by Amazon`. |
| Condição | Uma substituição que define o valor da condição de uma listagem, independentemente do atributo de condição atribuído à listagem.<br><br>**Exemplo**: A maioria dos produtos do catálogo são Novas condições, mas você tem um produto em estado de renovação. Você pode exibir a listagem, [criar uma substituição de condição](./creating-editing-overrides.md#edit-override-single-listing) e definir a condição Refurbada para a listagem.<br><br>**Observação:** não está disponível para produtos definidos como  `Fulfilled by Amazon`. |
| Notas do vendedor | Uma substituição que define a seção _Notas do vendedor_ da listagem. Este campo pode ser usado para adicionar informações adicionais relacionadas ao produto ou à substituição aplicada, normalmente usada para descrever a condição de produtos &quot;não novos&quot;. O texto neste campo é exibido com a listagem do comprador. Notas de venda não podem ser adicionadas para uma listagem com um valor de condição `New`. <br><br>**Exemplo**: Você tem um produto em  `Refurbished` condição. Normalmente, os produtos nessa condição não incluem manuais ou documentos, mas você tem um fornecedor diferente para esse produto que inclui um manual. Você pode exibir a listagem, [criar uma sobreposição de notas de vendedor](./creating-editing-overrides.md#edit-override-single-listing), e adicionar sua nota de texto exclusiva a esta listagem sobre o manual para que o comprador saiba que ele está incluído.<br><br>**Observação**: Se um produto tiver uma condição definida de  `New`, você poderá inserir uma sobreposição de notas de vendedor, mas a Amazon não exibirá as notas de venda de um  `New` produto. |

Você pode criar, editar ou remover uma substituição para uma [listagem única](./creating-editing-overrides.md#edit-override-single-listing). Nas guias _[!UICONTROL Inactive]_,_[!UICONTROL Active]_ e _[!UICONTROL Ineligible]_, você pode clicar em **[!UICONTROL Select]**na coluna_[!UICONTROL Action]_ e escolher **[!UICONTROL Create Override]**. A ação _[!UICONTROL Edit Overrides]_está disponível somente quando uma listagem tem uma substituição aplicada e é exibida na guia_[!UICONTROL Overrides]_.

Você também pode criar, editar ou remover uma substituição para [várias listagens](./creating-editing-overrides.md#edit-override-multiple-listings). Nas guias _[!UICONTROL Inactive]_,_[!UICONTROL Active]_ e _[!UICONTROL Ineligible]_, você pode clicar em **[!UICONTROL Select]**na coluna_[!UICONTROL Action]_ e escolher **[!UICONTROL Edit Listing Overrides]**.

Remover uma substituição informa à listagem que use os valores definidos pelas configurações e regras da listagem.

Ao definir uma substituição, você também pode optar por inserir um único tipo de substituição ou qualquer combinação dos tipos.

Consulte [Criar e editar substituições](./creating-editing-overrides.md).

>[!NOTE]
>
>Se houver listagens em andamento, o número de listagens será exibido em uma mensagem acima das guias.

![Guia Substituições](assets/amazon-overrides.png)

As home pages do canal de vendas do Amazon compartilham alguns [controles do espaço de trabalho](./workspace-controls.md) comuns que permitem personalizar os dados exibidos.

## Colunas padrão

| Coluna | Descrição |
|---|---|
| [!UICONTROL Amazon Seller SKU] | A SKU (Stock Keeping Unit) atribuída pela Amazon a um produto para identificar o produto, as opções, o preço e o fabricante. |
| [!UICONTROL ASIN] | Um bloco exclusivo de 10 letras e/ou números que identifica itens.<br><br>ASIN significa os números de identificação padrão da Amazon. Um ASIN é um bloco exclusivo de 10 letras e/ou números que identifica itens. Para livros, o ASIN é o mesmo que o número ISBN, mas para todos os outros produtos, um novo ASIN é criado quando o item é carregado em seu catálogo. Você pode encontrar um ASIN de itens na página de detalhes do produto no Amazon, juntamente com mais detalhes relacionados ao item. |
| [!UICONTROL Condition Override] | A nova condição definida na substituição. Se a substituição aplicada à listagem não for uma substituição de condição, `Not Selected` aparecerá nesta coluna. |
| [!UICONTROL Product Listing Name] | O nome do produto. |
| [!UICONTROL Seller Notes Override] | As novas notas do vendedor definidas na substituição. Se a substituição aplicada à listagem não for esse tipo de substituição, essa coluna ficará em branco. |
| [!UICONTROL Handling Override] | O novo tempo de manuseio definido na substituição (em dias). Se a substituição aplicada à listagem não for uma substituição de tempo de manipulação, essa coluna ficará em branco. |
| [!UICONTROL List Price Override] | O novo preço da listagem definido na sobreposição. Se a substituição aplicada à listagem não for uma substituição de preço, `N/A` aparecerá nesta coluna. |
| [!UICONTROL Action] | Lista de ações disponíveis que podem ser aplicadas a uma lista específica. Para aplicar uma ação, na coluna _[!UICONTROL Action]_, clique em **[!UICONTROL Select]**e escolha uma opção:<ul><li>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md#edit-override-single-listing)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
