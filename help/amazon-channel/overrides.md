---
title: Canal de vendas da Amazon - [!UICONTROL Overrides]
description: O Amazon Sales Channel fornece a guia Sobreposições para ajudar você a identificar e gerenciar como está aplicando sobreposições nas listagens do Amazon.
feature: Sales Channels, Price Rules
exl-id: e31bbbf9-b20d-42fd-a419-93d596e40be2
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# [!UICONTROL Overrides]

A variável _[!UICONTROL Overrides]_mostra suas listagens do Amazon às quais você aplicou uma substituição. Uma substituição é uma configuração específica de uma lista que pode ser usada para definir um valor definido para uma lista. Uma substituição aplicada a uma listagem define a configuração da listagem, independentemente de outras configurações ou regras de listagem definidas para as quais a listagem é elegível. Quando uma substituição é aplicada a uma listagem, ela é exibida na_[!UICONTROL Overrides]_ guia. O valor definido na substituição aparece na coluna apropriada para a lista. Há quatro tipos de sobreposições que podem ser aplicadas: Preço, Tempo de Manuseio, Condição e Notas do Vendedor.

## Tipos de sobreposições

| Tipo | Descrição |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Preço | Uma substituição que define o preço da lista, ignorando todas as outras configurações de preço para a lista. <br><br>**Exemplo**: você definiu uma regra de preço com desconto de 20% que se aplica a todos os produtos em uma categoria específica do catálogo. Você tem um produto novo no mercado e a demanda é alta, então você não quer que o preço com desconto seja aplicado à lista mesmo que o produto esteja nessa categoria. É possível selecionar a lista, [criar uma substituição de preço](./creating-editing-overrides.md#edit-override-single-listing)e definir o preço de lista em uma substituição de preço. |
| Tempo de manuseio | Uma substituição que define o tempo de manipulação para uma listagem, ignorando o tempo de manipulação padrão definido nas configurações de listagem.<br><br>**Exemplo**: o tempo de manipulação padrão das listagens é definido como 2 dias. Você tem um produto que é frágil e requer um dia extra para garantir sua embalagem especial para o transporte. É possível exibir a listagem, [criar uma substituição de tempo de manuseio](./creating-editing-overrides.md#edit-override-single-listing)e definirá o tempo de manuseio em três dias.<br><br>**Nota:** Não disponível para produtos definidos como `Fulfilled by Amazon`. |
| Condição | Uma substituição que define o valor de condição de uma listagem, independentemente do atributo de condição atribuído à listagem.<br><br>**Exemplo**: a maioria dos produtos no catálogo é Nova condição, mas você tem um produto que está em Condição recondicionada. É possível exibir a listagem, [criar uma substituição de condição](./creating-editing-overrides.md#edit-override-single-listing)e definir a condição Recondicionada para a lista.<br><br>**Nota:** Não disponível para produtos definidos como `Fulfilled by Amazon`. |
| Notas do vendedor | Uma substituição que define o _Notas do vendedor_ seção da lista. Este campo pode ser usado para adicionar mais informações relacionadas ao produto ou à substituição aplicada, normalmente usada para descrever a condição de produtos &quot;não novos&quot;. O texto neste campo aparece com a listagem para o comprador. As notas do vendedor não podem ser adicionadas a uma lista com um valor de condição de `New`. <br><br>**Exemplo**: você tem um produto que está em `Refurbished` condição. Normalmente, os produtos nessa condição não incluem manuais ou documentos, mas você tem um fornecedor diferente para esse produto que inclui um manual. É possível exibir a listagem, [criar uma substituição de notas do vendedor](./creating-editing-overrides.md#edit-override-single-listing)e adicione sua nota de texto exclusiva a esta lista sobre o manual para que o comprador saiba que ele foi incluído.<br><br>**Nota**: se um produto tiver uma condição definida de `New`, você pode inserir uma substituição de notas de vendedor, mas o Amazon não exibe notas de vendedor para uma `New` produto. |

É possível criar, editar ou remover uma sobreposição para uma [lista única](./creating-editing-overrides.md#edit-override-single-listing). No _[!UICONTROL Inactive]_,_[!UICONTROL Active]_, e _[!UICONTROL Ineligible]_, é possível clicar em **[!UICONTROL Select]**no_[!UICONTROL Action]_ e escolha **[!UICONTROL Create Override]**. A variável _[!UICONTROL Edit Overrides]_ação está disponível somente quando uma listagem tem uma substituição aplicada e é exibida na_[!UICONTROL Overrides]_ guia.

Também é possível criar, editar ou remover uma substituição para [várias listagens](./creating-editing-overrides.md#edit-override-multiple-listings). No _[!UICONTROL Inactive]_,_[!UICONTROL Active]_, e _[!UICONTROL Ineligible]_, é possível clicar em **[!UICONTROL Select]**no_[!UICONTROL Action]_ e escolha **[!UICONTROL Edit Listing Overrides]**.

Remover uma substituição informa à lista para usar os valores definidos pelas configurações e regras da lista.

Ao definir uma sobreposição, você também pode optar por informar um único tipo de sobreposição ou qualquer combinação dos tipos.

Consulte [Criar e editar sobreposições](./creating-editing-overrides.md).

>[!NOTE]
>
>Se você tiver listagens em andamento, o número de listagens será exibido em uma mensagem acima das guias.

![Guia Sobreposições](assets/amazon-overrides.png){width="600" zoomable="yes"}

As home pages dos canais de vendas do Amazon compartilham algumas informações [controles do espaço de trabalho](./workspace-controls.md) que permitem personalizar os dados exibidos.

## Colunas padrão

| Coluna | Descrição |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | A SKU (Unidade de manutenção de estoque) atribuída pela Amazon a um produto para identificar o produto, as opções, o preço e o fabricante. |
| [!UICONTROL ASIN] | Um bloco exclusivo de 10 letras e/ou números que identificam itens.<br><br>ASIN significa Números de identificação padrão da Amazon. Um ASIN é um bloco exclusivo de 10 letras e/ou números que identificam itens. Para livros, o ASIN é o mesmo que o número ISBN, mas para todos os outros produtos, um novo ASIN é criado quando o item é carregado para o seu catálogo. Você pode encontrar um ASIN de itens na página de detalhes do produto no Amazon, juntamente com mais detalhes relacionados ao item. |
| [!UICONTROL Condition Override] | A nova condição definida na substituição. Se a substituição aplicada à lista não for uma substituição de condição, `Not Selected` aparece nesta coluna. |
| [!UICONTROL Product Listing Name] | O nome do produto. |
| [!UICONTROL Seller Notes Override] | As notas do novo vendedor definidas na substituição. Se a substituição aplicada à lista não for esse tipo de substituição, essa coluna ficará em branco. |
| [!UICONTROL Handling Override] | O novo tempo de manuseio definido na substituição (em dias). Se a substituição aplicada à lista não for uma substituição de tempo de manuseio, esta coluna ficará em branco. |
| [!UICONTROL List Price Override] | O novo preço de lista definido na substituição. Se a sobreposição aplicada à lista não for uma sobreposição de preço, `N/A` aparece nesta coluna. |
| [!UICONTROL Action] | Lista de ações disponíveis que podem ser aplicadas a uma lista específica. Para aplicar uma ação, na _[!UICONTROL Action]_clique em **[!UICONTROL Select]**e escolha uma opção:<ul><li>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md#edit-override-single-listing)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
