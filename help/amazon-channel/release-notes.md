---
title: '[!DNL Amazon Sales Channel] Notas de versão'
description: Revise as notas de versão para obter informações sobre tudo [!DNL Amazon Sales Channel] versões.
exl-id: 792782e0-9097-42f7-9fc0-509ece02e407
source-git-commit: 10d88821deabbd7481b74f21a5196d0ec1808f9a
workflow-type: tm+mt
source-wordcount: '2258'
ht-degree: 0%

---

# Notas de versão

>[!IMPORTANT]
>
> [!DNL Amazon sales channel] O pode ser instalado em instâncias com o Magento Open Source, Adobe Commerce e Adobe Commerce nas versões 2.3.x e 2.4.x da infraestrutura em nuvem. A extensão não é mais suportada no Adobe Commerce 2.1, Magento Open Source 2.2 ou Magento 1.
> <br>Suporte disponível para [!DNL Amazon sales channel]  versões 4.0.0 e 4.1.0 somente no Adobe Commerce 2.3.x.
> <br>[!DNL Amazon sales channel] A versão 4.2.0+ é compatível com as versões 2.3.x do Adobe Commerce, mas o suporte está disponível somente para as versões 2.4.x do Adobe Commerce.

Estas notas de versão descrevem a versão inicial do [!DNL Amazon sales channel] e incluem:

![Novo](../assets/new.svg) Novos recursos
![Problema corrigido](../assets/fix.svg) Correções e aprimoramentos
![Problema conhecido](../assets/bug.svg) Problemas conhecidos

Consulte [Versões futuras](https://devdocs.magento.com/release/){target="_blank"} para controle de versão, suporte e compatibilidade.

## v4.4.4

[!DNL Amazon sales channel]  O 4.4.4 é compatível com as versões 2.3.x e 2.4.0 do Adobe Commerce, mas só é compatível com as versões 2.4.1+, do Magento Open Source, Adobe Commerce e Adobe Commerce na infraestrutura em nuvem.

![Problema corrigido](../assets/fix.svg) Suporte adicionado para Adobe Commerce 2.4.6 e PHP 8.2.

![Problema corrigido](../assets/fix.svg) Ruído reduzido nos registros.

![Problema corrigido](../assets/fix.svg) Melhoria na estabilidade das atualizações de envio.

![Problema corrigido](../assets/fix.svg) Simplificou o processo para executar uma única extração semelhante a uma ação ou para aplicar a partir da CLI.

![Problema corrigido](../assets/fix.svg) Atualização da dependência para `magento/services-connector`.

![Problema corrigido](../assets/fix.svg) Correção de problemas de sincronização em contas do Reino Unido com código de país inválido.

![Problema corrigido](../assets/fix.svg) A entity_type_id codificada para a entidade de produto de catálogo causa problemas com a Origem de Preço de Magento.

![Problema corrigido](../assets/fix.svg) Correção de um problema que impedia que contas excluídas em um backend de outra instância também fossem excluídas da interface do usuário.

![Problema corrigido](../assets/fix.svg) Correção de um problema em que algumas regras do carrinho quebravam a importação de ordem.

## v4.4.3

[!DNL Amazon sales channel]  O 4.4.3 é compatível com as versões 2.3.x e 2.4.0 do Adobe Commerce, mas só é compatível com as versões 2.4.1+, do Magento Open Source, Adobe Commerce e Adobe Commerce na infraestrutura em nuvem.

Esta versão do [!DNL Amazon sales channel] inclui a seguinte correção.

![Correção](../assets/fix.svg) Adição de suporte para o Adobe Commerce 2.4.4.

## v4.4.2

[!DNL Amazon sales channel]  O 4.4.2 é compatível com as versões 2.3.x e 2.4.0 do Adobe Commerce, mas só é compatível com as versões 2.4.1+, do Magento Open Source, Adobe Commerce e Adobe Commerce na infraestrutura em nuvem.

Esta versão do [!DNL Amazon sales channel] O inclui as seguintes correções.

![Correção](../assets/fix.svg) Dependências atualizadas para oferecer suporte a outras extensões atualizadas.
![Correção](../assets/fix.svg) Adição de suporte para PHP 8.1.

## v4.4.1

[!DNL Amazon sales channel] O 4.4.1 é compatível com as versões 2.3.x e 2.4.0 do Adobe Commerce, mas só é compatível com as versões 2.4.1+, do Magento Open Source, Adobe Commerce e Adobe Commerce na infraestrutura em nuvem.

Esta versão do [!DNL Amazon sales channel]  inclui a seguinte correção.

![Correção](../assets/fix.svg) Alteração na forma como a Adobe Commerce recebe a _Nome do usuário_ do Amazon. Anteriormente, ocorria um erro durante a criação do pedido quando o _Nome do usuário_ o campo continha caracteres especiais. A Adobe Commerce agora recebe a _Nome do usuário_ Os dados do e do filtram os caracteres especiais para que a ordem possa ser criada com sucesso.

## v4.4.0

[!DNL Amazon sales channel] O 4.4.0 é compatível com as versões 2.3.x e 2.4.0 do Adobe Commerce, mas só é compatível com as versões 2.4.1+, do Magento Open Source, Adobe Commerce e Adobe Commerce na infraestrutura em nuvem.

Esta versão do [!DNL Amazon sales channel] O inclui os seguintes aprimoramentos e correções.

![Novo](../assets/new.svg) Adição do suporte para o Modo somente leitura na configuração. Consulte [configurações de canal de vendas](sales-channel-settings.md).

![Correção](../assets/fix.svg) Alterado o fluxo de dados para que várias cópias da mesma instância possam buscar atualizações simultaneamente.

![Correção](../assets/fix.svg) Alteração do processo de sincronização para sincronizar informações da conta. Adição de um trabalho cron para sincronização com a conta remota e adição da mesma funcionalidade aos comandos da CLI.

![Correção](../assets/fix.svg) Adição de argumentos e flags de comando CLI para obter controle mais preciso.

![Correção](../assets/fix.svg) Correção da origem das tarefas em segundo plano (cron) na configuração do sistema.

![Correção](../assets/fix.svg) Correção do problema que impedia a criação de pedidos quando o código do país era definido como Porto Rico (PR).

## v4.3.0

[!DNL Amazon sales channel] O 4.3.0 é compatível com as versões 2.3.x e 2.4.0 do Adobe Commerce. O suporte está disponível somente para as versões 2.4.1+, do Magento Open Source, Adobe Commerce e Adobe Commerce na infraestrutura em nuvem.

Esta versão do [!DNL Amazon sales channel] O inclui os seguintes aprimoramentos e correções.

![Correção](../assets/fix.svg) <!--CHAN-xxxx-->A variável _Detalhes do pedido_ recurso foi reprojetado e não depende mais do _Importar Ordens_ configuração. Os detalhes do pedido agora aparecem na interface do Sales Channel Amazon para todos os pedidos.

![Correção](../assets/fix.svg) No _[!UICONTROL Marketing]_no Admin, o nome foi alterado de_[!UICONTROL Amazon]_ para _[!UICONTROL Amazon Sales Channel]_.

![Problema conhecido](../assets/bug.svg) **Importante**: os problemas conhecidos com a compatibilidade do Adobe Commerce 2.4.0 são resolvidos na versão 2.4.1 do Adobe Commerce.

- Processos cron do Amazon em `error` state
- A instalação com o Commerce 2.4.0 falha ao criar lojas no banco de dados
- A criação do produto falha quando o MSI é instalado

## v4.2.0

[!DNL Amazon sales channel] A 4.2.0 é compatível com o Adobe Commerce versão 2.3.x, mas é compatível apenas com as versões 2.4.x do Magento Open Source, Adobe Commerce e Adobe Commerce na infraestrutura em nuvem. Se você tiver uma [!DNL Amazon sales channel] versão instalada e tentar atualizar seu Adobe Commerce para a versão 2.4.0, você será solicitado a atualizar a extensão antes de concluir a atualização do Adobe Commerce.

Esta versão do [!DNL Amazon sales channel] O inclui um novo recurso, juntamente com melhorias e correções.

![Problema conhecido](../assets/bug.svg) Quando [!DNL Amazon sales channel] O 4.2.0 é integrado à versão 2.4.0 e [Inventory management](https://docs.magento.com/user-guide/catalog/inventory.html) estiver ativado, há um problema conhecido que impede a adição de produtos no catálogo do Commerce. Esse problema será resolvido em uma versão futura do Commerce.

![Novo](../assets/new.svg) [!DNL Amazon sales channel] O foi aprimorado para aceitar dados de endereço baseados em texto e correspondê-los a formatos de endereço padronizados, incluindo cidade, estado e código postal. Essa atualização permite que os dados de pedido e envio sincronizem-se (sincronizem) com o Amazon sem erros de endereço.<br/>Por exemplo, um comprador insere a cidade, o estado, o CEP como `Escondido, californiA 92025-1501`. O Sales Channel Amazon importa e faz a correspondência dos dados no formato padrão como `Escondido, CA 92025`, e sincroniza de volta ao Amazon nesse formato padronizado.

![Novo](../assets/new.svg) Suporte adicionado para o PHP 7.4.

![Novo](../assets/new.svg) <!--CHAN-4334-->Adição de suporte para o Adobe Commerce 2.4.x. As versões anteriores podem ser compatíveis com o Commerce 2.4.x, mas não são compatíveis. Consulte [Versões futuras](https://devdocs.magento.com/release/){:target=&quot;_blank&quot;} para compatibilidade de versão. O Sales Channel Amazon deve ser atualizado para 4.2.0 antes que a atualização 2.4.0 do Adobe Commerce possa ser concluída.

![Correção](../assets/fix.svg) <!--CHAN-4431-->Correção de um problema que causava uma _Acesso negado_ erro para clientes do Reino Unido.

![Correção](../assets/fix.svg) <!--CHAN-4394-->Correção de um problema que impedia a sincronização do status de envio do Amazon com a ordem do Commerce correspondente, &quot;bloqueando&quot; o status de envio da ordem como `Pending` no Commerce e `Unshipped` no Amazon. Com o novo recurso de endereço padronizado, esses erros de status do delivery foram resolvidos.

![Correção](../assets/fix.svg) <!--ticket#-->Sincronização de pedido atualizada para ignorar importações de pedido com falha, reduzindo assim várias tentativas de sincronização e permitindo o processamento de importações subsequentes, com solicitações de sincronização de pedido enviadas a cada cinco minutos. Os erros de sincronização ainda são registrados no log de erros, mas marcados como &quot;processados&quot; para permitir outras funções de log. Além disso, [!DNL Amazon sales channel] O agora remove automaticamente os dados em excesso coletados para pedidos que não são criados no Commerce.

![Correção](../assets/fix.svg) Atualização do registro de erros para coletar mais informações sobre erros de exceção não detectados e de atualização de extensão.

![Correção](../assets/fix.svg) <!--ticket#-->Correção de um problema que causava a sincronização inicial do _preço mais baixo_ dados a falharem devido a uma falha _preço_ valor.

![Correção](../assets/fix.svg) <!--CHAN-4410-->Correção de problemas que causavam erros de filtragem no _Pedidos do Amazon_ exibir quando o campo de intervalo de datas é deixado em branco.

![Correção](../assets/fix.svg) <!--CHAN-4439-->Correção de um problema que causava erros de sincronização de estoque e atendimento relacionados à quantidade. A extensão agora arredonda para baixo os valores de quantidade inseridos como decimais antes de sincronizar com o Amazon.<br/> Por exemplo, quando um comerciante insere manualmente uma quantidade de `2.5`, a extensão arredonda o valor para baixo para `2` e sincroniza a quantidade atualizada com o Amazon.

## v4.1.0

O Amazon Sales Channel 4.1.0 é compatível com o Adobe Commerce 2.3.x de Commerce Open Source, Adobe Commerce e Adobe Commerce na infraestrutura em nuvem. Essa versão do Sales Channel Amazon inclui aprimoramentos na interface do usuário, juntamente com pequenas correções de erros.

![Novo](../assets/new.svg) <!--4247, 4230-->Alteração do processo de importação de ordem para alinhar-se aos requisitos de ordem do Commerce. Essas alterações corrigem problemas que impediam o Commerce de criar a ordem correspondente para uma ordem importada. Consulte [Gerenciar Pedidos](managing-orders.md) para obter informações sobre bloqueadores de pedidos e soluções.

![Novo](../assets/new.svg) <!--CHAN-CHAN-4167, 4297, 4311, 4312, 4324-->Atualização do _Pedidos recentes_ do painel de armazenamento e adicionou um novo _Todos os pedidos_ exibição que mostra todos os seus pedidos do Amazon, incluindo opções de filtro e paginação para exibir mais pedidos. Consulte [Painel da Amazon Store](amazon-store-dashboard.md) e [Exibir Pedidos do Amazon](amazon-orders-all.md).

![Novo](../assets/new.svg) Adição de _[!UICONTROL Order Notes]_coluna do projeto reprojetado_[!UICONTROL Amazon Orders]_ tabela em ambos _[!UICONTROL Recent Orders]_e_[!UICONTROL All Orders]_ exibições. _[!UICONTROL Order Notes]_informe ao comerciante que há um problema com a importação do pedido. Consulte [Exibir Pedidos do Amazon](amazon-orders-all.md).

![Novo](../assets/new.svg) <!--CHAN-4013-->Atualização dos parâmetros de condição do produto para alinhar-se à [Amazon renovado](https://sell.amazon.com/programs/renewed) programa. Consulte [Produtos renovados](renewed-products.md).

![Novo](../assets/new.svg) <!--CHAN-3680-->Atualizado [Detalhes do pedido Amazon](amazon-order-details.md) para incluir &quot;dados genéricos&quot; para pedidos atendidos pela Amazon. Consulte [Preenchido por](fulfilled-by.md).

![Correção](../assets/fix.svg) <!--CHAN-4069-->Correção de um problema que causava a distorção de ícones no cartão de memória.

![Correção](../assets/fix.svg) <!--CHAN-4165-->Correção de um erro que impedia a _Logon_ tela de aparecimento depois que a sessão expirar.

![Correção](../assets/fix.svg) <!--CHAN-4211-->Correção de um problema que impedia que a quantia de imposto da ordem do Amazon fosse importada para a nova ordem do Commerce.

![Correção](../assets/fix.svg) <!--CHAN-4234-->Correção de um problema que fazia com que os totais de receita exibidos no painel da loja incluíssem pedidos em `Canceled` ou `Error` status.

![Correção](../assets/fix.svg) <!--CHAN-4326-->Correção de um problema que causava erros de importação de pedido associados a extensões de terceiros que usam o _Magento Shipping_ métodos para criar pedidos.

![Correção](../assets/fix.svg) <!--CHAN-4357-->Correção de um problema que causava erros ao executar a sincronização cron. Um bloqueio foi adicionado ao comando da CLI que impede que dois trabalhos cron sejam sincronizados ao mesmo tempo.

![Correção](../assets/fix.svg) Atualização da política de segurança de conteúdo para oferecer suporte ao Commerce versão 2.3.5.

## v4.0.0

O Amazon Sales Channel 4.0.0 é compatível com as versões 2.3.0, 2.3.1, 2.3.2, 2.3.3 e 2.3.4 do Magento Open Source, Adobe Commerce e Adobe Commerce na infraestrutura em nuvem. Essa versão do Sales Channel Amazon inclui muitas atualizações na interface do usuário, juntamente com pequenas correções de erros.

>[!IMPORTANT]
>
>O Sales Channel Amazon 4.0.0 não é compatível com o Adobe Commerce 2.3.5. Para obter suporte com o Adobe Commerce 2.3.5, atualize para o Amazon Sales Channel 4.1.0.

![Novo](../assets/new.svg) Introduziu um novo [Sales Channel Amazon](amazon-sales-channel-home.md) página inicial com &quot;exibição de cartão&quot; aprimorada para informações da loja.

![Novo](../assets/new.svg) Introduziu um novo [painel de armazenamento](amazon-store-dashboard.md) com as informações de listagem, pedidos recentes e configuração de loja.

![Novo](../assets/new.svg) Introduziu uma abordagem mais simples e [processo de integração](amazon-onboarding-home.md) e [configurações de loja padrão](default-store-settings.md) para integrar suas lojas com mais rapidez.

![Problema conhecido](../assets/bug.svg) <!--CHAN-4102--> Quando [criação de atributos](managing-attributes.md) para importar imagens de listagens e **Armazenar visualizações** está definida como `All Store Views (Global)`, um problema conhecido impede que imagens sejam importadas para todas as exibições de loja. Se você alterar a configuração de **Exibições de armazenamento (para importar valores)** para um armazenamento específico, as imagens são importadas para esse armazenamento.

## v3.0.1

O Amazon Sales Channel 3.0.1 é compatível com as versões 2.2.4+ e 2.3.x do Adobe Commerce do Magento Open Source, Adobe Commerce e Adobe Commerce na infraestrutura em nuvem.

![Correção](../assets/fix.svg) **Configurações do campo numérico**: <!--CHAN-3779-->Os campos que exigem um valor baseado em numérico foram atualizados para aceitar apenas caracteres numéricos. Exemplo: Configurações da Regra de Precificação > campo Quantia de Ajuste

![Correção](../assets/fix.svg) **Links do guia do usuário**: <!--CHAN-3778-->Incorreto _Guia do usuário_ Os links foram corrigidos.

![Correção](../assets/fix.svg) **Listagens de Amazon Duplicadas**: <!--CHAN-3593-->Um problema relatado anteriormente que causava listagens duplicadas do Amazon foi corrigido. Antes desta versão, a extensão adicionava o Código do país da região do Amazon aos valores de SKU ao importar listas. A lista correspondia ao item de catálogo, mas a extensão criou uma lista nova e duplicada com o SKU anexado. Com esta versão, a extensão não modifica o SKU de listas importadas e nenhuma alteração é feita nas listas existentes. Você pode usar o [!UICONTROL End Listing(s)] opção on Amazon para remover listagens duplicadas.

## v3.0.0

O Amazon Sales Channel 3.0.0 é compatível com as versões 2.2.4+ e 2.3.x do Adobe Commerce do Magento Open Source, Adobe Commerce e Adobe Commerce na infraestrutura em nuvem.

![Novo](../assets/new.svg) **Amazon UK Marketplace Agora Disponível**: os usuários podem escolher o marketplace do Reino Unido ao criar e integrar uma loja de Commerce. Esta atualização do Reino Unido inclui suporte adicional para:

- [Serviço de Cálculo de IVA da Amazon](https://sell.amazon.co.uk/learn/vat-resources){target="_blank"}

- [Código de imposto do produto](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"} informações.

![Novo](../assets/new.svg) **Registro aprimorado**: <!--CHAN-3642, 3672-->Implementou o **Habilitar o log de depuração** recurso para coletar dados adicionais de sincronização quando a solução de problemas for necessária. Consulte a [Configurações do Sales Channel](https://docs.magento.com/user-guide/configuration/sales-channels/global-settings.html) tópico na Referência de configuração.

![Correção](../assets/fix.svg) **Catálogo de produtos**: <!--CHAN-3687-->Correção de um problema que impedia que imagens importadas com uma listagem do Amazon fossem aplicadas ao produto de catálogo do Commerce correspondente.

![Correção](../assets/fix.svg) **Criação do pedido**: <!--CHAN-3708-->Correção de um problema que impedia o Commerce de criar pedidos para um pedido do Amazon que não correspondia a um produto de catálogo do Commerce.

![Problema conhecido](../assets/bug.svg) **Listagens de Amazon Duplicadas**: <!--CHAN-3593-->Esse problema faz com que o catálogo crie um item para uma lista importada, usando o mesmo SKU, mas com um código de região adicionado no final. Em seguida, o Amazon processa o SKU modificado como um novo item e cria uma lista. Esse problema será resolvido em uma versão futura.

## v2.0.0

O Amazon Sales Channel 2.0.0 é compatível com as versões 2.2.4+ e 2.3.x do Magento Open Source, Adobe Commerce e Adobe Commerce na infraestrutura em nuvem.

>[!NOTE]
>
>A versão 1.0.0 estava disponível somente na versão limitada.

![Novo](../assets/new.svg)  **Integração e manutenção simplificadas**: adicione e integre com sua conta de vendedor do Amazon por meio de um processo passo a passo com instruções detalhadas disponíveis por meio do administrador. Mantenha suas lojas, contas e produtos listados por meio de um painel.

![Novo](../assets/new.svg)  **Suporte a várias contas**: gerencie e monitore várias marcas e regiões de marketplace do Amazon por meio do Administrador.

![Novo](../assets/new.svg)  **Preços inteligentes**: Defina regras automatizadas de reprecificação para aumentar suas chances para o Buy Box cobiçado. Defina os preços para ajustar dinamicamente ao preço de Buy Box atual ou ao preço mais baixo do concorrente. Defina limites para reprecificação para proteger sua margem.

![Novo](../assets/new.svg)  **Gerenciamento de Listagem**: automatize as listagens de produtos e sincronize seu catálogo do Commerce com o Amazon Marketplace usando as regras de listagem. Adicione substituições específicas para controlar com precisão suas ofertas. Monitore e gerencie todas as suas listagens diretamente do Administrador.

![Novo](../assets/new.svg)  **Inventory management consistente**: Mantenha as quantidades de seu inventário do Commerce e do Amazon em sincronização constante.

![Novo](../assets/new.svg)  **Gerenciamento de Pedidos e de Fulfillment**: controle os pedidos da Amazon por meio do painel, com comunicação contínua e atualizações de inventário. Complete e rastreie as entregas da ordem como atendidas pela Amazon, atendidas pelo comerciante ou uma combinação de métodos.

![Problema conhecido](../assets/bug.svg)  Você pode encontrar tempos de espera mais longos para atualizar quantidades de produtos. As atualizações da quantidade de produtos podem levar aproximadamente duas horas para serem sincronizadas.

![Problema conhecido](../assets/bug.svg)  As ordens importadas podem ter um tipo de _Prime_ ou _Premium_ pedidos. Você deve verificar esses pedidos em sua conta de vendedor da Amazon.

![Problema conhecido](../assets/bug.svg)  Produtos agrupados não qualificados podem ser exibidos como Qualificados para listagem no Amazon. Um dos produtos no produto agrupado pode não ser elegível. Se encontrar problemas, verifique o status de qualificação dos itens de produtos agrupados.

![Problema conhecido](../assets/bug.svg)  Ao usar o Inventory management para Commerce 2.3.x, uma reindexação parcial do estoque pode não ser acionada ao criar um pedido. A quantidade vendável recalcula por hora, o que pode causar venda excessiva durante esse intervalo de atualização.
