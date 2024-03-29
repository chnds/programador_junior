
### Tutorial de Instalação Local
Este tutorial irá guiá-lo através do processo de instalação do sistema de monitoramento de ramais em seu ambiente local. Certifique-se de ter instalado previamente um servidor web (como Apache) e um servidor de banco de dados MySQL ou MariaDB em sua máquina.

- Passo 1: Configuração do Ambiente
Certifique-se de ter o PHP instalado em sua máquina. Você pode verificar digitando php -v no terminal ou prompt de comando. Se não estiver instalado, baixe e instale o PHP a partir do site oficial (https://www.php.net/).

Baixe os arquivos do sistema de monitoramento de ramais e extraia-os em seu diretório de servidor web.

- Passo 2: Configuração do Banco de Dados
Importe o dump da base de dados comandos.sql fornecido no arquivo zip para o seu servidor de banco de dados. Você pode fazer isso usando o utilitário de linha de comando mysql ou através de uma interface gráfica como o phpMyAdmin.
bash

mysql -u seu_usuario -p sua_base_de_dados 
Após importar o dump, certifique-se de configurar as credenciais do banco de dados no arquivo config.php. Substitua os valores de DB_HOST, DB_USER, DB_PASS e DB_NAME com as configurações do seu ambiente local.
php

define('DB_HOST', 'localhost');
define('DB_USER', 'seu_usuario');
define('DB_PASS', 'sua_senha');
define('DB_NAME', 'seu_banco_de_dados');

- Passo 3: Configuração do Servidor Web
Certifique-se de que o seu servidor web está configurado corretamente para executar arquivos PHP. Você pode verificar se o PHP está funcionando corretamente acessando http://localhost/home em seu navegador. Crie um arquivo info.php no diretório raiz do seu servidor web com o seguinte conteúdo:
php

<?php phpinfo(); ?>
Certifique-se de que os arquivos .htaccess estão funcionando corretamente e a reescrita de URL está ativada. Se estiver usando o Apache, verifique se o módulo mod_rewrite está habilitado.
- Passo 4: Executando o Sistema
Após configurar o ambiente e o banco de dados, você pode acessar o sistema de monitoramento de ramais digitando o URL em seu navegador:


http://localhost/home
- Passo 5: Testando o Sistema
Após acessar o sistema, verifique se você pode visualizar os cartões de monitoramento de ramais corretamente, incluindo as correções e melhorias implementadas.

### Exemplos de melhoria: 

- Barra de pesquisa de ramais
- Ao clicar no ícone do Card, é possível ver mais informações.
- Front end mais atrativo.
- Arquivos JSON para facilitar a leitura e manipulaçao dos dados


Teste a funcionalidade de atualização automática dos dados a cada 10 segundos e verifique se as informações na tela são atualizadas corretamente.
Obs: pode ocorrer atrasos devido o cachê na leitura dos arquivos JSON.