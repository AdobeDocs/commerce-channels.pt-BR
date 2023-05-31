---
title: Gerenciar Listagens
description: '"Gerenciar listas de canais de vendas para um [!DNL Commerce] armazenamento com o Gerenciador de canal para Adobe Commerce e Magento Open Source.'''
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# Gerenciar Listagens

Gerenciar listas de produtos para o [!DNL Walmart Marketplace] canal de vendas na interface do usuário do Gerenciador de canais.

O Status de uma lista individual indica onde o produto está na [!DNL Channel Manager] fluxo de trabalho para que você possa determinar as próximas etapas e resolver erros.

![Página de listagens de um canal de vendas conectado](assets/listings-dashboard-view.png){width="500" zoomable="yes"}

Você pode concluir as seguintes tarefas a partir da exibição Listagem.

* Exibir listagens atuais
* Classificar e filtrar as listagens
* Adicionar produtos
* Combinar produtos
* Rastrear status da lista
* Revisar descrição do erro para listagens com status de erro

## Exibir listagens de produtos

1. No Administrador, acesse [!UICONTROL **Marketing** > **Gerenciador de canais**].

1. Na lista Loja, selecione o ícone de olho em uma linha de entrada de loja para abrir a visualização de loja.

1. Selecionar [!UICONTROL **Listagens**].

1. Classifique as *Listagem* selecione qualquer cabeçalho de coluna na variável *Listagem* tabela.

1. Filtre o *Listagem* selecione um dos cartões de contagem de status.

1. Redefinir a ordem de classificação e remover filtros selecionando **Atualizar produtos**.

## Adicionar [!DNL Commerce] produtos para o Gerenciador de canal

Crie o sortimento de produtos para o [!DNL Walmart Marketplace] concluindo as seguintes tarefas:

* [Adicione produtos do seu [!DNL Commerce] catálogo de produtos para [!DNL Channel Manager]](add-products-to-channel-store.md)

* [Mapear atributos do catálogo](map-catalog-attributes.md#configure-product-attribute-settings)

## Combinar produtos em [!DNL Walmart]

É possível criar ofertas de produtos no [!DNL Walmart Marketplace] usando a correspondência de produtos ou fazendo upload manual de listas de produtos para novos produtos.

* **[Combinar produtos no Walmart](connect-listings-to-marketplace.md)**—Conectar listas de produtos do seu canal ao [!DNL Walmart Marketplace] atualizando as listagens existentes que vendem o mesmo produto. Os critérios de correspondência são determinados pelo [configuração de mapeamento de atributo](map-catalog-attributes.md) para o seu canal.

* **[Fazer upload manual de novas listagens](connect-listings-to-marketplace.md#upload-new-product-listings)**—Para produtos que não correspondem a uma lista existente em [!DNL Walmart Marketplace], use um [!DNL Walmart] categoria de produto Modelo do Excel para fazer upload em massa de listagens de produtos.

## Listando Controles e Descrições de Coluna

As tabelas a seguir descrevem os controles e colunas disponíveis para [!UICONTROL Listings].

**Controles para[!UICONTROL Listings]**

| **Controle** | **Descrição** |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Add Products] | Abre a [!UICONTROL Admin Product Catalog] selecione os produtos a serem adicionados ao seu [!DNL Walmart Marketplace] ou atualizar atributos de produto para atender aos requisitos de listagem do Walmart Marketplace. |
| [!UICONTROL Match products on Walmart] | Após selecionar um ou mais produtos em [!UICONTROL Draft] status, selecione [!UICONTROL Match products on Walmart] para verificar ofertas de produtos que podem ser adicionadas a um existente [!DNL Walmart Marketplace] listagem. |
| [!UICONTROL Refresh products] | Atualizar a exibição com a lista e o status mais atuais. Esse controle também redefine a exibição de listagem para a ordem de classificação padrão e remove os filtros. |
| [!UICONTROL Filter by *Status*] | Mostre apenas as listagens com um status específico selecionando um dos cartões de status acima da tabela Listagem. Remover o filtro selecionando **[!UICONTROL Refresh products]**. |
| [!UICONTROL Sort products] | Altere a ordem de classificação para a lista selecionando qualquer cabeçalho de coluna. |


**Descrições da coluna**

| **Campo** | **Descrição** |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name] | Nome do produto da [!DNL Commerce] catálogo da loja. |
| [!UICONTROL SKU (Unique ID)] | O SKU atribuído ao produto na variável [!DNL Commerce] catálogo. |
| [!UICONTROL  Quantity] | Quantidade de inventário disponível no Adobe Commerce ou Magento Open Source. |
| [!UICONTROL Price] | O preço do produto do [!DNL Commerce] catálogo da loja. As atualizações de preço de catálogo são sincronizadas com o Gerenciador de canal e enviadas para [!DNL Walmart Marketplace]  para que os itens listados mostrem o preço atual. |
| [!UICONTROL Status] | Indica o status atual do pedido na [!DNL Commerce] fluxo de trabalho do pedido. O status é atualizado quando você adiciona produtos com sucesso ao [!DNL Channel Manager] e quando você faz a correspondência de produtos no mercado. Se uma operação falhar, a lista mostrará um status de erro. Depois de corrigir o erro, [!DNL Channel Manager] repete a operação e atualiza o status. |
| [!UICONTROL Error Description] | Fornece informações adicionais sobre erros para produtos com um `[!DNL Error]` status. |

### Sobre o status da lista

No espaço de trabalho de Listagem, o rótulo Status mostra onde um produto está no [!DNL Channel Manager] para que você possa determinar as próximas etapas e resolver erros. As listagens podem ter os seguintes rótulos de status:

* **[!UICONTROL Draft]**-Identifica os produtos que não foram [enviado para [!DNL Walmart] para correspondência](connect-listings-to-marketplace.md#match-products).

* **[!UICONTROL Processing]**—Identifica produtos enviados para correspondência no [!DNL Walmart Marketplace]. Os produtos permanecem em *Processando* status até que o [!DNL Walmart] retorna uma mensagem de status HTTP que indica se a correspondência foi bem-sucedida ou se houve um erro. Pode levar até 30 minutos para que a operação de correspondência seja concluída no [!DNL Walmart Marketplace].

* **[!UICONTROL Match]**-Identifica produtos que foram correspondidos com êxito em [!DNL Walmart].

   Uma correspondência ocorre quando o valor do atributo do produto — código UPC por exemplo — corresponde ao valor UPC em um [!DNL Walmart Marketplace] listagem. Quando um produto é correspondente, a oferta de produto do Commerce é adicionada à lista existente.

   Verifique a [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) painel para revisar a lista de produtos atualizada e verificar os detalhes do produto, o preço e a quantidade do estoque.

* **[!UICONTROL Match - Match in Stage]**—Identifica produtos correspondentes em [!DNL Walmart] que não pode ser conectado até que o [!DNL Walmart Marketplace] a loja está ativa. Os produtos com esse status se conectam automaticamente quando a variável [!DNL Walmart Marketplace] a loja fica ativa.

* **[!UICONTROL Error]**—Identifica produtos que não corresponderam a um existente [!DNL Walmart Marketplace] listagem.

* **[!UICONTROL Error description]**— Fornece informações detalhadas sobre o erro de listagem.

   Após resolver o erro, reenvie o produto para correspondência. Consulte [Solução de problemas de erros de correspondência de produtos](connect-listings-to-marketplace.md#troubleshoot-product-match-errors).
