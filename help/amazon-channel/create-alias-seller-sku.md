---
title: Criar um alias Amazon Seller SKU
description: Você pode usar o Alias Amazon Seller SKU para criar listagens de Amazon multirregionais a partir de seus produtos de catálogo do Commerce.
exl-id: df3cafbf-58df-4c93-9e63-20feb6f4e7ed
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 0%

---

# Criar um alias Amazon Seller SKU

Um [!DNL Alias Amazon Seller SKU] é usado para criar uma lista do Amazon com o mesmo produto na [!DNL Commerce] catálogo. Se você é um vendedor de Amazon experiente, pode estar familiarizado com o [SKU global da Amazon](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=201394090){target="_blank"} SKU específica do Marketplace para inventário e envio. Seguindo princípios semelhantes para o canal de vendas da Amazon, o SKU do vendedor da Amazon controla as informações da lista de produtos em nível multiregional e a [!DNL Alias Amazon Seller SKU] pode ser usado para controlar informações de lista de produtos em um nível específico de região.

Esta função pode ser usada para executar duas funções:

- Criar um [!DNL Alias Amazon Seller SKU] para um dos seus [!DNL Commerce] produtos de catálogo para controlar informações de listagem específicas da região.

   **Exemplo**: você é um vendedor nas regiões dos EUA e Canadá. Lembre-se de que cada uma das lojas de canal de vendas da Amazon pode receber apenas uma região da Amazon durante a configuração. Portanto, você tem uma loja de canais de vendas da Amazon com uma região definida dos EUA e outra loja com uma região definida do Canadá. Ambas as lojas compartilham seu [!DNL Commerce] catálogo para listar informações em ambas as regiões, incluindo os atributos de produto Amazon Seller SKU e ASIN. Assim, as listagens do produto de catálogo seriam as mesmas em ambas as lojas, compartilhando preços, estoque/quantidade e outros atributos de produto. Mas, seu estoque para seus navios de loja do Canadá de um local do Canadá, e seus navios de loja dos EUA de um local dos EUA. Assim, você deve controlar a quantidade da lista separadamente para cada loja. Para realizar esse tipo de controle específico de região, você pode criar um SKU de vendedor Alias Amazon.

   Basicamente, você pode criar um SKU de Alias Amazon Seller que esteja vinculado ao mesmo produto de catálogo e possa ser usado para republicar a mesma lista nessa região.

- Criar um [!DNL Alias Amazon Seller SKU] e corresponder a um de seus [!DNL Commerce] produtos do catálogo para duas listagens do Amazon.

   **Exemplo**: você tem um produto de catálogo que corresponde a uma lista do Amazon. Como o Amazon frequentemente tem várias listas que representam o mesmo produto, você descobre outra lista do Amazon para o mesmo produto, mas a Amazon atribuiu uma ASIN diferente à lista. Para aumentar a visibilidade do produto a ser incluído, é necessário corresponder o produto de catálogo à ASIN diferente e criar listas para ambos os valores de ASIN. Para fazer isso, você pode criar um SKU de vendedor Alias Amazon.

   Essencialmente, você pode criar um [!DNL Alias Amazon Seller SKU] que pode ser usado para corresponder um único produto de catálogo a uma segunda lista do Amazon e criar uma lista para o ASIN recém-correspondido. Nesse cenário, você teria duas listagens do Amazon para o mesmo produto de catálogo.

   Depois de criar um SKU de Vendedor Amazon Alias, você pode usar suas configurações de listagem, regras e substituições para controlar as informações de listagem para a região. Os atributos de produto que podem ser definidos por região para uma lista incluem quantidade/estoque, método de preenchimento, condição, qualificação de produto e tempo de manuseio.

## Usado para uma finalidade específica da região {#region-specific}

Exibir a listagem no _[!UICONTROL Product Listings]_página (_[!UICONTROL Inactive]_, _Ativo_, _Inelegível_ ou _Terminado_ guia ).

1. Em _[!UICONTROL Actions]_, clique em **[!UICONTROL Create Alias Seller SKU]**.

1. Para **[!UICONTROL Assign New Seller SKU]**, informe um valor alfanumérico exclusivo.

   Esse valor deve ser exclusivo (não usado para nenhum outro produto ou alias em seu catálogo).

1. Para **[!UICONTROL Assign New ASIN]**, não faça alterações.

   Esse valor é preenchido automaticamente com o ASIN do produto que corresponde ao produto de catálogo. Alterar esse valor corresponde ao produto de catálogo para duas listagens do Amazon com base na ASIN.

1. Alterne a **[!UICONTROL Remove Existing Seller SKU]** conforme necessário.

   - `Yes` - Escolha excluir a lista e criar uma lista usando as novas informações fornecidas.

   - `No` - Opte por criar uma lista e manter a lista antiga inalterada.

1. Clique em **[!UICONTROL Save Listing Update]**.

## Usado para corresponder um único produto de catálogo a duas listagens do Amazon

1. Exibir a listagem no _[!UICONTROL Product Listings]_página (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Ineligible]_ ou _[!UICONTROL Ended]_guias).

1. Em _[!UICONTROL Actions]_, clique em **[!UICONTROL Create Alias Seller SKU]**.

1. Para **[!UICONTROL Assign New Seller SKU]**, informe um valor alfanumérico exclusivo.

   Esse valor deve ser exclusivo (não usado para nenhum outro produto ou alias em seu catálogo).

1. Para **[!UICONTROL Assign New ASIN]**, informe um valor alfanumérico exclusivo.

   Esse valor é preenchido automaticamente com o ASIN do produto que corresponde ao produto de catálogo. Alterar esse valor corresponde ao produto de catálogo para duas listagens do Amazon com base na ASIN.

1. Alterne a **[!UICONTROL Remove Existing Seller SKU]** conforme necessário.

   - `Yes` - Escolha excluir a lista e criar uma lista usando as novas informações fornecidas.

   - `No` - Opte por criar outra lista e manter a lista antiga inalterada.

1. Clique em **[!UICONTROL Save Listing Update]**.

![criar um alias Amazon Seller SKU](assets/amazon-alias-sku-create.png){width="600" zoomable="yes"}

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Assign New Seller SKU] | Insira um novo valor alfanumérico exclusivo para ser vinculado ao SKU original do vendedor da Amazon. Esse número é usado somente pelo canal de vendas da Amazon para corresponder ao seu produto de catálogo. Você pode usar qualquer valor de SKU, mas o valor só pode ser usado uma vez no catálogo. |
| [!UICONTROL Assign New ASIN] | Insira o valor ASIN da lista à qual você deseja corresponder ao seu produto de catálogo. Modifique esse campo somente ao corresponder um único produto de catálogo à ASIN para outra lista do mesmo produto. Esse valor deve corresponder ao ASIN atribuído pelo Amazon ou a listagem não será rejeitada pelo Amazon. |
| [!UICONTROL Remove Existing Seller SKU] | Opções:<ul><li>**[!UICONTROL Yes]** - Escolha excluir a lista e criar uma lista usando as novas informações fornecidas. A nova lista aparece no campo _[!UICONTROL Active]_e a lista antiga será movida para a guia_ Terminado _guia.</li><li>**[!UICONTROL No]** - Opte por criar outra lista e manter a lista antiga inalterada. Ambas as listas são exibidas na guia Ativo após a criação da nova lista.</li></ul> |
