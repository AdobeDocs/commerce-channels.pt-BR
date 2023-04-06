---
title: '[!DNL Amazon Sales Channel] Notas de versão'
description: Revise as notas de versão para obter informações sobre todas as [!DNL Amazon Sales Channel] versões.
exl-id: 792782e0-9097-42f7-9fc0-509ece02e407
source-git-commit: 3b2f60ad2796ee1fdc8808fc0941d76a603b2213
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Notas de versão

>[!IMPORTANT]
>
> [!DNL Amazon sales channel] pode ser instalado em instâncias com o Magento Open Source, Adobe Commerce e Adobe Commerce nas versões 2.3.x e 2.4.x da infraestrutura em nuvem. A extensão não é mais suportada no Adobe Commerce 2.1, Magento Open Source 2.2 ou Magento 1.
> <br>Suporte disponível para [!DNL Amazon sales channel]  versões 4.0.0 e 4.1.0 somente nas versões Adobe Commerce 2.3.x.
> <br>[!DNL Amazon sales channel] A versão 4.2.0+ é compatível com as versões 2.3.x do Adobe Commerce, mas o suporte está disponível somente para as versões 2.4.x do Adobe Commerce.

Essas notas de versão descrevem a versão inicial do [!DNL Amazon sales channel] e incluem:

![Novo](../assets/new.svg) Novos recursos
![Problema corrigido](../assets/fix.svg) Correções e melhorias
![Problema conhecido](../assets/bug.svg) Problemas conhecidos

Consulte [Próximas versões](https://devdocs.magento.com/release/){target="_blank"} para controle de versão, suporte e compatibilidade.

## v4.4.4

*7 de março de 2023*

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"}

![Problema corrigido](../assets/fix.svg) Adição de suporte para Adobe Commerce 2.4.6 e PHP 8.2.

![Problema corrigido](../assets/fix.svg) Ruído reduzido em logs.

![Problema corrigido](../assets/fix.svg) Melhor estabilidade de atualizações de extração.

![Problema corrigido](../assets/fix.svg) Simplificado o processo para executar pull de ação única ou para aplicar a partir da CLI.

![Problema corrigido](../assets/fix.svg) Atualização da dependência para `magento/services-connector`.

![Problema corrigido](../assets/fix.svg) Correção de problemas de sincronização em contas do Reino Unido com código de país inválido.

![Problema corrigido](../assets/fix.svg) Codificação rígida da entity_type_id para a entidade de produto de catálogo causa problemas com a Fonte de preço de Magento.

![Problema corrigido](../assets/fix.svg) Correção de um problema que impedia que contas excluídas em um backend de outra instância também fossem excluídas da interface do usuário.

![Problema corrigido](../assets/fix.svg) Correção de um problema com algumas regras do carrinho que quebravam a importação de ordens.

## v4.4.3

*7 de março de 2023*

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"}

![Correção](../assets/fix.svg) Adição de suporte ao Adobe Commerce 2.4.4.

## v4.4.2

*11 de novembro de 2021*

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"}

![Correção](../assets/fix.svg) Dependências atualizadas para suportar outras extensões atualizadas.
![Correção](../assets/fix.svg) Adição de suporte para PHP 8.1.

## v4.4.1

*11 de novembro de 2021*

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"}

![Correção](../assets/fix.svg) Alterada a forma como o Adobe Commerce recebe a variável _Nome do usuário_ do Amazon. Anteriormente, havia um erro durante a criação do pedido quando a função _Nome do usuário_ O campo continha caracteres especiais. O Adobe Commerce agora recebe o _Nome do usuário_ e filtra os caracteres especiais para que a ordem possa ser criada com êxito.

## v4.4.0

*9 de abril de 2021*

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"}

![Novo](../assets/new.svg) Adição de suporte para Modo somente leitura à configuração. Consulte [configurações de canal de vendas](sales-channel-settings.md).

![Correção](../assets/fix.svg) Fluxo de dados alterado para que várias cópias da mesma instância possam buscar atualizações simultaneamente.

![Correção](../assets/fix.svg) Alteração do processo de sincronização para sincronizar informações da conta. Adição de um trabalho cron para sincronizar com a conta remota e adição da mesma funcionalidade aos comandos CLI.

![Correção](../assets/fix.svg) Adição de argumentos e sinalizadores de comando CLI para um controle mais preciso.

![Correção](../assets/fix.svg) Correção da fonte de tarefas em segundo plano (cron) na configuração do sistema.

![Correção](../assets/fix.svg) Correção do problema que impedia a criação de pedidos quando o código do país era definido como Porto Rico (PR).

## v4.3.0

*3 de março de 2021*

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"}

![Correção](../assets/fix.svg) <!--CHAN-xxxx-->O _Detalhes do pedido_ foi reprojetado e não depende mais do _Importar Ordens_ configuração. Os detalhes do pedido agora são exibidos na interface do Sales Channel Amazon para todos os pedidos.

![Correção](../assets/fix.svg) No _[!UICONTROL Marketing]_no menu Admin, o nome foi alterado de_[!UICONTROL Amazon]_ para _[!UICONTROL Amazon Sales Channel]_.

![Problema conhecido](../assets/bug.svg) **Importante**: Problemas conhecidos com a compatibilidade do Adobe Commerce 2.4.0 são resolvidos na versão Adobe Commerce 2.4.1.

- O Amazon cron processa em `error` state
- A instalação com o Commerce 2.4.0 falha ao criar lojas no banco de dados
- A criação do produto falha quando o MSI está instalado

## v4.2.0

*3 de março de 2021*

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"}

Se você tiver uma [!DNL Amazon sales channel] instalada e tentar atualizar seu Adobe Commerce para a versão 2.4.0, será solicitado que você atualize a extensão antes de concluir a atualização do Adobe Commerce.

![Problema conhecido](../assets/bug.svg) When [!DNL Amazon sales channel] 4.2.0 é integrado à versão 2.4.0 e [Inventory management](https://docs.magento.com/user-guide/catalog/inventory.html) estiver habilitado, há um problema conhecido que impede a adição de produtos no catálogo do Commerce. Esse problema será resolvido em uma versão futura do Commerce.

![Novo](../assets/new.svg) [!DNL Amazon sales channel] O foi aprimorado para aceitar dados de endereço baseados em texto e corresponder aos formatos de endereço padronizados, incluindo cidade, estado e código postal. Essa atualização permite que o pedido e o envio de dados sejam sincronizados (sincronizados) com o Amazon sem erros de endereço.<br/>Por exemplo, um comprador insere a cidade, o estado, o código postal como `Escondido, californiA 92025-1501`. O Amazon Sales Channel importa e corresponde os dados ao formato padrão como `Escondido, CA 92025`e, em seguida, sincroniza de volta ao Amazon nesse formato padronizado.

![Novo](../assets/new.svg) Adição de suporte para PHP 7.4.

![Novo](../assets/new.svg) <!--CHAN-4334-->Adição de suporte para Adobe Commerce 2.4.x. As versões anteriores podem ser compatíveis com o Commerce 2.4.x, mas não são compatíveis. Consulte [Próximas versões](https://devdocs.magento.com/release/){:target=&quot;_blank&quot;} para compatibilidade de versão. O Amazon Sales Channel deve ser atualizado para 4.2.0 antes que a atualização do Adobe Commerce 2.4.0 possa ser concluída.

![Correção](../assets/fix.svg) <!--CHAN-4431-->Correção de um problema que causava um _Acesso negado_ para clientes do Reino Unido.

![Correção](../assets/fix.svg) <!--CHAN-4394-->Correção de um problema que impedia que o status de envio do Amazon fosse sincronizado com a ordem de Comércio correspondente, &quot;bloqueando&quot; assim o status de envio do pedido como `Pending` no Commerce e `Unshipped` no Amazon. Com o novo recurso de endereço padronizado, esses erros de status de envio foram resolvidos.

![Correção](../assets/fix.svg) <!--ticket#-->A sincronização de pedidos (sincronização) foi atualizada para ignorar importações de pedidos com falha, reduzindo assim várias tentativas de sincronização e permitindo que importações subsequentes fossem processadas, com solicitações de sincronização de pedidos enviadas a cada cinco minutos. Os erros de sincronização ainda são registrados no log de erros, mas marcados como &quot;processados&quot; para permitir outras funções de registro. Além disso, [!DNL Amazon sales channel] O agora remove automaticamente os dados em excesso coletados para pedidos que não são criados no Commerce.

![Correção](../assets/fix.svg) Atualização do registro de erros para coletar mais informações para erros de exceção e atualização de extensão não capturados.

![Correção](../assets/fix.svg) <!--ticket#-->Correção de um problema que causava a sincronização inicial do _preço mais baixo_ dados que falharam devido a um _preço_ valor.

![Correção](../assets/fix.svg) <!--CHAN-4410-->Correção de problemas que causavam erros de filtragem no _Pedidos Amazon_ exibir quando o campo de intervalo de datas for deixado em branco.

![Correção](../assets/fix.svg) <!--CHAN-4439-->Correção de um problema que causava erros de sincronização de estoque e de atendimento relacionados à quantidade. A extensão agora arredonda os valores de quantidade inseridos como decimal antes de sincronizar com o Amazon.<br/> Por exemplo, quando um comerciante insere manualmente uma quantidade de `2.5`, a extensão arredonda o valor para baixo `2` e sincroniza a quantidade atualizada com o Amazon.

## v4.1.0

*7 de maio de 2020*

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"}

![Novo](../assets/new.svg) <!--4247, 4230-->Alteração do processo de importação do pedido para alinhar-se aos requisitos do pedido de Comércio. Essas alterações corrigem problemas que impediam o Commerce de criar o pedido correspondente para um pedido importado. Consulte [Gerenciar pedidos](managing-orders.md) para obter informações sobre bloqueadores de pedidos e soluções.

![Novo](../assets/new.svg) <!--CHAN-CHAN-4167, 4297, 4311, 4312, 4324-->Atualização do _Pedidos recentes_ seção do painel de loja e adição de um novo _Todos os pedidos_ exibição que mostra todos os pedidos da Amazon, incluindo opções de filtro e paginação para visualizar mais pedidos. Consulte [Painel da Amazon Store](amazon-store-dashboard.md) e [Exibir pedidos da Amazon](amazon-orders-all.md).

![Novo](../assets/new.svg) Adicionado o _[!UICONTROL Order Notes]_coluna de redesenho_[!UICONTROL Amazon Orders]_ tabela em ambos _[!UICONTROL Recent Orders]_e_[!UICONTROL All Orders]_ exibições. _[!UICONTROL Order Notes]_informe ao comerciante que há um problema com a importação do pedido. Consulte [Exibir pedidos da Amazon](amazon-orders-all.md).

![Novo](../assets/new.svg) <!--CHAN-4013-->Atualização dos parâmetros de condição do produto para alinhar-se ao [Amazon Renovado](https://sell.amazon.com/programs/renewed) programa. Consulte [Produtos Renovados](renewed-products.md).

![Novo](../assets/new.svg) <!--CHAN-3680-->Atualizado [Detalhes do pedido Amazon](amazon-order-details.md) incluir &quot;dados genéricos&quot; para pedidos realizados pela Amazon. Consulte [Cumprido por](fulfilled-by.md).

![Correção](../assets/fix.svg) <!--CHAN-4069-->Correção de um problema que causava a distorção de ícones na placa de loja.

![Correção](../assets/fix.svg) <!--CHAN-4165-->Correção de um erro que impedia o _Logon_ da exibição após o tempo limite da sessão.

![Correção](../assets/fix.svg) <!--CHAN-4211-->Correção de um problema que impedia a importação do valor do imposto de pedido do Amazon para o novo pedido de Comércio.

![Correção](../assets/fix.svg) <!--CHAN-4234-->Correção de um problema que fazia com que os totais de receita exibidos no painel de loja incluíssem pedidos em `Canceled` ou `Error` status.

![Correção](../assets/fix.svg) <!--CHAN-4326-->Correção de um problema que causava erros de importação de pedido associados a extensões de terceiros que usavam _Magento Shipping_ métodos para criar pedidos.

![Correção](../assets/fix.svg) <!--CHAN-4357-->Correção de um problema que causava erros ao executar a sincronização cron. Um bloqueio foi adicionado ao comando CLI que impede que dois trabalhos do cron sejam sincronizados ao mesmo tempo.

![Correção](../assets/fix.svg) Política de segurança de conteúdo atualizada para oferecer suporte ao Commerce versão 2.3.5.

## v4.0.0

*25 de março de 2020*

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"}

>[!IMPORTANT]
>
>O Amazon Sales Channel 4.0.0 não é compatível com o Adobe Commerce 2.3.5. Para obter suporte com o Adobe Commerce 2.3.5, atualize para o Amazon Sales Channel 4.1.0.

![Novo](../assets/new.svg) Introduziu um novo [Sales Channel Amazon](amazon-sales-channel-home.md) página inicial com &quot;exibição de cartão&quot; aprimorada para suas informações de loja.

![Novo](../assets/new.svg) Introduziu um novo [painel de loja](amazon-store-dashboard.md) com listagem, pedidos recentes e informações de configuração de armazenamento.

![Novo](../assets/new.svg) Introduziu um [processo de integração](amazon-onboarding-home.md) e [configurações padrão do armazenamento](default-store-settings.md) para integrar suas lojas mais rapidamente.

![Problema conhecido](../assets/bug.svg) <!--CHAN-4102--> When [criação de atributos](managing-attributes.md) para importar imagens de listas e **Armazenar exibições** está definida como `All Store Views (Global)`, existe um problema conhecido que impede a importação de imagens para todas as exibições da loja. Se você alterar a configuração de **Armazenar Exibições (para importar valores para o)** para uma loja específica, as imagens são importadas para essa loja.

## v3.0.1

*11 de novembro de 2019*

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"}

![Correção](../assets/fix.svg) **Configurações de campo numérico**: <!--CHAN-3779-->Os campos que exigem um valor com base numérica foram atualizados para aceitar somente caracteres numéricos. Exemplo: Configurações da Regra de Preço > Campo Quantia de Ajuste

![Correção](../assets/fix.svg) **Links do guia do usuário**: <!--CHAN-3778-->Incorreto _Guia do usuário_ os links foram corrigidos.

![Correção](../assets/fix.svg) **Duplicar as listagens do Amazon**: <!--CHAN-3593-->Um problema reportado anteriormente que causa listas Amazon duplicadas foi corrigido. Antes desta versão, a extensão adicionava o Código do país da região do Amazon aos valores de SKU ao importar listagens. A listagem correspondeu ao item de catálogo, mas a extensão criou uma nova listagem duplicada com o SKU anexado. Com esta versão, a extensão não modifica o SKU de listagens importadas e nenhuma alteração é feita em listagens existentes. Você pode usar o [!UICONTROL End Listing(s)] na opção Amazon para remover listas duplicadas.

## v3.0.0

*7 de outubro de 2019*

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"}

![Novo](../assets/new.svg) **Amazon UK Marketplace já disponível**: Os usuários podem escolher o mercado do Reino Unido ao criar e integrar uma loja de Comércio. Esta atualização do Reino Unido inclui suporte adicional para:

- [Serviço de Cálculo de IVA Amazon](https://sell.amazon.co.uk/learn/vat-resources){target="_blank"}

- [Código de imposto do produto](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"} informações.

![Novo](../assets/new.svg) **Registro aprimorado**: <!--CHAN-3642, 3672-->Implementou o **Ativar o registro de depuração** para coletar dados de sincronização adicionais quando a solução de problemas for necessária. Consulte a [Configurações do Sales Channel](https://docs.magento.com/user-guide/configuration/sales-channels/global-settings.html) no tópico Referência de configuração.

![Correção](../assets/fix.svg) **Catálogo de produtos**: <!--CHAN-3687-->Correção de um problema que impedia que imagens importadas com uma listagem do Amazon fossem aplicadas ao produto de catálogo do Commerce correspondente.

![Correção](../assets/fix.svg) **Criação de pedidos**: <!--CHAN-3708-->Correção de um problema que impedia o Commerce de criar pedidos para um pedido Amazon que não correspondia a um produto de catálogo do Commerce.

![Problema conhecido](../assets/bug.svg) **Duplicar as listagens do Amazon**: <!--CHAN-3593-->Esse problema faz com que o catálogo crie um item para uma listagem importada, usando o mesmo SKU, mas com um código de região adicionado no final. A Amazon então processa o SKU modificado como um novo item e cria uma listagem. Esse problema será resolvido em uma versão futura.

## v2.0.0

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"}

>[!NOTE]
>
>A versão 1.0.0 estava disponível somente na versão limitada.

![Novo](../assets/new.svg)  **Integração e manutenção simplificadas**: Adicione e integre-se à sua conta do Amazon Seller por meio de um processo passo a passo com instruções detalhadas disponíveis por meio do Administrador. Mantenha suas lojas, contas e produtos listados por meio de um painel.

![Novo](../assets/new.svg)  **Suporte a várias contas**: Gerencie e monitore várias marcas e regiões do mercado da Amazon por meio do Administrador.

![Novo](../assets/new.svg)  **Preços inteligentes**: Defina regras de reprecificação automatizadas para aumentar suas chances para o Buy Box desejado. Defina os preços para ajustarem-se dinamicamente ao preço de Buy Box atual ou ao preço mais baixo do concorrente. Defina limites para o redirecionamento de preços para proteger sua margem.

![Novo](../assets/new.svg)  **Gerenciamento de listagem**: Automatize listas de produtos e sincronize seu catálogo de comércio com o Amazon Marketplace usando regras de listagem. Adicione substituições específicas para controlar com precisão suas ofertas. Monitore e gerencie todas as suas listagens diretamente do Administrador.

![Novo](../assets/new.svg)  **Inventory management consistente**: Mantenha as quantidades de inventário do Commerce e do Amazon em sincronização constante.

![Novo](../assets/new.svg)  **Gerenciamento de Ordem e Cumprimento**: Acompanhe os pedidos do Amazon pelo painel, com comunicações e atualizações de inventário ininterruptas. Concluir e rastrear entregas de pedidos conforme a Amazon, um comerciante atendido ou uma combinação de métodos.

![Problema conhecido](../assets/bug.svg)  Você pode encontrar tempos de espera mais longos para atualizar as quantidades do produto. As atualizações para a quantidade do produto podem levar aproximadamente duas horas para serem sincronizadas.

![Problema conhecido](../assets/bug.svg)  As ordens importadas podem ter um tipo de _Prime_ ou _Premium_ ordens. Você deve verificar esses pedidos em sua conta de vendedor da Amazon.

![Problema conhecido](../assets/bug.svg)  Produtos integrados não elegíveis podem ser exibidos como Elegíveis para listagem no Amazon. Um dos produtos do produto empacotado pode não ser elegível. Se encontrar problemas, verifique o status de qualificação para itens de produtos empacotados.

![Problema conhecido](../assets/bug.svg)  Ao usar o Inventory management para Commerce 2.3.x, uma reindexação de ações parcial pode não ser acionada quando um pedido é criado. A quantidade comercializável recalcula por hora, o que pode causar sobrevendas durante esse intervalo de atualização.
