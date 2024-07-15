---
title: Canal de vendas do Amazon - Ações de lista de produtos
description: Use as configurações de Ações de listagem de produtos para definir como o catálogo do Commerce interage com o Amazon.
redirect_from: /sales-channels/asc/ob-product-listing-actions.html
feature: Sales Channels, Products, Merchandising, Configuration
exl-id: c7d3f22c-05c6-4826-99eb-543bac462cf8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# Ações de lista de produtos

As configurações de ações de listagem de produtos fazem parte das configurações de listagem de lojas. As configurações de listagem são acessadas no [painel de armazenamento](./amazon-store-dashboard.md).

Essas configurações definem como o catálogo interage com o Amazon. Estas configurações:

- Indique se os produtos do catálogo do [!DNL Commerce] que atendem aos requisitos de qualificação da Amazon são automaticamente enviados para a sua conta do [!DNL Amazon Seller Central] para criar listas.

- Definir o tempo de manuseio padrão de um pedido. Esse valor define o número de dias necessários para que você processe e envie um pedido. Por exemplo, se alguém selecionar um envio de dois dias, esse tempo de trânsito de remessa não será iniciado até que o processamento seja concluído e os pacotes sejam entregues a uma transportadora. O tempo total de delivery é (tempo de manuseio + tempo em trânsito + qualquer feriado).

## Definir configurações

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda a seção _[!UICONTROL Product Listing Actions]_.

1. Para **[!UICONTROL Automatic List Action]** (obrigatório), escolha uma opção:

   - `Automatically List Eligible Products` - (Padrão) Escolha quando deseja que seus produtos de catálogo [!DNL Commerce] (que atendem aos requisitos de qualificação da Amazon) sejam publicados automaticamente na Amazon e criem Listagens do Amazon.

   - `Do Not Automatically List Eligible Products` - Escolha quando deseja selecionar manualmente seus produtos de catálogo [!DNL Commerce] qualificados e criar listas do Amazon. Quando selecionados, os produtos do catálogo que atendem aos seus critérios de listagem e contêm todas as informações necessárias são exibidos na guia [_[!UICONTROL Ready to List]_](./ready-to-list.md) para publicação manual no Amazon.

1. Para **[!UICONTROL Default Handling Time]** (obrigatório), insira o número de dias necessários para o prazo de entrega antes da remessa.

   O valor padrão é `2` dias.

   >[!NOTE]
   >
   >Esse valor de tempo de entrega padrão só tem efeito para as listagens do Amazon criadas por meio do canal de vendas do Amazon. Qualquer listagem do Amazon criada na sua conta [!DNL Amazon Seller Central] usa o tempo de manipulação padrão definido no Amazon.

1. Quando terminar, clique em **[!UICONTROL Save listing settings]**.

![Ações de listagem de produtos](assets/amazon-product-listing-actions.png){width="600" zoomable="yes"}

| Campo | Descrição |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Automatic List Action] | Opções:<ul><li>**[!UICONTROL Automatically List Eligible Products]** - (Recomendado) Escolha quando deseja que seus produtos de catálogo do [!DNL Commerce] (que atendam aos requisitos de qualificação da Amazon) sejam publicados automaticamente na Amazon e criem Listagens do Amazon. Quando escolhida, a guia [_[!UICONTROL Ready to List]_](./ready-to-list.md) não é exibida. </li><li>**[!UICONTROL Do Not Automatically List Eligible Products]** - Escolha quando deseja selecionar manualmente [!DNL Commerce] produtos de catálogo qualificados e criar Listagens do Amazon. Quando selecionados, os produtos do catálogo que atendem aos seus critérios de listagem e contêm todas as informações necessárias são exibidos na guia [_[!UICONTROL Ready to List]_](./ready-to-list.md) para publicação manual.</li></ul> |
| [!UICONTROL Default Handling Time] | O valor numérico que representa o número de dias, em geral, necessários para processar e entregar seus pedidos. O valor padrão é `2`. Esse valor é usado para listagens do Amazon criadas em [!DNL Commerce] e publicadas no Amazon. O tempo de manipulação padrão das listagens do Amazon antes da integração com o [!DNL Commerce] não é afetado por essa configuração.<br><br>O valor definido no canal de vendas da Amazon não substitui o tempo de manuseio padrão definido em uma lista existente do Amazon. Quando um **[!UICONTROL Handling Time Override]** é ativado e depois removido, o Tempo de manuseio de um pedido é revertido para o valor definido aqui.<br><br>Se você tiver produtos com tempos de manuseio diferentes, poderá criar uma Substituição de Tempo de Manuseio no nível específico do produto. Você pode gerenciar o tratamento de substituições de tempo na guia [_[!UICONTROL Overrides]_](./overrides.md), oferecendo flexibilidade para gerenciar a satisfação do produto. Se não houver substituição de tempo de manuseio em [!DNL Commerce] para um produto, o padrão de tempo de manuseio será o valor definido na lista do Amazon.<br><br>O Tempo de Manuseio é um atributo regional. Quando o valor é alterado para uma listagem, a alteração afeta todas as listagens que compartilham o [!DNL Amazon Seller SKU] em todas as lojas Amazon que existem para a mesma região (definida em [integração de loja](./store-integration.md)). No entanto, alterar o valor de um [!DNL Amazon Seller SKU] compartilhado na região da América do Norte não afeta os mesmos produtos listados em um armazenamento com uma região definida diferente. O armazenamento da região com a data de criação mais antiga controla a prioridade das configurações de Tempo de manuseio padrão. |

**Acesso rápido** - [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
