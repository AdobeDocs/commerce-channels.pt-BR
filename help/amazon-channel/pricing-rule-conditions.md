---
title: Canal de vendas da Amazon - Condições de regra de preço
description: Use as condições da regra de preço para determinar quais produtos são elegíveis para a regra de preço de lista.
feature: Sales Channels, Price Rules
exl-id: 39b03a2e-15c6-4c56-b0e0-7c6823e95fa8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# Condições da regra de preço

As condições determinam quais produtos são elegíveis para a regra de preço. A definição das condições para suas regras de preços do Amazon segue a mesma lógica e processo que a definição das condições para as [Regras de preço do carrinho](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html) em [!DNL Commerce].

>[!IMPORTANT]
>
>Se sua regra de preço se aplicar a todos os produtos no catálogo [!DNL Commerce], deixe esta seção em branco.

É possível clicar em qualquer área nas condições em negrito para ver as várias opções.

## Exemplo: criar uma condição de regra de preço

Esse processo pode ser simples ou detalhado, dependendo da configuração do catálogo. Você pode definir suas condições para que, quando `ALL` ou `ANY` das condições forem `TRUE` ou `FALSE` para um produto, o produto esteja qualificado para a regra de preço a ser aplicada.

As condições são baseadas em seus [atributos de produto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html). Para aplicar a regra a todos os produtos, deixe a seção conditions em branco.

>[!NOTE]
>
>Se você deseja definir uma condição com base em um atributo de produto específico, as **Condições de Uso da Regra Promo** do atributo devem ser definidas como `Yes` nas [Propriedades da vitrine](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-product-create.html) do atributo.

![Condição de regra de preço - linha 1](assets/ob-price-rules-condition-1.png){width="600" zoomable="yes"}

Este exemplo define uma regra que aplica um desconto de 25% a todos os produtos definidos na categoria `Books`.

A declaração da regra tem dois links em negrito que, quando clicados, mostram as opções dessa parte da declaração de condição. Se você salvar a condição sem alterar uma opção em negrito, a regra se aplica a todos os seus produtos.

- Clique em **[!UICONTROL ALL]** e escolha `ALL` ou `ANY`.
- Clique em **[!UICONTROL TRUE]** e escolha `TRUE` ou `FALSE`.
- Para aplicar a regra a todos os produtos, deixe a condição inalterada.

Você pode criar condições diferentes alterando a combinação desses valores. Neste exemplo, a seguinte condição é usada:

`If ALL of these conditions are TRUE:`

1. Para mostrar os atributos disponíveis aos quais a condição se aplica, clique no ícone Adicionar (![Ícone Adicionar](assets/btn-add-grn.png)) no início da linha de condição e selecione um atributo no qual basear a condição.

   **[!UICONTROL Conditions Combination]** - Opte por criar outro conjunto de condições `All/Any` e `True/False` dentro da condição existente.

   ![Combinação de condições da regra de preço](assets/ob-conditions-combinations.png){width="500"}

   **[!UICONTROL Product Attribute]** - Os atributos de produto disponíveis dependem da [configuração do atributo](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-product-create.html). Para que um atributo seja exibido na lista, *[!UICONTROL Use for Promo Rule Conditions]* para o atributo deve ser definido como `Yes` nas propriedades da vitrine.

   - Para **[!UICONTROL Product Attribute]**, escolha o atributo que deseja definir como a base da condição. Para este exemplo, a condição selecionada é `Category`.

     ![Condição de regra de preço - linha 2, parte 2](assets/ob-price-rule-condition-2.png){width="500"}

     A condição selecionada aparece na instrução, seguida por mais dois links em negrito. As opções diferem dependendo do atributo de produto selecionado.

     Depois que você define o atributo, ele não pode ser editado. Para alterar o atributo, você deve excluir a linha e adicionar o novo atributo. Você pode excluir uma linha de condição clicando no ícone Excluir (![Excluir](assets/btn-del-red.png) no final da linha.

   - Clique em **[!UICONTROL is]** e escolha o operador de comparação que descreve a condição a ser atendida pelos produtos.

     Neste exemplo, o operador de comparação é `is`. As opções disponíveis dependem do atributo selecionado na etapa anterior e podem incluir diferentes opções de comparação. As opções podem incluir valores correspondentes, sem incluir ou incluir pelo menos um de um valor, e maiores que, iguais a e menores que um valor numérico. Neste exemplo, as opções são `is` e `is not`.

   - Clique em **[!UICONTROL ...]** e escolha o valor do atributo no qual a condição se baseia. As opções dependem da configuração do atributo.

     Talvez seja solicitado que você selecione uma opção ou insira um valor para a condição. Para este exemplo, o campo aparece em branco. Para selecionar suas categorias para a regra, clique no ícone de seletor (![ícone de seletor](assets/btn-chooser.png)) para mostrar suas opções de seleção. Esta regra é para _Livros_, marque a caixa de seleção **[!UICONTROL Books]**. O número da categoria é preenchido. Para aceitar suas seleções de categoria, clique no ícone de marca de seleção verde (![Ícone de marca de seleção](assets/btn-check-mark-green.png)).

     ![Condição de regra de preço - linha 2, parte 3](assets/ob-price-rule-condition-3.png){width="500"}

     O item selecionado aparece na instrução para concluir a condição.

     ![Condição de regra de preço - linha 2, parte 4](assets/ob-price-rule-condition-4.png){width="500"}

     Este exemplo de condição está concluído. Conforme dito, essa condição significa que qualquer produto no catálogo [!DNL Commerce] que tenha uma categoria definida de Livros (`4`) está qualificado para essa regra de preço. Você pode adicionar mais linhas de condição para restringir ainda mais seus produtos qualificados.

1. Para adicionar outra linha de condição à instrução, retorne à Etapa 1 e repita o processo até que todas as condições desejadas sejam concluídas.

   Você pode excluir uma linha da declaração de condição a qualquer momento clicando no ícone Excluir (![Ícone Excluir](assets/btn-del-red.png)) no final da linha.
