---
title: Criar um SKU Alias Amazon Seletor
description: Você pode usar o SKU Alias Amazon Seller para criar listagens de Amazon multi-regionais de seus produtos de catálogo comercial.
exl-id: df3cafbf-58df-4c93-9e63-20feb6f4e7ed
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---

# Criar um SKU Alias Amazon Seletor

Um [!DNL Alias Amazon Seller SKU] é usado para criar uma listagem do Amazon a partir do mesmo produto em seu catálogo [!DNL Commerce]. Se você for um vendedor experiente da Amazon, talvez esteja familiarizado com o [SKU Global da Amazon](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=201394090){target=&quot;_blank&quot;} e SKU específico do Marketplace para inventário e envio. Seguindo princípios semelhantes para o canal de vendas da Amazon, o SKU do vendedor da Amazon controla as informações de listagem de produtos em nível multi-regional, e o [!DNL Alias Amazon Seller SKU] pode ser usado para controlar as informações de listagem de produtos em um nível específico de região.

Essa função pode ser usada para executar duas funções:

- Crie um [!DNL Alias Amazon Seller SKU] para um dos produtos de catálogo [!DNL Commerce] para controlar as informações de listagem específicas da região.

   **Exemplo**: Você vende tanto nos Estados Unidos quanto no Canadá. Lembre-se, cada uma das lojas de canal de vendas da Amazon só pode receber uma região do Amazon durante a configuração. Portanto, você tem uma loja de canais de vendas da Amazon com uma região definida dos EUA e outra loja com uma região definida do Canadá. Ambas as lojas compartilham seu catálogo [!DNL Commerce] para listar informações em ambas as regiões, incluindo os atributos de produto do Amazon Vendedor SKU e ASIN. Portanto, as listas do produto de catálogo seriam as mesmas em ambas as lojas, compartilhando preços, estoque/quantidade e outros atributos do produto. Mas seu estoque para o Canadá armazena navios de um local no Canadá e seus estoques dos EUA são de um local nos EUA. Assim, você deve controlar a quantidade da listagem para cada loja separadamente. Para realizar esse tipo de controle específico da região, você pode criar um SKU Alias Amazon Seller .

   Essencialmente, você pode criar um SKU Alias Amazon Venler vinculado ao mesmo produto de catálogo e pode ser usado para republicar a mesma listagem nessa região.

- Crie um [!DNL Alias Amazon Seller SKU] e corresponda um dos seus produtos de catálogo [!DNL Commerce] a duas listagens do Amazon.

   **Exemplo**: Você tem um produto de catálogo que corresponde a uma lista do Amazon. Como o Amazon frequentemente tem várias listagens que representam o mesmo produto, você descobre outra listagem do Amazon para o mesmo produto, mas a Amazon atribuiu um ASIN diferente à listagem. Para aumentar a visibilidade do produto para incluir, você deseja combinar o produto do catálogo com o ASIN diferente e criar listagens para ambos os valores do ASIN. Para fazer isso, você pode criar um SKU Alias Amazon Seller .

   Essencialmente, você pode criar um [!DNL Alias Amazon Seller SKU] que pode ser usado para corresponder um único produto de catálogo a uma segunda listagem do Amazon e criar uma listagem para o ASIN recém-compatível. Nesse cenário, você teria duas listagens do Amazon para o mesmo produto de catálogo.

   Depois de criar um SKU Alias Amazon Seller, você pode usar suas configurações de listagem, regras e substituições para controlar as informações de listagem da região. Os atributos de produto que podem ser definidos por região para uma listagem incluem quantidade/estoque, método de preenchimento, condição, qualificação de produto e tempo de manuseio.

## Usado para uma finalidade específica de uma região {#region-specific}

Visualize a listagem na página _[!UICONTROL Product Listings]_(_[!UICONTROL Inactive]_, _Ativo_, _Inelegível_ ou _Encerrado_).

1. Em _[!UICONTROL Actions]_, clique em **[!UICONTROL Create Alias Seller SKU]**.

1. Para **[!UICONTROL Assign New Seller SKU]**, insira um valor alfanumérico exclusivo.

   Esse valor deve ser exclusivo (não usado para qualquer outro produto ou alias no catálogo).

1. Para **[!UICONTROL Assign New ASIN]**, não faça alterações.

   Esse valor é preenchido automaticamente com o ASIN do produto correspondente ao produto de catálogo. Alterar esse valor corresponde o produto do catálogo a duas listagens do Amazon com base no ASIN.

1. Alterne a opção **[!UICONTROL Remove Existing Seller SKU]** conforme necessário.

   - `Yes` - Escolha excluir a listagem e criar uma listagem usando as novas informações fornecidas.

   - `No` - Escolha criar uma listagem e manter a listagem antiga inalterada.

1. Clique em **[!UICONTROL Save Listing Update]**.

## Usado para corresponder um único produto de catálogo a duas listagens do Amazon

1. Visualize a listagem na página _[!UICONTROL Product Listings]_(_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Ineligible]_ ou _[!UICONTROL Ended]_guias).

1. Em _[!UICONTROL Actions]_, clique em **[!UICONTROL Create Alias Seller SKU]**.

1. Para **[!UICONTROL Assign New Seller SKU]**, insira um valor alfanumérico exclusivo.

   Esse valor deve ser exclusivo (não usado para qualquer outro produto ou alias no catálogo).

1. Para **[!UICONTROL Assign New ASIN]**, insira um valor alfanumérico exclusivo.

   Esse valor é preenchido automaticamente com o ASIN do produto correspondente ao produto de catálogo. Alterar esse valor corresponde o produto do catálogo a duas listagens do Amazon com base no ASIN.

1. Alterne a opção **[!UICONTROL Remove Existing Seller SKU]** conforme necessário.

   - `Yes` - Escolha excluir a listagem e criar uma listagem usando as novas informações fornecidas.

   - `No` - Escolha criar outra listagem e manter a listagem antiga inalterada.

1. Clique em **[!UICONTROL Save Listing Update]**.

![criar um SKU Alias Amazon Seller](assets/amazon-alias-sku-create.png)

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Assign New Seller SKU] | Insira um novo valor alfanumérico exclusivo a ser vinculado ao SKU original do vendedor de Amazon. Esse número é usado somente pelo canal de vendas da Amazon para corresponder ao produto do catálogo. Você pode usar qualquer valor de SKU, mas o valor só pode ser usado uma vez no catálogo. |
| [!UICONTROL Assign New ASIN] | Insira o valor de ASIN para a listagem para a qual você deseja corresponder o produto do catálogo. Somente modifique esse campo ao corresponder um único produto de catálogo ao ASIN para outra listagem do mesmo produto. Esse valor deve corresponder ao ASIN atribuído pelo Amazon ou a listagem não será rejeitada pelo Amazon. |
| [!UICONTROL Remove Existing Seller SKU] | Opções:<ul><li>**[!UICONTROL Yes]** - Escolha excluir a listagem e criar uma listagem usando as novas informações fornecidas. A nova listagem é exibida na guia _[!UICONTROL Active]_e a listagem antiga é movida para a guia_ Encerrada _.</li><li>**[!UICONTROL No]** - Escolha criar outra listagem e manter a listagem antiga inalterada. Ambas as listagens são exibidas na guia Ativo depois que a nova listagem é criada.</li></ul> |
