---
title: "[!UICONTROL Amazon Stores] view"
description: Acesse a visualização Amazon Stores para analisar rapidamente as estatísticas básicas de cada uma das lojas Amazon e acessar as opções de gerenciamento.
exl-id: 1376cd84-da81-4d3b-a5be-218aa802eed6
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# [!UICONTROL Amazon Stores] exibir

Ao visualizar a página inicial do canal de vendas do Amazon, a variável _Lojas Amazon_ A visualização é aberta por padrão.

![Visualização Amazon Stores](assets/amazon-sales-channel-home-tabs.png){width="600" zoomable="yes"}

A variável _[!UICONTROL Amazon Stores]_A exibição do mostra um &quot;cartão de armazenamento&quot; para cada armazenamento do Amazon, juntamente com algumas opções básicas de estatística e gerenciamento. As informações resumidas mostradas em cada cartão incluem cada status de armazenamento, data de criação, data da última atualização, listagens que precisam de atenção (exemplo: Listagens incompletas) e as atribuídas [!DNL Commerce] site.

Ao visualizar a variável _[!UICONTROL Amazon Store]_exibir, cada cartão de loja permite:

- Para abrir uma loja [painel](./amazon-store-dashboard.md), clique em **[!UICONTROL View Store]**.

- Para alterar o status de um armazenamento ou excluir um armazenamento, clique em **[!UICONTROL Action]** e escolha:

   - **[!UICONTROL Activate]** / **[!UICONTROL Deactivate]** - Optar por alterar o status do armazenamento para `Active` ou `Inactive`, respectivamente.

      Alterar um `Inactive` armazenar em `Active` o status ativa as listas e a atividade de ordem para a loja, usando as configurações da loja atual (como configurações de lista, regras de preço e sobreposições).

      Alterando o status de uma loja de `Active` para `Inactive` o status suspende as listas e a atividade de pedidos da loja. Um armazenamento inativo retém todas as configurações e listas de armazenamento, mas interrompe temporariamente a sincronização de preço, quantidade e gerenciamento de pedidos até que o armazenamento seja alterado novamente para `Active` status. Esse recurso permite controlar a atividade da loja no nível Regional, sem a necessidade de recriar ou reintegrar a loja da Amazon ou a perda de dados históricos de pedidos e vendas.

   - **[!UICONTROL Delete]** - Escolha excluir um armazenamento que não é mais necessário.

      Escolha quando deseja excluir um armazenamento do Amazon existente e suas configurações de integração com o [!DNL Amazon Seller Central] conta. Excluir a conta remove a loja do canal de vendas da Amazon, juntamente com todas as configurações da conta, listas, logs e outras informações relacionadas a esta loja. O armazenamento não pode ser recuperado após a exclusão. Um novo armazenamento deve ser criado.

>[!NOTE]
>Para alterar o site atribuído ao armazenamento durante a integração, você deve excluir o armazenamento e adicionar o armazenamento novamente com o site diferente definido durante a integração do armazenamento.

| Cartão de armazenamento | Descrição |
|--- |--- |
| Seção superior | Inclui: <br>O ícone de região do armazenamento, definido durante [integração de loja](./store-integration.md).<br> O valor atribuído _[!UICONTROL Magento Website]_, definido durante a integração de lojas.<br>A variável_[!UICONTROL Status]_ da sua loja. Opções: **[!UICONTROL Active]** - A integração da loja é concluída e verificada com o Amazon e está disponível para atividade de vendas. **[!UICONTROL Inactive]** - A integração da loja foi concluída, mas não está em uso ou disponível para a atividade de vendas. Quando `Inactive`, suas vendas do Amazon estão pausadas. Quando `Active`, a receita de vendas e as configurações adicionais são salvas para atualização antes da ativação.<br>A variável *[!UICONTROL Last Updated]* data da alteração mais recente na configuração da Amazon store.<br>A variável *[!UICONTROL Created]* data em que a loja do Amazon foi criada no canal de vendas do Amazon. |
| Seção do meio | Inclui um gráfico de resumo de atividades de armazenamento dos últimos 30 dias e inclui um alerta para qualquer listagem que precise de atenção. |
| Seção inferior | Inclui as opções Exibir armazenamento e Ação.<br>Para abrir a loja [painel](./amazon-store-dashboard.md), clique em **[!UICONTROL View Store]**.<br>Para ativar, desativar ou excluir um armazenamento, clique em **[!UICONTROL Actions]**. |
