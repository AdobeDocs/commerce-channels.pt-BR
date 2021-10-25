---
title: Criar e editar substituições
description: Use as substituições do Sales Channel do Amazon para aplicar suas alterações a uma única listagem do Amazon ou a várias listagens.
exl-id: 3a254883-b88c-4c94-b4d5-8d7754b9afd2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# Criar e editar substituições

Você pode criar e substituir para uma listagem ou editar ou remover uma substituição que tenha sido aplicada a uma listagem. As substituições definem um valor definido para uma listagem específica.

## Criar uma substituição para uma única listagem

O _[!UICONTROL Create Override]_A ação está disponível ao exibir listas no_[!UICONTROL Inactive]_, _[!UICONTROL Active]_e_[!UICONTROL Ineligible]_ guias.

1. Exibir uma listagem em uma _[!UICONTROL Products Listings]_página (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_e_[!UICONTROL Ineligible]_ ).

1. No _[!UICONTROL Action]_coluna, clique em **[!UICONTROL Select]**>**[!UICONTROL Create Override]**para abrir a página Substituições da lista de produtos .

   ![criar substituição da listagem do Amazon](assets/amazon-select-create-override.png)

1. Para garantir que você esteja visualizando a lista correta, verifique o _[!UICONTROL Listing Details]_.

1. Determine o tipo de substituição que você está criando.

   Você pode definir um único tipo de substituição ou qualquer combinação de tipos para a listagem (Preço, Tempo de Manuseio, Condição, Notas do Vendedor).

   - **Preço** - Clique **[!UICONTROL Change Listing Price]** e insira seu valor de preço definido para **[!UICONTROL Price Override]**.
   - **Tempo de manipulação** - Clique **[!UICONTROL Change Handling Time]** e insira o valor de tempo definido (em dias) para **[!UICONTROL Handling Time Override]**.
   - **Condição** - Clique **[!UICONTROL Change Condition]** e escolha a opção correta para a variável **[!UICONTROL Condition Override]**.
   - **Notas do vendedor** - Clique **[!UICONTROL Change Seller Notes]** e insira o texto de suas notas para **[!UICONTROL Seller Notes Override]**.

1. Clique em **[!UICONTROL Save Listing Override]**.

   O _[!UICONTROL Product Listing Overrides]_fecha a página. O status da listagem muda para `Relist in Progress`. A alteração será publicada no Amazon com a próxima sincronização de dados (conforme configurado nas configurações do cron). A listagem também é adicionada ao_[!UICONTROL Overrides]_ guia .

O exemplo a seguir mostra uma substituição que define um novo preço de `$55`, um novo período de tratamento de `1 day`, uma nova condição de `Used; Like New`e o novo texto Nota do vendedor.

![Exemplo de substituição da listagem do Amazon](assets/amazon-overrides-edit.png)

## Editar ou remover uma substituição para uma única listagem {#edit-override-single-listing}

O _[!UICONTROL Edit Overrides]_A ação está disponível ao exibir listas no_[!UICONTROL Overrides]_ guia .

1. Exibir uma listagem no _[!UICONTROL Product Listings]_página (_[!UICONTROL Overrides]_ ).

1. No _[!UICONTROL Action]_coluna, clique em **[!UICONTROL Select]**>**[!UICONTROL Edit Overrides]**.

   O _[!UICONTROL Product Listing Overrides]_será aberta.

   ![Selecione uma substituição de listagem do Amazon](assets/amazon-select-edit-overrides.png)

1. Para garantir que você esteja substituindo a lista correta, verifique a _[!UICONTROL Listing Details]_.

1. Para editar seu _[!UICONTROL Override]_, defina as seções para o tipo que deseja alterar (Preço, Tempo de Manuseio, Condição, Notas do Vendedor).

   Para manter um tipo de substituição igual, selecione `No Change To <override type>` (padrão). Essa configuração deixa o valor de substituição definido anteriormente inalterado.

   - **Preço** - Clique **[!UICONTROL Change Listing Price]** e insira seu valor de preço definido para **[!UICONTROL Price Override]**.
   - **Tempo de manipulação** - Clique **[!UICONTROL Change Handling Time]** e insira o valor de tempo definido (em dias) para **[!UICONTROL Handling Time Override]**.
   - **Condição** - Clique **[!UICONTROL Change Condition]** e escolha a opção correta para **[!UICONTROL Condition Override]**.
   - **Notas do vendedor** - Clique **[!UICONTROL Change Seller Notes]** e insira o texto de suas notas para **[!UICONTROL Seller Notes Override]**.

1. Para remover um tipo de substituição, clique em **Remover** para cada um dos tipos que você deseja remover. Se não for removido, o valor definido anteriormente permanecerá na substituição.

1. Clique em **[!UICONTROL Save Listing Override]**.

   O _[!UICONTROL Product Listing Overrides]_fecha a página. O status da listagem muda para `Relist in Progress`. A alteração será publicada no Amazon com a próxima sincronização de dados (conforme configurado nas configurações do cron). Se ainda não estiver listado, as listagens também serão adicionadas ao grupo_[!UICONTROL Overrides]_ guia .

Pocalhar no _Criar uma substituição_ exemplo. O exemplo a seguir mostra uma edição da substituição criada anteriormente que define um novo preço de `$50`, remove a substituição de Tempo de manipulação e mantém as substituições anteriores de Condição e Notas do vendedor .

![Edição ou remoção de uma substituição](assets/amazon-overrides-edit-2.png)
__

## Editar ou remover uma substituição para várias listagens {#edit-override-multiple-listings}

O _[!UICONTROL Edit Listing Overrides]_está disponível no_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_ e _[!UICONTROL Ineligible]_guias.

>[!NOTE]
>
>Como você está modificando substituições de várias listagens, a variável _[!UICONTROL Listing Details]_não é exibida como ao modificar uma única listagem.

1. Exibir a listagem em um _[!UICONTROL Products Listings]_página (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_ e _[!UICONTROL Ineligible]_).

1. Marque a caixa de seleção na coluna do lado esquerdo para cada uma das listagens que deseja modificar.

1. Em _[!UICONTROL Actions]_, clique em **[!UICONTROL Edit Listing Overrides]**.

   O _[!UICONTROL Product Listing Overrides]_será aberta.

   ![Selecione uma substituição de listagem do Amazon](assets/amazon-actions-edit-listing-overrides.png)

1. Para editar seu _[!UICONTROL Override]_, defina as seções para o tipo que deseja alterar (Preço, Tempo de Manuseio, Condição, Notas do Vendedor).

   Para manter uma substituição igual, selecione `No Change To <override type>` (padrão). Essa configuração deixa o valor de substituição definido anteriormente inalterado.

   - **Preço** - Clique **[!UICONTROL Change Listing Price]** e insira seu valor de preço definido para **[!UICONTROL Price Override]**.
   - **Tempo de manipulação** - Clique **[!UICONTROL Change Handling Time]** e insira o valor de tempo definido (em dias) para **[!UICONTROL Handling Time Override]**.
   - **Condição** - Clique **[!UICONTROL Change Condition]** e escolha a opção correta para **[!UICONTROL Condition Override]**.
   - **Notas do vendedor** - Clique **[!UICONTROL Change Seller Notes]** e insira o texto de suas notas para **[!UICONTROL Seller Notes Override]**.

1. Para remover um tipo de substituição, clique em **[!UICONTROL Remove]** para cada um dos tipos que você deseja remover. Se não for removido, o valor definido anteriormente permanecerá na substituição.

1. Clique em **[!UICONTROL Save Listing Override]**.

   O _[!UICONTROL Product Listing Overrides]_fecha a página. O status das listagens muda para `Relist in Progress`. A alteração será publicada no Amazon com a próxima sincronização de dados (conforme configurado nas configurações do cron). Se ainda não estiver listado, as listagens também serão adicionadas ao grupo_[!UICONTROL Overrides]_ guia .

### Tipos de substituição

| Substituir | Descrição |
|--- |--- |
| [!UICONTROL Price Override] | Uma substituição de preço define o preço das listagens. Essa substituição tem prioridade sobre todas as configurações automatizadas até que a substituição seja removida.<br><br>Para substituir o preço do seu produto, escolha **[!UICONTROL Change Listing Price]** e insira o novo preço para **[!UICONTROL Price Override]**. |
| [!UICONTROL Handling Time Override] | Uma substituição de tempo de manuseio define o tempo necessário (em dias) para processar e enviar produtos. Uma substituição de tempo de manuseio tem prioridade sobre todas as configurações de tempo de manuseio automatizado e padrão até que a substituição seja removida.<br><br>O valor que existe no _[!UICONTROL Handling Time Override]_é o seu tempo de manipulação padrão definido em sua [listar configurações](./listing-settings.md) ou seu tempo de manipulação de substituição definido. Se você remover uma substituição de tempo de manuseio, a listagem assumirá como padrão o tempo de manuseio definido em suas configurações de listagem.<br><br>Para definir uma substituição de tempo de manipulação, escolha **[!UICONTROL Change Handling Time]**e insira o novo tempo de manipulação (em dias) para **[!UICONTROL Handling Time Override]**. |
| [!UICONTROL Condition Override] | Para substituir a condição de listagem, escolha **[!UICONTROL Change Condition]** e escolha a nova condição de **Substituição de condição**. |
| [!UICONTROL Seller Notes Override] | Para produtos em seu catálogo que são definidos com uma condição diferente de `New`, uma nota de vendedor pode ser adicionada para detalhar ainda mais o produto e sua condição para possíveis compradores. Você pode inserir uma sobreposição de nota de vendedor para um `New` produto de condição, mas o Amazon não exibe a nota.<br><br>Para substituir as Notas do Vendedor, escolha **[!UICONTROL Change Seller Notes]** e insira a nova nota para **[!UICONTROL Seller Notes Override]**. |
