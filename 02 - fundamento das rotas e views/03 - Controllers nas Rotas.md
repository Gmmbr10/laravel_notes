# Controllers nas Rotas

Pensando em rotas que temos processamentos de dados, não é ideal ficar colocando a nossa lógica dentro de um arquivo de rota.

Então, para podermos processar os dados que recebemos, utilizamos os **Controllers** que ficam localizados na pasta `app/Http/Controllers`.

## Como criar Controllers?

Basta executar o código:

```bash

php artisan make:controller NomeController

```

E pronto, temos o Controller criado com sucesso.

## Vamos refatorar aquele pequeno código que fizemos?

```php

/********************/
/*arquivo do controller*/
/*
* vai ter mais coisas, porém aqui será apenas um exemplo!!!
*/

class UserController {
  public function getProfile($username) {
    return view('users',compact('username'));
  }
}

/********************/
/*arquivo das rotas*/

Route::get("/user/{username}",[UserController::class,'getProfile']);

/********************/
/*arquivo user.blade.php*/
<?php

echo $username;

?>
```


> ## Dicas
> - Importe os arquivos no começo do arquivo das rotas, para deixar com menos código
> - Se você uma rota com parâmetro e outra com o mesmo caminho porém com uma rota fixa, exemplo `/user/{username}` e `/user/me`, deixe a rota que contenha a variável por último.