---
title: Publicar listagens no Walmart
description: Publique listas de produtos do Commerce no Walmart Marketplace para começar a vender.
source-git-commit: 2a9bd2f8f91e672786c36f5e132f99bcab59dd00
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---

# Publicar listagens no Walmart

Como outros mercados, o Walmart permite que vendedores de terceiros listem itens que são vendidos por outros.

A plataforma usa identificadores de produtos como UPC e GTIN para corresponder itens que já estão à venda.
Para produtos correspondentes, a listagem existente do Walmart Marketplace é atualizada para incluir a oferta do produto Commerce.
Geralmente, os produtos com os preços mais baixos aparecem primeiro nos resultados. Mas outros fatores como resenhas também afetam o posicionamento.

## Corresponder fluxo de trabalho

Quando você faz a correspondência de produtos, o Gerenciador de Canais envia os dados do produto para o Walmart Marketplace para procurar listas existentes com valores de atributo que correspondem ao atributo de produto Comércio mapeado.

Se uma correspondência for encontrada, a lista de produtos existente será atualizada para adicionar sua oferta.

## Pré-requisitos

Antes de corresponder produtos, verifique se os valores de atributos do catálogo de produtos atendem aos requisitos do Walmart e defina as configurações de atributos. Consulte [Configurar correspondência de produtos](map-product-attributes-for-matching.md)

## Selecionar e combinar produtos

1. Abra um canal de vendas conectado.

1. De **[!UICONTROL Listings]**, selecione os produtos para correspondência que estão em *[!UICONTROL Draft]* status.

   ![Selecione produtos em Listagens e envie para correspondência](assets/products-in-marketplace-sales-channel.png)

1. Selecionar **[!UICONTROL Match Products]**.

   Uma mensagem indica o número de produtos enviados para correspondência.

   ![Enviar produtos para o canal de vendas ligado](assets/products-submit-for-matching.png)

   Pode levar até 30 minutos para o Walmart Marketplace concluir a operação de correspondência.

   O status dos produtos selecionados muda para *[!UICONTROL Processing]* até que as operações de correspondência sejam concluídas. Pode levar até 30 minutos para o Walmart Marketplace concluir a operação de correspondência.

## Verificar status de correspondência

1. Selecionar **Atualizar produtos** para atualizar o status de produto mais atual.

1. Verifique o status do produto.

   Após a conclusão da correspondência, o status pode ser *Corresponder* ou *Erro*.

   * **[!UICONTROL Match]** indica que o produto foi correspondido com êxito. Sua oferta de produto foi publicada em uma lista existente do Walmart.

   * **[!UICONTROL Error]** indica uma das seguintes opções:

      * Ocorreu um erro e a operação de correspondência falhou.

      * Nenhuma correspondência foi encontrada.

      * Correspondência encontrada, mas produto publicado como preparado porque a variável [O armazenamento do Marketplace não está ativo](walmart-prerequisites.md#walmart-marketplace-store-status).

## Solução de problemas de erros de correspondência do produto

Se a operação de correspondência do produto falhar, o Walmart Marketplace retornará um código de erro e o Gerenciador de canais exibirá o status do erro nas informações da lista de produtos.

Exibir detalhes das mensagens de erro ao passar o mouse sobre **Erro** rótulo do status. Erros comuns retornados são valores de ID de produto formatados incorretamente ou atributos necessários ausentes.

## Corrigir valores da ID do produto

| Tipo | Descrição | Exemplo |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12, o número de 12 dígitos, incluindo o dígito de verificação.</br></br>Se o seu UPC tiver menos de 12 dígitos, como UPC-E, que tem 8 dígitos, adicione</br>zeros à esquerda para atender ao requisito. | Alterar de `45678912345` para `045678912345` |
| GTIN | GTIN-14, o número de 14 dígitos, incluindo o dígito de verificação.</br></br>Se o GTIN tiver menos de 14 dígitos, adicione zeros à esquerda </br>para satisfazer o requisito. | Alterar `456789123456` para `0045678912345` |
| EAN | GTIN-13, o número de 13 dígitos, incluindo o dígito de verificação.</br></br>Se o EAN tiver menos de 13 dígitos, adicione a linha à esquerda</br>zeros para atender ao requisito. | Alterar de `4567891234` para `0004567891234` |

Para obter detalhes sobre os códigos de erro do Walmart Marketplace, consulte o [Ajuda do Walmart Seller](https://sellerhelp.walmart.com/s/guide?article=000005844).
