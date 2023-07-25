---
title: Criar atributos de comércio para o Amazon
description: Antes de concluir o processo de integração do canal de vendas do Amazon, verifique se você tem a [!UICONTROL Commerce] atributos do produto.
role: Admin
feature: Sales Channels, Products, Configuration
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# Criar atributos de comércio para o Amazon

Antes de integrar o [!DNL Amazon Seller Central] contas, é uma prática recomendada adicionar [!DNL Commerce] [atributos do produto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) para mapear suas listagens de produtos. Após concluir a integração, você poderá gerenciar os atributos do produto por meio da [Atributos](./managing-attributes.md) guia do [Página inicial do canal de vendas do Amazon](./amazon-sales-channel-home.md) página.

Essas instruções detalham como criar [!DNL Commerce] atributos para Amazon ASIN e Amazon Condition. É recomendável criar atributos adicionais, incluindo Amazon EAN, Amazon ISBN e Amazon UPC. Você também pode criar um atributo de Preço Amazon se quiser usar o preço de lista Amazon como uma origem de preço para regras de precificação. Esses atributos são usados ao definir as configurações de lista e preço durante a integração. Use esses atributos também ao criar listagens do Amazon e ao atualizar e sincronizar suas [!DNL Commerce] catálogo com suas listagens do Amazon.

As configurações de Pesquisa no catálogo permitem definir parâmetros de pesquisa correspondentes que ajudam a mapear [!DNL Commerce] produtos com listagens do Amazon. Quando mapeado, o Amazon ativa ações relacionadas a preço, quantidade, substituições e sincronização de pedidos e produtos.

A definição desses valores aumenta o potencial para correspondências exatas, minimizando a necessidade de corresponder manualmente as listas de produtos posteriormente. Adicionar os atributos como parte da sua integração [tarefas de pré-configuração](./amazon-pre-setup-tasks.md), o canal de vendas da Amazon tem um maior potencial para corresponder automaticamente seus produtos durante a integração e sincroniza dados de produto entre o Amazon e o [!DNL Commerce] após a integração.

Se você criar apenas o atributo ASIN do Amazon (sem adicionar valores ASIN por produto), seu [!DNL Commerce] Os produtos do podem não corresponder automaticamente às suas listagens do Amazon. Você pode combinar seus produtos manualmente por meio do _Análise da loja_. No entanto, a correspondência manual não cria os elementos de dados necessários para compartilhar e sincronizar os dados do produto.

>[!IMPORTANT]
>
>Se você atualizar um ASIN, UPC ou outro elemento de dados de um produto correspondido manualmente, será necessário atualizar os dados em ambos os locais: o [!DNL Commerce] catálogo e a lista no seu [!DNL Amazon Seller Central] conta.

## Criar o atributo de produto Amazon ASIN

1. Faça logon no [!DNL Commerce] Admin.

1. Clique em **[!UICONTROL Stores]** no menu do lado esquerdo.

1. No _[!UICONTROL Attributes]_clique em **[!UICONTROL Product]**.

1. Para abrir as propriedades dos atributos, clique em **[!UICONTROL Add New Attribute]**.

1. Para **[!UICONTROL Default Label]**, insira `Amazon ASIN` (o nome do seu atributo).

1. Para **[!UICONTROL Catalog Input Type for Store Owner]**, escolha `Text Field`.

1. Para **[!UICONTROL Values Required]**, escolha `No`.

   Embora um Amazon ASIN seja necessário para listar um produto no Amazon, alguns de seus produtos de catálogo podem não estar listados no Amazon.

1. Expanda a _[!UICONTROL Advanced Attribute Properties]_e defina as opções:

   - Para **[!UICONTROL Attribute Code]**, insira `amazon_asin`.

   - Para **[!UICONTROL Scope]**, escolha `Global`.

   - Para **[!UICONTROL Unique Value]**, escolha `No`.

   - Para **[!UICONTROL Input Validation for Store Owner]**, escolha `None`.

   - Para **[!UICONTROL Add to Column Options]**, escolha `Yes`.

   - Para **[!UICONTROL Use in Filter Options]**, escolha `Yes`.

1. Clique em **[!UICONTROL Save Attribute]**.

![Atributo ASIN do Amazon](assets/creating-asin-attribute.png){width="600" zoomable="yes"}

## Criar o atributo de produto Condição Amazon

1. Faça logon no [!DNL Commerce] Admin.

1. Clique em **[!UICONTROL Stores]** no menu do lado esquerdo.

1. No _[!UICONTROL Attributes]_clique em **[!UICONTROL Product]**.

1. Para abrir as propriedades do atributo, clique em **[!UICONTROL Add New Attribute]**.

1. Para **[!UICONTROL Default Label]**, insira `Amazon Condition` (o nome do seu atributo).

1. Para **[!UICONTROL Catalog Input Type for Store Owner]**, escolha `Dropdown`.

   A variável _[!UICONTROL Manage Options (Values of your Attribute)]_é exibida.

1. Para **[!UICONTROL Values Required]**, escolha `No`.

1. Para **[!UICONTROL Manage Options (Values for your Attribute)]**, adicione cada uma das opções de condição.

   As condições padrão do Amazon incluem:

   - `New: Refurbished: Used`
   - `Like New: Used`
   - `Very Good: Used`
   - `Good: Used`
   - `Acceptable: Collectible`
   - `Like New; Collectible`
   - `Very Good: Collectible`
   - `Good: Collectible; Acceptable`

1. Clique em **[!UICONTROL Add Option]**.

1. Selecione o **[!UICONTROL Is Default]** para a condição que você deseja que seja a seleção padrão.

1. No _[!UICONTROL Admin]_insira o texto do rótulo da condição que está adicionando (como `New`, `Used`, e `Used-Like New`)

1. Clique em **[!UICONTROL Add Option]** para adicionar mais opções, conforme necessário.

1. Expandir _[!UICONTROL Advanced Attribute Properties]_e defina as opções.

   - Para **[!UICONTROL Attribute Code]**, insira `amazon_condition`.

   - Para **[!UICONTROL Scope]**, escolha `Global`.

   - Para **[!UICONTROL Unique Value]**, escolha `No`.

   - Para **[!UICONTROL Input Validation for Store Owner]**, escolha `None`.

   - Para **[!UICONTROL Add to Column Options]**, escolha `Yes`.

   - Para **[!UICONTROL Use in Filter Options]**, escolha `Yes`.

1. Clique em **[!UICONTROL Save Attribute]**.

![Atributo de Condição Amazon](assets/creating-amazon-condition-attribute.png){width="600" zoomable="yes"}

![Ícone Avançar](assets/btn-next.png) [**Continue em Adicionar ou verificar a chave de API**](./amazon-verify-api-key.md)
