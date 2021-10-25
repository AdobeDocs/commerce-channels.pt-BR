---
title: Configurações padrão da loja
description: Modifique as configurações padrão do Commerce para personalizar o Amazon Sales Channel para sua loja.
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Configurações de armazenamento padrão

Depois que sua loja estiver conectada e você configurar sua primeira regra de listagem, a sincronização de dados entre o Amazon e o [!DNL Commerce] inicia. Há vários tipos de configurações de loja que permitem personalizar sua loja de acordo com suas necessidades. As configurações de armazenamento são acessadas na loja [painel](./amazon-store-dashboard.md).

As configurações de armazenamento incluem:

- [**[!UICONTROL Listing settings]**](./listing-settings.md) - Controle como o catálogo de produtos interage com o [!DNL Amazon Marketplace].

- [**[!UICONTROL Order settings]**](./order-settings.md) - Controle como os pedidos da Amazon são gerenciados.

- [**[!UICONTROL Listing rules]**](./listing-rules.md) - Defina quais produtos de catálogo estão qualificados para serem listados no Amazon.

- [**[!UICONTROL Pricing rules]**](./pricing-products.md) - Defina como o preço da lista Amazon é alterado para listas qualificadas.

- **[!UICONTROL Store reports]** - [Análise de preços competitiva](./competitive-price-analysis.md) e [melhorias na listagem](./listing-improvements.md).

- **[!UICONTROL Logs]** - [Alterações na listagem](./listing-changes-log.md) e [erros de comunicação](./communication-errors-log.md).

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md) - Revise as configurações de nome do armazenamento do email e do canal de vendas da Amazon no [!DNL Commerce] Administrador

## Algumas configurações padrão importantes

| Configuração | Padrão | Descrição | Localização |
|--- |--- |--- |--- |
| [!UICONTROL Import Amazon Orders] | `Enabled` | Cria correspondências [!DNL Commerce] pedidos quando novos pedidos são recebidos da Amazon, permitindo que os pedidos sejam gerenciados na [[!DNL Commerce] Pedidos](https://docs.magento.com/user-guide/sales/orders.html)Fluxo de trabalho {target=&quot;_blank&quot;}. When `Disabled`, informações de ordem de importação de pedidos do Amazon para revisão, mas os pedidos devem ser gerenciados em [!DNL Amazon Seller Central] conta. | [Configurações da ordem](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | Os dados do cliente de pedidos da Amazon não são importados para o seu [!DNL Commerce] banco de dados. Os pedidos importados do Amazon são processados como check-out de convidado. Se quiser criar a [!DNL Commerce] banco de dados do cliente, você deve alterar essa configuração para `Build New Customer Account`. | [Configurações da ordem](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] produtos de catálogo (que atendem aos requisitos de qualificação da Amazon) para publicar automaticamente no Amazon e criar listagens do Amazon. Se quiser revisar e publicar manualmente seus produtos, altere essa configuração para `Do Not Automatically List Eligible Products`. Os produtos que aguardam a publicação manual são exibidos na [_Pronto para listar_](./ready-to-list.md) guia . | [Ações de listagem de produtos](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | Define o atributo de fonte de preço usado como base para suas listagens do Amazon. Se não quiser usar a variável [!DNL Commerce] `Price` como seu preço base para o qual suas regras de preços se baseiam, você deve alterar essa configuração para um atributo diferente. | [Preço de Listagem](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | O comerciante atende a todos os pedidos. Se você usar o Cumprimento pela Amazon ou usar uma combinação de métodos de cumprimento, deverá alterar essa configuração. | [Cumprido por](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | Se todos os seus produtos forem a mesma condição, você poderá selecionar uma das opções de condição do Amazon para representar todos os seus produtos. Se o catálogo contém produtos em condições diferentes (como Novo, Usado e Refurorado), é necessário alterar essa configuração para `Assign Condition Using Product Attribute` e mapeie seu [!DNL Commerce] atributos de condição para suas condições de listagem do Amazon. | [Condição de listagem de produtos](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | nenhum | Defina as regras usadas para determinar quais produtos o canal de vendas do Amazon publica no Amazon. Essas regras fornecem muitas opções para criar regras simples e complexas para incluir ou excluir produtos como listas. | [Regras de listagem](./listing-rules.md) |
| Regras de Preços | nenhum | Defina seu atributo de preço de listagem do Amazon diferente do definido _[!UICONTROL Magento Price Source]_em seu [Preço de Listagem](./listing-price.md). Para ajustar o preço da listagem (para cima ou para baixo) em relação ao valor de_[!UICONTROL Magento Price Source]_ , criar regras. | [Regras de Preços](./pricing-products.md) |

Para obter mais informações, consulte [Configurações da loja](./ob-store-review.md).
