---
title: '''Instalar [!DNL Channel Manager]'''
description: '"Instale o[!DNL Channel Manager] extensão.'''
exl-id: cb593ebd-f077-4a79-a661-bedf4cc70f97
source-git-commit: 638ba8c595652e66aa5f15f5207855c6d2b872d7
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---


# Instalar [!DNL Channel Manager]

Revise o [requisitos](onboard.md#requirements) e reúna as informações necessárias antes de instalar o Gerenciador de canais.

## Instalar a extensão

As instruções de instalação do Gerenciador de canais dependem do Adobe Commerce ou Magento Open Source ser implantado no local ou na infraestrutura de nuvem.

- Instalar em um [Instância no local](#install-on-an-on-premises-instance).

- Instalar em um [[!DNL Adobe Commerce] na instância da infraestrutura em nuvem](#install-adobe-commerce-on-cloud-infrastructure)

Ambos os métodos exigem o uso da CLI (Command Line Interface, interface de linha de comando).

>[!NOTE]
>
>Para obter ajuda com a instalação [!DNL Commerce] software usando a CLI, consulte [Instalação geral da CLI](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;}.

### Instalar em uma instância local

Use estas instruções para instalar [!DNL Channel Manager] no Adobe Commerce e no Magento Open Source para uma instância no local.

1. Faça logon no [!DNL Commerce] como um [usuário com permissões](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/file-system-perms.html){target=&quot;_blank&quot;} para gravar no [!DNL Commerce] sistema de arquivos.

1. Coloque seu site em [modo de manutenção](https://devdocs.magento.com/guides/v2.4/install-gde/install/cli/install-cli-subcommands-maint.html){target=&quot;_blank&quot;}.

   ```bash
   $ bin/magento maintenance:enable
   ```

1. No [!DNL Commerce] diretório raiz do projeto, adicione o Gerenciador de canais a `composer.json`.

   ```bash
    composer require magento/channel-manager --no-update
   ```

1. Se solicitado, insira as chaves de acesso em [!DNL Commerce] conta.

   Sua chave pública é seu nome de usuário; sua chave privada é sua senha.

1. Atualize as dependências e instale a extensão.

   ```bash
   composer update magento/channel-manager
   ```

   O `composer update` O comando atualiza somente as dependências necessárias para [!DNL Channel Manager]. Para atualizar todas as dependências, use este comando: `composer update`.

1. Aguarde até que o Composer conclua a atualização das dependências do projeto e resolva quaisquer erros.

1. Verifique a instalação do módulo:

   - Verifique o status do módulo.

      ```bash
      bin/magento module:status Magento_SalesChannels
      ```

      Resposta de exemplo:

      ```terminal
      Module is enabled
      ```

   - Se o módulo não estiver ativado, ative-o.

   ```bash
   bin/magento module:enable Magento_SalesChannels
   ```

1. Registre a extensão .

   ```bash
   bin/magento setup:upgrade
   ```

1. Se solicitado, recompile seu [!DNL Commerce] projeto.

   ```bash
   bin/magento setup:di:compile
   ```

1. Limpe o cache.

   ```bash
   bin/magento cache:clean
   ```

1. Desative o modo de manutenção.

   ```bash
   bin/magento maintenance:disable
   ```

### Instalar em uma instância do Adobe Commerce on Cloud Infrastructure

Trabalhe em uma ramificação de desenvolvimento ao adicionar uma extensão à instância da nuvem.

Para obter ajuda com o uso de ramificações, consulte [Introdução à criação de ramificações](https://devdocs.magento.com/cloud/env/environments-start.html#getstarted){target=&quot;_blank&quot;} na documentação do desenvolvedor do Adobe Commerce.

Durante a instalação, o nome da extensão (`magento\channel-manager`) é inserido automaticamente no [app/etc/config.php](https://devdocs.magento.com/cloud/live/sens-data-over.html#configuration-data)Arquivo {target=&quot;_blank&quot;}. Não é necessário editar o arquivo diretamente.

1. Na estação de trabalho local, altere para o diretório raiz do projeto Cloud.

1. Criar ou fazer check-out de um desenvolvimento [ramificação](https://devdocs-beta.magento.com/cloud/env/environments-start.html#getstarted){target=&quot;_blank&quot;}.

1. Com o nome do Composer, adicione a extensão ao `require` da seção `composer.json` arquivo.

   ```bash
   composer require require magento/module-sales-channels-extension --no-update
   ```

1. Atualize as dependências e instale a extensão.

   ```bash
   composer update magento/module-sales-channels-extension
   ```

   O `composer update` O comando atualiza somente as dependências necessárias para [!DNL Channel Manager]. Para atualizar todas as dependências, use este comando: `composer update`.

1. Adicionar, confirmar e enviar alterações de código-push - inclua alterações nas duas `composer.lock` e `composer.json` arquivo.

   ```bash
   $ git add -A
   ```

   ```bash
   $ git commit -m “Install channel manager extension” 
   ```

   ```bash
   $ git push origin <branch-name>
   ```

1. Depois que o processo de criação e implantação for concluído, use o SSH para fazer logon no ambiente remoto e verificar se a extensão foi instalada corretamente.

```bash
   bin/magento module:status Magento_SalesChannels
```

Resposta de exemplo:

```terminal
Module is enabled
```

Se o módulo estiver desativado, [habilite-a no ambiente local](https://devdocs.magento.com/cloud/howtos/install-components.html#manage-extensions) e implante as alterações.


1. Depois de instalar a extensão com êxito, faça logon no [!UICONTROL Admin] para [configurar o Conector de serviços do Commerce](connect.md).

   >[!NOTE]
   >
   >Para obter instruções sobre como atualizar o Gerenciador de canais para uma nova versão, consulte [Atualizar módulos e extensões](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html){target=&quot;_blank&quot;}.


## Solução de problemas

Use as informações a seguir para resolver erros que ocorrem durante o processo de instalação do Gerenciador de Canais.

### Chaves do Composer Incorretas

Se a variável [chaves de acesso](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target=&quot;_blank&quot;} usado para autenticar no repositório do Composer são inválidos ou não estão vinculados ao [!DNL MAGE ID] usado para se inscrever na [!DNL Channel Manager] , o seguinte erro é exibido.

```terminal
Could not find a matching version of package magento/channel-manager. Check the package spelling, your version constraint and that the package is available in a stability which matches your minimum-stability (stable).
```

Verifique a configuração da chave:

1. Encontre a localização da variável `auth.json` arquivo:

   ```bash
   $ composer config –global home
   ```

1. Visualize o `auth.json` arquivo.

   ```bash
   $ cat /path/to/auth.json
   ```

1. Verifique se as credenciais no auth.json correspondem [as chaves associadas à MAGE ID](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target=&quot;_blank&quot;} usado para registrar-se no serviço Gerenciador de Canais.

### Memória insuficiente para PHP

O erro a seguir é exibido se o sistema não tiver memória suficiente alocada para PHP.

```terminal
Fatal error: Allowed memory size of 2146435072 bytes exhausted (tried to allocate 4096 bytes) in phar:///usr/local/bin/composer/src/Composer/DependencyResolver/RuleWatchGraph.php on line 52
```

Use qualquer um dos métodos a seguir para resolver o problema de memória:

- [Aumente o limite de memória para PHP](https://devdocs.magento.com/cloud/project/magento-app-php-ini.html#increase-php-memory-limit){target=&quot;_blank&quot;} no ambiente `php.ini` arquivo. Além disso, verifique se a instância do Commerce tem a variável [valores recomendados](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html){target=&quot;_blank&quot;} para outras configurações de PHP.

- Especifique o limite de memória a partir da linha de comando.

   ```bash
   $ php -d memory_limit=-1 \[path to composer]/composer require magento/payment-services.
   ```

   Por exemplo:

   ```bash
   $ php-d memory_limit=-1 vendor/bin/composer require magento/channel-manager
   ```

### Vista ausente

Se você receber um erro sobre um ausente `process_catalog_exporter_view` durante a instalação do Gerenciador de canais, tente [atualizar os indexadores](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-index.html#config-cli-subcommands-index-reindex){target=&quot;_blank&quot;}.

```bash
php bin/magento indexer:refresh
```

### Erros de implantação na nuvem

Para problemas ao implantar a extensão na nuvem, consulte [falha na implantação de extensão](https://devdocs.magento.com/cloud/trouble/trouble_comp-deploy-fail.html){target=&quot;_blank&quot;}.
