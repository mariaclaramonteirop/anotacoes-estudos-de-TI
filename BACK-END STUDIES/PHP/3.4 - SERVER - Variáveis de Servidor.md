[SERVER](https://www.php.net/manual/pt_BR/reserved.variables.server.php) - A superglobal $_SERVER no PHP serve para fornecer informações sobre o ambiente do servidor e a requisição HTTP atual. Ela é essencial para acessar detalhes sobre como o script PHP está sendo executado e as características da requisição que o acionou.

Aqui estão algumas das principais funções e usos da superglobal $_SERVER:

1. **Identificação do Ambiente do Servidor**: $_SERVER fornece informações sobre o servidor onde o script está sendo executado, como o nome do host, a versão do software do servidor, e o sistema operacional.
``` php
echo "Nome do Host: " . $_SERVER['HTTP_HOST'] . "<br>";
echo "Versão do Software do Servidor: " . $_SERVER['SERVER_SOFTWARE'] . "<br>";
echo "Sistema Operacional do Servidor: " . php_uname('s') . "<br>";

```

2. **Detalhes da Requisição HTTP**: É possível obter detalhes sobre a requisição HTTP atual, como o método utilizado (GET, POST, etc.), os parâmetros da URL, o endereço IP do cliente, e a string de User-Agent do navegador.
```php
echo "Método da Requisição: " . $_SERVER['REQUEST_METHOD'] . "<br>";
echo "Endereço IP do Cliente: " . $_SERVER['REMOTE_ADDR'] . "<br>";
echo "String de User-Agent: " . $_SERVER['HTTP_USER_AGENT'] . "<br>";

```

3. **Personalização Dinâmica de Páginas**: Com base nas informações fornecidas por $_SERVER, é possível personalizar dinamicamente o conteúdo das páginas da web. Por exemplo, você pode adaptar a saída do seu script PHP com base no navegador do usuário ou no método de requisição utilizado.
```php
if(strpos($_SERVER['HTTP_USER_AGENT'], 'Firefox') !== false) {
    echo "Você está usando o Firefox!<br>";
} elseif(strpos($_SERVER['HTTP_USER_AGENT'], 'Chrome') !== false) {
    echo "Você está usando o Chrome!<br>";
} else {
    echo "Seu navegador não é suportado.<br>";
}

```

1. **Segurança e Autenticação**: Algumas chaves em $_SERVER são usadas em sistemas de autenticação e segurança para validar a origem da requisição ou tomar decisões com base no ambiente do servidor.
```php
if($_SERVER['HTTPS'] === 'on') {
    echo "Esta é uma conexão segura.<br>";
} else {
    echo "Esta não é uma conexão segura.<br>";
}
```

5. **Depuração e Registro de Atividades**: As informações disponíveis em $_SERVER são frequentemente utilizadas para fins de depuração, registro de atividades e auditoria, ajudando os desenvolvedores a entender melhor como seus scripts estão sendo acessados e executados.
```php
// Log do IP do cliente e da página acessada
$logfile = fopen('access.log', 'a');
fwrite($logfile, date('Y-m-d H:i:s') . " - IP: " . $_SERVER['REMOTE_ADDR'] . " - Página: " . $_SERVER['REQUEST_URI'] . "\n");
fclose($logfile);

```

## Reutilizando o exemplo da superglobal $_ ENV

No exemplo a seguir, foi utilizado o __ DIR __ para localizar o diretório  do index.php desde a raiz.
```php
//index.php
require __DIR__.'/vendor/autoload.php';

$dotenv = Dotenv\Dotenv::createImmutable(__DIR__); // DIR localiza o diretório raiz do index.php
$dotenv->load();
```

A superglobal $_ SERVER, tem um indice que faz a mesma coisa, o `DOCUMENT_ROOT`. Logo podemos substituir o __ DIR __ pelo $_ SERVER['DOCUMENT_ROOT'].

```php
//index.php
require __DIR__.'/vendor/autoload.php';

$dotenv = Dotenv\Dotenv::createImmutable($_SERVER['DOCUMENT_ROOT']); // $_SERVER['DOCUMENT_ROOT'] localiza o diretório raiz do index.php
$dotenv->load();
```
