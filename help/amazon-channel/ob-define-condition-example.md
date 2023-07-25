---
title: "Exemplo: definir uma condição para regras de listagem do Amazon"
description: Ao criar suas regras de listagem, defina condições para identificar os produtos do catálogo do Commerce a serem listados no Amazon Marketplace.
feature: Sales Channels, Products, Configuration
exl-id: 8a48acfc-d31b-4919-bef7-8c300f0f9d94
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 0%

---

# Exemplo: definir uma condição

## Condições

É possível clicar em qualquer área nas condições em negrito para ver as várias opções.

**Não adicione condições se todos os produtos do site selecionado estiverem qualificados.**

>[!NOTE]
>
>Há um conjunto complexo de processos de back-end para se comunicar diretamente com os sistemas da Amazon. Com base no número de itens que você está tentando listar e na ocupação dos sistemas da Amazon (como Black Friday), pode levar algum tempo para que seus itens sejam listados no Amazon.

Consulte a seção Condições de [Criando uma Regra de Preço do Carrinho](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog-create.html).

## Definir uma condição

Esse processo pode ser simples ou detalhado, dependendo da configuração do catálogo. Você pode configurar suas condições para que, quando `ALL` ou `ANY` das condições definidas são `TRUE` ou `FALSE` para um produto, o produto está qualificado para ser listado no Amazon.

As condições são baseadas nos valores de atributo do produto existentes. Para aplicar a regra a todos os produtos, deixe a seção conditions em branco.

>[!NOTE]
>
>Se quiser definir uma condição com base em um atributo de produto específico, defina o **[!UICONTROL Use for Promo Rule Conditions]** configuração do atributo para `Yes`. Você pode acessar essa configuração no [Propriedades da vitrine](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes-add.html) página do atributo.

![Condição - linha 1](assets/ob-listing-rule-conditions-start.png){width="500"}

A regra neste exemplo define uma regra que define a qualificação do Amazon para todos os produtos de catálogo que têm o _AMAZON FBA_ atributo definido como `Yes`.

A instrução da regra tem dois links em negrito que, quando clicados, exibem as opções dessa parte da instrução. Se você salvar a condição sem alterar uma opção em negrito, a regra se aplica a todos os seus produtos.

- Clique em **[!UICONTROL ALL]** e escolha `ALL` ou `ANY`.
- Clique em **[!UICONTROL TRUE]** e escolha `TRUE` ou `FALSE`.
- Para aplicar a regra a todos os produtos, deixe a condição inalterada.

Você pode criar condições diferentes alterando a combinação desses valores. Neste exemplo, a seguinte condição é usada:

`If ALL of these conditions are TRUE:`

1. Clique no botão Adicionar (![Ícone Adicionar](assets/btn-add-grn.png)) no início da linha de condição e selecione um atributo no qual basear a condição, como uma combinação de condições ou um atributo de produto.

   - **[!UICONTROL Conditions Combination]** - Opte por permitir que você crie outro conjunto de `All/Any` e `True/False` condições no conjunto existente.

     ![Combinação de condições](assets/ob-conditions-combinations.png){width="500"}

   - **[!UICONTROL Product Attribute]** - Os atributos do produto dependem da configuração do atributo. Para que um atributo seja exibido na lista, ele deve ser configurado para uso nas condições de regra promocional. Consulte a _Usar para condições de regra promocional_ in [Atributos do produto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

     Na lista abaixo **[!UICONTROL Product Attribute]**, escolha o atributo que deseja usar como a base da condição. Neste exemplo, a condição selecionada é `Amazon FBA`.

     ![Linha de condição 2, parte 2](assets/ob-condition-attribute-dropdown.png){width="350"}

     A condição selecionada aparece na instrução, seguida por mais dois links em negrito. As opções diferem dependendo do atributo de produto selecionado.

     Depois que você define o atributo, ele não pode ser alterado. Para alterar o atributo, você deve excluir a linha e adicionar o novo atributo. Você pode excluir uma linha de condição clicando no botão Excluir (![Ícone Excluir](assets/btn-del-red.png)) no final da linha.

      1. Clique em **[!UICONTROL is]** e escolha o operador de comparação que descreve a condição dos produtos a serem atendidos.

         Para este exemplo, o operador de comparação é `is`. As opções disponíveis dependem do atributo selecionado na etapa anterior. As opções podem incluir diferentes opções de comparação, como valores correspondentes, sem incluir ou incluir pelo menos um de um valor, e maior que, igual a e menor que um valor numérico. Neste exemplo, as opções são `is` e `is not`.

      1. Clique em **[!UICONTROL ...]** e escolha o valor do atributo no qual a condição se baseia.

         As opções dependem da configuração do atributo. Você poderá ser solicitado a selecionar uma opção ou a inserir texto ou valores numéricos para a condição. Neste exemplo, a seleção é `Yes`.

         O item selecionado aparece na instrução para concluir a condição.

         ![Linha de condição 2, parte 3](assets/ob-listing-rule-condition-is.png){width="500"}

   Essa condição está concluída. Conforme dito, essa condição significa que qualquer produto em seu [!DNL Commerce] catálogo que tem o atributo FBA do Amazon definido como um valor de `Yes` está qualificado para listagem na Amazon para a região e loja. Você pode adicionar mais linhas de condição para restringir ainda mais seus produtos qualificados.

1, Para adicionar outra linha de condição à instrução, retorne à etapa 1 e repita o processo até que todas as condições desejadas sejam concluídas.

Você pode excluir uma linha da declaração de condição a qualquer momento clicando no botão Excluir (![Ícone Excluir](assets/btn-del-red.png)) no final da linha.
