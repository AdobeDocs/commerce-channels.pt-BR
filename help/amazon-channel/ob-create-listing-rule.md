---
title: Criar uma regra de listagem do Amazon
description: Ao concluir o processo de integração do canal de vendas do Amazon, crie as regras de lista iniciais para gerar listas do Amazon para o seu [!DNL Commerce] produtos.
role: Admin
feature: Sales Channels, Products, Merchandising, Configuration
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Criar uma regra de listagem do Amazon

As regras de listagem podem ser definidas durante a integração, mas também podem ser modificadas a qualquer momento. Após a integração, você pode acessar o [regras de listagem](./listing-rules.md) na loja [painel](./amazon-store-dashboard.md).

## Criar uma regra de listagem durante a integração

1. Após a conexão da loja, clique em **[!UICONTROL View Store]** para o armazenamento adicionado.

   A loja [painel](./amazon-store-dashboard.md) aparece com `No products listed to Amazon` mensagem.

1. Clique em **[!UICONTROL Preview and List Eligible Products]**.

   A variável _[!UICONTROL Listing Rules]_é exibida.

1. Defina as condições desejadas para a qualificação de produtos a serem listados no Amazon e clique em **[!UICONTROL Preview changes]** ou clique em **[!UICONTROL Preview changes]** para ignorar esta etapa.

   Consulte [Exemplo: definir uma condição](./ob-define-condition-example.md).

1. Revise suas listas na Visualização da lista:

   ![Visualização da listagem](assets/amazon-ob-listing-preview.png){width="600" zoomable="yes"}

   - **[!UICONTROL Ineligible Listings]** - Os produtos listados nesta guia não estão qualificados para a lista do Amazon com base nas configurações de regra de lista atuais.

     Produtos não qualificados não são publicados no Amazon. Se um produto inelegível já estiver listado no Amazon e você corresponder a lista do Amazon ao seu [!DNL Commerce] produto de catálogo, a quantidade da lista do Amazon muda para `0` para impedir as vendas do produto. Para remover manualmente uma listagem do Amazon, consulte [Encerramento de uma listagem do Amazon](./end-listings-manually.md). Os produtos que não estão qualificados pelos requisitos do Amazon não estão listados aqui. Esses produtos estão listados no [[!UICONTROL Inactive Listings] guia](./inactive-listings.md).

     Para alterar um `Ineligible` listando em um `Eligible` listar, repita esse processo e modifique suas regras de listagem.

   - **[!UICONTROL Eligible Listings]** - Os produtos listados nesta guia são elegíveis para a lista do Amazon com base na configuração atual da regra de lista e são elegíveis pelos requisitos do Amazon. Essa guia inclui suas listagens existentes do Amazon que são importadas (se você tiver **[!UICONTROL Import Third Party Listings]** definir como `Import Listing` no seu [Configurações de listagem](./listing-settings.md)).

   - **[!UICONTROL New Listings]** - Os produtos listados nesta guia incluem o [!DNL Commerce] catalogar produtos que são recém-qualificados para a listagem do Amazon com base na configuração de sua regra de listagem atual e criar listagens do Amazon.

1. Quando terminar, clique em **[!UICONTROL Save and Close]**.

   A loja [painel](./amazon-store-dashboard.md) é aberto.

Após a conclusão da integração de um armazenamento, a sincronização de informações entre [!DNL Commerce] e o Amazon é iniciado. Suas listagens do Amazon são importadas para o [!DNL Commerce] e tente corresponder com os produtos em seu [!DNL Commerce] Catálogo.

Você pode visualizar as informações do seu pedido Amazon na _[!UICONTROL Recent Orders]_seção do painel de armazenamento. Consulte [Armazenar painel](./amazon-store-dashboard.md) ou [Gerenciar Pedidos](./managing-orders.md).

>[!IMPORTANT]
>
>Há algumas configurações importantes da loja (listas, preços, regras, preenchimento, etc.) que têm valores padrão para uma nova loja. Para garantir que sua loja esteja configurada para suas necessidades específicas, revise [configurações da loja](./default-store-settings.md) .

![Ícone Avançar](assets/btn-next.png) [**Continuar com as configurações padrão da loja**](./default-store-settings.md)
