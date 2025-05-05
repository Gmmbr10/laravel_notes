# Wildcards em rotas

Wildcards seriam parâmetros passados para determinada rota através da url.

## Como fazer?

Sempre que você quiser criar uma rota com wildcard você deve colocar entre chaves `{}` o nome do parâmetro, além disso, você deve colocá-lo nos parâmetros da função com o mesmo nome.

```php

Route::get("/user/{username}",function($username){
  return 'hello '. $username;
});

```

## E se eu quiser passar para uma view?

Podemos também basta fazer o mesmo passo a passo, porém no instante em que usamos o `view()`  temos duas formas:

### Forma 1

Passando como parâmetro, após o nome da view, como array com chave e valor

```php

Route::get("/user/{username}",function($username){
  return view("user",["username"=>$username]);
});

/********************/
/*arquivo user.blade.php*/
<?php

echo $username;

?>
```

### Forma 2

Passando como parâmetro, a função compact(), que já transforma o nome da variável em um array de chave e valor.

```php

Route::get("/user/{username}",function($username){
  return view("user",compact("username"));
});

/********************/
/*arquivo user.blade.php*/
<?php

echo $username;

?>
```