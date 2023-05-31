---
title: Tarefas de pré-configuração do [!DNL Amazon sales channel]
description: Revise as tarefas necessárias que devem ser concluídas antes de integrar sua loja de Adobe Commerce ou Magento Open Source no Sales Channel Amazon.
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 0%

---

# Tarefas de pré-configuração do [!DNL Amazon sales channel]

Antes [Integração da loja](./store-integration.md), você deve garantir que seus [!DNL Amazon Seller Central] e seu [!DNL Commerce] conta estão prontas para a integração. Para uma integração bem-sucedida, há algumas tarefas de pré-configuração necessárias.

Quando você configura sua primeira loja do Amazon no canal de vendas do Amazon, uma lista de tarefas de configuração é exibida. É recomendável que você revise essas tarefas antes de [adicionar uma loja da Amazon](./store-integration.md). Depois de adicionar sua primeira loja, você pode revisar essas tarefas na visualização Learning and Preparation do canal de vendas do Amazon [home page](./amazon-sales-channel-home.md).

## 1. Ativar tarefas em segundo plano no [!DNL Commerce]

Todos os produtos e dados sincronizados entre [!DNL Commerce] e o Amazon é gerenciado por um [trabalho cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html). Quando você conclui tarefas como adicionar ou atualizar listas e receber ordens, um trabalho cron envia e recebe dados entre suas [!DNL Commerce] back-end e seu [!DNL Amazon Seller Central] conta.

- [Ativar [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html).

- Para desempenho máximo, [set [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/config/advanced/system.html) para ser executado uma vez a cada cinco minutos.

## 2. Crie seu [!DNL Amazon Seller Central] account

Antes de começar a configurar seu canal de vendas do Amazon, você deve ter um [!DNL Amazon Seller Central] conta. Se você não tiver uma conta do Amazon Seller na [América do Norte (US, CA, MX)](https://sell.amazon.com/){target="_blank"} or [European (UK)](https://sell.amazon.co.uk/sell-online/beginners-guide){target="_blank"} , você pode concluir o processo de configuração da conta de vendedor do Amazon.

O canal de vendas da Amazon exige um [!DNL Professional Seller] conta em [!DNL Amazon Seller Central]. A Amazon cobra uma assinatura mensal e taxas de venda. Consulte [Amazon: escolha seu plano de vendas](https://sell.amazon.com/pricing.html){target="_blank"}.

## 3. Certifique-se de que você é um vendedor Amazon aprovado

Para integrar, você deve ter um [!DNL Amazon Seller Central] conta. Sua conta não deve ter restrições para produtos ou categorias. Alguns produtos e categorias exigem aprovação antes da criação de listas. Revise as políticas da Amazon para categoria e aprovação de produtos para garantir que seus produtos sejam aprovados. Consulte [Amazon: categorias e produtos que exigem aprovação](https://sellercentral.amazon.com/gp/help/200333160){target="_blank"} (logon da Central de Vendedores necessário).

Também é importante garantir que você tenha configurado o seguinte no [!DNL Amazon Seller Central] conta:

- Certifique-se de que sua política de devolução seja tão boa quanto ou melhor do que a política de devolução da Amazon. Consulte [Amazon: política de devolução](https://www.amazon.com/gp/help/customer/display.html){target="_blank"}.

- Certifique-se de que suas configurações de imposto estejam definidas. Consulte [Amazon: Políticas de Impostos](https://sellercentral.amazon.com/gp/help/external/help.html){target="_blank"} (logon da Central de Vendedores necessário).

- Verifique se os métodos de envio estão configurados com precisão. Para configurar os métodos de entrega que [!DNL Commerce] são oferecidos aos clientes para atender aos seus pedidos da Amazon, atualize o [Amazon: Configurações de envio](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target="_blank"} no seu [!DNL Amazon Seller Central] conta.

## 4. Certifique-se de que seu VAT esteja configurado para suas lojas

(Usado principalmente por vendedores do Reino Unido.) A Amazon recomenda se inscrever no [Serviço de Cálculo de IVA da Amazon](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target="_blank"}. Se escolher um método diferente, é responsável pela conformidade com o IVA.

>[!NOTE]
>
>Pode levar de 10 a 14 dias para que a Amazon verifique e ative sua conta do Serviço de Cálculo de IVA.

## 5. Aumentar o número de correspondências automáticas de catálogo

Durante a integração, o canal de vendas da Amazon usa atributos de produto para corresponder suas listas existentes do Amazon (se aplicável) a produtos existentes em seu [!DNL Commerce] catálogo. Após a integração, esses atributos de produto são usados para publicar o [!DNL Commerce] itens de catálogo para uma lista do Amazon e para sincronizar os dados do produto entre [!DNL Commerce] e Amazon.

Para ter o número mais alto de [!DNL Commerce] automaticamente com as listagens do Amazon, você deve criar um conjunto de atributos de produto para [!DNL Commerce] catálogo. Antes de configurar sua loja de canais de vendas da Amazon, você deve adicionar [!DNL Commerce] atributos de produto para corresponder a esses atributos do Amazon, por exemplo: ASIN, EAN, ISBN, UPC ou GCID. Consulte [Criar um atributo de produto no [!DNL Commerce]](./ob-creating-magento-attributes.md).

## 6. Configure sua moeda e conversão (conforme necessário)

Se a loja da Amazon usar uma moeda diferente da configurada para a [!DNL Commerce] armazenar, [ativar a moeda](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html) e defina o [taxa de conversão de moeda](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-update.html).

## 7. Crie um atributo de condição de produto (conforme necessário)

Se suas listagens do Amazon contiverem mais de uma condição de produto (como _novo_, _usado_ ou _curtir o novo_), crie um [!DNL Commerce] atribuir e atribuir valores de condição. Você deve mapear esse atributo durante a integração para o atributo de produto Condição Amazon. Consulte [Criação de atributos para o Amazon](./ob-creating-magento-attributes.md).

## 8. Configure seu [!DNL Amazon Seller Central] método de envio

Para configurar métodos de envio que você deseja oferecer para atender aos seus pedidos do Amazon, consulte _Configurações e configurações de envio_ no seu [!DNL Amazon Seller Central] conta.

## Configurações adicionais

Quando sua conta do Amazon está configurada e ativa, há vários [!DNL Commerce] recomendações que ajudam a simplificar o processo de integração dos canais de vendas da Amazon.

### Analise e observe todos os produtos que deseja excluir

Talvez você não queira que alguns produtos sejam listados no Amazon. O canal de vendas do Amazon tem um mecanismo de regras de listagem usado para determinar quais produtos estão qualificados para publicação no Amazon. [Regras de listagem](./listing-rules.md) permitem selecionar subconjuntos de produtos a serem publicados (ou não) no seu [!DNL Amazon Seller Central] por seleção de categoria ou definindo um ou mais atributos de produto. Curtir [!DNL Commerce] [catálogo](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html) ou [carrinho de compras](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html) regras de preço, os atributos de produto usados para a qualificação de listagem do Amazon devem ter **[!UICONTROL Use for Promo Rule Conditions]** definir como `Yes`. Consulte a **[!UICONTROL Use for Promo Rule Conditions]** in [Atributos do produto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

### Defina seu [!DNL Amazon Seller Central] região para inativo

Para ajudar a facilitar a transição de dados sem erros durante a integração, é recomendável definir a região do Amazon como `Inactive` status em Configurações > Informações da conta > Configurações de férias. Quando a configuração estiver concluída, altere o status novamente para `Active` no Amazon.

![Ícone Avançar](assets/btn-next.png) [**Continue em Criação [!DNL Commerce] Atributos**](./ob-creating-magento-attributes.md)
