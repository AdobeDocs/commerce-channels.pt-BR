---
title: Práticas recomendadas e limitações para  [!DNL Amazon sales channel]
description: Examine as práticas recomendadas e limitações ao usar o canal de vendas da Amazon para Adobe Commerce e Magento Open Source.
role: Leader, Admin, User
feature: Sales Channels, Best Practices
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Práticas recomendadas e limitações para [!DNL Amazon sales channel]

As práticas recomendadas incluem:

- O canal de vendas da Amazon pode afetar suas listagens do Amazon aumentando ou diminuindo os preços, sincronizando informações de produtos (incluindo estoque disponível) e adicionando, atualizando e encerrando (excluindo) as listagens. Revise suas listas por status durante a instalação e ajuste suas configurações ([configurações de listagem](./listing-settings.md), [regras de listagem](./listing-rules.md), [regras de preços](./pricing-products.md), [substituições](./overrides.md) e assim por diante) antes de concluir a configuração da loja. Essas configurações também podem ser modificadas após a configuração, conforme necessário.

- O canal de vendas da Amazon pode definir suas regras de preços para ajustar automaticamente o preço da lista. As proteções automatizadas de preços incluem os recursos [andar de preço](./floor-price.md) e [teto opcional](./optional-ceiling-price.md) das [Regras inteligentes de reprecificação](./intelligent-repricing-rules.md). O uso dessas proteções ajuda a garantir que os preços de sua lista não fiquem abaixo do seu custo ou acima de um preço definido.

- A sincronização de dados entre o canal de vendas da Amazon e o Amazon é controlada pelas suas configurações do [[!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html). A limitação integrada entre o [!DNL Commerce] e o Amazon ajuda a garantir uma transmissão de dados suave e eficiente, mas durante tempos de tráfego intenso de comércio eletrônico (como Black Friday), os sistemas da Amazon podem levar mais tempo do que o normal para serem atualizados. Defina o cron do [!DNL Commerce] para ser executado uma vez a cada cinco minutos.

- O canal de vendas da Amazon importa as informações de pedido da Amazon. Para gerenciar seus pedidos do Amazon no canal de vendas da Amazon, certifique-se de que suas [configurações de pedido](./order-settings.md) estejam definidas para importar e criar um pedido [!DNL Commerce] correspondente para cada pedido do Amazon. Se não estiver definido, você só poderá exibir as informações do pedido Amazon. Todos os impostos para vendas através da Amazon ainda são gerenciados e remetidos através da sua conta [!DNL Amazon Seller Central]. Em alguns estados, a Amazon é obrigada a cobrar e remeter impostos automaticamente. Para outros estados, os vendedores têm a opção de calcular impostos manual ou automaticamente. Consulte [Amazon: Políticas Fiscais](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/){target="_blank"}. Talvez seja necessário fazer logon na conta [!DNL Amazon Seller Central] para exibir a documentação da política fiscal da Amazon.

- Para regiões do Reino Unido, é prática recomendada inscrever-se no [Serviço de Cálculo de IVA da Amazon](https://sell.amazon.co.uk/learn/vat-resources/){target="_blank"} antes de integrar o canal de vendas da Amazon.

  >[!NOTE]
  >
  >Pode levar de 10 a 14 dias para que a Amazon verifique e ative sua conta do Serviço de Cálculo de IVA.

As limitações incluem:

- Os tipos de pacote, cartão-presente e produto agrupado que fazem parte do catálogo do [!DNL Commerce] não têm suporte no canal de vendas da Amazon para listagem no Amazon.

- O canal de vendas do Amazon não pode criar uma lista para um produto que não tenha uma lista do Amazon existente ou anterior. Se um produto não existir em [!DNL Amazon Seller Central] com uma ASIN, ele deverá ser adicionado em [!DNL Amazon Seller Central] para que a Amazon possa atribuir uma ASIN a esse produto. Depois que um produto é adicionado ao Amazon e uma lista é criada, a lista pode corresponder ao catálogo no canal de vendas do Amazon e ser sincronizada.
