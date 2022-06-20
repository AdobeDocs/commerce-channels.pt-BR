---
title: Gerenciar Listagens
description: Gerenciar listas de canais de vendas de um [!DNL Commerce] armazene com o Channel Manager para Adobe Commerce e Magento Open Source.
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: 690eeb5d03b23cac11f3c14b04601c514c76e0bd
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Gerenciar listas

Gerencie as listas de produtos para o [!DNL Walmart Marketplace] canal de vendas da interface do usuário do Gerenciador de canais.

O Status de uma listagem individual indica onde o produto está na [!DNL Channel Manager] para determinar as próximas etapas e resolver erros.

![Página Listagens de um canal de vendas conectado](assets/listings-dashboard-view.png)

Você pode concluir as seguintes tarefas na exibição em Lista.

* Exibir listagens atuais
* Classifique e filtre as listagens
* Adicionar produtos
* Produtos correspondentes
* Rastrear o status da listagem
* Descrição de erro para qualquer lista de produtos com um status de erro

## Exibir listas de produtos

1. Em Admin, acesse [!UICONTROL **Marketing** > **Gerenciador de canais**].

1. Na lista Loja, selecione o ícone de olho em uma linha de entrada de loja para abrir a exibição de loja.

1. Selecionar [!UICONTROL **Listagens**].

1. Classifique o *Listagem* exibir selecionando qualquer cabeçalho de coluna na *Listagem* tabela.

1. Filtre o *Listagem* visualize selecionando um dos cartões de contagem de status.

1. Redefina a ordem de classificação e remova os filtros selecionando **Atualizar produtos**.

## Adicionar produtos do Commerce ao Channel Manager

Crie a classificação do produto para a [!DNL Walmart Marketplace] , concluindo as seguintes tarefas:

* [Adicionar produtos da [!DNL Commerce] catálogo de produtos para [!DNL Channel Manager]](add-products-to-channel-store.md)

* [Mapear atributos do catálogo](map-catalog-attributes.md#configure-product-attribute-settings)

## Corresponder produtos em [!DNL Walmart]

Você pode criar ofertas de produtos na [!DNL Walmart Marketplace] usando a correspondência de produtos ou fazendo upload manual das listagens de produtos para novos produtos.

* **[Produtos correspondentes no Walmart](connect-listings-to-marketplace.md)**—Conecte listas de produtos do seu canal ao [!DNL Walmart Marketplace] atualizando listas existentes que vendem o mesmo produto. Os critérios de correspondência são determinados pela variável [configuração de mapeamento de atributo](map-catalog-attributes.md) para o seu canal.

* **[Fazer upload manual de novas listagens](connect-listings-to-marketplace.md#upload-new-product-listings)**—Para produtos que não correspondem a uma listagem existente em [!DNL Walmart Marketplace]use um [!DNL Walmart] categoria do produto modelo do Excel para fazer upload em massa das listas de produtos.

## Controles de listagem e Descrições de coluna

As tabelas a seguir descrevem os controles e colunas disponíveis para [!UICONTROL Listings].

**Controles para[!UICONTROL Listings]**

| **Controle** | **Descrição** |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Add Products] | Abre a variável [!UICONTROL Admin Product Catalog] página para selecionar produtos para adicionar a sua [!DNL Walmart Marketplace] ou para atualizar atributos de produto para atender aos requisitos de listagem do Walmart Marketplace. |
| [!UICONTROL Match products on Walmart] | Após selecionar um ou mais produtos no status Rascunho, selecione Corresponder produtos em [!DNL Walmart] para verificar ofertas de produtos que podem ser adicionadas a um [!DNL Walmart Marketplace] listagem. |
| [!UICONTROL Refresh products] | Atualize a exibição com a lista e o status mais atuais. Esse controle também redefine a exibição de listagem para a ordem de classificação padrão e remove quaisquer filtros. |
| [!UICONTROL Filter by *Status*] | Mostrar somente listagens com um status específico selecionando um dos cartões de contagem de status acima da tabela Listagem. Use o *Atualizar produtos* para remover o filtro. |
| [!UICONTROL Sort products] | Altere a ordem de classificação para listagem selecionando qualquer cabeçalho de coluna. |


**Descrições das colunas**

| **Campo** | **Descrição** |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name] | Nome do produto da [!DNL Commerce] catálogo de loja. |
| [!UICONTROL SKU (Unique ID)] | O SKU atribuído ao produto no [!DNL Commerce] catálogo. |
| [!UICONTROL  Quantity] | Quantidade de inventário disponível no Adobe Commerce ou Magento Open Source. |
| [!UICONTROL Price] | O preço do produto da [!DNL Commerce] catálogo de loja. As atualizações de preço do catálogo são sincronizadas com o Gerenciador de canais e enviadas para [!DNL Walmart Marketplace]  para que os itens listados mostrem o preço atual. |
| [!UICONTROL Status] | Indica o status atual do pedido na [!DNL Commerce] fluxo de trabalho do pedido. O status é atualizado quando você adiciona produtos ao [!DNL Channel Manager] e quando você combinar produtos no mercado. Se uma operação falhar, a listagem mostra um status de erro. Depois de corrigir o erro, [!DNL Channel Manager] tenta novamente a operação e atualiza o status. |
| [!UICONTROL Error Description] | Fornece informações de erro adicionais para produtos com uma `[!DNL Error]` status. |
| [!UICONTROL Status Detail] | Fornece informações adicionais para produtos com *Erro* ou *Corresponder* status. |

### Sobre o status da listagem

Na área de trabalho Listagem , o rótulo Status mostra onde um produto está na [!DNL Channel Manager] para determinar as próximas etapas e resolver erros. As listagens podem ter os seguintes rótulos de status:

* **[!UICONTROL Draft]**-Identifica produtos que não foram [apresentada para [!DNL Walmart] para correspondência](connect-listings-to-marketplace.md#match-products).

* **[!UICONTROL Processing]**—Identifica produtos enviados para correspondência no [!DNL Walmart Marketplace]. Os produtos permanecem em *Processamento* até que o [!DNL Walmart] retorna uma mensagem HTTP status que indica se a correspondência foi bem-sucedida ou se houve um erro. Pode levar até 30 minutos para que a operação de correspondência seja concluída na variável [!DNL Walmart Marketplace].

* **[!UICONTROL Match]**-Identifica os produtos que foram correspondidos com êxito em [!DNL Walmart].

   Uma correspondência ocorre quando o valor do atributo do produto (código UPC, por exemplo) corresponde ao valor UPC em um [!DNL Walmart Marketplace] listagem. Quando um produto corresponde, a oferta do Commerce é adicionada ao produto existente [!DNL Walmart] listagem.

   Verifique a [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) painel para revisar a lista de produtos atualizada e verificar os detalhes do produto, o preço e a quantidade do inventário.

* **[!UICONTROL Match - Match in Stage]**—Identifica produtos correspondentes a [!DNL Walmart] que não podem ser conectadas até que a variável [!DNL Walmart Marketplace] loja está ativa. Os produtos com esse status se conectam automaticamente quando a função [!DNL Walmart Marketplace] a loja entra em funcionamento.

* **[!UICONTROL Error]**—Identifica produtos que não correspondiam a um [!DNL Walmart Marketplace] listagem.

* **[!UICONTROL Error description]**—Fornece informações detalhadas sobre o erro de listagem.

   Depois de resolver o erro, envie novamente o produto para correspondência. Consulte [Solução de problemas de erros de correspondência do produto](connect-listings-to-marketplace.md#troubleshoot-product-match-errors).
