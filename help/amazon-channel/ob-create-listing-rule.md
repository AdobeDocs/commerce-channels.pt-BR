---
title: '"Integração: Criar regra de listagem'''
description: Ao concluir o processo de integração do canal de vendas da Amazon, crie as regras de listagem iniciais para gerar listagens da Amazon para seu [!DNL Commerce] produtos.
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Integração: Criar regra de listagem

As regras de listagem podem ser definidas durante a integração, mas também podem ser modificadas a qualquer momento. Após a integração, você pode acessar o [regras de listagem](./listing-rules.md) na loja [painel](./amazon-store-dashboard.md).

## Criar uma regra de listagem durante a integração

1. Depois que a loja estiver conectada, clique em **[!UICONTROL View Store]** para a loja adicionada.

   A loja [painel](./amazon-store-dashboard.md) é exibido com o `No products listed to Amazon` mensagem.

1. Clique em **[!UICONTROL Preview and List Eligible Products]**.

   O _[!UICONTROL Listing Rules]_será exibida.

1. Defina as condições desejadas para a qualificação dos produtos a serem listados no Amazon e clique em **[!UICONTROL Preview changes]** ou clique em **[!UICONTROL Preview changes]** para ignorar esta etapa.

   Consulte [Exemplo: Definir uma condição](./ob-define-condition-example.md).

1. Revise suas listagens na Visualização de listagem:

   ![Visualização de listagem](assets/amazon-ob-listing-preview.png)

   - **[!UICONTROL Ineligible Listings]** - Os produtos listados nesta guia não estão qualificados para a listagem do Amazon com base nas configurações atuais da regra de listagem.

      Produtos inelegíveis não são publicados na Amazon. Se um produto inelegível já estiver listado no Amazon e você corresponder a listagem do Amazon ao seu [!DNL Commerce] produto de catálogo, a quantidade para a listagem do Amazon muda para `0` Impedir a venda do produto. Para remover manualmente uma listagem do Amazon, consulte [Encerrar uma listagem do Amazon](./end-listings-manually.md). Os produtos que não estão qualificados pelos requisitos do Amazon não estão listados aqui. Esses produtos estão listados no [[!UICONTROL Inactive Listings] guia](./inactive-listings.md).

      Para alterar uma `Ineligible` listar para um `Eligible` listar, repita esse processo e modifique suas regras de listagem.

   - **[!UICONTROL Eligible Listings]** - Os produtos listados nesta guia estão qualificados para a listagem do Amazon com base na sua configuração de regra de listagem atual e estão qualificados pelos requisitos do Amazon. Esta guia inclui as listagens existentes do Amazon que foram importadas (caso **[!UICONTROL Import Third Party Listings]** defina como `Import Listing` em seu [Configurações de listagem](./listing-settings.md)).

   - **[!UICONTROL New Listings]** - Os produtos listados nesta guia incluem o [!DNL Commerce] produtos de catálogo recém-qualificados para a listagem do Amazon com base na sua configuração de regra de listagem atual e crie listagens do Amazon.

1. Ao concluir, clique em **[!UICONTROL Save and Close]**.

   A loja [painel](./amazon-store-dashboard.md) é aberto.

Após a conclusão da integração de uma loja, as informações são sincronizadas entre [!DNL Commerce] e Amazon é iniciado. As listas do Amazon são importadas para [!DNL Commerce] e tentar corresponder com os produtos na sua [!DNL Commerce] Catálogo.

Você pode exibir suas informações de pedido da Amazon no _[!UICONTROL Recent Orders]_do painel de loja. Consulte [Painel de armazenamento](./amazon-store-dashboard.md) ou [Gerenciar pedidos](./managing-orders.md).

>[!IMPORTANT]
>
>Há algumas configurações de armazenamento importantes (listagens, preços, regras, cumprimento, etc.) que têm valores padrão para uma nova loja. Para garantir que sua loja esteja configurada para suas necessidades específicas, revise [configurações de armazenamento](./default-store-settings.md) .

![Ícone Próximo](assets/btn-next.png) [**Continuar para as configurações padrão da loja**](./default-store-settings.md)
