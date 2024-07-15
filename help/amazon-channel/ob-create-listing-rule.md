---
title: Criar uma regra de listagem do Amazon
description: Ao concluir o processo de integração do canal de vendas do Amazon, crie as regras de listagem iniciais para gerar listagens do Amazon para seus produtos  [!DNL Commerce] .
role: Admin
feature: Sales Channels, Products, Merchandising, Configuration
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Criar uma regra de listagem do Amazon

As regras de listagem podem ser definidas durante a integração, mas também podem ser modificadas a qualquer momento. Após a integração, você pode acessar as [regras de listagem](./listing-rules.md) no [painel](./amazon-store-dashboard.md) do armazenamento.

## Criar uma regra de listagem durante a integração

1. Depois que o armazenamento for conectado, clique em **[!UICONTROL View Store]** para o armazenamento adicionado.

   O [painel](./amazon-store-dashboard.md) do armazenamento aparece com a mensagem `No products listed to Amazon`.

1. Clique em **[!UICONTROL Preview and List Eligible Products]**.

   A página _[!UICONTROL Listing Rules]_é exibida.

1. Defina as condições desejadas para a qualificação de produtos a serem listados no Amazon e clique em **[!UICONTROL Preview changes]**, ou clique em **[!UICONTROL Preview changes]** para ignorar esta etapa.

   Consulte [Exemplo: Definir uma Condição](./ob-define-condition-example.md).

1. Revise suas listas na Visualização da lista:

   ![Visualização da listagem](assets/amazon-ob-listing-preview.png){width="600" zoomable="yes"}

   - **[!UICONTROL Ineligible Listings]** - Os produtos listados nesta guia não estão qualificados para a listagem do Amazon com base nas suas configurações de regra de listagem atuais.

     Produtos não qualificados não são publicados no Amazon. Se um produto inelegível já estiver listado no Amazon e você corresponder a listagem do Amazon ao seu produto de catálogo [!DNL Commerce], a quantidade para a listagem do Amazon será alterada para `0` para impedir as vendas do produto. Para remover manualmente uma listagem do Amazon, consulte [Encerramento de uma listagem do Amazon](./end-listings-manually.md). Os produtos que não estão qualificados pelos requisitos do Amazon não estão listados aqui. Esses produtos estão listados na guia [[!UICONTROL Inactive Listings]](./inactive-listings.md).

     Para alterar uma listagem `Ineligible` para uma listagem `Eligible`, repita esse processo e modifique suas regras de listagem.

   - **[!UICONTROL Eligible Listings]** - Os produtos listados nesta guia estão qualificados para a listagem do Amazon com base na sua configuração de regra de listagem atual e estão qualificados pelos requisitos do Amazon. Esta guia inclui suas listagens existentes do Amazon que são importadas (se você tiver **[!UICONTROL Import Third Party Listings]** definido como `Import Listing` em suas [Configurações de Listagem](./listing-settings.md)).

   - **[!UICONTROL New Listings]** - Os produtos listados nesta guia incluem seus produtos de catálogo do [!DNL Commerce] que são recém-qualificados para a listagem do Amazon com base na configuração da sua regra de listagem atual e criam listagens do Amazon.

1. Quando terminar, clique em **[!UICONTROL Save and Close]**.

   O [painel](./amazon-store-dashboard.md) do armazenamento é aberto.

Após a conclusão da integração de um armazenamento, a sincronização de informações entre o [!DNL Commerce] e o Amazon é iniciada. Suas listagens do Amazon são importadas para o [!DNL Commerce] e tentam corresponder com os produtos do seu Catálogo do [!DNL Commerce].

Você pode exibir suas informações de pedido do Amazon na seção _[!UICONTROL Recent Orders]_do painel da loja. Consulte [Armazenar Painel](./amazon-store-dashboard.md) ou [Gerenciar Pedidos](./managing-orders.md).

>[!IMPORTANT]
>
>Há algumas configurações importantes da loja (listas, preços, regras, preenchimento, etc.) que têm valores padrão para uma nova loja. Para garantir que seu armazenamento esteja configurado de acordo com suas necessidades específicas, revise suas [configurações de armazenamento](./default-store-settings.md).

![Próximo ícone](assets/btn-next.png) [**Continuar com as Configurações de Armazenamento Padrão**](./default-store-settings.md)
