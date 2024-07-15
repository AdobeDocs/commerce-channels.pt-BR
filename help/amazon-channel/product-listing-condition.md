---
title: Canal de vendas do Amazon - Condição de lista de produtos
description: Use as configurações de Condição de listagem de produtos para mapear seus produtos da Commerce para uma condição de produto do Amazon, como "Novo" ou "Recondicionado".
feature: Sales Channels, Products, Merchandising
exl-id: f37ce3cf-7bfc-4dee-931e-a603008a71b8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Condição de lista de produtos

As configurações de condição de lista de produtos fazem parte das configurações de lista da loja. Você pode acessar as configurações de listagem no [painel de armazenamento](./amazon-store-dashboard.md).

O Amazon exige que uma lista de produtos tenha uma condição definida. Se todos os seus produtos forem a mesma condição, você poderá selecionar uma das opções de condição do Amazon para representar todos os seus produtos como seu valor de condição global. As condições padrão do Amazon incluem:

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
>Se você vender produtos renovados (recondicionados), deverá se inscrever no [!DNL Amazon Renewed Program]. Consulte [Produtos renovados](./renewed-products.md).

No entanto, se o catálogo contiver produtos em condições diferentes (como Novo, Usado e Recondicionado), você deverá escolher **[!UICONTROL Assign Condition Using Product Attribute]**. Essa configuração permite mapear o atributo de condição [!DNL Commerce] e os valores para as condições da sua lista do Amazon.

Durante [Tarefas de pré-configuração](./amazon-pre-setup-tasks.md), é recomendável criar um atributo de produto [!DNL Commerce] para a condição de um produto. Se você oferecer produtos em várias condições e não tiver criado um atributo de condição, consulte [Criar um atributo de produto em [!DNL Commerce]](./ob-creating-magento-attributes.md). Depois que o atributo de condição for criado, você poderá atribuir um valor de condição a cada um dos produtos no catálogo [!DNL Commerce].

## Definir configurações

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda a seção **[!UICONTROL Product Listing Condition]**.

1. Para **[!UICONTROL Listing Product Condition]**, escolha uma opção.

   Escolha uma das condições padrão do Amazon para o valor de condição global para todas as suas listagens. Configuração padrão `New`.

   Se você tiver produtos/listagens com condições diferentes, escolha `Assign Condition Using Product Attribute` para definir suas configurações de condição de produto nos campos adicionais exibidos.

1. Para o **Atributo de Condição**, escolha o atributo [!DNL Commerce] para mapear valores para cada um dos atributos de condição padrão do Amazon.

   Se você tiver produtos na condição `Used` ou `Collectible`, mas não fizer outras distinções, será possível mapear para uma única condição do Amazon `Used` ou `Collectible` e deixar as outras em branco. Este método mapeia todas as condições de `Used` ou `Collectible` para a única condição Usada ou Coletável do Amazon.

   Por exemplo, você tem uma única condição `Used` para seus produtos. Ao mapear, você escolhe se deseja mapear para a condição do Amazon `Used; Like New`, `Used; Very Good`, `Used; Good` ou `Used; Acceptable`. Preencha o campo somente para a condição Amazon desejada, deixando as outras opções do `Used` definidas como `--Select Option--`. Na imagem de exemplo, todos os produtos [!DNL Commerce] na condição `Used` são mapeados para a condição `Used; Very Good` do Amazon.

   Você também pode inserir texto descritivo para suas condições, exceto `New`.

1. Quando terminar, clique em **[!UICONTROL Save listing settings]**.

![Condição de listagem de produtos](assets/amazon-product-listing-condition.png){width="600" zoomable="yes"}

| Campo | Descrição |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Listing Product Condition] | A condição das suas listagens de produtos. Opções: `New` / `Refurbished` / `Used: Like New` / `Used: Very Good` / `Used: Good` / `Used: Acceptable` / `Collectible: Like New` / `Collectible: Very Good` / `Collectible: Good` / `Collectible: Acceptable` / `Assign Condition Using Product Attribute`<br><br>Se você vender uma única condição de produto, escolha uma das condições padrão do Amazon. Se o catálogo do [!DNL Commerce] contiver produtos em várias condições, escolha `Assign Condition Using Product Attribute`. |
| [!UICONTROL Condition Attribute] | O atributo [!DNL Commerce] que define a condição dos seus produtos. Selecione o atributo Magneto criado para mapear para o atributo de condição Amazon. No [exemplo de Tarefas de Pré-Instalação](./ob-creating-magento-attributes.md) recomenda-se nomeá-lo como `Amazon Condition`. Quando selecionados, campos adicionais são exibidos para mapear as condições padrão do Amazon. |
| [!UICONTROL Additional Condition fields] | Para cada uma das condições padrão do Amazon, escolha a condição correspondente. As opções são os rótulos de condição que você adicionou quando [criou seu atributo de condição do Amazon](./ob-creating-magento-attributes.md).<br><br>Se você tiver produtos na condição `Used` ou `Collectible`, mas não fizer distinção adicional, será possível mapear para uma única condição do Amazon `Used` ou `Collectible` e deixar as outras em branco. Este método mapeia todas as condições `Used` ou `Collectible` para a única condição Usada ou Coletável do Amazon. |

**Acesso rápido** - [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
