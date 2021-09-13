---
title: Práticas recomendadas e limitações do canal de vendas da Amazon
description: Revise as práticas recomendadas e limitações ao usar o canal de vendas da Amazon para o Adobe Commerce e o Magento Open Source.
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Práticas recomendadas e limitações do canal de vendas da Amazon

As práticas recomendadas incluem:

- O canal de vendas da Amazon pode afetar suas listagens do Amazon aumentando ou diminuindo preços, sincronizando informações do produto (incluindo estoque disponível) e adicionando, atualizando e terminando (excluindo) as listagens. Revise suas listas por status durante a configuração e ajuste suas configurações ([listando configurações](./listing-settings.md), [listando regras](./listing-rules.md), [regras de precificação](./pricing-products.md), [substitui](./overrides.md) e assim por diante) antes de concluir a configuração da loja. Essas configurações também podem ser modificadas após a configuração, conforme necessário.

- O canal de vendas da Amazon pode definir suas regras de preços para ajustar automaticamente seu preço de listagem. As salvaguardas automatizadas de preços incluem o [preço mínimo](./floor-price.md) e [preço máximo opcional](./optional-ceiling-price.md) recursos de [Regras inteligentes de reprecificação](./intelligent-repricing-rules.md). O uso dessas salvaguardas ajuda a garantir que seus preços de listagem não fiquem abaixo de seu custo ou acima de um preço definido.

- A sincronização de dados entre o canal de vendas da Amazon e o Amazon é controlada por suas configurações [[!DNL Commerce] cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}. A limitação integrada entre [!DNL Commerce] e o Amazon ajuda a garantir a transmissão de dados tranquila e eficiente, mas durante os tempos de alto tráfego de eCommerce (como Black Friday), os sistemas da Amazon podem demorar mais do que o normal para serem atualizados. Defina seu [!DNL Commerce] cron para ser executado uma vez a cada cinco minutos.

- O canal de vendas da Amazon importa suas informações de pedido da Amazon. Para gerenciar seus pedidos da Amazon no canal de vendas da Amazon, você deve garantir que as [configurações de pedido](./order-settings.md) estejam definidas para importar e criar um pedido [!DNL Commerce] correspondente para cada pedido da Amazon. Se não estiver definido, você só poderá exibir suas informações de pedido do Amazon. Todos os impostos para vendas por meio do Amazon ainda são gerenciados e enviados por meio da sua conta [!DNL Amazon Seller Central]. Em alguns estados, a Amazon é obrigada a coletar e enviar impostos automaticamente. Para outros estados, os vendedores têm a opção de calcular impostos manual ou automaticamente. Consulte [Amazon: Políticas de Imposto](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/){target=&quot;_blank&quot;}. Talvez seja necessário fazer logon em sua conta [!DNL Amazon Seller Central] para visualizar a documentação da política de impostos do Amazon.

- Para regiões do Reino Unido, é uma prática recomendada inscrever-se no [Amazon VAT Calculation Service](https://sell.amazon.co.uk/learn/vat-resources/){target=&quot;_blank&quot;} antes de integrar o canal de vendas da Amazon.


   >[!NOTE]
   >
   >Pode levar de 10 a 14 dias para a Amazon verificar e ativar sua conta do Serviço de Cálculo de IVA.

As limitações incluem:

- Pacote, cartão-presente e tipos de produto agrupados que fazem parte do seu catálogo [!DNL Commerce] não são suportados pelo canal de vendas da Amazon para serem listados no Amazon.

- O canal de vendas da Amazon não pode criar uma listagem para um produto que não tenha uma listagem Amazon existente ou anterior. Se um produto não existir em [!DNL Amazon Seller Central] com um ASIN, ele deverá ser adicionado em [!DNL Amazon Seller Central] para que o Amazon possa atribuir um ASIN ao produto. Depois que um produto é adicionado no Amazon e uma listagem é criada, a listagem pode ser correspondida com seu catálogo no canal de vendas da Amazon e sincronizada.
