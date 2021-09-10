---
title: Criar [!DNL Commerce] Atributos para Amazon
description: Antes de concluir o processo de integração do canal de vendas da Amazon, verifique se você tem os [!UICONTROL Commerce] atributos de produto necessários.
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# Criar atributos [!DNL Commerce] para Amazon

Antes de integrar suas contas [!DNL Amazon Seller Central], é uma prática recomendada adicionar [!DNL Commerce] [atributos do produto](https://docs.magento.com/user-guide/stores/attributes-product.html){:target=&quot;_blank&quot;} para mapear suas listas de produtos. Após concluir a integração, você pode gerenciar os atributos de produto por meio da guia [Attributes](./managing-attributes.md) da página [inicial do canal de vendas do Amazon](./amazon-sales-channel-home.md).

Essas instruções detalham como criar atributos [!DNL Commerce] para Amazon ASIN e Amazon Condition. É recomendável criar atributos adicionais, incluindo Amazon EAN, Amazon ISBN e Amazon UPC. Você também pode criar um atributo de preço da Amazon se quiser usar seu preço de listagem da Amazon como uma fonte de preço para as regras de preços. Esses atributos são usados ao definir suas configurações de listagem e preço durante a integração. Use também esses atributos ao criar listas do Amazon e ao atualizar e sincronizar seu catálogo [!DNL Commerce] com suas listas do Amazon.

As configurações de Pesquisa de catálogo permitem que você defina parâmetros de pesquisa correspondentes que ajudam a mapear produtos [!DNL Commerce] qualificados com listas do Amazon. Quando mapeado, o Amazon ativa ações relacionadas a preços, quantidade, substituições e sincronização de pedido e produto.

A definição desses valores aumenta a possibilidade de correspondências exatas, minimizando a necessidade de corresponder manualmente as listas de produtos posteriormente. Adicionando os atributos como parte de suas [tarefas de pré-configuração](./amazon-pre-setup-tasks.md), o canal de vendas da Amazon tem um potencial maior para automaticamente corresponder seus produtos durante a integração e sincroniza dados de produto entre o Amazon e [!DNL Commerce] após a integração.

Se você criar apenas o atributo Amazon ASIN (sem adicionar valores ASIN por produto), seus produtos [!DNL Commerce] podem não corresponder automaticamente às suas listagens Amazon. Você pode fazer a correspondência manual de seus produtos por meio de _Store Review_. No entanto, a correspondência manual não cria os elementos de dados necessários para compartilhar e sincronizar os dados do produto.

>[!IMPORTANT]
>
>Se você atualizar um ASIN, UPC ou outro elemento de dados para um produto compatível manualmente, você deve atualizar os dados em ambos os lugares: seu catálogo [!DNL Commerce] e a listagem em sua conta [!DNL Amazon Seller Central].

## Criar o atributo de produto Amazon ASIN

1. Faça logon no [!DNL Commerce] Administrador.

1. Clique em **[!UICONTROL Stores]** no menu à esquerda.

1. Na seção _[!UICONTROL Attributes]_, clique em **[!UICONTROL Product]**.

1. Para abrir as propriedades dos atributos, clique em **[!UICONTROL Add New Attribute]**.

1. Para **[!UICONTROL Default Label]**, digite `Amazon ASIN` (o nome do atributo).

1. Para **[!UICONTROL Catalog Input Type for Store Owner]**, escolha `Text Field`.

1. Para **[!UICONTROL Values Required]**, escolha `No`.

   Embora um ASIN da Amazon seja necessário para listar um produto no Amazon, alguns dos produtos de catálogo podem não estar listados no Amazon.

1. Expanda a seção _[!UICONTROL Advanced Attribute Properties]_e defina as opções:

   - Para **[!UICONTROL Attribute Code]**, digite `amazon_asin`.

   - Para **[!UICONTROL Scope]**, escolha `Global`.

   - Para **[!UICONTROL Unique Value]**, escolha `No`.

   - Para **[!UICONTROL Input Validation for Store Owner]**, escolha `None`.

   - Para **[!UICONTROL Add to Column Options]**, escolha `Yes`.

   - Para **[!UICONTROL Use in Filter Options]**, escolha `Yes`.

1. Clique em **[!UICONTROL Save Attribute]**.

![Atributo Amazon ASIN](assets/creating-asin-attribute.png)

## Criar o atributo de produto Condição do Amazon

1. Faça logon no [!DNL Commerce] Administrador.

1. Clique em **[!UICONTROL Stores]** no menu à esquerda.

1. Na seção _[!UICONTROL Attributes]_, clique em **[!UICONTROL Product]**.

1. Para abrir as propriedades do atributo, clique em **[!UICONTROL Add New Attribute]**.

1. Para **[!UICONTROL Default Label]**, digite `Amazon Condition` (o nome do atributo).

1. Para **[!UICONTROL Catalog Input Type for Store Owner]**, escolha `Dropdown`.

   A seção _[!UICONTROL Manage Options (Values of your Attribute)]_é exibida.

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

1. Selecione a opção **[!UICONTROL Is Default]** para a condição que você deseja que seja a seleção padrão.

1. Na coluna _[!UICONTROL Admin]_, insira o texto do rótulo da condição que está sendo adicionada (como `New`, `Used` e `Used-Like New`)

1. Clique em **[!UICONTROL Add Option]** para adicionar mais opções, conforme necessário.

1. Expanda a seção _[!UICONTROL Advanced Attribute Properties]_e defina as opções.

   - Para **[!UICONTROL Attribute Code]**, digite `amazon_condition`.

   - Para **[!UICONTROL Scope]**, escolha `Global`.

   - Para **[!UICONTROL Unique Value]**, escolha `No`.

   - Para **[!UICONTROL Input Validation for Store Owner]**, escolha `None`.

   - Para **[!UICONTROL Add to Column Options]**, escolha `Yes`.

   - Para **[!UICONTROL Use in Filter Options]**, escolha `Yes`.

1. Clique em **[!UICONTROL Save Attribute]**.

![Atributo Condição Amazon](assets/creating-amazon-condition-attribute.png)

![Próximo ](assets/btn-next.png) [**íconeContinuar para adicionar ou verificar a chave da API**](./amazon-verify-api-key.md)
