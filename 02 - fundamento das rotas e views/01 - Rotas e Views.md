# Rotas e Views

Para rodar o nosso projeto, iremos utilizar sempre o comando a seguir:

```bash
php artisan serve
```

## Onde ficam as rotas?

Dentro da pasta `routes` temos o arquivo `web.php`.

Nele ficam localizados todas as nossas rotas, e elas são escritas igual a maneira abaixo:

```php

Route::get("/rota",function(){
  return view("nome_da_view");
});

```

Sempre será uma estrutura que indica o método, nome da rota e uma função anônima que terá algum tipo de retorno.

Nesse exemplo a função `view()` é responsável por carregar as nossas views.

Essas views ficam no seguinte caminho `resources/views/nome_da_view.blade.php`

> Sempre passe o texto que fica antes da extensão `.blade.php` para a `view()`.
