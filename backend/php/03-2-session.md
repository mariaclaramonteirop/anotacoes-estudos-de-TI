- [SESSION](https://www.php.net/manual/pt_BR/features.sessions.php#:~:text=Sessões%20¶,apelo%20do%20seu%20web%20site.) -> Sessões **são uma forma simples de armazenar dados para usuários individuais usando um ID de sessão único**. Sessões podem ser usadas para persistir informações entre requisições de páginas.

- Para criar e resgatar uma Sessão usa-se o $_SESSION['nomeDaSessao'] e pode-se atribuir um valor a ela:  $_SESSION['nomeDaSessao']=ValorDaSessao;
``` php
$_SESSION['name'] = 'Maria';

// em outro arquivo ela pode ser resgatada
echo $_SESSION['name'];
```

- Porém para que essa sessão seja criada, ela precisa ser **INICIADA**. Para iniciar uma sessão usa-se o **session_start()**.
	- Para Resgatar e EXIBIR o valor da sessão, o session_start(); precisa estar no arquivo em que essa sessão será resgatada.
``` php
session_start();

$_SESSION['name'] = 'Maria';

// em outro arquivo ela pode ser resgatada
echo $_SESSION['name'];
```

- **IMPORTANTE** -> No navegador o valor guardado é o ID da Sessão e não o valor dela, logo, não é possível resgatar/acessar os valores dessa sessão pelo navegador.

- se for preciso localizar e descobrir qual o id da sua sessão, pode-se utilizar o session_id(); Ele vai exibir o identificador(ID) da sessão criada;
``` php
session_start();

echo session_id(); // exibe o ID da sessão

$_SESSION['name'] = 'Maria';

// em outro arquivo ela pode ser resgatada
echo $_SESSION['name'];
```

- Para verificar a existência de uma sessão podemos usar o isset()
``` PHP

if(isset($_SESSION['name']))
{
	echo 'Sessão existe' . $_SESSION['name'];
}else{
	 echo 'Sessão não existe';
}

// OU com Operador Ternário

echo (isset($_SESSION['name'])) ? echo 'Sessão existe' . $_SESSION['name'] :'Sessão não existe';

```

- Para excluir **uma** sessão pode-se usar o unset()
``` PHP
unset($_SESSION['name']);

echo (isset($_SESSION['name'])) ? echo 'Sessão existe' . $_SESSION['name'] :'Sessão não existe';

```

- Para excluir todas as sessões de uma vez, pode-se usar o session_destroy()
``` PHP
session_destroy();

echo (isset($_SESSION['name'])) ? echo 'Sessão existe' . $_SESSION['name'] :'Sessão não existe';

```

- Para gerar um novo id para sessão,   pode-se usar o session_regenerate_id()
``` php
session_start();

session_regenerate_id()

echo session_id(); // exibe o ID da sessão

$_SESSION['name'] = 'Maria';
```

### Manipulação de Sessão

- **Modificar e Acessar Sessões:** Além de atribuir valores diretamente a `$_SESSION['nomeDaSessao']`, você também pode modificar ou acessar os valores existentes da mesma forma. Por exemplo:

``` php 
    $_SESSION['name'] = 'João'; // Atribui um valor
    $_SESSION['name'] = 'Ana'; // Modifica o valor existente
```

### Configurações de Sessão

- **Configurações de Sessão:** O comportamento das sessões pode ser configurado no arquivo php.ini ou no código PHP usando `session_set_cookie_params()` e outras funções relacionadas a sessões, como `session_cache_expire()` para definir o tempo de expiração do cache da sessão.

### Segurança

- **Segurança:** É importante considerar questões de segurança ao lidar com sessões. Por exemplo, evite confiar apenas na sessão para autenticação e autorização; use HTTPS para proteger os dados da sessão durante a transmissão; e evite o uso de IDs de sessão em URLs para evitar ataques de session fixation.

### Controle de Cache

- **Controle de Cache:** O cabeçalho HTTP `Cache-Control` pode ser usado para controlar o cache de páginas que contêm informações de sessão. Certifique-se de configurar adequadamente os cabeçalhos de resposta para evitar o armazenamento em cache de páginas confidenciais.

### Armazenamento de Dados

- **Armazenamento de Dados:** Embora `$_SESSION` seja útil para armazenar pequenas quantidades de dados, é importante não abusar dele para evitar o consumo excessivo de memória do servidor. Considere outras opções de armazenamento, como bancos de dados, para dados mais complexos ou sensíveis.
