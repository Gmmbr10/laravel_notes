# Helpers em Controllers

Dentro do Laravel, temos diversas funções que podem nos auxiliar a criar aplicações de diferentes formas.

## Alguns exemplos

Podemos retornar um `json` quando determinada rota for requisitada:

```php

class UserController {
  public function getProfile($username) {
    return response()->json(['parametro'=>'valor']);
  }
}

```

Podemos também redirecionar para outra rota:

```php

class UserController {
  public function getProfile($username) {
    return redirect('/user');
  }
}

```

**Mas e se em algum momento eu trocar o nome da rota?**

Podemos resolver isso nomeando a rota. Mas como fazemos isso?

Da seguinte maneira:

```php

Route::get("/user/{username}",[UserController::class,'getProfile'])->name('nome-da-rota');

```

E quando for redirecionar fazemos o seguinte:

```php

class UserController {
  public function getProfile($username) {
    return redirect(route('nome-da-rota',['parametro'=>'valor']));
  }
}

```

> Se a rota precisar de parâmetros, passamos eles em um array, como no exemplo acima
>
> Caso não tenha, podemos passar apenas o nome da rota