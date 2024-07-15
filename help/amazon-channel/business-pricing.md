---
title: "[!DNL (B2B) Business Price] para listagens do Amazon"
description: Você pode listar seus [!DNL Commerce] produtos de loja no site de Negócios (B2B) do Amazon habilitando negócios em sua conta do Amazon [!DNL Seller Central] .
role: Admin
level: Intermediate
feature: Sales Channels, Configuration, B2B, Tools and External Services, Merchandising, Integration
exl-id: 12a6cb2d-7a22-4b6d-9e94-ce91d564f42f
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# [!DNL (B2B) Business Price] para listagens do Amazon

(B2B) As configurações de Preço comercial fazem parte das configurações de lista da loja. As configurações de listagem são acessadas no [painel de armazenamento do Amazon](./amazon-store-dashboard.md).

O [!DNL Amazon Business] é um mercado exclusivo de contas comerciais registradas da Amazon e só está disponível nos Estados Unidos, França, Alemanha e Reino Unido. Se o marketplace permitir preços de negócios B2B, ele será editável nas configurações da lista.

O [!DNL B2B Business Pricing] permite que comerciantes com contas comerciais comprem entre si com o desempenho esperado da experiência de compra do Amazon. Com os preços de negócios B2B, as empresas podem oferecer preços em camadas com base na quantidade comprada.

Para que seus produtos sejam listados no site [!DNL Amazon Business (B2B)], primeiro você deve habilitar negócios em sua conta [!DNL Amazon Seller Central]. Para obter mais informações sobre o recurso B2B, consulte [Amazon: Central B2B](https://sellercentral.amazon.com/gp/help/G202161480/){target="_blank"} (requer logon da Central do Vendedor).

## Definir configurações de [!DNL (B2B) Business Price]

1. Clique em **[!UICONTROL Listing Settings]** no painel da loja.

1. Expanda a seção _[!UICONTROL (B2B) Business Price]_.

1. Para **[!UICONTROL Enable Business Pricing]**, escolha uma opção.

   - `Disabled` - (Padrão) Escolha quando você não deseja habilitar as vendas B2B. Todos os outros campos desta seção são desativados quando escolhidos.

   - `Enabled` - Escolha quando deseja habilitar as vendas B2B. Quando ativado, o preço comercial é definido como igual ao preço de lista depois que todas as regras de precificação forem aplicadas. O preço comercial segue o escopo de preços do site, se habilitado. Um preço comercial não pode ser inferior a US$ 1.

1. Para **[!UICONTROL Enable Tiered Pricing]**, escolha uma opção.

   - `Disabled` - (Padrão) Escolha quando deseja o mesmo preço de lista para todas as quantidades da ordem. Quando escolhidos, todos os _[!UICONTROL Pricing Level]_campos desta seção serão desabilitados.

   - `Enabled` - Escolha quando deseja habilitar ajustes de preços com base na quantidade da ordem. Quando escolhidos, os campos _[!UICONTROL Pricing Level]_são habilitados.

1. Conclua as configurações de **[!UICONTROL Pricing Level]**.

   Você pode definir até cinco configurações de quantidade/desconto que definem a camada de preços para suas listas de negócios. Em cada linha, insira o valor do limite de quantidade e o percentual de desconto a ser aplicado. Por exemplo, se você inserir `5` no primeiro campo da primeira linha e `5` no segundo campo, o preço aplicará um desconto de 5% quando outra empresa comprar uma quantidade de 5 ou mais.

1. Quando terminar, clique em **[!UICONTROL Save listing settings]**.

![Preços de Negócios da Amazon (B2B)](assets/amazon-business-pricing.png){width="500" zoomable="yes"}

| Campo | Descrição |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Business Pricing] | Opções: <ul><li>**[!UICONTROL Disabled]** - (Padrão) Escolha quando você não deseja habilitar as vendas entre empresas. Quando selecionados, todos os outros campos desta seção são desativados.</li><li>**[!UICONTROL Enabled]** - Escolha quando deseja habilitar as vendas da empresa para a empresa. Quando escolhido, o preço comercial é definido como igual ao preço de lista após a aplicação de todas as regras de preço. O preço comercial segue o escopo de preços do site, se habilitado. Um preço comercial não pode ser inferior a US$ 1.</li></ul> |
| [!UICONTROL Enable Tiered Pricing] | (obrigatório) Opções: <ul><li>**[!UICONTROL Disabled]** - (Padrão) Escolha quando deseja o mesmo preço de lista para todas as quantidades da ordem. Quando escolhidos, todos os _[!UICONTROL Pricing Level]_campos desta seção serão desabilitados.</li><li>**[!UICONTROL Enabled]** - Escolha quando deseja habilitar os preços que se ajustam com base na quantidade da ordem. Quando escolhidos, os campos _[!UICONTROL Pricing Level]_são habilitados.</li></ul> |
| [!UICONTROL Pricing Level One-Five (qty/discount)] | Quando a Precificação em Camadas está habilitada, você pode definir até cinco configurações de quantidade/desconto que definem a precificação em camada para suas listagens de negócios. Em cada linha, insira o valor do limite de quantidade e o percentual de desconto a ser aplicado. Por exemplo, se você inserir `5` no primeiro campo da primeira linha e `5` no segundo campo, o preço aplicará um desconto de 5% quando outra empresa comprar uma quantidade de cinco ou mais. |

**Acesso rápido** - [!UICONTROL Listing Settings] seções

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
