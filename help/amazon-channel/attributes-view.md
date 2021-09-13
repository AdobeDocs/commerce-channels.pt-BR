---
title: Atributos
description: O Amazon Sales Channel fornece a guia [!UICONTROL Attributes] para monitorar a lista de atributos do Amazon e Commerce e como eles são mapeados para correspondência de produtos.
exl-id: fc08cd6e-eef9-4e71-82b1-5443e14800ce
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Atributos

A exibição _[!UICONTROL Attributes]_mostra a lista de atributos Amazon e [!DNL Commerce]. A lista também indica atributos que foram mapeados para a correspondência do produto. Para obter mais informações, consulte [Gerenciar atributos](./managing-attributes.md).

![Exibição de atributos](assets/amazon-attributes-view.png)

Na exibição _[!UICONTROL Attributes]_, você e revisem as configurações do atributo na tabela e [crie ou edite](./creating-attributes.md) um atributo.

## Exibir sua lista de atributos

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Clique em **[!UICONTROL Attributes]** no menu à esquerda, localize um atributo do Amazon e revise sua lista de atributos.

1. Crie ou edite um atributo, conforme necessário:

   - Para [criar](./creating-attributes.md#create-an-attribute) e definir os Valores de Atributo Correspondentes para o atributo, clique em **[!UICONTROL Create]**.

   - Para desativar ou [editar as configurações](./creating-attributes.md#edit-an-attribute) ou Corresponder aos valores do atributo para o atributo, clique em **[!UICONTROL Edit]**.

      Editar um atributo inclui alterar o mapeamento de atributo para correspondência de produto.

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Country] | O país para a atividade de vendas definida em **[!DNL Amazon Marketplace]País** durante [integração de loja](./store-integration.md). |
| [!UICONTROL ID] | Valor de atributo genérico gerado por [!DNL Commerce] quando o atributo é criado. |
| [!UICONTROL Amazon Attribute Name] | O nome do atributo importado do Amazon. |
| [!UICONTROL Product Catalog Attribute Code] | Se mapeado, o atributo [!DNL Commerce] atribuído para mapear para _[!UICONTROL Amazon Attribute Name]_para catálogos correspondentes e produtos de listagem. |
| [!UICONTROL Overwrite Magento Values] | Se o atributo estiver definido como `Overwrite Existing Magento Values` nas Configurações de atributo, a tabela mostrará `Enabled`. Ativado significa que, quando as informações atualizadas do produto para o atributo são recebidas do Amazon, as novas informações atualizam (substituem) as informações correspondentes do produto no catálogo [!DNL Commerce]. Também pode afetar seus produtos listados em suas lojas [!DNL Commerce]. |
| Status | Indica se os valores do atributo foram importados para [!DNL Commerce] e mapeados para um atributo [!DNL Commerce]. Opções: `Enabled` / `Disabled` |
| Ação | Indica as opções de tarefa disponíveis para o atributo. Opções: `Create` / `Edit` |
