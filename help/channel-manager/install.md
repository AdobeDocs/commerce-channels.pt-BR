---
title: 'Instalar [!DNL Channel Manager]'
description: '''Instalar o[!DNL Channel Manager] extensão."'
role: Admin, Developer
feature: Sales Channels, Install
exl-id: cb593ebd-f077-4a79-a661-bedf4cc70f97
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---


# Instalar [!DNL Channel Manager]

Revise o [requisitos](onboard.md#requirements) e colete as informações necessárias antes de instalar o Channel Manager.

## Instalar a extensão

As instruções de instalação do Channel Manager dependem se o Adobe Commerce ou o Magento Open Source é implantado no local ou na infraestrutura em nuvem.

- Instalar em um [Instância local](#install-on-an-on-premises-instance).

- Instalar em um [[!DNL Adobe Commerce] na instância da infraestrutura em nuvem](#install-adobe-commerce-on-cloud-infrastructure)

Ambos os métodos exigem o uso da CLI (Command Line Interface, interface de linha de comando).

>[!NOTE]
>
>Para obter ajuda com a instalação do [!DNL Commerce] usando a CLI, consulte [Instalar uma extensão](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

### Instalar em uma instância local

Use estas instruções para instalar o [!DNL Channel Manager] no Adobe Commerce e no Magento Open Source para uma instância local.

1. Faça logon no [!DNL Commerce] servidor as a [usuário com permissões](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/file-system/configure-permissions.html) para gravar na [!DNL Commerce] sistema de arquivos.

1. Coloque seu site em [modo de manutenção](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/maintenance-mode.html).

   ```bash
   $ bin/magento maintenance:enable
   ```

1. No [!DNL Commerce] diretório raiz do projeto, adicionar Gerenciador de canal a `composer.json`.

   ```bash
    composer require magento/channel-manager --no-update
   ```

1. Se solicitado, insira as chaves de acesso do [!DNL Commerce] conta.

   Sua chave pública é seu nome de usuário; sua chave privada é sua senha.

1. Atualize as dependências e instale a extensão.

   ```bash
   composer update magento/channel-manager
   ```

   A variável `composer update` atualiza somente as dependências necessárias para [!DNL Channel Manager]. Para atualizar todas as dependências, use este comando: `composer update`.

1. Aguarde até que o Composer conclua a atualização das dependências do projeto e resolva quaisquer erros.

1. Verifique a instalação do módulo:

   - Verifique o status do módulo.

     ```bash
     bin/magento module:status Magento_SalesChannels
     ```

     Exemplo de resposta:

     ```terminal
     Module is enabled
     ```

   - Se o módulo não estiver ativado, ative-o.

   ```bash
   bin/magento module:enable Magento_SalesChannels
   ```

1. Registre a extensão.

   ```bash
   bin/magento setup:upgrade
   ```

1. Se solicitado, recompile o [!DNL Commerce] projeto.

   ```bash
   bin/magento setup:di:compile
   ```

1. Limpe o cache.

   ```bash
   bin/magento cache:clean
   ```

1. Desabilitar modo de manutenção.

   ```bash
   bin/magento maintenance:disable
   ```

### Instalar em uma instância do Adobe Commerce na infraestrutura em nuvem

Trabalhe em uma ramificação de desenvolvimento ao adicionar uma extensão à instância da nuvem.

Para obter ajuda sobre como usar ramificações, consulte [Introdução à criação de ramificações](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/cli-branches.html) no _Guia do Commerce na infraestrutura em nuvem_.

Durante a instalação, o nome da extensão (`magento\channel-manager`) é inserido automaticamente no [app/etc/config.php](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/store-settings.html) arquivo. Não é necessário editar o arquivo diretamente.

1. Na estação de trabalho local, altere para o diretório raiz do projeto na nuvem.

1. Criar ou conferir um desenvolvimento [ramificação](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/cli-branches.html).

1. Usando o nome do Compositor, adicione a extensão ao `require` seção do `composer.json` arquivo.

   ```bash
   composer require magento/module-sales-channels-extension --no-update
   ```

1. Atualize as dependências e instale a extensão.

   ```bash
   composer update magento/module-sales-channels-extension
   ```

   A variável `composer update` atualiza somente as dependências necessárias para [!DNL Channel Manager]. Para atualizar todas as dependências, use este comando: `composer update`.

1. Adicionar, confirmar e enviar alterações de código - incluir alterações em ambos os `composer.lock` e `composer.json` arquivo.

   ```bash
   $ git add -A
   ```

   ```bash
   $ git commit -m "Install channel manager extension" 
   ```

   ```bash
   $ git push origin <branch-name>
   ```

1. Depois que o processo de criação e implantação for concluído, use o SSH para fazer logon no ambiente remoto e verificar se a extensão foi instalada corretamente.

```bash
   bin/magento module:status Magento_SalesChannels
```

Exemplo de resposta:

```terminal
Module is enabled
```

Se o módulo estiver desativado, [habilite-o em seu ambiente local](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/extensions.html) e implantar suas alterações.


1. Depois de instalar a extensão com êxito, faça logon na [!UICONTROL Admin] para [configurar o Commerce Services Connector](connect.md).

   >[!NOTE]
   >
   >Para obter instruções sobre como atualizar o Gerenciador de canais para uma nova versão, consulte [Atualizar módulos e extensões](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html).


## Solução de problemas

Use as informações a seguir para resolver erros que ocorrem durante o processo de instalação do Gerenciador de Canais.

### Chaves do compositor incorretas

Se a variável [chaves de acesso](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) para autenticar no repositório do Composer são inválidos ou não estão vinculados ao [!DNL MAGE ID] usado para se inscrever no [!DNL Channel Manager] serviço, o seguinte erro é exibido.

```terminal
Could not find a matching version of package magento/channel-manager. Check the package spelling, your version constraint and that the package is available in a stability which matches your minimum-stability (stable).
```

Verifique a configuração da chave:

1. Localize o `auth.json` arquivo:

   ```bash
   $ composer config –global home
   ```

1. Exibir o `auth.json` arquivo.

   ```bash
   $ cat /path/to/auth.json
   ```

1. Verifique se as credenciais no auth.json correspondem [as chaves associadas à ID da IMAGEM](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) utilizado para registrar-se no serviço Gerenciador de canais.

### Memória insuficiente para o PHP

O seguinte erro é exibido se o sistema não tem memória suficiente alocada para o PHP.

```terminal
Fatal error: Allowed memory size of 2146435072 bytes exhausted (tried to allocate 4096 bytes) in phar:///usr/local/bin/composer/src/Composer/DependencyResolver/RuleWatchGraph.php on line 52
```

Use um dos seguintes métodos para resolver o problema de memória:

- [Aumentar o limite de memória do PHP](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/php-settings.html) no ambiente `php.ini` arquivo. Além disso, verifique se a instância do Commerce tem o [valores recomendados](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) para outras configurações do PHP.

- Especifique o limite de memória na linha de comando.

  ```bash
  $ php -d memory_limit=-1 \[path to composer]/composer require magento/payment-services.
  ```

  Por exemplo:

  ```bash
  $ php-d memory_limit=-1 vendor/bin/composer require magento/channel-manager
  ```

### Visualização ausente

Se você receber um erro sobre uma falha `process_catalog_exporter_view` durante a instalação do Gerenciador de canais, tente [atualizar os indexadores](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html).

```bash
php bin/magento indexer:refresh
```

### Erros de implantação de nuvem

Para problemas ao implantar a extensão na nuvem, consulte [falha na implantação da extensão](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment.html).
