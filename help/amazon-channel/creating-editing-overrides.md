---
title: Criar e editar substituições de canal de vendas do Amazon
description: Use substituições do Amazon Sales Channel para aplicar suas alterações a uma única lista do Amazon ou a várias listas.
feature: Sales Channels, Products, Configuration
exl-id: 3a254883-b88c-4c94-b4d5-8d7754b9afd2
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 0%

---

# Criar e editar sobreposições

É possível criar e substituir para uma lista ou editar ou remover uma substituição que tenha sido aplicada a uma lista. As substituições definem um valor definido para uma lista específica.

## Criar uma substituição para uma única lista

A ação _[!UICONTROL Create Override]_está disponível ao exibir listas nas guias_[!UICONTROL Inactive]_, _[!UICONTROL Active]_e_[!UICONTROL Ineligible]_.

1. Exibir uma listagem em uma página _[!UICONTROL Products Listings]_(guias_[!UICONTROL Inactive]_, _[!UICONTROL Active]_e_[!UICONTROL Ineligible]_).

1. Na coluna _[!UICONTROL Action]_, clique em **[!UICONTROL Select]**>**[!UICONTROL Create Override]**para abrir a página Substituições de Listagem de Produtos.

   ![criar substituição de listagem do Amazon](assets/amazon-select-create-override.png){width="220"}

1. Para garantir que você esteja visualizando a lista correta, verifique o _[!UICONTROL Listing Details]_.

1. Determine o tipo de sobreposição que está sendo criada.

   Você pode definir um único tipo de sobreposição ou qualquer combinação de tipos para a lista (Preço, Tempo de Manuseio, Condição, Notas do Vendedor).

   - **Preço** - Clique em **[!UICONTROL Change Listing Price]** e insira seu valor de preço definido para **[!UICONTROL Price Override]**.
   - **Tempo de Manuseio** - Clique em **[!UICONTROL Change Handling Time]** e insira o valor de tempo definido (em dias) para **[!UICONTROL Handling Time Override]**.
   - **Condição** - Clique em **[!UICONTROL Change Condition]** e escolha a opção correta para **[!UICONTROL Condition Override]**.
   - **Notas do Vendedor** - Clique em **[!UICONTROL Change Seller Notes]** e insira o texto das suas notas para **[!UICONTROL Seller Notes Override]**.

1. Clique em **[!UICONTROL Save Listing Override]**.

   A página _[!UICONTROL Product Listing Overrides]_é fechada. O status da listagem muda para `Relist in Progress`. A alteração será publicada no Amazon com a próxima sincronização de dados (conforme definido nas configurações cron). A listagem também é adicionada à guia_[!UICONTROL Overrides]_.

O exemplo a seguir mostra uma substituição que define um novo preço de `$55`, um novo tempo de manipulação de `1 day`, uma nova condição de `Used; Like New` e um novo texto de Nota ao Vendedor.

![Exemplo de substituição de listagem do Amazon](assets/amazon-overrides-edit.png){width="600" zoomable="yes"}

## Editar ou remover uma sobreposição de uma única lista {#edit-override-single-listing}

A ação _[!UICONTROL Edit Overrides]_está disponível ao exibir listas na guia_[!UICONTROL Overrides]_.

1. Exibir uma listagem na página _[!UICONTROL Product Listings]_(guia_[!UICONTROL Overrides]_).

1. Na coluna _[!UICONTROL Action]_, clique em **[!UICONTROL Select]**>**[!UICONTROL Edit Overrides]**.

   A página _[!UICONTROL Product Listing Overrides]_é aberta.

   ![Selecione uma substituição de listagem do Amazon](assets/amazon-select-edit-overrides.png){width="125"}

1. Para garantir que você esteja substituindo a lista correta, verifique o _[!UICONTROL Listing Details]_.

1. Para editar as configurações de _[!UICONTROL Override]_, defina as seções para o tipo que deseja alterar (Preço, Tempo de Manuseio, Condição, Notas do Vendedor).

   Para manter o mesmo tipo de substituição, selecione `No Change To <override type>` (padrão). Essa configuração deixa o valor de substituição definido anteriormente inalterado.

   - **Preço** - Clique em **[!UICONTROL Change Listing Price]** e insira seu valor de preço definido para **[!UICONTROL Price Override]**.
   - **Tempo de Manuseio** - Clique em **[!UICONTROL Change Handling Time]** e insira o valor de tempo definido (em dias) para **[!UICONTROL Handling Time Override]**.
   - **Condição** - Clique em **[!UICONTROL Change Condition]** e escolha a opção correta para **[!UICONTROL Condition Override]**.
   - **Notas do Vendedor** - Clique em **[!UICONTROL Change Seller Notes]** e insira o texto das suas notas para **[!UICONTROL Seller Notes Override]**.

1. Para remover um tipo de substituição, clique em **Remover** para cada um dos tipos que deseja remover. Se não for removido, o valor definido anteriormente permanecerá na substituição.

1. Clique em **[!UICONTROL Save Listing Override]**.

   A página _[!UICONTROL Product Listing Overrides]_é fechada. O status da listagem muda para `Relist in Progress`. A alteração será publicada no Amazon com a próxima sincronização de dados (conforme definido nas configurações cron). Se ainda não estiverem listadas, as listagens também serão adicionadas à guia_[!UICONTROL Overrides]_.

Acumulando no exemplo _Criar uma Substituição_. O exemplo a seguir mostra uma edição da substituição criada anteriormente que define um novo preço de `$50`, remove a substituição de Tempo de Manuseio e mantém as substituições anteriores de Condição e Notas do Vendedor.

![Editando ou removendo uma substituição](assets/amazon-overrides-edit-2.png){width="600" zoomable="yes"}
__

## Editar ou remover uma substituição para várias listagens {#edit-override-multiple-listings}

A ação _[!UICONTROL Edit Listing Overrides]_está disponível nas guias_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_ e _[!UICONTROL Ineligible]_.

>[!NOTE]
>
>Como você está modificando substituições para várias listagens, a seção _[!UICONTROL Listing Details]_não é exibida como ocorre ao modificar uma única listagem.

1. Exibir a listagem em uma página _[!UICONTROL Products Listings]_(_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_ e _[!UICONTROL Ineligible]_guias).

1. Marque a caixa de seleção na coluna do lado esquerdo de cada listagem que você deseja modificar.

1. Em _[!UICONTROL Actions]_, clique em **[!UICONTROL Edit Listing Overrides]**.

   A página _[!UICONTROL Product Listing Overrides]_é aberta.

   ![Selecione uma substituição de listagem do Amazon](assets/amazon-actions-edit-listing-overrides.png){width="200"}

1. Para editar as configurações de _[!UICONTROL Override]_, defina as seções para o tipo que deseja alterar (Preço, Tempo de Manuseio, Condição, Notas do Vendedor).

   Para manter uma substituição igual, selecione `No Change To <override type>` (padrão). Essa configuração deixa o valor de substituição definido anteriormente inalterado.

   - **Preço** - Clique em **[!UICONTROL Change Listing Price]** e insira seu valor de preço definido para **[!UICONTROL Price Override]**.
   - **Tempo de Manuseio** - Clique em **[!UICONTROL Change Handling Time]** e insira o valor de tempo definido (em dias) para **[!UICONTROL Handling Time Override]**.
   - **Condição** - Clique em **[!UICONTROL Change Condition]** e escolha a opção correta para **[!UICONTROL Condition Override]**.
   - **Notas do Vendedor** - Clique em **[!UICONTROL Change Seller Notes]** e insira o texto das suas notas para **[!UICONTROL Seller Notes Override]**.

1. Para remover um tipo de substituição, clique em **[!UICONTROL Remove]** para cada um dos tipos que deseja remover. Se não for removido, o valor definido anteriormente permanecerá na substituição.

1. Clique em **[!UICONTROL Save Listing Override]**.

   A página _[!UICONTROL Product Listing Overrides]_é fechada. O status das listagens muda para `Relist in Progress`. A alteração será publicada no Amazon com a próxima sincronização de dados (conforme definido nas configurações cron). Se ainda não estiverem listadas, as listagens também serão adicionadas à guia_[!UICONTROL Overrides]_.

### Substituir tipos

| Substituir | Descrição |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Override] | Uma substituição de preço define o preço das listagens. Essa substituição tem prioridade sobre todas as configurações automatizadas até que seja removida.<br><br>Para substituir o preço do seu produto, escolha **[!UICONTROL Change Listing Price]** e insira o novo preço para **[!UICONTROL Price Override]**. |
| [!UICONTROL Handling Time Override] | Uma substituição de tempo de manuseio define o tempo gasto (em dias) para processar e enviar produtos. Uma substituição de tempo de manuseio tem prioridade sobre todas as configurações de tempo de manuseio automatizadas e padrão até que a substituição seja removida.<br><br>O valor existente na caixa _[!UICONTROL Handling Time Override]_é o tempo de manipulação padrão definido nas [configurações da lista](./listing-settings.md) ou o tempo de manipulação de substituição definido. Se você remover uma substituição de tempo de manuseio, a lista assumirá como padrão o tempo de manuseio definido nas configurações da lista.<br><br>Para definir uma substituição de tempo de manuseio, escolha **[!UICONTROL Change Handling Time]**e insira o novo tempo de manuseio (em dias) para **[!UICONTROL Handling Time Override]**. |
| [!UICONTROL Condition Override] | Para substituir a Condição de Listagem, escolha **[!UICONTROL Change Condition]** e escolha a nova condição em **Substituição de Condição**. |
| [!UICONTROL Seller Notes Override] | Para produtos em seu catálogo definidos com uma condição diferente de `New`, uma nota ao vendedor pode ser adicionada para detalhar ainda mais seu produto e sua condição para possíveis compradores. Você pode inserir uma substituição da nota do vendedor para um produto de condição `New`, mas o Amazon não exibe a nota.<br><br>Para substituir as Notas do Vendedor, escolha **[!UICONTROL Change Seller Notes]** e insira a nova nota para **[!UICONTROL Seller Notes Override]**. |
