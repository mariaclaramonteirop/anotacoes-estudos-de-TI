- Várias variáveis pré-definidas no PHP são "superglobais", que significa que elas estão disponíveis em todos os escopos para todo o script. Não há necessidade de fazer **==global $variable;==** para acessá-lo dentro de funções ou métodos.
- Os nomes das variáveis Super Globais sempre serão declarados em CAPSLOCK
	Estas variáveis superglobais são:
	
	- [$GLOBALS](https://www.php.net/manual/pt_BR/reserved.variables.globals.php)
	- [$_SERVER](https://www.php.net/manual/pt_BR/reserved.variables.server.php)
	- [$_GET](https://www.php.net/manual/pt_BR/reserved.variables.get.php)
	- [$_POST](https://www.php.net/manual/pt_BR/reserved.variables.post.php)
	- [$_FILES](https://www.php.net/manual/pt_BR/reserved.variables.files.php)
	- [$_COOKIE](https://www.php.net/manual/pt_BR/reserved.variables.cookies.php)
	- [$_SESSION](https://www.php.net/manual/pt_BR/reserved.variables.session.php)
	- [$_REQUEST](https://www.php.net/manual/pt_BR/reserved.variables.request.php)
	- [$_ENV](https://www.php.net/manual/pt_BR/reserved.variables.environment.php)
	
- Exemplo: 
	- COOKIE - É valor guardado no navegador que pode ser resgatado em qualquer parte/local do sistema. Um cookie tem um prazo de validade.
