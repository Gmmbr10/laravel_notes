# Forms, CSRF e Demonstrações

Sempre que você vai criar um formulário, você tem que validar ele usando a diretiva `@csrf`

Da seguinte maneira:

```php

<form method="POST" action="{{route('')}}">
  @csrf
</form>

```

Caso queira passar um método diferente de `POST` ou `GET`, você usa a diretiva `@method('METODO')`