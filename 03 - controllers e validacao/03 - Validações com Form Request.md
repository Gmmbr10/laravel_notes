# Validações com FormRequest

Ainda dentro de validações, podemos abstrair o nosso código para simplificar e melhorar a legibilidade dele.

Para isso, podemos criar os nossos `FormRequest`, uma maneira simplificada de validação. Vejamos:

Primeiro você deve criar e identificar o validador, da seguinte maneira:

```bash
php artisan make:request NomeRequest
```

Você irá reparar que dentro da pasta `app/Http` será criada a pasta `Requests` e dentro terá o seu `FormRequest`.

Ao abrir ele você terá dois métodos, `rules` e `authorize`.

O método `authorize` deve sempre retornar `true`, caso você precise de algo específico, é aqui que você irá fazer o código que autoriza ou não.

Já o método `rules` fica responsável pelas validações, igual ao do exemplo anterior:

```php

class NomeRequest
{
  public function authorize()
  {
    return true;
  }

  public function rules()
  {
    return [
      'name' => 'required',
      'age' => 'required|numeric'
    ];
  }
}

```

**E como fica no controller?**

Você no lugar de passar `Request $request` você passa `NomeRequest $request`, sem precisar do método `$this->validate()`:

```php

public function getProfile(NomeRequest $request)
{
  // código do método
}

```