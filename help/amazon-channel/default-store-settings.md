---
title: Configurações da loja padrão
description: Modifique as configurações padrão do Commerce para personalizar o Sales Channel do Amazon para sua loja.
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Configurações da loja padrão

Depois que a loja estiver conectada e você configurar a primeira regra de listagem, a sincronização de dados entre o Amazon e [!DNL Commerce] O é iniciado. Há vários tipos de configurações de loja que permitem personalizar a loja de acordo com suas necessidades. As configurações da loja são acessadas nela [painel](./amazon-store-dashboard.md).

As configurações de armazenamento incluem:

- [**[!UICONTROL Listing settings]**](./listing-settings.md) - Controlar como o catálogo de produtos interage com a [!DNL Amazon Marketplace].

- [**[!UICONTROL Order settings]**](./order-settings.md) - Controlar como os pedidos da Amazon são gerenciados.

- [**[!UICONTROL Listing rules]**](./listing-rules.md) - Definir quais produtos de catálogo estão qualificados para serem listados no Amazon.

- [**[!UICONTROL Pricing rules]**](./pricing-products.md) - Definir como o preço de lista do Amazon é alterado para as listagens qualificadas.

- **[!UICONTROL Store reports]** - [Análise de preço competitiva](./competitive-price-analysis.md) e [melhorias na lista](./listing-improvements.md).

- **[!UICONTROL Logs]** - [Listando alterações](./listing-changes-log.md) e [erros de comunicação](./communication-errors-log.md).

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md) - Revisar as configurações de email e nome do armazenamento do canal de vendas da Amazon no [!DNL Commerce] Admin.

## Algumas configurações padrão importantes

| Configuração | Padrão | Descrição | Localização |
|--- |--- |--- |--- |
| [!UICONTROL Import Amazon Orders] | `Enabled` | Cria um correspondente [!DNL Commerce] pedidos quando novos pedidos são recebidos da Amazon, permitindo que os pedidos sejam gerenciados no [[!DNL Commerce] Pedidos](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"} fluxo de trabalho. Quando `Disabled`, o Amazon solicita as informações de ordem de importação para revisão, mas os pedidos devem ser gerenciados no [!DNL Amazon Seller Central] conta. | [Configurações do pedido](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | Os dados do cliente de pedidos da Amazon não são importados para o [!DNL Commerce] banco de dados. Os pedidos Amazon importados são processados como check-out de convidado. Se você quiser criar seu [!DNL Commerce] banco de dados do cliente, você deve alterar essa configuração para `Build New Customer Account`. | [Configurações do pedido](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] produtos de catálogo (que atendem aos requisitos de qualificação da Amazon) para publicar automaticamente no Amazon e criar Listagens do Amazon. Se quiser revisar e publicar manualmente seus produtos, altere essa configuração para `Do Not Automatically List Eligible Products`. Os produtos que aguardam publicação manual são exibidos no [_Pronto para Listar_](./ready-to-list.md) guia. | [Ações de listagem de produtos](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | Define o atributo de origem de preço usado como a base para suas listagens do Amazon. Se não quiser usar o plug-in [!DNL Commerce] `Price` como seu preço base no qual suas regras de precificação se baseiam, você deve alterar essa configuração para um atributo diferente. | [Preço de Listagem](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | O comerciante atende a todas as ordens. Se você usar Abastecimento por Amazon ou uma combinação de métodos de preenchimento, deverá alterar essa configuração. | [Preenchido por](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | Se todos os seus produtos estiverem na mesma condição, você poderá selecionar uma das opções de condição do Amazon para representar todos os seus produtos. Se o catálogo contiver produtos em condições diferentes (como Novo, Usado e Recondicionado), você deverá alterar essa configuração para `Assign Condition Using Product Attribute` e mapear seu [!DNL Commerce] atributos de condição para suas condições de lista do Amazon. | [Condição de listagem de produtos](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | nenhum | Defina as regras usadas para determinar quais produtos o canal de vendas do Amazon publica para o Amazon. Essas regras fornecem muitas opções para criar regras simples a complexas para incluir ou excluir produtos como listas. | [Regras de listagem](./listing-rules.md) |
| Regras de preços | nenhum | Defina seu atributo de preço de lista do Amazon diferente do definido _[!UICONTROL Magento Price Source]_no seu [Preço de Listagem](./listing-price.md). Para ajustar o preço da lista (para cima ou para baixo) em relação ao_[!UICONTROL Magento Price Source]_ criar regras. | [Regras de preços](./pricing-products.md) |

Para obter mais informações, consulte [Configurações da loja](./ob-store-review.md).
