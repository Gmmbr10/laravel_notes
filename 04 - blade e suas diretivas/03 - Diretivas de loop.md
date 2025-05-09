# Diretivas de loop

Eles funcionam da mesma maneira colocamos em um código puro, trocando apenas as chaves `{}` por `@`.

Exemplos:

```php

@for($i=1; $i<=10; $i++)
  {{$i}}
@endfor

@while(condicao)

  @if(condicao)
  @endif
@endwhile

```