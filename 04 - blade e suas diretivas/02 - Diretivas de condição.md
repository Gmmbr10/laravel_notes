# Diretivas de condição

Existem diversas formas de realizar condicionais, uma delas é igual a que fazemos nos nossos códigos:

```php

@if(condicional)
  executa
@elseif(condicional)
  executa
@else
  executa
@endif

```

Mas uma diferença entre os nossos códigos e as nossas diretivas pode ser a **negação**.

Sabemos que durante um código podemos negar determinada condição, mas como fazemos isso no blade?

Assim:

```php

@unless(condicao)

  executa se a condição for false

@endunless
```

Assim funciona para algumas funções padrões do php como o `isset()`, `empty()`, entre outras funções, E elas funcionam da mesma maneira, inicia com `@` e quando você quiser terminar determinado bloco use `@endcomando`.

```php

@isset(condicao)
  executa
@endisset

@empty(condicao)
  executa
@endempty

```