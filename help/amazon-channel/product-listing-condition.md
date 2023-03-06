---
title: Condição de listagem de produtos
description: Use as configurações de Condição de listagem de produtos para mapear seus produtos do Commerce para uma condição de produto do Amazon, como "Novo" ou "Recondicionado".
redirect_from: /sales-channels/asc/ob-product-listing-condition.html
exl-id: f37ce3cf-7bfc-4dee-931e-a603008a71b8
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# Condição de listagem de produtos

As configurações de condição de lista de produtos fazem parte das configurações de lista da loja. É possível acessar as configurações da lista no [painel de armazenamento](./amazon-store-dashboard.md).

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

No entanto, se o catálogo contiver produtos em condições diferentes (como Novo, Usado e Recondicionado), você deverá escolher **[!UICONTROL Assign Condition Using Product Attribute]**. Essa configuração permite mapear os [!DNL Commerce] atributo de condição e valores para as condições da sua lista do Amazon.

Durante [Tarefas de pré-configuração](./amazon-pre-setup-tasks.md), é recomendável criar um [!DNL Commerce] atributo de produto para a condição de um produto. Se você oferecer produtos em várias condições e não tiver criado um atributo de condição, consulte [Criar um atributo de produto no [!DNL Commerce]](./ob-creating-magento-attributes.md). Após a criação do atributo de condição, é possível atribuir um valor de condição a cada um dos produtos no [!DNL Commerce] catálogo.

## Definir configurações

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda a **[!UICONTROL Product Listing Condition]** seção.

1. Para **[!UICONTROL Listing Product Condition]**, escolha uma opção.

   Escolha uma das condições padrão do Amazon para o valor de condição global para todas as suas listagens. A configuração padrão é `New`.

   Se você tiver produtos/listagens com condições diferentes, escolha `Assign Condition Using Product Attribute` para definir as configurações de condição do produto nos campos adicionais exibidos.

1. Para **Atributo de Condição**, escolha o [!DNL Commerce] atributo para mapear valores para cada um dos atributos de condição padrão do Amazon.

   Se você tiver produtos na `Used` ou `Collectible` condição, mas você não fizer distinção adicional, será possível mapear para um único `Used` ou `Collectible` Amazon e deixe os outros em branco. Esse método mapeia todos os `Used` ou `Collectible` para a única condição Amazon Used ou Collectible.

   Por exemplo, você tem um único `Used` condição para seus produtos. Ao mapear, você escolhe se deseja mapear para a condição do Amazon `Used; Like New`, `Used; Very Good`, `Used; Good`ou `Used; Acceptable`. Preencha o campo somente para a condição do Amazon desejada, deixando o outro `Used` opções definidas como `--Select Option--`. Na imagem de exemplo, todas as [!DNL Commerce] produtos em `Used` são mapeadas para a variável Amazon `Used; Very Good` condição.

   Você também pode inserir texto descritivo para suas condições, exceto `New`.

1. Quando terminar, clique em **[!UICONTROL Save listing settings]**.

![Condição de lista de produtos](assets/amazon-product-listing-condition.png)

| Campo | Descrição |
|---|---|
| [!UICONTROL Listing Product Condition] | A condição das suas listagens de produtos. Opções: `New` / `Refurbished` / `Used: Like New` / `Used: Very Good` / `Used: Good` / `Used: Acceptable` / `Collectible: Like New` / `Collectible: Very Good` / `Collectible: Good` / `Collectible: Acceptable` / `Assign Condition Using Product Attribute`<br><br>Se você vender uma única condição de produto, escolha uma das condições padrão do Amazon. Se o seu [!DNL Commerce] catálogo contém produtos em várias condições, escolha `Assign Condition Using Product Attribute`. |
| [!UICONTROL Condition Attribute] | A variável [!DNL Commerce] que define a condição dos seus produtos. Selecione o atributo Magneto criado para mapear para o atributo de condição Amazon. No [Exemplo de tarefas de pré-configuração](./ob-creating-magento-attributes.md) recomenda nomeá-lo como `Amazon Condition`. Quando selecionados, campos adicionais são exibidos para mapear as condições padrão do Amazon. |
| [!UICONTROL Additional Condition fields] | Para cada uma das condições padrão do Amazon, escolha a condição correspondente. As opções são os rótulos de condição que você adicionou ao [criou seu atributo de condição do Amazon](./ob-creating-magento-attributes.md).<br><br>Se você tiver produtos na `Used` ou `Collectible` condição, mas você não fizer distinção adicional, será possível mapear para um único `Used` ou `Collectible` Amazon e deixe os outros em branco. Este método mapeia todas as `Used` ou `Collectible` para a única condição Amazon Used ou Collectible. |

**Acesso rápido** - [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
