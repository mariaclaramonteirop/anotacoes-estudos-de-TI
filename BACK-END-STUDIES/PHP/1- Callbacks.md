### Callbacks
- São funções passadas como parâmetros para outras funções

```php
function teste1($nome){
	return 'Olá,meu nome é' . $nome;
}

funtion teste2($callback){
	return $callback('Alex'); // indica que será retornarda uma função
}

echo teste2('teste1'); // a primeira função deve ser chamada como uma string
```

- Para verificar se é um callback, usa-se o **is_callable( )**
	- Ele verificará se a váriavel que está sendo passada é um função, ou seja, um callback
```php
function teste1($nome){
	return 'Olá,meu nome é' . $nome;
}

funtion teste2($callback){

	if(is_callable($callback)) {
		return $callback('Alex'); // indica que será retornarda uma função
	}
}

echo teste2('teste1'); // a primeira função deve ser chamada como uma string
```

- call_user_func(Função, ... $parametros....)

```php
function teste1($nome){
	return 'Olá,meu nome é' . $nome;
}

echo call_user_func('teste1',$nome);
echo call_user_func('teste1');// esse dará erro, pois um parametro é esperado
```

- Para trabalhar com o método de um objeto usando o call_user_func(), deve-se chamar um array, onde o primeiro valor do array vai ser o objeto e o segundo será o método e se o método estiver esperando um parâmetro, ele será o segundo argumento da função call_user_func()

```php
class User 
{
	public function teste1($nome, $age)
	{
		return 'Olá,meu nome é' . $nome . 'e minha idade é' . $age;
	}
}
$user = new User;
echo call_user_func([$user, 'teste1'],'Alex', 23);
echo call_user_func(['User', 'teste1'],'Alex', 23);

```

- call_user_func() dentro de outras funções
```php
function teste1($nome){
	return 'Olá,meu nome é' . $nome;
}

funtion teste2($callback)
{
	return call_user_func($callback, 'Alex'); 
}

echo teste2('teste');
```
