---
title: '"Integração: Criar regra de listagem'''
description: Ao concluir o processo de integração do canal de vendas da Amazon, crie as regras de listagem iniciais para gerar listagens do Amazon para seus produtos  [!DNL Commerce] .
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Integração: Criar regra de listagem

As regras de listagem podem ser definidas durante a integração, mas também podem ser modificadas a qualquer momento. Após a integração, você pode acessar as [regras de listagem](./listing-rules.md) no armazenamento [painel](./amazon-store-dashboard.md).

## Criar uma regra de listagem durante a integração

1. Depois que a loja estiver conectada, clique em **[!UICONTROL View Store]** para a loja adicionada.

   O armazenamento [painel](./amazon-store-dashboard.md) aparece com a mensagem `No products listed to Amazon`.

1. Clique em **[!UICONTROL Preview and List Eligible Products]**.

   A página _[!UICONTROL Listing Rules]_é exibida.

1. Defina as condições desejadas para a qualificação dos produtos a serem listados no Amazon e clique em **[!UICONTROL Preview changes]**, ou clique em **[!UICONTROL Preview changes]** para ignorar esta etapa.

   Consulte [Exemplo: Defina uma Condição](./ob-define-condition-example.md).

1. Revise suas listagens na Visualização de listagem:

   ![Visualização de listagem](assets/amazon-ob-listing-preview.png)

   - **[!UICONTROL Ineligible Listings]** - Os produtos listados nesta guia não estão qualificados para a listagem do Amazon com base nas configurações atuais da regra de listagem.

      Produtos inelegíveis não são publicados na Amazon. Se um produto inelegível já estiver listado no Amazon e você corresponder a listagem do Amazon ao seu [!DNL Commerce] produto de catálogo, a quantidade para a listagem do Amazon será alterada para `0` para impedir as vendas do produto. Para remover manualmente uma listagem do Amazon, consulte [Encerrando uma listagem do Amazon](./end-listings-manually.md). Os produtos que não estão qualificados pelos requisitos do Amazon não estão listados aqui. Esses produtos estão listados na guia [[!UICONTROL Inactive Listings]](./inactive-listings.md).

      Para alterar uma lista `Ineligible` para uma lista `Eligible`, repita esse processo e modifique suas regras de listagem.

   - **[!UICONTROL Eligible Listings]** - Os produtos listados nesta guia estão qualificados para a listagem do Amazon com base na sua configuração de regra de listagem atual e estão qualificados pelos requisitos do Amazon. Esta guia inclui as listagens existentes do Amazon que são importadas (se você tiver **[!UICONTROL Import Third Party Listings]** definido como `Import Listing` em [Configurações de listagem](./listing-settings.md)).

   - **[!UICONTROL New Listings]** - Os produtos listados nesta guia incluem os produtos de  [!DNL Commerce] catálogo que foram recentemente qualificados para a listagem do Amazon com base na configuração atual da regra de listagem e criam listagens do Amazon.

1. Quando terminar, clique em **[!UICONTROL Save and Close]**.

   O armazenamento [painel](./amazon-store-dashboard.md) é aberto.

Após a conclusão da integração de uma loja, a sincronização de informações entre [!DNL Commerce] e o Amazon é iniciada. Suas listagens do Amazon são importadas para [!DNL Commerce] e tentam corresponder com produtos em seu [!DNL Commerce] Catálogo.

Você pode exibir suas informações de pedido do Amazon na seção _[!UICONTROL Recent Orders]_do painel da loja. Consulte [Armazenar painel](./amazon-store-dashboard.md) ou [Gerenciar pedidos](./managing-orders.md).

>[!IMPORTANT]
>
>Há algumas configurações de armazenamento importantes (listagens, preços, regras, cumprimento, etc.) que têm valores padrão para uma nova loja. Para garantir que sua loja esteja configurada para suas necessidades específicas, revise as [configurações de loja](./default-store-settings.md) .

![Próximo ](assets/btn-next.png) [**íconeContinuar com as configurações padrão da loja**](./default-store-settings.md)
