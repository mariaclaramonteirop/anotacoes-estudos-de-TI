
- ENV - Em PHP, o `ENV` refere-se ao ambiente de execução do programa, que armazena variáveis de ambiente disponíveis para o script em execução. As variáveis de ambiente são definidas pelo sistema operacional ou pelo servidor da web e são acessadas pelo PHP através da superglobal `$_ENV`.

- Essas variáveis de ambiente podem conter informações úteis, como configurações específicas do servidor, diretórios de arquivos temporários, credenciais de banco de dados, entre outras. O acesso a essas informações por meio do `$_ENV` permite que os scripts PHP sejam configurados dinamicamente com base no ambiente de execução.

- Se você der um var_dump na supergloba **ENV** são exibidas diversas variáveis de ambiente.
``` php
var_dump($_ENV);
```

Para acessar uma variável de ambiente específica, você pode simplesmente usar sua chave como índice no array `$_ENV`. Por exemplo:
``` php
$database_host = $_ENV['DB_HOST'];
$database_user = $_ENV['DB_USER'];
$database_pass = $_ENV['DB_PASS'];
```

1. **Acessando variáveis de ambiente em um script PHP:**

```php
// Suponha que as variáveis de ambiente DB_HOST, DB_USER e DB_PASS estejam definidas

// Acessando as variáveis de ambiente
$database_host = $_ENV['DB_HOST'];
$database_user = $_ENV['DB_USER'];
$database_pass = $_ENV['DB_PASS'];

// Usando as variáveis de ambiente para conectar ao banco de dados
$conn = new mysqli($database_host, $database_user, $database_pass);
if ($conn->connect_error) {
    die("Erro ao conectar ao banco de dados: " . $conn->connect_error);
}
echo "Conexão bem-sucedida ao banco de dados!";
```

2. **Definindo variáveis de ambiente no servidor ou arquivo .env:**

No servidor ou arquivo `.env`, você pode definir as variáveis de ambiente da seguinte maneira:

```
DB_HOST=seu_host
DB_USER=seu_usuario
DB_PASS=sua_senha
```

E então, no código PHP, você pode acessá-las como mostrado no exemplo anterior.

3. **Definindo variáveis de ambiente programaticamente:**
	- **putenv** — Define o valor de uma variável de ambiente

```php
// Definindo variáveis de ambiente programaticamente
putenv("DB_HOST=seu_host");
putenv("DB_USER=seu_usuario");
putenv("DB_PASS=sua_senha");

// Acessando as variáveis de ambiente
$database_host = $_ENV['DB_HOST'];
$database_user = $_ENV['DB_USER'];
$database_pass = $_ENV['DB_PASS'];

// Usando as variáveis de ambiente para conectar ao banco de dados
$conn = new mysqli($database_host, $database_user, $database_pass);
if ($conn->connect_error) {
    die("Erro ao conectar ao banco de dados: " . $conn->connect_error);
}
echo "Conexão bem-sucedida ao banco de dados!";
```

4. **Carregando variáveis de ambiente de um arquivo .env usando vlucas/phpdotenv:**

Para usar a biblioteca `vlucas/phpdotenv`, primeiro, você precisa instalá-la via Composer:

```
composer require vlucas/phpdotenv
```

Depois, você pode usar o seguinte código para carregar/Resgatar  as variáveis de ambiente de um arquivo `.env`, inclusive as variáveis que você mesmo criou:

```php
require __DIR__.'/vendor/autoload.php';

$dotenv = Dotenv\Dotenv::createImmutable(__DIR__);
$dotenv->load();
```

Isso carregará automaticamente as variáveis de ambiente definidas no arquivo `.env` e você poderá acessá-las como nos exemplos anteriores.

Se você der um **var_dump** novamente na superglobal  **ENV**  note que a variável que você adicionou no arquivo `.env` aparece junto com as variáveis padrões.