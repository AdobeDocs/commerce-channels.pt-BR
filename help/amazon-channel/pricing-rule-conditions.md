---
title: Condições das regras de preço
description: Use as condições da regra de preço para determinar quais produtos estão qualificados para a regra de preço de listagem.
redirect_from: /sales-channels/asc/ob-pricing-rules-conditions.html: 
exl-id: 39b03a2e-15c6-4c56-b0e0-7c6823e95fa8
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 0
ht-degree: 0%

---

# Condições das regras de preço

As condições determinam quais produtos são elegíveis para a regra de preço. A definição das condições para suas regras de preço do Amazon segue a mesma lógica e o mesmo processo que a definição das condições para [Regras de preço do carrinho](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){:target=&quot;_blank&quot;} em [!DNL Commerce].

>[!IMPORTANT]
>
>Se sua regra de preço se aplicar a todos os produtos em seu catálogo [!DNL Commerce], deixe esta seção em branco.

Qualquer área nas condições em negrito pode ser clicada para ver as várias opções.

## Exemplo: criar uma condição de regra de preço

Esse processo pode ser simples ou detalhado, dependendo da configuração do catálogo. Você pode definir suas condições para que, quando `ALL` ou `ANY` das condições forem `TRUE` ou `FALSE` para um produto, o produto esteja qualificado para a regra de preços a ser aplicada.

As condições são baseadas em seus [atributos do produto](https://docs.magento.com/user-guide/catalog/product-attributes.html){:target=&quot;_blank&quot;}. Para aplicar a regra a todos os produtos, deixe a seção condições em branco.

>[!NOTE]
>
>Se você quiser definir uma condição com base em um atributo de produto específico, **Usar para condições de regra promocional** para o atributo deverá ser definido como `Yes` em [Propriedades da frente de loja](https://docs.magento.com/user-guide/stores/attribute-product-create.html){:target=&quot;_blank&quot;} para o atributo.

![Condição da regra de preço - linha 1](assets/ob-price-rules-condition-1.png)

Este exemplo define uma regra que aplica um desconto de 25% a todos os produtos definidos na categoria `Books`.

A instrução da regra tem dois links em negrito, que, quando clicados, mostram as opções para essa parte da declaração de condição. Se você salvar a condição sem alterar uma opção em negrito, a regra se aplica a todos os seus produtos.

- Clique em **[!UICONTROL ALL]** e escolha `ALL` ou `ANY`.
- Clique em **[!UICONTROL TRUE]** e escolha `TRUE` ou `FALSE`.
- Para aplicar a regra a todos os produtos, mantenha a condição inalterada.

Você pode criar condições diferentes alterando a combinação desses valores. Neste exemplo, a seguinte condição é usada:

`If ALL of these conditions are TRUE:`

1. Para mostrar os atributos disponíveis para os quais a condição se aplica, clique no ícone Adicionar (![Adicionar ícone](assets/btn-add-grn.png)) no início da linha de condição e selecione um atributo no qual basear a condição.

   **[!UICONTROL Conditions Combination]** - Escolha criar outro conjunto de  `All/Any` e  `True/False` condições dentro da condição existente.

   ![Combinação de condições de regra de preço](assets/ob-conditions-combinations.png)

   **[!UICONTROL Product Attribute]** - Os atributos de produto disponíveis dependem da  [configuração do atributo](https://docs.magento.com/user-guide/stores/attribute-product-create.html){:target=&quot;_blank&quot;}. Para que um atributo seja exibido na lista, *[!UICONTROL Use for Promo Rule Conditions]* para o atributo deve ser definido como `Yes` em suas [propriedades da loja](https://docs.magento.com/user-guide/stores/attribute-product-create.html){:target=&quot;_blank&quot;}.

   - Para **[!UICONTROL Product Attribute]**, escolha o atributo que deseja definir como a base da condição. Para este exemplo, a condição selecionada é `Category`.

      ![Condição da regra de preço - linha 2, parte 2](assets/ob-price-rule-condition-2.png)

      A condição selecionada aparece na instrução, seguida por mais dois links em negrito. As opções diferem dependendo do atributo de produto selecionado.

      Após definir o atributo, ele não poderá ser editado. Para alterar o atributo, você deve excluir a linha e adicionar o novo atributo. Você pode excluir uma linha de condição clicando no ícone Excluir (![Excluir](assets/btn-del-red.png) no final da linha.

   - Clique em **[!UICONTROL is]** e escolha o operador de comparação que descreve a condição para que os produtos atendam.

      Para este exemplo, o operador de comparação é `is`. As opções disponíveis dependem do atributo selecionado na etapa anterior e podem incluir opções de comparação diferentes. As opções podem incluir valores correspondentes, não incluindo ou incluindo pelo menos um de um valor e maior que, igual a e menor que um valor numérico. Neste exemplo, as opções são `is` e `is not`.

   - Clique em **[!UICONTROL ...]** e escolha o valor do atributo no qual a condição se baseia. As opções dependem da configuração do atributo.

      Você pode ser solicitado a selecionar uma opção ou inserir um valor para a condição. Para este exemplo, o campo aparece em branco. Para selecionar suas categorias para a regra, clique no ícone do seletor (![ícone do Seletor](assets/btn-chooser.png)) para mostrar suas opções de seleção. Essa regra é para _Livros_, marque a caixa de seleção **[!UICONTROL Books]**. O número da categoria é preenchido. Para aceitar suas seleções de categoria, clique no ícone de marca de seleção verde (![Ícone de marca de seleção](assets/btn-check-mark-green.png)).

      ![Condição da regra de preço - linha 2, parte 3](assets/ob-price-rule-condition-3.png)

      O item selecionado aparece na instrução para concluir a condição.

      ![Condição da regra de preço - linha 2, parte 4](assets/ob-price-rule-condition-4.png)

      Essa condição de exemplo foi concluída. Conforme declarado, essa condição significa que qualquer produto em seu catálogo [!DNL Commerce] que tenha uma categoria definida de Livros (`4`) está qualificado para essa regra de preços. Você pode adicionar mais linhas de condição para restringir ainda mais seus produtos qualificados.

1. Para adicionar outra linha de condição à instrução, volte para a Etapa 1 e repita o processo até que todas as condições desejadas sejam concluídas.

   Você pode excluir uma linha da declaração de condição a qualquer momento clicando no ícone Excluir (![Excluir](assets/btn-del-red.png)) no final da linha.
