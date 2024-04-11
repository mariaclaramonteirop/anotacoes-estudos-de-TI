Usa-se a função **isset($variavel)**

```php
$name = 'Maria';

echo isset($name);

// 1 - thruty
// 2 - falsy
// se o valor da variavel for nulo, não será retornado nada
```

Pode ser usado também com Array's **isset($nomeArray['indice'])**
```php
$person = ['name' => 'Maria', 'age'=> 25];

echo isset($person['name']);

// 1 - thruty
// 2 - falsy
// se o valor da variavel for nulo, não será retornado nada

```
