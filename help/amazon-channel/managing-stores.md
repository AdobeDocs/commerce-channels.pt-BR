---
title: "[!UICONTROL Amazon Stores] exibição"
description: Acesse a visualização Amazon Stores para analisar rapidamente as estatísticas básicas de cada uma das lojas Amazon e acessar as opções de gerenciamento.
feature: Sales Channels, Storefront
exl-id: 1376cd84-da81-4d3b-a5be-218aa802eed6
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# Visualização [!UICONTROL Amazon Stores]

Ao exibir a home page do canal de vendas do Amazon, a exibição _Amazon Stores_ é aberta por padrão.

![Exibição das lojas Amazon](assets/amazon-sales-channel-home-tabs.png){width="600" zoomable="yes"}

A exibição _[!UICONTROL Amazon Stores]_mostra um &quot;cartão de loja&quot; para cada loja da Amazon, juntamente com algumas opções básicas de estatística e gerenciamento. As informações de resumo mostradas em cada cartão incluem cada status de armazenamento, data de criação, data da última atualização, listagens que precisam de atenção (exemplo: Listagens Incompletas) e o site [!DNL Commerce] atribuído.

Ao exibir a exibição _[!UICONTROL Amazon Store]_, cada cartão de loja permite:

- Para abrir um [painel](./amazon-store-dashboard.md) de armazenamento, clique em **[!UICONTROL View Store]**.

- Para alterar o status de um armazenamento ou excluir um armazenamento, clique em **[!UICONTROL Action]** e escolha:

   - **[!UICONTROL Activate]** / **[!UICONTROL Deactivate]** - Escolha alterar o status do armazenamento para `Active` ou `Inactive`, respectivamente.

     A alteração do status de um armazenamento `Inactive` para `Active` ativa as listas e a atividade de pedido do armazenamento, usando as configurações de armazenamento atuais do armazenamento (como configurações de listagem, regras de preço e substituições).

     A alteração do status de um armazenamento de `Active` para `Inactive` suspende as listagens e a atividade do pedido do armazenamento. Um armazenamento inativo retém todas as configurações e listagens de armazenamento, mas interrompe temporariamente a sincronização de preço, quantidade e gerenciamento de pedidos até que o armazenamento seja alterado de volta para o status `Active`. Esse recurso permite controlar a atividade da loja no nível Regional, sem a necessidade de recriar ou reintegrar a loja da Amazon ou a perda de dados históricos de pedidos e vendas.

   - **[!UICONTROL Delete]** - Escolha excluir um armazenamento que não é mais necessário.

     Escolha quando deseja excluir um armazenamento do Amazon existente e suas configurações de integração com a conta [!DNL Amazon Seller Central]. Excluir a conta remove a loja do canal de vendas da Amazon, juntamente com todas as configurações da conta, listas, logs e outras informações relacionadas a esta loja. O armazenamento não pode ser recuperado após a exclusão. Um novo armazenamento deve ser criado.

>[!NOTE]
>Para alterar o site atribuído ao armazenamento durante a integração, você deve excluir o armazenamento e adicionar o armazenamento novamente com o site diferente definido durante a integração do armazenamento.

| Cartão de armazenamento | Descrição |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Seção superior | Inclui: <br>O ícone de região do armazenamento, definido durante a [integração de armazenamento](./store-integration.md).<br> O _[!UICONTROL Magento Website]_atribuído, definido durante a integração de armazenamento.<br>O_[!UICONTROL Status]_ de seu armazenamento. Opções: **[!UICONTROL Active]** - A integração da loja foi concluída e verificada com o Amazon e está disponível para atividade de vendas. **[!UICONTROL Inactive]** - A integração da loja foi concluída, mas não está em uso ou disponível para a atividade de vendas. Quando `Inactive`, suas vendas do Amazon são pausadas. Quando `Active`, a receita de vendas e as configurações adicionais são salvas para atualização antes da ativação.<br>A data *[!UICONTROL Last Updated]* da alteração mais recente na configuração da loja do Amazon.<br>A data *[!UICONTROL Created]* quando a loja do Amazon foi criada no canal de vendas do Amazon. |
| Seção do meio | Inclui um gráfico de resumo de atividades de armazenamento dos últimos 30 dias e inclui um alerta para qualquer listagem que precise de atenção. |
| Seção inferior | Inclui as opções Exibir armazenamento e Ação.<br>Para abrir o [painel](./amazon-store-dashboard.md) do armazenamento, clique em **[!UICONTROL View Store]**.<br>Para ativar, desativar ou excluir um armazenamento, clique em **[!UICONTROL Actions]**. |
