---
title: Gerenciar listas de produtos por ação
description: À medida que você gerencia as listas do Amazon, pode aplicar uma ação a listas individuais ou múltiplas.
exl-id: 1cbf16fb-15eb-484b-bea7-28017a0d0c60
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Gerenciar listas de produtos por ação

O _[!UICONTROL Product Listings]_A página contém várias guias das quais você pode visualizar os status de todas as suas listagens e corresponder seus produtos às listagens do Amazon.

As tarefas de listagem disponíveis diferem um pouco em cada guia, mas a variável [controles do espaço de trabalho](./workspace-controls.md) são iguais e permitem personalizar os dados exibidos para suas listagens.

Opções em **[!UICONTROL Actions]** pode aplicar a ação a várias listagens, enquanto as opções em **[!UICONTROL Select]** no _[!UICONTROL Action]_aplicar a ação somente à lista individual.

Consulte também [Gerenciar listagens por status/guia](./managing-listings-by-tab.md).

| Ação | Descrição | Guias |
|--- |--- |--- |
| [[!UICONTROL Re-attempt auto match to Amazon Listing]](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) | Usado para mover os produtos incompletos de volta pelo processo correspondente. Para tentar fazer a correspondência novamente, você deve modificar o [Listagem](./listing-settings.md) e [Pesquisa no catálogo](./catalog-search.md) configurações para aumentar o potencial para correspondência automática. | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md) | Faça a correspondência manual dos produtos de catálogo com as listas do Amazon selecionando uma lista para correspondência, digitando uma ASIN para corresponder ou atribuindo uma condição ausente. | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL View Details]](./product-listing-details.md) | Veja informações adicionais sobre seus produtos ativos, incluindo o Log de atividades de listagem, que mostra as alterações em um SKU/Produto individual. | [[!UICONTROL Incomplete]](./incomplete-listings.md)<br>[[!UICONTROL New Third Party]](./new-third-party-listings.md)<br>[[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md) | Crie um [!DNL Commerce] catálogo de produtos usando as informações importadas com a lista Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| Tentar Correspondência Automática | Tente uma correspondência automática entre os [!DNL Commerce] catálogo e suas listagens do Amazon com base nas configurações de critérios de pesquisa. Para tentar fazer a correspondência novamente, você deve modificar o [Listagem](./listing-settings.md) e [Pesquisa no catálogo](./catalog-search.md) configurações para aumentar o potencial para correspondência automática. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md) | Selecione manualmente um produto existente no [!DNL Commerce] e atribuí-lo à listagem do Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md) | Crie um [!DNL Commerce] catálogo de produtos usando as informações importadas com a lista Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md) | (Ação em massa) Usada para manter uma listagem que foi encerrada ou para listar manualmente um produto que atende à qualificação de regras de listagem, mas que _[!UICONTROL Product Listing Actions]_não está definido como `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Publish On Amazon]](./publish-listings-manually.md) | (Ação de listagem única) Usada para manter uma listagem que foi encerrada. Essa ação também é usada para listar manualmente um produto que atende à qualificação de regras de listagem quando _[!UICONTROL Product Listing Actions]_não está definido como `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md) | (Ação em massa) Usada para terminar e remover manualmente as listagens de seus produtos que existem no Amazon. As listagens adicionadas podem ser listadas novamente, desde que atendam à qualificação de suas regras de listagem. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md) | (Ação em massa) Edite manualmente uma &quot;substituição&quot; existente que define o preço, o tempo de tratamento, a condição e o texto das notas do vendedor para uma listagem individual, ignorando outros padrões, configurações e regras da listagem. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Override]](./creating-editing-overrides.md) | Criar manualmente uma &quot;substituição&quot; que defina o preço, o tempo de manuseio, a condição e o texto de notas de vendedor para uma listagem individual, ignorando outros padrões, configurações e regras da listagem. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md) | Usado se o ASIN correspondeu ao produto do catálogo deve ser modificado (por exemplo: se o produto correspondeu à lista incorreta de ASIN). | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md) | Pode atender duas funções:<br><br>Pode ser usado para criar uma relação de 1 para 2 entre o produto de catálogo e duas listagens do Amazon. Exemplo: A Amazon tem o produto listado com valores de ASIN diferentes. Você pode combinar seu produto de catálogo único com ambas as listagens do ASIN do produto.<br><br>Pode ser usado para controlar uma listagem em diferentes regiões do Amazon. Exemplo: Você tem um produto de catálogo que tem diferentes métodos de entrega definidos com base na região Amazon (região dos EUA é FBA e região do Canadá é FBM). Para controlar estoque/quantidade, você pode criar um SKU de vendedor de alias e depender do mesmo produto nessa região com um SKU de vendedor diferente. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Switch to Fulfilled by Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings) | Usado para modificar o método de preenchimento associado ao seu produto (preenchido pela Amazon: FBA ou preenchido pelo comerciante: FBM). | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL End Listing]](./end-listings-manually.md) | (Ação de lista única) Usada para encerrar e remover manualmente as listagens de seus produtos que existem no Amazon. As listagens adicionadas podem ser listadas novamente, desde que atendam à qualificação de suas regras de listagem. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Override]](./creating-editing-overrides.md) | (Ação de listagem única) Edite manualmente uma &quot;sobreposição&quot; existente que define o preço, o tempo de manuseio, a condição e o texto das notas do vendedor para uma listagem individual, ignorando outros padrões, configurações e regras da listagem. | [[!UICONTROL Overrides]](./overrides.md) |

## Acessar listas de produtos

1. No _Administrador_ barra lateral, vá para **Marketing** > _Canais_ > **Sales Channel Amazon**.

1. Clique em **Exibir Loja** no cartão da loja.

1. No painel da loja, clique em **Gerenciar Listagens** no _Listagens de armazenamento_ seção.
