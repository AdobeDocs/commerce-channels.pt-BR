---
title: '[!DNL Amazon Sales Channel] notas de versão'
description: Revise as notas de versão para obter informações sobre todas as  [!DNL Amazon Sales Channel]  versões.
feature: Sales Channels, Release Notes
exl-id: 792782e0-9097-42f7-9fc0-509ece02e407
source-git-commit: df8bbec23d34b53a0e694c924aca5b1ed41e4d08
workflow-type: tm+mt
source-wordcount: '2010'
ht-degree: 0%

---

# Notas de versão do [!DNL Amazon Sales Channel]

>[!IMPORTANT]
>
> O [!DNL Amazon sales channel] pode ser instalado em instâncias com o Magento Open Source, Adobe Commerce e Adobe Commerce nas versões 2.3.x e 2.4.x da infraestrutura em nuvem. A extensão não é mais suportada no Adobe Commerce 2.1, Magento Open Source 2.2 ou Magento 1.
> <br>O suporte está disponível para [!DNL Amazon sales channel] versões 4.0.0 e 4.1.0 somente nas versões 2.3.x do Adobe Commerce.
> <br>[!DNL Amazon sales channel] A versão 4.2.0+ é compatível com as versões 2.3.x do Adobe Commerce, mas o suporte está disponível somente para as versões 2.4.x do Adobe Commerce.
>

Estas notas de versão descrevem a versão inicial do [!DNL Amazon sales channel] e incluem:

![Novos](../assets/new.svg) Novos recursos
![Problema corrigido](../assets/fix.svg) Correções e melhorias
![Problema conhecido](../assets/bug.svg) Problemas conhecidos

Consulte [Versões futuras](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) para obter controle de versão, suporte e compatibilidade.

Consulte [Disponibilidade do Produto](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) para saber quais versões do Adobe Commerce oferecem suporte a esta extensão.

## v4.5.0

*30 de agosto de 2023*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"}

![Novo](../assets/new.svg) Adicionado o gateway da API Adobe.IO, mudando de MAGI, para melhorar a segurança da autenticação. O `ServicesId` fornece uma nova interface para gerenciar suas credenciais de Adobe.IO, semelhante a outros [Adobe Commerce Services](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html).

>[!NOTE]
>
>Os comerciantes devem garantir que as [chaves de API privadas e públicas](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html) sejam atualizadas para produção.


![Correção de um problema](../assets/fix.svg) Identificou um problema de definição de configuração e corrigiu o fluxo de criação de ordens.

## v4.4.4

*7 de março de 2023*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"}

![Problema corrigido](../assets/fix.svg) Adição de suporte para Adobe Commerce 2.4.6 e PHP 8.2.

![Correção de um problema](../assets/fix.svg): ruído reduzido nos logs.

![Correção de um problema](../assets/fix.svg) Melhoria na estabilidade das atualizações de envio.

![Correção de um problema](../assets/fix.svg) Simplificou o processo para executar uma única extração semelhante a uma ação ou para aplicar a partir da CLI.

![Problema corrigido](../assets/fix.svg) Atualizou a dependência para `magento/services-connector`.

![Correção de um problema](../assets/fix.svg) Correção de problemas de sincronização em contas do Reino Unido com código de país inválido.

![Problema corrigido](../assets/fix.svg) O entity_type_id da entidade do produto de catálogo contém problemas com o Magento Price Source.

![Correção de um problema](../assets/fix.svg) que impedia que contas excluídas em uma infraestrutura de outra instância também fossem excluídas da interface do usuário.

![Correção de um problema](../assets/fix.svg) que corrigia um problema em que algumas regras do carrinho quebravam a importação da ordem.

## v4.4.3

*7 de março de 2023*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"}

![Correção](../assets/fix.svg) Adicionado suporte para o Adobe Commerce 2.4.4.

## v4.4.2

*11 de novembro de 2021*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"}

![Correção](../assets/fix.svg) Atualizou as dependências para dar suporte a outras extensões atualizadas.
![Correção](../assets/fix.svg) Suporte adicionado para PHP 8.1.

## v4.4.1

*11 de novembro de 2021*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"}

![Correção](../assets/fix.svg) alterada a maneira como a Adobe Commerce recebe o campo _Nome de Usuário_ da Amazon. Anteriormente, ocorria um erro durante a criação do pedido quando o campo _Nome de Usuário_ continha caracteres especiais. A Adobe Commerce agora recebe os dados do _Nome de usuário_ e filtra os caracteres especiais para que a ordem possa ser criada com êxito.

## v4.4.0

*9 de abril de 2021*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"}

![Novo](../assets/new.svg) Adicionou suporte para Modo Somente Leitura à configuração. Consulte [configurações de canal de vendas](sales-channel-settings.md).

![Correção](../assets/fix.svg) alterou o fluxo de dados para que várias cópias da mesma instância pudessem buscar atualizações simultaneamente.

![Correção](../assets/fix.svg) Alterou o processo de sincronização para sincronizar informações da conta. Adição de um trabalho cron para sincronização com a conta remota e adição da mesma funcionalidade aos comandos da CLI.

![Correção](../assets/fix.svg) Adicionados argumentos e sinalizadores de comando CLI para obter controle mais preciso.

![Correção](../assets/fix.svg) Corrigiu o Source de tarefas em segundo plano (cron) na configuração do sistema.

![Correção](../assets/fix.svg) Corrigiu o problema que impedia a criação de pedidos quando o código do país estava definido como Porto Rico (PR).

## v4.3.0

*3 de março de 2021*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"}

![Correção](../assets/fix.svg) <!--CHAN-xxxx-->O recurso _Detalhes do Pedido_ foi reprojetado e não depende mais da configuração _Importar Pedidos_. Os detalhes do pedido agora aparecem na interface do Sales Channel Amazon para todos os pedidos.

![Correção](../assets/fix.svg) No menu _[!UICONTROL Marketing]_do Administrador, o nome foi alterado de_[!UICONTROL Amazon]_ para _[!UICONTROL Amazon Sales Channel]_.

![Problema conhecido](../assets/bug.svg) **Importante**: problemas conhecidos com a compatibilidade do Adobe Commerce 2.4.0 são resolvidos na versão Adobe Commerce 2.4.1.

- Processos cron do Amazon no estado `error`
- A instalação com o Commerce 2.4.0 falha ao criar armazenamentos no banco de dados
- A criação do produto falha quando o MSI é instalado

## v4.2.0

*3 de março de 2021*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"}

Se você tiver uma versão anterior do [!DNL Amazon sales channel] instalada e tentar atualizar seu Adobe Commerce para a versão 2.4.0, será solicitado a atualizar a extensão antes de concluir a atualização do Adobe Commerce.

![Problema conhecido](../assets/bug.svg) Quando o [!DNL Amazon sales channel] 4.2.0 está integrado à versão 2.4.0 e o [Inventory management](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html?lang=en) está habilitado, há um problema conhecido que impede a adição de produtos ao catálogo do Commerce. Esse problema será abordado em uma versão futura do Commerce.

![Novo](../assets/new.svg) [!DNL Amazon sales channel] foi aprimorado para aceitar dados de endereço baseados em texto e corresponder a formatos de endereço padronizados, incluindo cidade, estado e código postal. Essa atualização permite que os dados de pedido e envio sincronizem-se (sincronizem) com o Amazon sem erros de endereço.<br/>Por exemplo, um comprador insere a cidade, o estado e o CEP como `Escondido, californiA 92025-1501`. O Amazon Sales Channel importa e faz a correspondência dos dados para o formato padrão como `Escondido, CA 92025`, e então sincroniza de volta para o Amazon nesse formato padronizado.

![Novo](../assets/new.svg) Suporte adicionado para o PHP 7.4.

![Novo](../assets/new.svg) <!--CHAN-4334-->Suporte adicionado para o Adobe Commerce 2.4.x. As versões anteriores podem ser compatíveis com o Commerce 2.4.x, mas não são compatíveis. Consulte [Próximas versões](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) para obter compatibilidade de versão. O Sales Channel Amazon deve ser atualizado para 4.2.0 antes que a atualização 2.4.0 do Adobe Commerce possa ser concluída.

![Correção](../assets/fix.svg) <!--CHAN-4431-->Corrigiu um problema que causava um erro de _Acesso Negado_ para clientes do Reino Unido.

![Correção](../assets/fix.svg) <!--CHAN-4394-->Corrigido um problema que impedia que o status de envio da Amazon fosse sincronizado com o pedido correspondente do Commerce, &quot;bloqueando&quot; o status de envio do pedido como `Pending` no Commerce e `Unshipped` no Amazon. Com o novo recurso de endereço padronizado, esses erros de status do delivery foram resolvidos.

![Correção](../assets/fix.svg) <!--ticket#-->A sincronização de ordem (sincronização) foi atualizada para ignorar importações de ordem com falha, reduzindo assim várias tentativas de sincronização e permitindo o processamento de importações subsequentes, com solicitações de sincronização de ordem enviadas a cada cinco minutos. Os erros de sincronização ainda são registrados no log de erros, mas marcados como &quot;processados&quot; para permitir outras funções de log. Além disso, o [!DNL Amazon sales channel] agora remove automaticamente os dados em excesso coletados para pedidos que não são criados no Commerce.

![Correção](../assets/fix.svg) O log de erros foi atualizado para coletar mais informações sobre erros de exceção e atualização de extensão não detectados.

![Correção](../assets/fix.svg) <!--ticket#-->Corrigiu um problema que causava a falha da sincronização inicial dos dados _preço mais baixo_ devido a um valor _preço_ ausente.

![Correção](../assets/fix.svg) <!--CHAN-4410-->Correção de problemas que causavam erros de filtragem na exibição _Pedidos de Amazon_ quando o campo de intervalo de datas é deixado em branco.

![Correção](../assets/fix.svg) <!--CHAN-4439-->Corrigiu um problema que causava erros de sincronização de estoque e atendimento relacionados à quantidade. A extensão agora arredonda para baixo os valores de quantidade inseridos como decimais antes de sincronizar com o Amazon.<br/> Por exemplo, quando um comerciante insere manualmente uma quantidade de `2.5`, a extensão arredonda o valor para baixo para `2` e sincroniza a quantidade atualizada com o Amazon.

## v4.1.0

*7 de maio de 2020*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"}

![Novo](../assets/new.svg) <!--4247, 4230-->Alterou o processo de importação de pedidos para alinhar-se aos requisitos de pedidos do Commerce. Essas alterações corrigem problemas que impediam o Commerce de criar o pedido correspondente a um pedido importado. Consulte [Gerenciar pedidos](managing-orders.md) para obter informações sobre bloqueadores de pedidos e soluções.

![Novo](../assets/new.svg) <!--CHAN-CHAN-4167, 4297, 4311, 4312, 4324-->Atualizou a seção _Pedidos recentes_ do painel da loja e adicionou uma nova exibição _Todos os pedidos_ que mostra todos os seus pedidos da Amazon, incluindo opções de filtro e paginação para exibir mais pedidos. Consulte [Painel da Amazon Store](amazon-store-dashboard.md) e [Exibir Pedidos do Amazon](amazon-orders-all.md).

![Novo](../assets/new.svg) Adicionada a coluna _[!UICONTROL Order Notes]_da tabela_[!UICONTROL Amazon Orders]_ reprojetada nas exibições _[!UICONTROL Recent Orders]_e_[!UICONTROL All Orders]_. _[!UICONTROL Order Notes]_informe ao comerciante que há um problema com a importação do pedido. Consulte [Exibir Pedidos Do Amazon](amazon-orders-all.md).

![Novo](../assets/new.svg) <!--CHAN-4013-->Os parâmetros de condição do produto foram atualizados para alinhar-se ao programa [Amazon Renovado](https://sell.amazon.com/programs/renewed). Consulte [Produtos renovados](renewed-products.md).

![Novo](../assets/new.svg) <!--CHAN-3680-->Atualização de [Detalhes de Pedidos da Amazon](amazon-order-details.md) para incluir &quot;dados genéricos&quot; para pedidos que são atendidos pela Amazon. Consulte [Preenchido por](fulfilled-by.md).

![Correção](../assets/fix.svg) <!--CHAN-4069-->Corrigiu um problema que causava a distorção de ícones no cartão de memória.

![Correção](../assets/fix.svg) <!--CHAN-4165-->Corrigido um erro que impedia que a tela _Logon_ aparecesse depois que a sessão expirasse.

![Correção](../assets/fix.svg) <!--CHAN-4211-->Corrigido um problema que impedia que o valor de imposto da ordem do Amazon fosse importado para a nova ordem do Commerce.

![Correção](../assets/fix.svg) <!--CHAN-4234-->Corrigiu um problema que fazia com que os totais de receita exibidos no painel da loja incluíssem pedidos no status `Canceled` ou `Error`.

![Correção](../assets/fix.svg) <!--CHAN-4326-->Corrigido um problema que causava erros de importação de pedidos associados a extensões de terceiros que usam métodos _Magento Shipping_ para criar pedidos.

![Correção](../assets/fix.svg) <!--CHAN-4357-->Corrigiu um problema que causava erros ao executar a sincronização CRON. Um bloqueio foi adicionado ao comando da CLI que impede que dois trabalhos cron sejam sincronizados ao mesmo tempo.

![Correção](../assets/fix.svg) Atualizada a política de segurança de conteúdo para suporte ao Commerce versão 2.3.5.

## v4.0.0

*25 de março de 2020*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"}

>[!IMPORTANT]
>
>O Sales Channel Amazon 4.0.0 não é compatível com o Adobe Commerce 2.3.5. Para obter suporte com o Adobe Commerce 2.3.5, atualize para o Amazon Sales Channel 4.1.0.

![Novo](../assets/new.svg) Apresentou uma nova página inicial do [Sales Channel do Amazon](amazon-sales-channel-home.md) com uma &quot;exibição de cartão&quot; aprimorada para suas informações de loja.

![Novo](../assets/new.svg) Apresentado um novo [painel de armazenamento](amazon-store-dashboard.md) com listagem, pedidos recentes e informações de configuração de armazenamento.

![Novo](../assets/new.svg) Introduziu um [processo de integração](amazon-onboarding-home.md) mais simples e simplificado[configurações padrão do armazenamento](default-store-settings.md) para integrar suas lojas com mais rapidez.

![Problema conhecido](../assets/bug.svg) <!--CHAN-4102--> Quando [criar atributos](managing-attributes.md) para importar imagens de listas e **Modos de Exibição de Armazenamento** está definido como `All Store Views (Global)`, existe um problema conhecido que impede as imagens de serem importadas para todos os modos de exibição de armazenamento. Se você alterar a configuração de **Exibições de Armazenamento (para importar valores)** para um armazenamento específico, as imagens serão importadas para esse armazenamento.

## v3.0.1

*11 de novembro de 2019*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"}

![Correção](../assets/fix.svg) **Configurações de Campo Numérico**: <!--CHAN-3779-->Os campos que exigem um valor baseado em numérico foram atualizados para aceitar apenas caracteres numéricos. Exemplo: Configurações da Regra de Precificação > campo Quantia de Ajuste

![Correção](../assets/fix.svg) **Links do Guia do Usuário**: <!--CHAN-3778-->Links incorretos do _Guia do Usuário_ foram corrigidos.

![Correção](../assets/fix.svg) **Duplicar Listagens do Amazon**: <!--CHAN-3593-->Um problema relatado anteriormente que causa listagens duplicadas do Amazon foi corrigido. Antes desta versão, a extensão adicionava o Código do país da região do Amazon aos valores de SKU ao importar listas. A lista correspondia ao item de catálogo, mas a extensão criou uma lista nova e duplicada com o SKU anexado. Com esta versão, a extensão não modifica o SKU de listas importadas e nenhuma alteração é feita nas listas existentes. Você pode usar a opção [!UICONTROL End Listing(s)] no Amazon para remover listagens duplicadas.

## v3.0.0

*7 de outubro de 2019*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"}

![Novo](../assets/new.svg) **Amazon UK Marketplace Agora Disponível**: os usuários podem escolher o marketplace do Reino Unido ao criar e integrar uma loja da Commerce. Esta atualização do Reino Unido inclui suporte adicional para:

- [Serviço de Cálculo de IVA da Amazon](https://sell.amazon.co.uk/learn/vat-resources){target="_blank"}

- Informações de [Código de Imposto do Produto](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}.

![Novo](../assets/new.svg) **Log aprimorado**: <!--CHAN-3642, 3672-->Implementou o recurso **Habilitar Log de Depuração** para coletar dados de sincronização adicionais quando a solução de problemas for necessária. Consulte o tópico [Configurações do Sales Channel](https://experienceleague.adobe.com/docs/commerce-admin/config/sales-channels.html) na referência de configuração.

![Correção](../assets/fix.svg) **Catálogo de Produtos**: <!--CHAN-3687-->Correção de um problema que impedia que imagens importadas com uma listagem Amazon fossem aplicadas ao produto de catálogo Commerce correspondente.

![Correção](../assets/fix.svg) **Criação de pedido**: <!--CHAN-3708-->Corrigido um problema que impedia a Commerce de criar pedidos para um pedido da Amazon que não correspondesse a um produto de catálogo da Commerce.

![Problema conhecido](../assets/bug.svg) **Duplicar Listagens do Amazon**: <!--CHAN-3593-->Esse problema faz com que o catálogo crie um item para uma listagem importada, usando o mesmo SKU, mas com um código de região adicionado ao final. Em seguida, o Amazon processa o SKU modificado como um novo item e cria uma lista. Esse problema será resolvido em uma versão futura.

## v2.0.0

[!BADGE Com suporte]{type=Informative tooltip="Compatível"}

>[!NOTE]
>
>A versão 1.0.0 estava disponível somente na versão limitada.

![Novo](../assets/new.svg) **Integração e manutenção simplificadas**: adicione e integre com sua conta de vendedor da Amazon por meio de um processo passo a passo com instruções detalhadas disponíveis por meio do Administrador. Mantenha suas lojas, contas e produtos listados por meio de um painel.

![Novo](../assets/new.svg) **Suporte a várias contas**: gerencie e monitore várias marcas de Amazon e regiões de marketplace por meio do Administrador.

![Novo](../assets/new.svg) **Preço inteligente**: defina regras de reavaliação de preço automatizadas para aumentar suas chances para o Buy Box cobiçado. Defina os preços para ajustar dinamicamente ao preço de Buy Box atual ou ao preço mais baixo do concorrente. Defina limites para reprecificação para proteger sua margem.

![Novo](../assets/new.svg) **Gerenciamento de listagem**: automatize as listagens de produtos e sincronize seu catálogo do Commerce com o Amazon Marketplace usando as regras de listagem. Adicione substituições específicas para controlar com precisão suas ofertas. Monitore e gerencie todas as suas listagens diretamente do Administrador.

![Novo](../assets/new.svg) **Inventory management consistente**: mantenha as quantidades de estoque da Commerce e da Amazon em sincronização constante.

![Novo](../assets/new.svg) **Gerenciamento de Pedidos e Atendimento**: controle pedidos da Amazon através do painel, com comunicação contínua e atualizações de inventário. Complete e rastreie as entregas da ordem como atendidas pela Amazon, atendidas pelo comerciante ou uma combinação de métodos.

![Problema conhecido](../assets/bug.svg) Talvez você encontre tempos de espera mais longos para atualizar quantidades de produtos. As atualizações da quantidade de produtos podem levar aproximadamente duas horas para serem sincronizadas.

![Problema conhecido](../assets/bug.svg) Pedidos importados podem ter um tipo de _Pedido principal_ ou _Pedido principal_. Você deve verificar esses pedidos em sua conta de vendedor da Amazon.

![Problema conhecido](../assets/bug.svg) Produtos agrupados inelegíveis podem ser exibidos como Qualificados para listagem no Amazon. Um dos produtos no produto agrupado pode não ser elegível. Se encontrar problemas, verifique o status de qualificação dos itens de produtos agrupados.

![Problema conhecido](../assets/bug.svg) Ao usar o Inventory management para Commerce 2.3.x, uma reindexação parcial de estoque pode não ser acionada quando um pedido é criado. A quantidade vendável recalcula por hora, o que pode causar venda excessiva durante esse intervalo de atualização.
