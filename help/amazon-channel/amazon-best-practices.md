---
title: Práticas recomendadas e limitações para [!DNL Amazon sales channel]
description: Examine as práticas recomendadas e limitações ao usar o canal de vendas da Amazon para Adobe Commerce e Magento Open Source.
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Práticas recomendadas e limitações para [!DNL Amazon sales channel]

As práticas recomendadas incluem:

- O canal de vendas da Amazon pode afetar suas listagens do Amazon aumentando ou diminuindo os preços, sincronizando informações de produtos (incluindo estoque disponível) e adicionando, atualizando e encerrando (excluindo) as listagens. Revise suas listas por status durante a configuração e ajuste suas configurações ([configurações de listagem](./listing-settings.md), [regras de listagem](./listing-rules.md), [regras de preços](./pricing-products.md), [sobreposições](./overrides.md)e assim por diante) antes de concluir a configuração da loja. Essas configurações também podem ser modificadas após a configuração, conforme necessário.

- O canal de vendas da Amazon pode definir suas regras de preços para ajustar automaticamente o preço da lista. As salvaguardas automatizadas de preços incluem [preço mínimo](./floor-price.md) e [preço máximo opcional](./optional-ceiling-price.md) recursos do [Regras inteligentes de reprecificação](./intelligent-repricing-rules.md). O uso dessas proteções ajuda a garantir que os preços de sua lista não fiquem abaixo do seu custo ou acima de um preço definido.

- A sincronização de dados entre o canal de vendas da Amazon e o Amazon é controlada pelo seu [[!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html) configurações. Limitação interna entre [!DNL Commerce] O e o Amazon ajudam a garantir uma transmissão de dados tranquila e eficiente, mas durante tempos de tráfego intenso de comércio eletrônico (como Black Friday), os sistemas da Amazon podem levar mais tempo do que o normal para serem atualizados. Defina seu [!DNL Commerce] cron para ser executado uma vez a cada cinco minutos.

- O canal de vendas da Amazon importa as informações de pedido da Amazon. Para gerenciar seus pedidos do Amazon no canal de vendas do Amazon, você deve garantir que seus [configurações do pedido](./order-settings.md) são definidos para importar e criar um correspondente [!DNL Commerce] para cada pedido do Amazon. Se não estiver definido, você só poderá exibir as informações do pedido Amazon. Todos os impostos sobre vendas através do Amazon ainda são gerenciados e remetidos através do seu [!DNL Amazon Seller Central] conta. Em alguns estados, a Amazon é obrigada a cobrar e remeter impostos automaticamente. Para outros estados, os vendedores têm a opção de calcular impostos manual ou automaticamente. Consulte [Amazon: Políticas de Impostos](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/){target="_blank"}. Talvez seja necessário fazer logon na [!DNL Amazon Seller Central] conta para exibir a documentação da política fiscal do Amazon.

- Para as regiões do Reino Unido, é prática recomendada se inscrever no [Serviço de Cálculo de IVA da Amazon](https://sell.amazon.co.uk/learn/vat-resources/){target="_blank"} antes da integração do canal de vendas do Amazon.


   >[!NOTE]
   >
   >Pode levar de 10 a 14 dias para que a Amazon verifique e ative sua conta do Serviço de Cálculo de IVA.

As limitações incluem:

- Tipos de pacote, cartão-presente e produto agrupados que fazem parte do seu [!DNL Commerce] catálogo não são compatíveis com o canal de vendas da Amazon para listagem na Amazon.

- O canal de vendas do Amazon não pode criar uma lista para um produto que não tenha uma lista do Amazon existente ou anterior. Se um produto não existir no [!DNL Amazon Seller Central] com uma ASIN, ela deve ser adicionada em [!DNL Amazon Seller Central] para que a Amazon possa atribuir um ASIN ao produto. Depois que um produto é adicionado ao Amazon e uma lista é criada, a lista pode corresponder ao catálogo no canal de vendas do Amazon e ser sincronizada.
