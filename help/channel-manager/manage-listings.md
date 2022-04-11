---
title: Gerenciar listas
description: Gerenciar listas de canais de vendas de um [!DNL Commerce] armazene com o Channel Manager para Adobe Commerce e Magento Open Source.
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: 30495c4e47f15c821206f7b0252b868b4e27d62d
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# Gerenciar Listagens

Gerenciar listas de produtos de um canal conectado [!UICONTROL Listings] na exibição de armazenamento de canais.

Use o *[!UICONTROL Listings]* espaço de trabalho para gerenciar o [!DNL Commerce] produtos colocados à venda no Walmart Marketplace. O Status de uma listagem individual indica onde o produto está na [!DNL Channel Manager] para determinar as próximas etapas e resolver erros.

![Página Listagens de um canal de vendas conectado](assets/products-submit-for-matching.png)

## Exibir listagens

1. Em Admin, acesse [!UICONTROL **Marketing** > Canais > **Gerenciador de canais**].

1. Na lista Loja de Canais, selecione o ícone de lápis na linha de entrada de uma loja para abrir a exibição de loja.

1. Selecionar [!UICONTROL **Listagens**].

## Adicionar produtos do Commerce ao Channel Manager

Conclua as seguintes tarefas para criar o sortimento de produto para o canal Walmart Marketplace :

* [Adicionar produtos do catálogo de produtos do Commerce ao Channel Manager](add-products-to-connected-channel.md)

* [Configurar correspondência de produtos](map-product-attributes-for-matching.md#configure-product-attribute-settings)

## Publicar produtos no Walmart

Você pode criar ofertas de produtos no Walmart usando a correspondência de produtos ou fazendo upload manual das listas de produtos para novos produtos. Para obter instruções, consulte [Publicar listagens no Walmart Marketplace](publish-listings-to-marketplace.md) conforme descrito nos seguintes tópicos:

* **[Produtos correspondentes no Walmart](publish-listings-to-marketplace.md)**- Publique listas de produtos do seu canal para o [!DNL Walmart Marketplace] atualizando listas existentes que vendem o mesmo produto. Os critérios de correspondência são determinados pela variável [configuração de mapeamento de atributo](map-product-attributes-for-matching.md) para o seu canal.

* **[Fazer upload manual de novas listagens](publish-listings-to-marketplace.md#upload-new-product-listings)-**-Para produtos que não correspondem a uma listagem existente no Walmart Marketplace, use um modelo Excel de categoria de produto Walmart para fazer upload em massa das listagens de produtos.

## Controles de listagem e descrições de campo

As tabelas a seguir descrevem os controles e campos disponíveis no [!UICONTROL Listings] página.

**Controles para[!UICONTROL Listings]**

| **Atributo** | **Nível de requisito** |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Refresh products] | Atualiza a exibição com a lista e o status mais atuais |
| [!UICONTROL Add Products ] | Abre a variável [!UICONTROL  Admin Product Catalog] página para selecionar produtos para adicionar a sua [!DNL Walmart Marketplace] ou para atualizar atributos de produto para atender aos requisitos de listagem do Walmart Marketplace. |
| [!UICONTROL Match products on Walmart] | Após selecionar um ou mais produtos no status Rascunho , selecione [!UICONTROL Match products on Walmart] para verificar ofertas de produtos que podem ser adicionadas a um [!DNL Walmart Marketplace] listagem. |


**Descrições das colunas**

| **Campo** | **Descrição** |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name] | Nome do produto da [!DNL Commerce] catálogo de loja. |
| [!UICONTROL SKU (Unique ID)] | O atributo mapeado usado para corresponder produtos no mercado. Esse nome de campo varia dependendo da configuração do atributo mapeado para [!DNL Channel Manager] listagens. Nesse caso, a operação de correspondência do produto usa o SKU do produto da [!DNL Commerce] catálogo para localizar um [!DNL Walmart Marketplace]  Listar com um valor de SKU que corresponda ao valor de SKU dos atributos de produto do Commerce. |
| [!UICONTROL  Quantity] | Quantidade de inventário disponível no Adobe Commerce ou Magento Open Source. |
| [!UICONTROL Price] | O preço do produto da [!DNL Commerce] catálogo de loja. As atualizações de preço do catálogo são sincronizadas com o Gerenciador de canais e enviadas para [!DNL Walmart Marketplace]  para que os itens listados mostrem o preço atual. |
| [!UICONTROL Status] | Indica o status atual do pedido na [!DNL Commerce] fluxo de trabalho do pedido. O status é atualizado quando você adiciona produtos ao [!DNL Channel Manager] e quando você combinar produtos no mercado. Se uma operação falhar, a listagem mostra um status de Erro. Depois de corrigir o erro, [!DNL Channel Manager] tenta novamente a operação e atualiza o status. |


### Sobre o status da listagem

Na área de trabalho Listagem , o rótulo Status mostra onde um produto está na [!DNL Channel Manager] para determinar as próximas etapas e resolver erros. As listagens podem ter os seguintes rótulos de status:

* **[!UICONTROL Draft]**-Identifica produtos que não foram [apresentada para [!DNL Walmart] para correspondência](publish-listings-to-marketplace.md#match-products).

* **[!UICONTROL Processing]**-Identifica produtos enviados para correspondência no [!DNL Walmart Marketplace]. Os produtos permanecem em *Processamento* até que o [!DNL Walmart] retorna uma mensagem HTTP status que indica se a correspondência foi bem-sucedida ou se houve um erro. Pode levar até 30 minutos para que a operação de correspondência seja concluída na variável [!DNL Walmart Marketplace].

* **[!UICONTROL Match]**-Identifica os produtos que foram correspondidos com êxito em [!DNL Walmart].

   Uma correspondência ocorre quando o valor do atributo do produto - código UPC, por exemplo, corresponde ao valor da UPC em um[!DNL Walmart Marketplace] listagem. Quando um produto corresponde, a oferta do Commerce é adicionada à lista Walmart existente.

   Verifique a [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) painel para revisar a lista de produtos atualizada e verificar os detalhes do produto, o preço e a quantidade do inventário.


* **[!UICONTROL Error]**-Identifica produtos que não correspondem a um [!DNL Walmart Marketplace] listagem. Visualize os detalhes do erro ao passar o mouse sobre a *Erro* rótulo do status.

   Depois de resolver o erro, envie novamente o produto para correspondência. Consulte [Solução de problemas de erros de correspondência do produto](https://docs.google.com/document/d/1bEbCyVLXJQQsbZvEwetJvZKWQJOKoiw5Ia1uB4Bs4uo/edit#heading=h.sz6eji8z9vzy).

* **[!UICONTROL Error - Match in Stage]**-Identifica os produtos correspondentes em [!DNL Walmart] que não pode ser publicado até que a [!DNL Walmart Marketplace] loja está ativa. Os produtos com esse status são publicados automaticamente quando a função [!DNL Walmart Marketplace] a loja entra em funcionamento.
