São mapas ordenados 
- relaciona **chave à valor**
Pode ser um valor inteiro ou string

Como declarar:
``` php
$a = array();
//
$a = [];
```

Suporta declaração de índices dinamicamente

``` php
$a[0] = 100;
$a[8] = 80;
$a[15] = 1800

var_dump($a);

// array(0=> 100, 8=> 80, 15 => 1800);
```

Acrescentando valores no fim do array, passar o [ ] vazio ou usar a funções array_push.
``` php
$a[0] = 100;
$a[8] = 80;
$a[] = 1800;//adiciona no final
array_push($a, 1700)//adiciona no final


var_dump($a);

// array(0=> 100, 8=> 80, 15 => 1800, 1700);
```
