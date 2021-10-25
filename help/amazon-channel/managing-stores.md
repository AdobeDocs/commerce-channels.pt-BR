---
title: Exibição das Amazon Stores
description: Acesse a exibição Amazon Stores para analisar rapidamente as estatísticas básicas de cada loja da Amazon e as opções de gerenciamento de acesso.
exl-id: 1376cd84-da81-4d3b-a5be-218aa802eed6
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Exibição das Amazon Stores

Ao visualizar a página inicial do canal de vendas da Amazon, a variável _Amazon Stores_ a exibição é aberta por padrão.

![Exibição das Amazon Stores](assets/amazon-sales-channel-home-tabs.png)

O _[!UICONTROL Amazon Stores]_A visualização mostra um &quot;cartão de loja&quot; para cada loja da Amazon junto com algumas estatísticas básicas e opções de gerenciamento. As informações de resumo mostradas em cada cartão incluem cada status de loja, data de criação, data da última atualização, listas que precisam de atenção (por exemplo: Listagens incompletas) e o atributo [!DNL Commerce] site.

Ao visualizar o _[!UICONTROL Amazon Store]_exibir, cada cartão de loja permite:

- Para abrir uma loja [painel](./amazon-store-dashboard.md), clique em **[!UICONTROL View Store]**.

- Para alterar o status de uma loja ou excluir uma loja, clique em **[!UICONTROL Action]** e escolha:

   - **[!UICONTROL Activate]** / **[!UICONTROL Deactivate]** - Escolha alterar o status do armazenamento para `Active` ou `Inactive`, respectivamente.

      Alteração de um `Inactive` armazenar para `Active` O status ativa as listagens e a atividade de pedido da loja, usando as configurações de armazenamento atuais da loja (como configurações de listagem, regras de preço e substituições).

      Alterar o status de uma loja de `Active` para `Inactive` status suspende as listagens e a atividade do pedido da loja. Uma Loja Inativa retém todas as configurações de armazenamento e listagens, mas interrompe temporariamente a sincronização de preços, quantidade e gerenciamento de pedidos até que a loja seja alterada de volta para `Active` status. Esse recurso permite controlar a atividade da loja no nível regional, sem a necessidade de recriar ou reintegrar a loja da Amazon ou a perda de dados históricos de pedido e vendas.

   - **[!UICONTROL Delete]** - Escolha excluir uma loja que não é mais necessária.

      Escolha quando deseja excluir uma Amazon store existente e suas configurações de integração com seu [!DNL Amazon Seller Central] conta. A exclusão da conta remove a loja do canal de vendas da Amazon, juntamente com todas as configurações da conta, listas, logs e outras informações relacionadas a essa loja. O armazenamento não pode ser recuperado após a exclusão. Um novo armazenamento deve ser criado.

>[!NOTE]
>Para alterar o site atribuído à loja durante a integração, você deve excluir a loja e adicionar a loja novamente com o site diferente definido durante a integração da loja.

| Cartão de armazenamento | Descrição |
|--- |--- |
| Seção superior | Inclui: <br>O ícone de região da loja, definido durante [integração de loja](./store-integration.md).<br> Os atributos atribuídos _[!UICONTROL Magento Website]_, definido durante a integração de loja.<br>O_[!UICONTROL Status]_ da sua loja. Opções: **[!UICONTROL Active]** - A integração da loja é concluída e verificada com o Amazon e está disponível para atividade de vendas. **[!UICONTROL Inactive]** - A integração de armazenamento está concluída, mas não está em uso ou disponível para a atividade de vendas. When `Inactive`, suas vendas da Amazon são pausadas. When `Active`, receita de vendas e configurações adicionais são salvas para atualização antes da ativação.<br>O *[!UICONTROL Last Updated]* data da alteração mais recente na configuração da loja da Amazon.<br>O *[!UICONTROL Created]* data em que a loja da Amazon foi criada no canal de vendas da Amazon. |
| Seção do meio | Inclui um gráfico resumido de atividades de loja nos últimos 30 dias e inclui e alerta para qualquer lista que precise de atenção. |
| Seção inferior | Inclui as opções Exibir armazenamento e Ação .<br>Para abrir a loja [painel](./amazon-store-dashboard.md), clique em **[!UICONTROL View Store]**.<br>Para ativar, desativar ou excluir uma loja, clique em **[!UICONTROL Actions]**. |
