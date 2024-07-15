---
title: Atributos para listagens do Amazon
description: O Amazon Sales Channel fornece a guia [!UICONTROL Attributes] para monitorar a lista de atributos Amazon e Commerce e como eles são mapeados para correspondência de produtos.
feature: Sales Channels, Products, Configuration
exl-id: fc08cd6e-eef9-4e71-82b1-5443e14800ce
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# Atributos para listagens do Amazon

A exibição _[!UICONTROL Attributes]_mostra sua lista de Amazon e atributos [!DNL Commerce]. A lista também indica atributos que foram mapeados para correspondência de produtos. Para obter mais informações, consulte [Gerenciar atributos](./managing-attributes.md).

![Exibição de atributos](assets/amazon-attributes-view.png){width="600" zoomable="yes"}

Na exibição _[!UICONTROL Attributes]_, você e o revisem suas configurações de atributo na tabela e [criem ou editem](./creating-attributes.md) um atributo.

## Exibir sua lista de atributos

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Clique em **[!UICONTROL Attributes]** no menu do lado esquerdo, localize um atributo do Amazon e revise sua lista de atributos.

1. Crie ou edite um atributo, conforme necessário:

   - Para [criar](./creating-attributes.md#create-an-attribute) e definir Valores de Atributos Correspondentes para o atributo, clique em **[!UICONTROL Create]**.

   - Para desativar ou [editar as configurações](./creating-attributes.md#edit-an-attribute) ou os Valores de Atributos Correspondentes para o atributo, clique em **[!UICONTROL Edit]**.

     A edição de um atributo inclui a alteração do mapeamento de atributos para a correspondência de produtos.

| Campo | Descrição |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Country] | O país para a atividade de vendas definida em **[!DNL Amazon Marketplace]País** durante a [integração de loja](./store-integration.md). |
| [!UICONTROL ID] | Valor de atributo genérico gerado por [!DNL Commerce] quando o atributo é criado. |
| [!UICONTROL Amazon Attribute Name] | O nome do atributo importado do Amazon. |
| [!UICONTROL Product Catalog Attribute Code] | Se mapeado, o atributo [!DNL Commerce] é atribuído para mapear para o _[!UICONTROL Amazon Attribute Name]_para catálogo correspondente e produtos de listagem. |
| [!UICONTROL Overwrite Magento Values] | Se o atributo estiver definido como `Overwrite Existing Magento Values` nas Configurações de Atributo, a tabela mostrará `Enabled`. Habilitado significa que, quando informações atualizadas do produto para o atributo forem recebidas da Amazon, as novas informações atualizarão (substituirão) as informações correspondentes do produto no catálogo [!DNL Commerce]. Ela também pode afetar seus produtos listados nas lojas do [!DNL Commerce]. |
| Status | Indica se os valores de atributo foram importados para [!DNL Commerce] e mapeados para um atributo [!DNL Commerce]. Opções: `Enabled` / `Disabled` |
| Ação | Indica as opções de tarefa disponíveis para o atributo. Opções: `Create` / `Edit` |
