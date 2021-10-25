---
title: Criar [!DNL Commerce] Atributos do Amazon
description: Antes de concluir o processo de integração do canal de vendas da Amazon, verifique se você tem o [!UICONTROL Commerce] atributos do produto.
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# Criar [!DNL Commerce] atributos para Amazon

Antes de integrar seu [!DNL Amazon Seller Central] é uma prática recomendada adicionar [!DNL Commerce] [atributos do produto](https://docs.magento.com/user-guide/stores/attributes-product.html){target=&quot;_blank&quot;} para mapear suas listas de produtos. Após concluir a integração, você pode gerenciar os atributos de produto por meio do [Atributos](./managing-attributes.md) da guia [Página inicial do canal de vendas da Amazon](./amazon-sales-channel-home.md) página.

Essas instruções detalham como criar [!DNL Commerce] atributos para Amazon ASIN e Amazon Condition. É recomendável criar atributos adicionais, incluindo Amazon EAN, Amazon ISBN e Amazon UPC. Você também pode criar um atributo de preço da Amazon se quiser usar seu preço de listagem da Amazon como uma fonte de preço para as regras de preços. Esses atributos são usados ao definir suas configurações de listagem e preço durante a integração. Use também esses atributos ao criar listas do Amazon e ao atualizar e sincronizar seu [!DNL Commerce] catálogo com suas listagens do Amazon.

As configurações de Pesquisa no catálogo permitem que você defina parâmetros de pesquisa correspondentes que ajudam a mapear as informações qualificadas [!DNL Commerce] produtos com listas do Amazon. Quando mapeado, o Amazon ativa ações relacionadas a preços, quantidade, substituições e sincronização de pedido e produto.

A definição desses valores aumenta a possibilidade de correspondências exatas, minimizando a necessidade de corresponder manualmente as listas de produtos posteriormente. Adicionar os atributos como parte de sua integração [tarefas de pré-configuração](./amazon-pre-setup-tasks.md), o canal de vendas da Amazon tem um potencial maior para combinar seus produtos automaticamente durante a integração e sincroniza os dados do produto entre o Amazon e a [!DNL Commerce] após a integração.

Se você criar apenas o atributo Amazon ASIN (sem adicionar valores ASIN por produto), sua [!DNL Commerce] Os produtos podem não corresponder automaticamente às suas listas do Amazon. Você pode fazer a correspondência manual de seus produtos por _Revisão da loja_. No entanto, a correspondência manual não cria os elementos de dados necessários para compartilhar e sincronizar os dados do produto.

>[!IMPORTANT]
>
>Se você atualizar um ASIN, UPC ou outro elemento de dados para um produto compatível manualmente, você deve atualizar os dados em ambos os lugares: your [!DNL Commerce] catálogo e a listagem em seu [!DNL Amazon Seller Central] conta.

## Criar o atributo de produto Amazon ASIN

1. Faça logon em seu [!DNL Commerce] Administrador

1. Clique em **[!UICONTROL Stores]** no menu à esquerda.

1. No _[!UICONTROL Attributes]_seção , clique em **[!UICONTROL Product]**.

1. Para abrir as propriedades dos atributos, clique em **[!UICONTROL Add New Attribute]**.

1. Para **[!UICONTROL Default Label]**, insira `Amazon ASIN` (o nome do seu atributo).

1. Para **[!UICONTROL Catalog Input Type for Store Owner]**, escolha `Text Field`.

1. Para **[!UICONTROL Values Required]**, escolha `No`.

   Embora um ASIN da Amazon seja necessário para listar um produto no Amazon, alguns dos produtos de catálogo podem não estar listados no Amazon.

1. Expanda o _[!UICONTROL Advanced Attribute Properties]_e defina as opções:

   - Para **[!UICONTROL Attribute Code]**, insira `amazon_asin`.

   - Para **[!UICONTROL Scope]**, escolha `Global`.

   - Para **[!UICONTROL Unique Value]**, escolha `No`.

   - Para **[!UICONTROL Input Validation for Store Owner]**, escolha `None`.

   - Para **[!UICONTROL Add to Column Options]**, escolha `Yes`.

   - Para **[!UICONTROL Use in Filter Options]**, escolha `Yes`.

1. Clique em **[!UICONTROL Save Attribute]**.

![Atributo Amazon ASIN](assets/creating-asin-attribute.png)

## Criar o atributo de produto Condição do Amazon

1. Faça logon em seu [!DNL Commerce] Administrador

1. Clique em **[!UICONTROL Stores]** no menu à esquerda.

1. No _[!UICONTROL Attributes]_seção , clique em **[!UICONTROL Product]**.

1. Para abrir as propriedades do atributo, clique em **[!UICONTROL Add New Attribute]**.

1. Para **[!UICONTROL Default Label]**, insira `Amazon Condition` (o nome do seu atributo).

1. Para **[!UICONTROL Catalog Input Type for Store Owner]**, escolha `Dropdown`.

   O _[!UICONTROL Manage Options (Values of your Attribute)]_é exibida.

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

1. No _[!UICONTROL Admin]_, insira o texto do rótulo da condição que você está adicionando (como `New`, `Used`e `Used-Like New`)

1. Clique em **[!UICONTROL Add Option]** para adicionar mais opções, conforme necessário.

1. Expandir _[!UICONTROL Advanced Attribute Properties]_e defina as opções.

   - Para **[!UICONTROL Attribute Code]**, insira `amazon_condition`.

   - Para **[!UICONTROL Scope]**, escolha `Global`.

   - Para **[!UICONTROL Unique Value]**, escolha `No`.

   - Para **[!UICONTROL Input Validation for Store Owner]**, escolha `None`.

   - Para **[!UICONTROL Add to Column Options]**, escolha `Yes`.

   - Para **[!UICONTROL Use in Filter Options]**, escolha `Yes`.

1. Clique em **[!UICONTROL Save Attribute]**.

![Atributo Condição Amazon](assets/creating-amazon-condition-attribute.png)

![Ícone Próximo](assets/btn-next.png) [**Continue a adicionar ou verificar a chave da API**](./amazon-verify-api-key.md)
