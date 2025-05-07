# Validações nos Controllers

Geralmente quando estamos desenvolvendo sistemas, são necessários dados.

E sempre que temos dados, temos que validar eles.

Por esse motivo, o laravel tem um facilitador para isso, o `validate`, uma extensão da classe `Controller`.

Vamos ver como usá-lo:

```php

class UserController extends Controller {
  public function getProfile(Request $request) {
    $this->validate($request, [
      'campo' => 'required|numeric...'
    ]);
  }
}

```

**`Request $request`:** É um tipo de dado usado para definir que dados foram enviados para aquela rota.

**`$this->validate($request),[])`:** Este processo é o responsável por validar os nossos dados.

Existem diversas formas de validar dados. Por isso, recomendo que olhe na documentação oficial do laravel [https://laravel.com/docs](https://laravel.com/docs).