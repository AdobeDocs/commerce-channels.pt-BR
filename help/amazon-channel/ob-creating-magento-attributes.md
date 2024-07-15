---
title: Criar atributos do Commerce para o Amazon
description: Antes de concluir o processo de integração do canal de vendas do Amazon, verifique se você tem os atributos de produto [!UICONTROL Commerce] necessários.
role: Admin
feature: Sales Channels, Products, Configuration
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Criar atributos do Commerce para o Amazon

Antes de integrar suas contas do [!DNL Amazon Seller Central], é uma prática recomendada adicionar [!DNL Commerce] [atributos do produto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) para mapear suas listas de produtos. Após concluir a integração, você poderá gerenciar os atributos do seu produto por meio da guia [Atributos](./managing-attributes.md) da página inicial do [canal de vendas do Amazon](./amazon-sales-channel-home.md).

Estas instruções detalham como criar atributos [!DNL Commerce] para Amazon ASIN e Condição Amazon. É recomendável criar atributos adicionais, incluindo Amazon EAN, Amazon ISBN e Amazon UPC. Você também pode criar um atributo de Preço Amazon se quiser usar o preço de lista Amazon como uma origem de preço para regras de precificação. Esses atributos são usados ao definir as configurações de lista e preço durante a integração. Use esses atributos também ao criar listagens do Amazon e ao atualizar e sincronizar o catálogo do [!DNL Commerce] com suas listagens do Amazon.

As configurações de Pesquisa no catálogo permitem que você defina parâmetros de pesquisa correspondentes que ajudam a mapear os produtos qualificados do [!DNL Commerce] com as listagens do Amazon. Quando mapeado, o Amazon ativa ações relacionadas a preço, quantidade, substituições e sincronização de pedidos e produtos.

A definição desses valores aumenta o potencial para correspondências exatas, minimizando a necessidade de corresponder manualmente as listas de produtos posteriormente. Adicionando os atributos como parte de suas [tarefas de pré-configuração](./amazon-pre-setup-tasks.md) de integração, o canal de vendas da Amazon tem um maior potencial para corresponder automaticamente seus produtos durante a integração e sincroniza os dados do produto entre o Amazon e o [!DNL Commerce] após a integração.

Se você criar apenas o atributo ASIN do Amazon (sem adicionar valores ASIN por produto), seus produtos do [!DNL Commerce] podem não corresponder automaticamente às suas listagens do Amazon. Você pode fazer a correspondência manual de seus produtos por meio da _Revisão da Loja_. No entanto, a correspondência manual não cria os elementos de dados necessários para compartilhar e sincronizar os dados do produto.

>[!IMPORTANT]
>
>Se você atualizar um ASIN, UPC ou outro elemento de dados de um produto correspondido manualmente, atualize os dados em ambos os locais: no catálogo [!DNL Commerce] e na lista da conta [!DNL Amazon Seller Central].

## Criar o atributo de produto Amazon ASIN

1. Faça logon no Administrador [!DNL Commerce].

1. Clique em **[!UICONTROL Stores]** no menu do lado esquerdo.

1. Na seção _[!UICONTROL Attributes]_, clique em **[!UICONTROL Product]**.

1. Para abrir as propriedades dos atributos, clique em **[!UICONTROL Add New Attribute]**.

1. Para **[!UICONTROL Default Label]**, insira `Amazon ASIN` (o nome do seu atributo).

1. Para **[!UICONTROL Catalog Input Type for Store Owner]**, escolha `Text Field`.

1. Para **[!UICONTROL Values Required]**, escolha `No`.

   Embora um Amazon ASIN seja necessário para listar um produto no Amazon, alguns de seus produtos de catálogo podem não estar listados no Amazon.

1. Expanda a seção _[!UICONTROL Advanced Attribute Properties]_e defina as opções:

   - Para **[!UICONTROL Attribute Code]**, digite `amazon_asin`.

   - Para **[!UICONTROL Scope]**, escolha `Global`.

   - Para **[!UICONTROL Unique Value]**, escolha `No`.

   - Para **[!UICONTROL Input Validation for Store Owner]**, escolha `None`.

   - Para **[!UICONTROL Add to Column Options]**, escolha `Yes`.

   - Para **[!UICONTROL Use in Filter Options]**, escolha `Yes`.

1. Clique em **[!UICONTROL Save Attribute]**.

![Atributo ASIN do Amazon](assets/creating-asin-attribute.png){width="600" zoomable="yes"}

## Criar o atributo de produto Condição Amazon

1. Faça logon no Administrador [!DNL Commerce].

1. Clique em **[!UICONTROL Stores]** no menu do lado esquerdo.

1. Na seção _[!UICONTROL Attributes]_, clique em **[!UICONTROL Product]**.

1. Para abrir as propriedades do atributo, clique em **[!UICONTROL Add New Attribute]**.

1. Para **[!UICONTROL Default Label]**, insira `Amazon Condition` (o nome do seu atributo).

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

1. Na coluna _[!UICONTROL Admin]_, insira o texto para o rótulo da condição que você está adicionando (como `New`, `Used` e `Used-Like New`)

1. Clique em **[!UICONTROL Add Option]** para adicionar mais opções, conforme necessário.

1. Expanda a seção _[!UICONTROL Advanced Attribute Properties]_e defina as opções.

   - Para **[!UICONTROL Attribute Code]**, digite `amazon_condition`.

   - Para **[!UICONTROL Scope]**, escolha `Global`.

   - Para **[!UICONTROL Unique Value]**, escolha `No`.

   - Para **[!UICONTROL Input Validation for Store Owner]**, escolha `None`.

   - Para **[!UICONTROL Add to Column Options]**, escolha `Yes`.

   - Para **[!UICONTROL Use in Filter Options]**, escolha `Yes`.

1. Clique em **[!UICONTROL Save Attribute]**.

![Atributo de Condição Amazon](assets/creating-amazon-condition-attribute.png){width="600" zoomable="yes"}

![Próximo ícone](assets/btn-next.png) [**Continuar para Adicionar ou Verificar a Chave de API**](./amazon-verify-api-key.md)
