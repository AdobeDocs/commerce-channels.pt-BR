---
title: Configurações padrão da loja
description: Modifique as configurações padrão do Commerce para personalizar o Amazon Sales Channel para sua loja.
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Configurações de armazenamento padrão

Depois que sua loja é conectada e você configurou sua primeira regra de listagem, a sincronização de dados entre o Amazon e [!DNL Commerce] é iniciada. Há vários tipos de configurações de loja que permitem personalizar sua loja de acordo com suas necessidades. As configurações de armazenamento são acessadas no armazenamento [painel](./amazon-store-dashboard.md).

As configurações de armazenamento incluem:

- [**[!UICONTROL Listing settings]**](./listing-settings.md) - Controle como o catálogo de produtos interage com o  [!DNL Amazon Marketplace].

- [**[!UICONTROL Order settings]**](./order-settings.md) - Controle como os pedidos da Amazon são gerenciados.

- [**[!UICONTROL Listing rules]**](./listing-rules.md) - Defina quais produtos de catálogo estão qualificados para serem listados no Amazon.

- [**[!UICONTROL Pricing rules]**](./pricing-products.md) - Defina como o preço da lista Amazon é alterado para listas qualificadas.

- **[!UICONTROL Store reports]** -  [Análise de preços competitiva ](./competitive-price-analysis.md) e melhorias na  [lista](./listing-improvements.md).

- **[!UICONTROL Logs]** -  [Listar ](./listing-changes-log.md) alterações e erros  [de comunicação](./communication-errors-log.md).

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md) - Revise as configurações de nome do armazenamento do email e do canal de vendas da Amazon no  [!DNL Commerce] Administrador.

## Algumas configurações padrão importantes

| Configuração | Padrão | Descrição | Localização |
|--- |--- |--- |--- |
| [!UICONTROL Import Amazon Orders] | `Enabled` | Cria ordens [!DNL Commerce] correspondentes quando novos pedidos são recebidos da Amazon, permitindo que os pedidos sejam gerenciados no fluxo de trabalho [[!DNL Commerce] Orders](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;} . Quando `Disabled`, o Amazon solicita informações de ordem de importação para revisão, mas os pedidos devem ser gerenciados em sua conta [!DNL Amazon Seller Central]. | [Configurações da ordem](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | Os dados do cliente dos pedidos da Amazon não são importados para o banco de dados [!DNL Commerce]. Os pedidos importados do Amazon são processados como check-out de convidado. Se quiser criar o banco de dados do cliente [!DNL Commerce], altere essa configuração para `Build New Customer Account`. | [Configurações da ordem](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] produtos de catálogo (que atendem aos requisitos de qualificação da Amazon) para publicar automaticamente no Amazon e criar listagens do Amazon. Se quiser revisar e publicar manualmente seus produtos, altere essa configuração para `Do Not Automatically List Eligible Products`. Os produtos que aguardam a publicação manual são exibidos na guia [_Pronto para lista_](./ready-to-list.md). | [Ações de listagem de produtos](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | Define o atributo de fonte de preço usado como base para suas listagens do Amazon. Se você não quiser usar o atributo [!DNL Commerce] `Price` como o preço base no qual suas regras de preços se baseiam, você deve alterar essa configuração para um atributo diferente. | [Preço de Listagem](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | O comerciante atende a todos os pedidos. Se você usar o Cumprimento pela Amazon ou usar uma combinação de métodos de cumprimento, deverá alterar essa configuração. | [Cumprido por](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | Se todos os seus produtos forem a mesma condição, você poderá selecionar uma das opções de condição do Amazon para representar todos os seus produtos. Se o catálogo contém produtos em condições diferentes (como Novo, Usado e Refurbado), você deve alterar essa configuração para `Assign Condition Using Product Attribute` e mapear os atributos de condição [!DNL Commerce] para as condições de listagem do Amazon. | [Condição de listagem de produtos](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | nenhum | Defina as regras usadas para determinar quais produtos o canal de vendas do Amazon publica no Amazon. Essas regras fornecem muitas opções para criar regras simples e complexas para incluir ou excluir produtos como listas. | [Regras de listagem](./listing-rules.md) |
| Regras de Preços | nenhum | Defina seu atributo de preço de listagem do Amazon diferente do _[!UICONTROL Magento Price Source]_definido em seu [Preço de Listagem](./listing-price.md). Para ajustar o preço da listagem (para cima ou para baixo) em relação à configuração_[!UICONTROL Magento Price Source]_, crie regras. | [Regras de Preços](./pricing-products.md) |

Para obter mais informações, consulte [Configurações de armazenamento](./ob-store-review.md).
