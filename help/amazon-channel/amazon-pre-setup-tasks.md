---
title: Tarefas de pré-configuração
description: Revise as tarefas necessárias a serem concluídas antes de integrar sua loja de Adobe Commerce ou Magento Open Source no Amazon Sales Channel.
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 0%

---

# Tarefas de pré-configuração

Antes de [Armazenar integração](./store-integration.md), você deve garantir que sua conta [!DNL Amazon Seller Central] e sua conta [!DNL Commerce] estejam prontas para a integração. Para integrar com êxito, há algumas tarefas pré-configuráveis necessárias.

Quando você configura sua primeira loja da Amazon no canal de vendas da Amazon, é exibida uma lista de tarefas de configuração. É recomendável revisar essas tarefas antes de [adicionar um Amazon store](./store-integration.md). Após adicionar sua primeira loja, você pode revisar essas tarefas na visualização Aprendizagem e preparação do canal de vendas da Amazon [home page](./amazon-sales-channel-home.md).

## 1. Habilitar tarefas em segundo plano em [!DNL Commerce]

Todos os produtos e dados sincronizados entre [!DNL Commerce] e o Amazon são gerenciados por um [trabalho cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}. Quando você conclui tarefas como adicionar ou atualizar listas e receber pedidos, um trabalho cron envia e recebe dados entre seu [!DNL Commerce] backend e sua conta [!DNL Amazon Seller Central].

- [ [!DNL Commerce] Ativar](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}.

- Para obter o desempenho máximo, [defina [!DNL Commerce] cron](https://docs.magento.com/user-guide/configuration/advanced/system.html){target=&quot;_blank&quot;} para ser executado uma vez a cada cinco minutos.

## 2. Crie sua conta [!DNL Amazon Seller Central]

Antes de começar a configurar seu canal de vendas da Amazon, você deve ter uma conta [!DNL Amazon Seller Central] ativa. Se você não tiver uma conta do Amazon Seller existente na região [América do Norte (EUA, CA, MX)](https://sell.amazon.com/){target=&quot;_blank&quot;} ou [Europeu (Reino Unido)](https://sell.amazon.co.uk/sell-online/beginners-guide){target=&quot;_blank&quot;}, poderá concluir o processo de configuração da conta do vendedor da Amazon.

O canal de vendas Amazon requer uma conta [!DNL Professional Seller] em [!DNL Amazon Seller Central]. A Amazon cobra uma assinatura mensal e as tarifas de venda. Consulte [Amazon: Escolha seu plano de venda](https://sell.amazon.com/pricing.html){target=&quot;_blank&quot;}.

## 3. Certifique-se de que você é um vendedor aprovado da Amazon

Para integrar, você deve ter uma conta [!DNL Amazon Seller Central] aprovada. Sua conta não deve ter restrições para produtos ou categorias. Alguns produtos e categorias exigem aprovação antes de criar listas. Revise as políticas da Amazon para obter aprovação de categoria e produto para garantir que seus produtos sejam aprovados. Consulte [Amazon: Categorias e produtos que exigem aprovação](https://sellercentral.amazon.com/gp/help/200333160){target=&quot;_blank&quot;} (logon do Seller Central necessário).

Também é importante garantir que você tenha configurado o seguinte na sua conta [!DNL Amazon Seller Central]:

- Certifique-se de que a política de retorno seja tão boa ou melhor que a política de retorno do Amazon. Consulte [Amazon: Política de Retorno](https://www.amazon.com/gp/help/customer/display.html){target=&quot;_blank&quot;}.

- Certifique-se de que as configurações de imposto estejam definidas. Consulte [Amazon: Políticas de Imposto](https://sellercentral.amazon.com/gp/help/external/help.html){target=&quot;_blank&quot;} (logon Central do vendedor necessário).

- Certifique-se de que seus métodos de envio estejam configurados com precisão. Para configurar os métodos de envio que [!DNL Commerce] são oferecidos aos clientes para atender aos seus pedidos da Amazon, atualize o [Amazon: Configurações de envio](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target=&quot;_blank&quot;} em sua conta [!DNL Amazon Seller Central].

## 4. Certifique-se de que o IVA esteja configurado para as suas lojas

(Utilizado principalmente pelos vendedores britânicos.) A Amazon recomenda se inscrever no [Serviço de Cálculo de IVA da Amazon](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target=&quot;_blank&quot;}. Se escolher um método diferente, você será responsável pela conformidade com o IVA.

>[!NOTE]
>
>Pode levar de 10 a 14 dias para a Amazon verificar e ativar sua conta do Serviço de Cálculo de IVA.

## 5. Aumente o número de correspondências automáticas de catálogo

Durante a integração, o canal de vendas da Amazon usa atributos de produto para corresponder às listagens existentes do Amazon (se aplicável) aos produtos existentes no catálogo [!DNL Commerce]. Após a integração, esses atributos de produto são usados para publicar os itens do catálogo [!DNL Commerce] em uma lista do Amazon e sincronizar os dados do produto entre [!DNL Commerce] e o Amazon.

Para ter o maior número de [!DNL Commerce] produtos automaticamente compatível com as listagens do Amazon, você deve criar um conjunto de atributos de produto para o catálogo [!DNL Commerce]. Antes de configurar a loja de canais de vendas da Amazon, você deve adicionar [!DNL Commerce] atributos de produto para corresponder a esses atributos do Amazon, por exemplo: ASIN, EAN, ISBN, UPC ou GCID. Consulte [Criar um atributo de produto em [!DNL Commerce]](./ob-creating-magento-attributes.md).

## 6. Configure sua moeda e conversão (conforme necessário)

Se o armazenamento da Amazon usar uma moeda diferente da configurada para o armazenamento [!DNL Commerce], [ative a moeda](https://docs.magento.com/user-guide/configuration/general/currency-setup.html){target=&quot;_blank&quot;} e defina a [taxa de conversão de moeda](https://docs.magento.com/user-guide/stores/currency-update.html){target=&quot;_blank&quot;}.

## 7. Crie um atributo de condição do produto (conforme necessário)

Se suas listagens do Amazon contiverem mais de uma condição de produto (como _new_, _used_ ou _like new_), crie um atributo [!DNL Commerce] e atribua valores de condição. Você deve mapear esse atributo durante a integração ao atributo de produto Condição do Amazon. Consulte [Criação de atributos para Amazon](./ob-creating-magento-attributes.md).

## 8. Configure seu método de entrega [!DNL Amazon Seller Central]

Para configurar métodos de envio que você deseja oferecer para atender aos seus pedidos do Amazon, consulte [Configurações e configurações de envio][10] em sua conta [!DNL Amazon Seller Central].

## Configurações adicionais

Quando sua conta do Amazon é configurada e ativa, há várias [!DNL Commerce] recomendações que ajudam a simplificar o processo de integração do canal de vendas da Amazon.

### Revise e anote quaisquer produtos que deseja excluir

Talvez você não queira que alguns produtos sejam listados no Amazon. O canal de vendas da Amazon tem um mecanismo de regra de listagem usado para determinar quais produtos estão qualificados para publicação no Amazon. [As ](./listing-rules.md) regras de listagem permitem selecionar subconjuntos de produtos a serem publicados (ou não) na sua  [!DNL Amazon Seller Central] conta, como por seleção de categoria ou por definição de um ou mais atributos de produto. Como [!DNL Commerce] [catalog](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;} ou [carrinho de compras](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}, as regras de preço dos atributos de produto usados para a qualificação de listagem do Amazon devem ter **[!UICONTROL Use for Promo Rule Conditions]** definido como `Yes`. Consulte o **[!UICONTROL Use for Promo Rule Conditions]** em [Atributos do produto](https://docs.magento.com/user-guide/stores/attributes-product.html){target=&quot;_blank&quot;}.

### Defina sua região [!DNL Amazon Seller Central] como inativa

Para ajudar a facilitar a transição de dados sem erros durante a integração, é recomendável definir sua região do Amazon para o status `Inactive` em Configurações > Informações da conta > Configurações de Férias. Consulte [Amazon: Listando Status de Férias][11]. Quando a configuração estiver concluída, altere o status de volta para `Active` no Amazon.

![Ícone ](assets/btn-next.png) [**Avançar para Criar  [!DNL Commerce] atributos**](./ob-creating-magento-attributes.md)
