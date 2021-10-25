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

Antes [Integração de loja](./store-integration.md), você deve garantir que [!DNL Amazon Seller Central] e sua [!DNL Commerce] estão prontas para a integração. Para integrar com êxito, há algumas tarefas pré-configuráveis necessárias.

Quando você configura sua primeira loja da Amazon no canal de vendas da Amazon, é exibida uma lista de tarefas de configuração. É recomendável revisar essas tarefas antes de [adicionar uma loja da Amazon](./store-integration.md). Após adicionar sua primeira loja, você pode revisar essas tarefas na visualização Aprendizagem e preparação do canal de vendas da Amazon [página inicial](./amazon-sales-channel-home.md).

## 1. Habilite tarefas em segundo plano em [!DNL Commerce]

Todos os produtos e dados sincronizados entre [!DNL Commerce] e o Amazon é gerenciado por um [trabalho cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}. Quando você conclui tarefas como adicionar ou atualizar listas e ordens de recebimento, um trabalho cron envia e recebe dados entre suas [!DNL Commerce] back-end e seu [!DNL Amazon Seller Central] conta.

- [Habilitar [!DNL Commerce] cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}.

- Para obter o máximo desempenho, [set [!DNL Commerce] cron](https://docs.magento.com/user-guide/configuration/advanced/system.html){target=&quot;_blank&quot;} será executado uma vez a cada cinco minutos.

## 2. Crie seu [!DNL Amazon Seller Central] account

Antes de começar a configurar seu canal de vendas da Amazon, você deve ter um [!DNL Amazon Seller Central] conta. Se você não tiver uma conta do Amazon Seller existente na [América do Norte (EUA, CA, MX)](https://sell.amazon.com/){target=&quot;_blank&quot;} ou [Europeu (Reino Unido)](https://sell.amazon.co.uk/sell-online/beginners-guide)Região {target=&quot;_blank&quot;}, você pode concluir o processo de configuração da conta de vendedor da Amazon.

O canal de vendas da Amazon requer um [!DNL Professional Seller] conta em [!DNL Amazon Seller Central]. A Amazon cobra uma assinatura mensal e as tarifas de venda. Consulte [Amazon: Escolha seu plano de venda](https://sell.amazon.com/pricing.html){target=&quot;_blank&quot;}.

## 3. Certifique-se de que você é um vendedor aprovado da Amazon

Para integrar, você deve ter um [!DNL Amazon Seller Central] conta. Sua conta não deve ter restrições para produtos ou categorias. Alguns produtos e categorias exigem aprovação antes de criar listas. Revise as políticas da Amazon para obter aprovação de categoria e produto para garantir que seus produtos sejam aprovados. Consulte [Amazon: Categorias e produtos que exigem aprovação](https://sellercentral.amazon.com/gp/help/200333160){target=&quot;_blank&quot;} (logon do Seller Central necessário).

Também é importante garantir que você tenha configurado o seguinte em [!DNL Amazon Seller Central] conta:

- Certifique-se de que a política de retorno seja tão boa ou melhor que a política de retorno do Amazon. Consulte [Amazon: Política de devolução](https://www.amazon.com/gp/help/customer/display.html){target=&quot;_blank&quot;}.

- Certifique-se de que as configurações de imposto estejam definidas. Consulte [Amazon: Políticas Fiscais](https://sellercentral.amazon.com/gp/help/external/help.html){target=&quot;_blank&quot;} (logon do Seller Central necessário).

- Certifique-se de que seus métodos de envio estejam configurados com precisão. Para configurar os métodos de entrega que [!DNL Commerce] são oferecidos aos clientes para atender aos seus pedidos da Amazon, atualize o [Amazon: Configurações de envio](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target=&quot;_blank&quot;} em seu [!DNL Amazon Seller Central] conta.

## 4. Certifique-se de que o IVA esteja configurado para as suas lojas

(Utilizado principalmente pelos vendedores britânicos.) A Amazon recomenda se inscrever na [Serviço de Cálculo de IVA Amazon](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target=&quot;_blank&quot;}. Se escolher um método diferente, você será responsável pela conformidade com o IVA.

>[!NOTE]
>
>Pode levar de 10 a 14 dias para a Amazon verificar e ativar sua conta do Serviço de Cálculo de IVA.

## 5. Aumente o número de correspondências automáticas de catálogo

Durante a integração, o canal de vendas da Amazon usa atributos de produto para corresponder às listas existentes do Amazon (se aplicável) aos produtos existentes em seu [!DNL Commerce] catálogo. Após a integração, esses atributos de produto são usados para publicar [!DNL Commerce] catalogar itens em uma lista da Amazon e sincronizar os dados do produto entre [!DNL Commerce] e Amazon.

Para ter o número mais alto de [!DNL Commerce] Os produtos correspondem automaticamente às listas do Amazon, você deve criar um conjunto de atributos de produto para [!DNL Commerce] catálogo. Antes de configurar a loja de canais de vendas da Amazon, você deve adicionar [!DNL Commerce] atributos de produto para corresponder a esses atributos do Amazon, por exemplo: ASIN, EAN, ISBN, UPC ou GCID. Consulte [Crie um atributo de produto em [!DNL Commerce]](./ob-creating-magento-attributes.md).

## 6. Configure sua moeda e conversão (conforme necessário)

Se a loja da Amazon usar uma moeda diferente da configurada para sua [!DNL Commerce] armazenamento, [ativar a moeda](https://docs.magento.com/user-guide/configuration/general/currency-setup.html){target=&quot;_blank&quot;} e defina o [taxa de conversão de moeda](https://docs.magento.com/user-guide/stores/currency-update.html){target=&quot;_blank&quot;}.

## 7. Crie um atributo de condição do produto (conforme necessário)

Se suas listas do Amazon contiverem mais de uma condição de produto (como _novo_, _used_ ou _como novo_), crie uma [!DNL Commerce] e atribuir valores de condição. Você deve mapear esse atributo durante a integração ao atributo de produto Condição do Amazon. Consulte [Criar atributos para o Amazon](./ob-creating-magento-attributes.md).

## 8. Configure seu [!DNL Amazon Seller Central] método de entrega

Para configurar métodos de envio que você deseja oferecer para atender aos seus pedidos da Amazon, consulte [Configurações e configurações de envio][10] em seu [!DNL Amazon Seller Central] conta.

## Configurações adicionais

Quando sua conta do Amazon está configurada e ativa, há várias [!DNL Commerce] recomendações que ajudam a simplificar o processo de integração do canal de vendas da Amazon.

### Revise e anote quaisquer produtos que deseja excluir

Talvez você não queira que alguns produtos sejam listados no Amazon. O canal de vendas da Amazon tem um mecanismo de regra de listagem usado para determinar quais produtos estão qualificados para publicação no Amazon. [Regras de listagem](./listing-rules.md) permite que você selecione subconjuntos de produtos a serem publicados (ou não) no seu [!DNL Amazon Seller Central] , por exemplo, por seleção de categoria ou definindo um ou mais atributos de produto. Like [!DNL Commerce] [catálogo](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;} ou [carrinho de compras](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;} regras de preço, atributos de produto usados para qualificação de listagem do Amazon devem ter **[!UICONTROL Use for Promo Rule Conditions]** defina como `Yes`. Consulte a **[!UICONTROL Use for Promo Rule Conditions]** em [Atributos do produto](https://docs.magento.com/user-guide/stores/attributes-product.html){target=&quot;_blank&quot;}.

### Defina seu [!DNL Amazon Seller Central] região para inativa

Para ajudar a facilitar a transição de dados sem erros durante a integração, é recomendável definir sua região do Amazon como `Inactive` em Configurações > Informações da conta > Configurações de férias. Consulte [Amazon: Status de Listagem para Férias][11]. Quando a configuração for concluída, altere o status de volta para `Active` no Amazon.

![Ícone Próximo](assets/btn-next.png) [**Continue a criar [!DNL Commerce] Atributos**](./ob-creating-magento-attributes.md)
