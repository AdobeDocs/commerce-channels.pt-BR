---
title: Conecte listagens ao Walmart
description: Conecte listagens de produtos do Commerce ao [!DNL Walmart Marketplace]para começar a vender.
exl-id: 78078b14-ebdd-415d-9486-66b0150167aa
source-git-commit: 418bb6a91817f49f3c3ae39a8d26370bfeb39099
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Conecte listagens ao Walmart

Como outros mercados, [!DNL Walmart] permite que vendedores de terceiros listem itens vendidos por outros.

- [!DNL Walmart Marketplace] usa identificadores de produtos como UPC e GTIN para corresponder produtos aos existentes [!DNL Walmart Marketplace] listagens.

- Para produtos correspondentes, a listagem do Walmart Marketplace é atualizada para incluir a oferta de produto do Commerce quando você conecta um produto do [!DNL Channel Manager].

- Geralmente, as ofertas de produto com os preços mais baixos aparecem primeiro na [!DNL Walmart Marketplace] listagem, mas outros fatores como revisões também afetam a disposição.

## Produtos correspondentes

Quando você corresponde produtos, o Gerenciador de canais envia os dados do produto para o [!DNL Walmart Marketplace] para procurar listas existentes com valores de atributo que correspondam ao atributo de produto Comércio mapeado. Os critérios de correspondência são determinados pela variável [configuração de mapeamento de atributo](map-catalog-attributes.md) para o seu canal de loja.

Se uma correspondência for encontrada, a lista de produtos existente será atualizada para adicionar sua oferta.

### Pré-requisitos

Antes de corresponder produtos, verifique se os valores de atributos do catálogo de produtos atendem aos requisitos do Walmart e defina as configurações de atributos do produto. Consulte [Mapear atributos do catálogo](map-catalog-attributes.md).

#### Selecionar e combinar produtos

1. Abra um canal de vendas conectado.

1. De **[!UICONTROL Listings]**, selecione os produtos para correspondência que estão em *[!UICONTROL Draft]* status.

   ![Selecione produtos em Listagens e envie para correspondência](assets/products-in-marketplace-sales-channel.png)

1. Selecionar **[!UICONTROL Match Products]**.

   Uma mensagem indica o número de produtos enviados para correspondência.

   ![Enviar produtos para o canal de vendas ligado](assets/products-submitted-for-matching.png)

   O status dos produtos selecionados muda para [!UICONTROL *Processamento*] até que a operação de correspondência seja concluída. Pode levar até 30 minutos para o Walmart Marketplace concluir a operação de correspondência.

### Verificar status de correspondência

Depois que a correspondência for concluída, selecione o **[!UICONTROL Refresh products]** para visualizar o status atual do produto. *Corresponder* ou *Erro*.

- **[!UICONTROL Match]** indica que o produto foi correspondido com êxito. Sua oferta de produto foi conectada a uma lista existente do Walmart Marketplace. Se a variável [O armazenamento do Marketplace não está ativo](walmart-requirements.md#walmart-marketplace-store-status), *[!UICONTROL Staged for Match]* é exibido no *[!UICONTROL Status detail]* coluna. Os produtos preparados são conectados automaticamente quando a função [!DNL Walmart Marketplace] a loja está ativada.

- **[!UICONTROL Error]** indica que a operação de correspondência falhou devido a um dos seguintes problemas:

   - [!DNL Channel Manager] não foi possível enviar para correspondência devido a um problema de conexão.

   - Nenhuma correspondência foi encontrada.

   - Correspondência encontrada, mas a listagem não pode ser conectada porque [!DNL Walmart Marketplace] retornou um código de erro. Consulte a **[!UICONTROL Error Description]** para obter informações sobre o problema.

### Verificar listagem no Walmart

Depois de combinar produtos, analise a lista de produtos atualizada e verifique os detalhes do produto, o preço e a quantidade do inventário da [[!UICONTROL Walmart Marketplace Seller Account Items] painel](https://seller.walmart.com/items-and-inventory/manage-items) para analisar o produto atualizado.

### Solução de problemas de erros de correspondência do produto

Se a operação de correspondência do produto falhar com um erro, a mensagem de erro será exibida no *[!UICONTROL Status detail]* na coluna [!UICONTROL Channel Manager] lista de produtos.

Erros comuns retornados são valores de ID de produto formatados incorretamente ou atributos necessários ausentes.

#### Corrigir valores da ID do produto

| Tipo | Descrição | Exemplo |
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12, o número de 12 dígitos, incluindo o dígito de verificação. </br></br>Se o seu UPC tiver menos de 12 dígitos, como o UPC-E, que tem 8 dígitos, adicione zeros finais para atender ao requisito. | Alterar de `45678912345` para `045678912345` |
| GTIN | GTIN-14, o número de 14 dígitos, incluindo o dígito de verificação. </br></br>Se o GTIN tiver menos de 14 dígitos, adicione zeros à esquerda </br>para satisfazer o requisito. | Alterar `456789123456` para `0045678912345` |
| EAN | GTIN-13, o número de 13 dígitos, incluindo o dígito de verificação. </br></br>Se o EAN tiver menos de 13 dígitos, adicione a linha à esquerda </br>zeros para atender ao requisito. | Alterar de `4567891234` para `0004567891234` |

Para obter detalhes sobre os códigos de erro do Walmart Marketplace, consulte o [Ajuda do Walmart Seller](https://sellerhelp.walmart.com/s/guide?article=000005844).

## Fazer upload de novas listas de produtos

Para produtos que não têm correspondência no Walmart Marketplace, use um modelo Excel de categoria de produto Walmart para fazer upload em massa das listagens de produtos. Você preenche o modelo Walmart usando dados de catálogo de produtos exportados da sua instância do Commerce.

Para obter novas listas de produtos, verifique seu catálogo de produtos para garantir que os produtos que você planeja vender no Walmart Marketplace tenham os atributos necessários para as listas de produtos do Walmart Marketplace .

**Listas do Walmart Marketplace - Requisitos de atributos**

| **Atributo** | **Nível de requisito** |
|--------------------------|-----------------------|
| SKU | Obrigatório |
| Nome do produto | Obrigatório |
| Tipo de ID do produto | Obrigatório |
| Identificação do produto | Obrigatório |
| Marca | Obrigatório |
| Descrição curta | Obrigatório |
| Preço de venda | Obrigatório |
| Descrição do site | Obrigatório |
| URL da imagem principal | Obrigatório |
| Peso da remessa | Obrigatório |
| Principais recursos | Recomendado |
| Número do modelo | Recomendado |
| Nome do fabricante | Recomendado |
| Número de peça do fabricante | Recomendado |
| Tamanho | Recomendado |
| Cor | Recomendado |
| URL da imagem principal | Opcional |
| URL da imagem adicional | Opcional |
| Fabricante | Opcional |

### Pré-requisitos

- Verifique se você atende à [Requisitos do Walmart](walmart-requirements.md).

- No catálogo de produtos do Commerce, verifique se a configuração de catálogo dos produtos a serem listados no Walmart Marketplace tem todos os atributos necessários e cumpre as Diretrizes de Conteúdo do Walmart Marketplace .

- Verifique se o trabalho cron está em execução para concluir a operação de exportação.

   - Para instâncias locais, consulte [Configurar e executar o cron](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-cron.html).

   - Para obter a infraestrutura de nuvem do Adobe, consulte [Configurar trabalhos do cron](https://devdocs.magento.com/cloud/configure/setup-cron-jobs.html).

### Crie o arquivo de dados do produto para fazer upload

1. Em seu [Conta do Vendedor do Walmart](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller), baixe um modelo de lista de produtos do Walmart Seller Center.

   - Na página Itens do catálogo do produto, selecione **[!UICONTROL Add Items]**. Em seguida, selecione **[!UICONTROL Add items in bulk]**.

      ![Adicionar itens na opção em massa na configuração de item do Walmart](assets/walmart-seller-account-add-items-bulk.png)

   - Na página de download, selecione **[!UICONTROL Full Setup]**. Em seguida, selecione uma categoria de item e baixe o modelo de categoria.

      ![Fazer download da opção de modelo de categoria na configuração de item do Walmart Marketplace](assets/walmart-seller-account-full-setup-download.png)

   - Verifique se o modelo inclui os atributos obrigatórios e recomendados para a lista de produtos.

1. No [!DNL Commerce] Administrador, selecione os dados do produto para exportar do site do Adobe Commerce.

   - Em Admin, selecione [!UICONTROL **Sistema** > Transferência de dados > **Exportar**].

   - No [!UICONTROL Export] na página [!UICONTROL Entity Type] , selecione [!UICONTROL **Produtos**].

   - No [!UICONTROL Entity Attributes] , configure os critérios de seleção para a exportação de dados do produto.
   ![Exporte a página de dados do produto no [!UICONTROL Commerce Admin]](assets/walmart-seller-account-full-setup-download.png)

   Use filtros para selecionar e configurar os valores do atributo que se aplicam às categorias de produto nas quais você vende. Certifique-se de incluir os atributos obrigatórios e recomendados do Walmart (Consulte [Exportar dados](https://docs.magento.com/user-guide/system/data-export.html) no Guia do usuário do Adobe Commerce para obter instruções detalhadas.)

   Para omitir um atributo da exportação, selecione o [!UICONTROL **Excluir**] caixa de seleção no início da linha.

1. Role até o final da tabela de atributos e selecione [!UICONTROL **Continuar**] para iniciar a exportação de dados.

   O arquivo de exportação CSV é processado por meio de uma fila de mensagens usando tarefas cron e salvo no `var/export/folder`. (Consulte [Gerenciar filas de mensagens](https://devdocs.magento.com/guides/v2.4/config-guide/mq/manage-message-queues.html) no *Guia do desenvolvedor do Commerce*.)

1. Abra o modelo do Excel para a categoria de produto do Walmart e use os recursos de macro do Excel para unir os dados do produto exportados ao modelo do Excel.

1. Faça upload do arquivo Excel com os dados do produto exportados.

   - Retorne à página Itens do catálogo de produtos na [Walmart Seller Center](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller).

   - Selecionar [!UICONTROL **Adicionar itens** > **Adicionar itens em massa**].
   - Arraste a planilha concluída até a seção Upload .
   - Selecionar [!UICONTROL **Enviar**].
   - Selecione o [!UICONTROL  **Feed de atividade**] para visualizar o progresso.

Para obter instruções completas, consulte [Adicionar itens em massa usando a especificação de item completo](https://sellerhelp.walmart.com/s/guide?article=000007680) no [!DNL *Ajuda do Walmart Seller*].
