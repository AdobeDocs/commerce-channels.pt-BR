---
title: Regras de listagem
description: Use as regras de listagem para determinar os produtos do catálogo de comércio publicados como listagens do Amazon Marketplace.
redirect_from: /sales-channels/asc/ob-listing-rules.html/sales-channels/asc/ob-listing-preview.html/sales-channels/asc/listing-rule-preview.html
exl-id: b28a625b-64cf-4119-98bb-f1ea33043c8f
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%

---

# Regras de listagem

Você pode acessar as regras de listagem para armazenar na [painel de loja](./amazon-store-dashboard.md).

As regras de listagem definem as regras para determinar quais produtos o canal de vendas do Amazon publica no Amazon. Essas regras fornecem muitas opções para criar regras simples e complexas para incluir ou excluir produtos como listas. Cada regra consiste em condições que definem os requisitos para a qualificação da lista de produtos.

Suas regras de listagem são sincronizadas continuamente com seu [!DNL Commerce] catálogo. Ao adicionar novos [!DNL Commerce] produtos que atendem aos requisitos de qualificação definidos pelas regras de listagem, os produtos são automaticamente processados para serem listados no Amazon.

- Se quiser que todos os seus produtos sejam publicados em uma lista da Amazon, não defina condições para as regras de listagem.

- Se quiser limitar quais produtos de catálogo são publicados no Amazon, defina suas condições de regra de listagem. A definição das condições para suas regras de listagem do Amazon segue a mesma lógica e o mesmo processo que a definição das condições para [Regras de preço do carrinho](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}.

- Se suas regras de listagem excluírem um produto, o status de elegibilidade desse produto será alterado para `Ineligible`. Produtos inelegíveis não são publicados na Amazon.

- Se um produto inelegível já estiver listado no Amazon e você corresponder a listagem do Amazon ao seu [!DNL Commerce] produto de catálogo, a quantidade para a listagem do Amazon muda para `0` Impedir a venda do produto. As listagens do Amazon podem ser [removido manualmente](./end-listings-manually.md).

As alterações na quantidade e no status de qualificação afetam todas as listagens que compartilham a SKU do vendedor de Amazon nos mercados existentes para lojas que vendem na mesma região (conforme definido em _[!UICONTROL Amazon Marketplace Country]_during [integração de loja](./store-integration.md)). No entanto, uma alteração em um [!DNL Amazon Seller SKU] em uma região não afeta as listagens do Amazon do produto em um país diferente.

![Regras de listagem](assets/ob-listing-rules.png)

## Definir configurações de regras de listagem

1. Clique em **[!UICONTROL Listing Rules]** no painel da loja.

1. Defina as condições desejadas para a qualificação de produtos a serem listados no Amazon.

Consulte [Exemplo: Definir uma condição](./ob-define-condition-example.md).

| Campo | Descrição |
|---|---|
| [!UICONTROL Websites] | As opções disponíveis dependem do [sites](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;} você configurou em seu [!DNL Commerce] configuração. Selecione o site para os produtos qualificados listados no Amazon. Somente um site pode ser selecionado, pois cada site requer uma loja exclusiva da Amazon criada no canal de vendas da Amazon. |
| [!UICONTROL Conditions] | Usado para definir a variável [!DNL Commerce] para qualificação de produto na região da Amazon. Consulte [Exemplo: Definir uma condição](./ob-define-condition-example.md). |

## Espaço de trabalho Condições

Qualquer área nas condições em negrito pode ser clicada para ver as várias opções.

- Não adicione condições se todos os produtos nos sites selecionados estiverem qualificados.
- Há um conjunto complexo de processos de back-end para se comunicar diretamente com os sistemas Amazon. Com base no número de itens que você está tentando listar e no quão ocupados os sistemas Amazon podem estar (como Black Friday), pode levar tempo para que seus itens sejam listados no Amazon.

Para obter mais informações sobre condições, consulte [Descreva as condições](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}.

## Visualização da regra de listagem

Ao modificar as definições de condição para as regras de listagem, você pode clicar em **[!UICONTROL Preview Changes]** para aplicar as alterações das regras e visualizar como as listagens são afetadas. Verifique suas listagens neste recurso de visualização de listagem antes de salvar as alterações na regra de listagem.

As listagens do Amazon são comparadas às regras e condições definidas. Você pode então revisar:

- Quais produtos são movidos para um status inelegível com base no seu [!DNL Amazon Seller Central] account
- Quais produtos migram de um estado inelegível para o status elegível
- Quais produtos são Novas listagens do Amazon e foram adicionados à sua listagem do Amazon a partir de seu produto qualificado [!DNL Commerce] products

A Visualização de listagem permite que você visualize suas possíveis listagens do Amazon e faça os ajustes necessários às suas regras de listagem.

Suas possíveis listagens do Amazon são preenchidas no _[!UICONTROL Listing Preview]_em uma das três guias:

- **[!UICONTROL Ineligible Listings]** - Os produtos listados não estão qualificados para a listagem do Amazon com base nas regras e condições atuais da listagem.

   Produtos inelegíveis não são publicados na Amazon. Se um produto inelegível já estiver listado no Amazon e você corresponder a listagem do Amazon ao seu [!DNL Commerce] produto de catálogo, a quantidade para a listagem do Amazon muda para `0` Impedir a venda do produto. Para remover manualmente uma listagem, consulte [Encerrar uma listagem do Amazon](./end-listings-manually.md). Os produtos que não estão qualificados pelos requisitos do Amazon não estão listados aqui. Esses produtos estão listados no [Guia Listagens Inativas](./inactive-listings.md).

- **[!UICONTROL Eligible Listings]** - Os produtos listados são qualificados para a listagem do Amazon com base nas regras e condições atuais da listagem e também são qualificados pelos requisitos do Amazon. Esta lista inclui as listagens existentes do Amazon que importam (se você **Importar Listagens de Terceiros** defina como `Import Listing` em [Configurações de listagem](./third-party-listing-settings.md)).

- **[!UICONTROL New Listings]** - Os produtos listados incluem seu [!DNL Commerce] produtos de catálogo recém-qualificados para a listagem do Amazon com base em suas regras e condições de listagem atuais, e crie e publique novas listagens do Amazon.

### Exibir a visualização da listagem

1. Clique em **[!UICONTROL Listing Rules]** no painel da loja.

1. Exibir ou adicionar [regras de listagem](./listing-rules.md).

1. Modifique seu [Condições da Regra de Listagem](./ob-define-condition-example.md).

1. Clique em **[!UICONTROL Preview Changes]**.

1. Revise e confirme suas listas no _[!UICONTROL Ineligible Listings]_,_[!UICONTROL Eligible Listings]_ e _[!UICONTROL New Listings]_guias.

1. Se as listagens corresponderem às suas expectativas, clique em **[!UICONTROL Save and close]**.

   Se as listagens não forem exibidas conforme o esperado, clique em **[!UICONTROL Back]** e modifique suas regras e condições até que suas listagens correspondam às suas expectativas.

![Visualização da regra de listagem](assets/amazon-listing-rule-preview.png)

### Listando registros de visualização

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Product ID] | O número sequencial exclusivo atribuído a um [!DNL Commerce] produto de catálogo quando é adicionado. |
| [!UICONTROL Thumbnail] | Mostra uma miniatura da imagem principal do produto. |
| [!UICONTROL Name] | O nome do produto, gerenciado no [!DNL Commerce] [grade de produtos](https://docs.magento.com/user-guide/catalog/products.html){target=&quot;_blank&quot;}. |
| [!UICONTROL Type] | O tipo de produto, gerenciado na variável [!DNL Commerce] grade de produtos. |
| [!UICONTROL Attribute Set] | O nome do conjunto de atributos usado como modelo para o produto, gerenciado na variável [!DNL Commerce] grade de produtos. |
| [!UICONTROL SKU] | A unidade única de manutenção de estoque atribuída ao produto, gerenciada no [!DNL Commerce] grade de produtos. |
| [!UICONTROL Visibility] | Indica onde o produto está visível, gerenciado na variável [!DNL Commerce] grade de produtos. Opções:<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| Status | Indica o status do produto, gerenciado no [!DNL Commerce] grade de produtos. Opções: `Enabled` / `Disabled` |

![Fluxo de trabalho de pré-visualização de listagem](assets/listing-preview-flowchart.png)
