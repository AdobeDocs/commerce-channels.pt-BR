---
title: Tarefas de pré-configuração de  [!DNL Amazon sales channel]
description: Revise as tarefas necessárias que devem ser concluídas antes de integrar sua loja de Adobe Commerce ou Magento Open Source no Sales Channel Amazon.
role: Admin, Developer
feature: Sales Channels, Install, Configuration
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Tarefas de pré-configuração para [!DNL Amazon sales channel]

Antes da [Integração da Loja](./store-integration.md), verifique se a conta do [!DNL Amazon Seller Central] e a conta do [!DNL Commerce] estão prontas para a integração. Para uma integração bem-sucedida, há algumas tarefas de pré-configuração necessárias.

Quando você configura sua primeira loja do Amazon no canal de vendas do Amazon, uma lista de tarefas de configuração é exibida. É recomendável examinar essas tarefas antes de [adicionar um armazenamento do Amazon](./store-integration.md). Depois de adicionar sua primeira loja, você pode revisar essas tarefas na exibição Aprendizado e Preparação do canal de vendas da Amazon [página inicial](./amazon-sales-channel-home.md).

## 1. Habilitar tarefas em segundo plano em [!DNL Commerce]

Todos os produtos e dados sincronizados entre o [!DNL Commerce] e o Amazon são gerenciados por um [trabalho do cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html). Quando você conclui tarefas como adicionar ou atualizar listas e receber pedidos, um trabalho cron envia e recebe dados entre o back-end do [!DNL Commerce] e a conta do [!DNL Amazon Seller Central].

- [Habilitar [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html).

- Para obter o desempenho máximo, [defina [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/config/advanced/system.html) para ser executado uma vez a cada cinco minutos.

## 2. Crie sua conta [!DNL Amazon Seller Central]

Antes de começar a configurar seu canal de vendas do Amazon, você deve ter uma conta [!DNL Amazon Seller Central] ativa. Se você não tiver uma conta de Vendedor Amazon existente na região [América do Norte (EUA, CA, MX)](https://sell.amazon.com/){target="_blank"} ou [Europa (Reino Unido)](https://sell.amazon.co.uk/sell-online/beginners-guide){target="_blank"}, poderá concluir o processo de configuração da conta de vendedor da Amazon.

O canal de vendas da Amazon requer uma conta [!DNL Professional Seller] em [!DNL Amazon Seller Central]. A Amazon cobra uma assinatura mensal e taxas de venda. Consulte [Amazon: escolha seu plano de vendas](https://sell.amazon.com/pricing.html){target="_blank"}.

## 3. Certifique-se de que você é um vendedor Amazon aprovado

Para integrar, você deve ter uma conta aprovada do [!DNL Amazon Seller Central]. Sua conta não deve ter restrições para produtos ou categorias. Alguns produtos e categorias exigem aprovação antes da criação de listas. Revise as políticas da Amazon para categoria e aprovação de produtos para garantir que seus produtos sejam aprovados. Consulte [Amazon: categorias e produtos que exigem aprovação](https://sellercentral.amazon.com/gp/help/200333160){target="_blank"} (logon Central do Vendedor necessário).

Também é importante garantir que você tenha configurado o seguinte na conta do [!DNL Amazon Seller Central]:

- Certifique-se de que sua política de devolução seja tão boa quanto ou melhor do que a política de devolução da Amazon. Consulte [Amazon: Política de Retorno](https://www.amazon.com/gp/help/customer/display.html){target="_blank"}.

- Certifique-se de que suas configurações de imposto estejam definidas. Consulte [Amazon: Políticas Fiscais](https://sellercentral.amazon.com/gp/help/external/help.html){target="_blank"} (logon Central do Vendedor necessário).

- Verifique se os métodos de envio estão configurados com precisão. Para configurar os métodos de envio que [!DNL Commerce] são oferecidos aos clientes para atender aos seus pedidos da Amazon, atualize a [Amazon: Configurações de Envio](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target="_blank"} na sua conta [!DNL Amazon Seller Central].

## 4. Certifique-se de que seu VAT esteja configurado para suas lojas

(Usado principalmente por vendedores do Reino Unido.) A Amazon recomenda se inscrever no [Serviço de Cálculo de IVA da Amazon](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target="_blank"}. Se escolher um método diferente, é responsável pela conformidade com o IVA.

>[!NOTE]
>
>Pode levar de 10 a 14 dias para que a Amazon verifique e ative sua conta do Serviço de Cálculo de IVA.

## 5. Aumentar o número de correspondências automáticas de catálogo

Durante a integração, o canal de vendas da Amazon usa atributos de produto para corresponder às suas listas existentes do Amazon (se aplicável) a produtos existentes no catálogo [!DNL Commerce]. Após a integração, esses atributos de produto são usados para publicar seus itens de catálogo do [!DNL Commerce] em uma lista da Amazon e para sincronizar os dados de produto entre o [!DNL Commerce] e a Amazon.

Para que o número mais alto de produtos do [!DNL Commerce] corresponda automaticamente às listagens do Amazon, você deve criar um conjunto de atributos de produto para o catálogo [!DNL Commerce]. Antes de configurar sua loja de canais de vendas do Amazon, você deve adicionar [!DNL Commerce] atributos de produto para corresponder a esses atributos do Amazon, por exemplo: ASIN, EAN, ISBN, UPC ou GCID. Consulte [Criar um atributo de produto em [!DNL Commerce]](./ob-creating-magento-attributes.md).

## 6. Configure sua moeda e conversão (conforme necessário)

Se o armazenamento do Amazon usar uma moeda diferente da configurada para o armazenamento do [!DNL Commerce], [habilite a moeda](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html) e defina a [taxa de conversão de moeda](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-update.html).

## 7. Crie um atributo de condição de produto (conforme necessário)

Se suas listas do Amazon contiverem mais de uma condição de produto (como _novo_, _usado_ ou _como novo_), crie um atributo [!DNL Commerce] e atribua valores de condição. Você deve mapear esse atributo durante a integração para o atributo de produto Condição Amazon. Consulte [Criação de atributos para o Amazon](./ob-creating-magento-attributes.md).

## 8. Configurar seu método de envio do [!DNL Amazon Seller Central]

Para configurar os métodos de envio que você deseja oferecer para atender aos seus pedidos da Amazon, consulte _Configurações e Configurações de Envio_ na sua conta [!DNL Amazon Seller Central].

## Configurações adicionais

Quando sua conta do Amazon está configurada e ativa, há várias recomendações do [!DNL Commerce] que ajudam a simplificar o processo de integração do canal de vendas do Amazon.

### Analise e observe todos os produtos que deseja excluir

Talvez você não queira que alguns produtos sejam listados no Amazon. O canal de vendas do Amazon tem um mecanismo de regras de listagem usado para determinar quais produtos estão qualificados para publicação no Amazon. [As regras de listagem](./listing-rules.md) permitem que você selecione subconjuntos de produtos a serem publicados (ou não) na sua conta [!DNL Amazon Seller Central], por exemplo, por seleção de categoria ou definindo um ou mais atributos de produto. Como as regras de preço do [!DNL Commerce] [catálogo](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html) ou [carrinho de compras](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html), os atributos de produto usados para a qualificação de listagem do Amazon devem ter **[!UICONTROL Use for Promo Rule Conditions]** definido como `Yes`. Consulte o **[!UICONTROL Use for Promo Rule Conditions]** em [Atributos do produto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

### Defina a região [!DNL Amazon Seller Central] como inativa

Para ajudar a facilitar a transição de dados sem erros durante a integração, é recomendável definir o status da região do Amazon como `Inactive` em Configurações > Informações da conta > Configurações de férias. Quando a configuração estiver concluída, altere o status novamente para `Active` no Amazon.

![Próximo ícone](assets/btn-next.png) [**Continue para Criar [!DNL Commerce] Atributos**](./ob-creating-magento-attributes.md)
