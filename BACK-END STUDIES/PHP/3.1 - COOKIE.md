- COOKIE - É valor guardado no navegador que pode ser resgatado em qualquer parte/local do sistema. Um cookie tem um prazo de validade.
	- Em PHP, cookies são pequenos pedaços de dados que são armazenados no navegador do usuário. Eles são comumente usados para armazenar informações temporárias, como preferências do usuário, dados de sessão ou qualquer outra informação que você queira lembrar entre diferentes páginas ou visitas ao site.

- Para criar um cookie usa-se o **setcookie('nomeCookie', 'valorCookie', tempoExpiração);** 
``` PHP
setcookie('name','maria',  time() + 24 * 60 * 60);// 2 dias para expiração

setcookie('curso','php',  strtotime('+5days')); // 5 dias para expiração

// Define um cookie com o nome "usuario" e o valor "joao"
setcookie("usuario", "joao", time() + 3600, "/"); // expira em 1 hora



```

- Para resgatar o cookie usa-se a superglobal $_COOKIE['nomeDoCookie'];
``` PHP
echo $_COOKIE['name'];
echo $_COOKIE['curso'];

```

- Para verificar a existência de um cookie podemos usar o isset()
``` PHP
$cookie = $_COOKIE['teste'];

if(isset($cookie))
{
	echo "O cookie " . $cookie . "está definido.";
}else{
	 echo "Cookie não existe";
}
```
Este código verifica se o cookie "teste" está definido e exibe uma mensagem.

Lembre-se de que os cookies são armazenados no navegador do usuário e podem ser desativados pelo usuário. Além disso, você deve ter cuidado ao armazenar informações sensíveis nos cookies, pois eles podem ser facilmente acessados e modificados pelo usuário, valide sempre os dados recebidos do cliente antes de utilizá-los.