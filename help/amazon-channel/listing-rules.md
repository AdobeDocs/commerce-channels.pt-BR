---
title: Regras de listagem
description: Use as regras de listagem para determinar os produtos do catálogo de comércio publicados como listagens do Amazon Marketplace.
redirect_from: /sales-channels/asc/ob-listing-rules.html: /sales-channels/asc/ob-listing-preview.html: /sales-channels/asc/listing-rule-preview.html: 
exl-id: b28a625b-64cf-4119-98bb-f1ea33043c8f
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 0
ht-degree: 0%

---

# Regras de listagem

Você pode acessar as regras de listagem para armazenar no [store dashboard](./amazon-store-dashboard.md).

As regras de listagem definem as regras para determinar quais produtos o canal de vendas do Amazon publica no Amazon. Essas regras fornecem muitas opções para criar regras simples e complexas para incluir ou excluir produtos como listas. Cada regra consiste em condições que definem os requisitos para a qualificação da lista de produtos.

Suas regras de listagem são sincronizadas continuamente com seu catálogo [!DNL Commerce]. Quando você adiciona novos [!DNL Commerce] produtos que atendem aos requisitos de qualificação definidos pelas regras de listagem, os produtos são automaticamente processados para listagem no Amazon.

- Se quiser que todos os seus produtos sejam publicados em uma lista da Amazon, não defina condições para as regras de listagem.

- Se quiser limitar quais produtos de catálogo são publicados no Amazon, defina suas condições de regra de listagem. A definição das condições para suas regras de listagem do Amazon segue a mesma lógica e o mesmo processo que a definição das condições para [Regras de Preço do Carrinho](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}.

- Se suas regras de listagem excluírem um produto, o status de elegibilidade desse produto será alterado para `Ineligible`. Produtos inelegíveis não são publicados na Amazon.

- Se um produto inelegível já estiver listado no Amazon e você corresponder a listagem do Amazon ao seu [!DNL Commerce] produto de catálogo, a quantidade para a listagem do Amazon será alterada para `0` para impedir as vendas do produto. As listagens do Amazon podem ser [removidas manualmente](./end-listings-manually.md).

As alterações na quantidade e no status de qualificação afetam todas as listagens que compartilham a SKU do Vendedor de Amazon nos mercados existentes para lojas que vendem na mesma região (conforme definido em _[!UICONTROL Amazon Marketplace Country]_durante [integração de loja](./store-integration.md)). No entanto, uma alteração em um [!DNL Amazon Seller SKU] compartilhado em uma região não afeta as listagens do Amazon do produto em um país diferente.

![Regras de listagem](assets/ob-listing-rules.png)

## Definir configurações de regras de listagem

1. Clique em **[!UICONTROL Listing Rules]** no painel da loja.

1. Defina as condições desejadas para a qualificação de produtos a serem listados no Amazon.

Consulte [Exemplo: Defina uma Condição](./ob-define-condition-example.md).

| Campo | Descrição |
|---|---|
| [!UICONTROL Websites] | As opções disponíveis dependem dos [sites](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;} que você configurou na configuração [!DNL Commerce]. Selecione o site para os produtos qualificados listados no Amazon. Somente um site pode ser selecionado, pois cada site requer uma loja exclusiva da Amazon criada no canal de vendas da Amazon. |
| [!UICONTROL Conditions] | Usado para definir os atributos [!DNL Commerce] para elegibilidade de produto na região do Amazon. Consulte [Exemplo: Defina uma Condição](./ob-define-condition-example.md). |

## Espaço de trabalho Condições

Qualquer área nas condições em negrito pode ser clicada para ver as várias opções.

- Não adicione condições se todos os produtos nos sites selecionados estiverem qualificados.
- Há um conjunto complexo de processos de back-end para se comunicar diretamente com os sistemas Amazon. Com base no número de itens que você está tentando listar e no quão ocupados os sistemas Amazon podem estar (como Black Friday), pode levar tempo para que seus itens sejam listados no Amazon.

Para obter mais informações sobre as condições, consulte [Descrever as Condições](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}.

## Visualização da regra de listagem

Ao modificar as definições de condição para as regras de listagem, você pode clicar em **[!UICONTROL Preview Changes]** para aplicar as alterações de regras e visualizar como as listagens são afetadas. Verifique suas listagens neste recurso de visualização de listagem antes de salvar as alterações na regra de listagem.

As listagens do Amazon são comparadas às regras e condições definidas. Você pode então revisar:

- Quais produtos são movidos para um status inelegível com base em sua conta [!DNL Amazon Seller Central] atual
- Quais produtos migram de um estado inelegível para o status elegível
- Quais produtos são as Novas listagens do Amazon e adicionadas à listagem do Amazon de seus produtos [!DNL Commerce] qualificados

A Visualização de listagem permite que você visualize suas possíveis listagens do Amazon e faça os ajustes necessários às suas regras de listagem.

Suas possíveis listagens do Amazon são preenchidas na página _[!UICONTROL Listing Preview]_em uma das três guias:

- **[!UICONTROL Ineligible Listings]** - Os produtos listados não estão qualificados para a listagem do Amazon com base nas regras e condições atuais da listagem.

   Produtos inelegíveis não são publicados na Amazon. Se um produto inelegível já estiver listado no Amazon e você corresponder a listagem do Amazon ao seu [!DNL Commerce] produto de catálogo, a quantidade para a listagem do Amazon será alterada para `0` para impedir as vendas do produto. Para remover manualmente uma listagem, consulte [Encerrar uma listagem do Amazon](./end-listings-manually.md). Os produtos que não estão qualificados pelos requisitos do Amazon não estão listados aqui. Esses produtos estão listados na [guia Listagens Inativas](./inactive-listings.md).

- **[!UICONTROL Eligible Listings]** - Os produtos listados são qualificados para a listagem do Amazon com base nas regras e condições atuais da listagem e também são qualificados pelos requisitos do Amazon. Esta lista inclui suas listagens existentes do Amazon que são importadas (se você tiver **Importar listagens de terceiros** definido como `Import Listing` em [Configurações de listagem](./third-party-listing-settings.md)).

- **[!UICONTROL New Listings]** - Os produtos listados incluem seus produtos  [!DNL Commerce] de catálogo recém-qualificados para a listagem do Amazon com base nas regras e condições atuais da listagem, e criam e publicam novas listagens do Amazon.

### Exibir a visualização da listagem

1. Clique em **[!UICONTROL Listing Rules]** no painel da loja.

1. Exiba ou adicione suas [regras de listagem](./listing-rules.md).

1. Modifique as [Condições da Regra de Listagem](./ob-define-condition-example.md).

1. Clique em **[!UICONTROL Preview Changes]**.

1. Revise e confirme suas listagens nas guias _[!UICONTROL Ineligible Listings]_,_[!UICONTROL Eligible Listings]_ e _[!UICONTROL New Listings]_.

1. Se as listagens corresponderem às suas expectativas, clique em **[!UICONTROL Save and close]**.

   Se suas listagens não aparecerem como esperado, clique em **[!UICONTROL Back]** e modifique suas regras e condições até que suas listagens correspondam às suas expectativas.

![Visualização da regra de listagem](assets/amazon-listing-rule-preview.png)

### Listando registros de visualização

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Product ID] | O número sequencial exclusivo atribuído a um produto de catálogo [!DNL Commerce] quando adicionado. |
| [!UICONTROL Thumbnail] | Mostra uma miniatura da imagem principal do produto. |
| [!UICONTROL Name] | O nome do produto, gerenciado na [!DNL Commerce] [grade de produtos](https://docs.magento.com/user-guide/catalog/products.html){target=&quot;_blank&quot;}. |
| [!UICONTROL Type] | O tipo de produto, gerenciado na grade de produtos [!DNL Commerce] . |
| [!UICONTROL Attribute Set] | O nome do conjunto de atributos usado como modelo para o produto, gerenciado na grade de produtos [!DNL Commerce]. |
| [!UICONTROL SKU] | A unidade exclusiva de manutenção de estoque atribuída ao produto, gerenciada na grade de produtos [!DNL Commerce]. |
| [!UICONTROL Visibility] | Indica onde o produto é visível, gerenciado na grade de produtos [!DNL Commerce]. Opções:<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| Status | Indica o status do produto, gerenciado na grade de produtos [!DNL Commerce]. Opções: `Enabled` / `Disabled` |

![Fluxo de trabalho de pré-visualização de listagem](assets/listing-preview-flowchart.png)
