---
title: Atributos
description: O Sales Channel da Amazon fornece a [!UICONTROL Attributes] para monitorar a lista de atributos do Amazon e do Commerce e como eles são mapeados para correspondência de produtos.
exl-id: fc08cd6e-eef9-4e71-82b1-5443e14800ce
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Atributos

A variável _[!UICONTROL Attributes]_exibir mostra sua lista de Amazon e [!DNL Commerce] atributos. A lista também indica atributos que foram mapeados para correspondência de produtos. Para obter mais informações, consulte [Gerenciar atributos](./managing-attributes.md).

![Exibição de atributos](assets/amazon-attributes-view.png)

No _[!UICONTROL Attributes]_exibir, você e revise suas configurações de atributo na tabela e [criar ou editar](./creating-attributes.md) um atributo.

## Exibir sua lista de atributos

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Clique em **[!UICONTROL Attributes]** no menu do lado esquerdo, localize um atributo do Amazon e revise sua lista de atributos.

1. Crie ou edite um atributo, conforme necessário:

   - Para [criar](./creating-attributes.md#create-an-attribute) e definir Valores de Atributos Correspondentes para o atributo, clique em **[!UICONTROL Create]**.

   - Para desativar ou [editar as configurações](./creating-attributes.md#edit-an-attribute) ou Valores de Atributos Correspondentes para o atributo, clique em **[!UICONTROL Edit]**.

      A edição de um atributo inclui a alteração do mapeamento de atributos para a correspondência de produtos.

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Country] | O país para a atividade de vendas definida em  **[!DNL Amazon Marketplace]País** durante [integração de loja](./store-integration.md). |
| [!UICONTROL ID] | Valor de atributo genérico gerado por [!DNL Commerce] quando o atributo é criado. |
| [!UICONTROL Amazon Attribute Name] | O nome do atributo importado do Amazon. |
| [!UICONTROL Product Catalog Attribute Code] | Se mapeado, o [!DNL Commerce] atributo atribuído para mapear para o _[!UICONTROL Amazon Attribute Name]_para corresponder produtos de catálogo e listagem. |
| [!UICONTROL Overwrite Magento Values] | Se o atributo estiver definido como `Overwrite Existing Magento Values` nas Configurações de atributo, a tabela mostra `Enabled`. Ativado significa que, quando informações atualizadas do produto para o atributo forem recebidas da Amazon, as novas informações atualizarão (substituirão) as informações correspondentes do produto em seu [!DNL Commerce] catálogo. Ela também pode afetar seus produtos listados na [!DNL Commerce] lojas. |
| Status | Indica se os valores de atributo foram importados para [!DNL Commerce] e mapeado para um [!DNL Commerce] atributo. Opções: `Enabled` / `Disabled` |
| Ação | Indica as opções de tarefa disponíveis para o atributo. Opções: `Create` / `Edit` |
