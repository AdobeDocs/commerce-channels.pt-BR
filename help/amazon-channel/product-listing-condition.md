---
title: Condição de listagem de produtos
description: 'Use as configurações da Condição de listagem de produtos para mapear seus produtos do Commerce a uma condição de produto Amazon, como "Novo" ou "Refurbado".'
redirect_from: /sales-channels/asc/ob-product-listing-condition.html: 
exl-id: f37ce3cf-7bfc-4dee-931e-a603008a71b8
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 526
ht-degree: 0%

---

# Condição de listagem do produto

As configurações de condição da listagem de produtos fazem parte das configurações da listagem de lojas. Você pode acessar as configurações de listagem no [armazenar painel](./amazon-store-dashboard.md).

O Amazon requer uma lista de produtos para ter uma condição definida. Se todos os seus produtos forem a mesma condição, você poderá selecionar uma das opções de condição do Amazon para representar todos os seus produtos como o valor de condição global. As condições padrão do Amazon incluem:

- `New`
- `Refurbished`
- `Used; Like New`
- `Used; Very Good`
- `Used; Good`
- `Used; Acceptable`
- `Collectible; Like New`
- `Collectible; Very Good`
- `Collectible; Good`
- `Collectible; Acceptable`

>[!IMPORTANT]
>
>Se você vender produtos renovados (recondicionados), deverá se inscrever no [!DNL Amazon Renewed Program]. Consulte [Produtos Renovados](./renewed-products.md).

No entanto, se o catálogo contiver produtos em condições diferentes (como Novo, Usado e Refurorado), você deverá escolher **[!UICONTROL Assign Condition Using Product Attribute]**. Essa configuração permite mapear o atributo de condição [!DNL Commerce] e os valores para as condições da listagem do Amazon.

Durante [Tarefas de pré-configuração](./amazon-pre-setup-tasks.md), é recomendável criar um atributo de produto [!DNL Commerce] para a condição de um produto. Se você oferecer produtos em várias condições e não tiver criado um atributo de condição, consulte [Criar um atributo de produto em [!DNL Commerce]](./ob-creating-magento-attributes.md). Após criar o atributo de condição, é possível atribuir um valor de condição a cada um dos produtos no catálogo [!DNL Commerce].

## Definir configurações

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda a seção **[!UICONTROL Product Listing Condition]**.

1. Para **[!UICONTROL Listing Product Condition]**, escolha uma opção.

   Escolha uma das condições padrão do Amazon para seu valor de condição global para todas as suas listagens. A configuração padrão é `New`.

   Se você tiver produtos/listagens que têm condições diferentes, escolha `Assign Condition Using Product Attribute` para definir as configurações de condição do produto nos campos adicionais exibidos.

1. Para **Atributo de condição**, escolha o atributo [!DNL Commerce] para mapear valores para cada um dos atributos de condição padrão do Amazon.

   Se você tiver produtos na condição `Used` ou `Collectible`, mas não fizer distinção adicional, poderá mapear para uma única condição `Used` ou `Collectible` Amazon e deixar os outros em branco. Este método mapeia todas as suas condições `Used` ou `Collectible` para a única condição Amazon Usada ou Coletiva.

   Por exemplo, você tem uma única condição `Used` para seus produtos. Ao mapear, você escolhe se deseja mapear para a condição do Amazon `Used; Like New`, `Used; Very Good`, `Used; Good` ou `Used; Acceptable`. Preencha o campo somente para a condição do Amazon desejada, deixando as outras opções `Used` definidas como `--Select Option--`. Na imagem de exemplo, todos os produtos [!DNL Commerce] na condição `Used` são mapeados para a condição `Used; Very Good` do Amazon.

   Você também pode inserir texto descritivo para suas condições, exceto `New`.

1. Quando terminar, clique em **[!UICONTROL Save listing settings]**.

![Condição de listagem do produto](assets/amazon-product-listing-condition.png)

| Campo | Descrição |
|---|---|
| [!UICONTROL Listing Product Condition] | A condição das suas listas de produtos. Opções: `New` / `Refurbished` / `Used: Like New` / `Used: Very Good` / `Used: Good` / `Used: Acceptable` / `Collectible: Like New` / `Collectible: Very Good` / `Collectible: Good` / `Collectible: Acceptable` / `Assign Condition Using Product Attribute`<br><br>Se vender uma única condição de produto, escolha uma das condições padrão do Amazon. Se o catálogo [!DNL Commerce] contém produtos em várias condições, escolha `Assign Condition Using Product Attribute`. |
| [!UICONTROL Condition Attribute] | O atributo [!DNL Commerce] que define a condição para seus produtos. Selecione o atributo Magneto criado para mapear para o atributo de condição do Amazon. No [Pre-Setup Tasks example](./ob-creating-magento-attributes.md) recomenda nomeá-lo como `Amazon Condition`. Quando selecionados, campos adicionais são exibidos para mapear as condições padrão do Amazon. |
| [!UICONTROL Additional Condition fields] | Para cada uma das condições padrão do Amazon, escolha a condição correspondente. As opções são os rótulos de condição adicionados quando você [criou o atributo de condição do Amazon](./ob-creating-magento-attributes.md).<br><br>Se você tiver produtos na  `Used` condição  `Collectible` ou , mas não fizer distinções, é possível mapear para uma única condição  `Used` ou  `Collectible` Amazon e deixar os outros em branco. Esse método mapeia todas as condições `Used` ou `Collectible` para a única condição Amazon Usada ou Coletiva. |

**Acesso rápido**  -  [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
