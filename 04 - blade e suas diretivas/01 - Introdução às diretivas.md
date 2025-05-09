# Introdução às diretivas

Agora partindo para o blade, podemos exibir dados enviados por nossos controllers.

De que maneira?

Temos maneira próxima ao php puro usando as tags `<?php ?>` e temos o mais recomendado dentro do blade:

```php

{{ $variavel }}

```

A forma acima seria o mesmo que a seguinte:

```php
<?php
echo $variavel;
?>
```

Além de exibir variáveis, podemos também criar condicionais, estrutura de repetição, entre outros.

De que maneira?

Você irá inserir um `@` antes de cada 'comando'. A única diferença é que o bloco não é representado por chaves `{}` e sim por `@endcomando`. Exemplo:

```php

@if(1==1)
 - deu certo
@endif

@foreach($args as $arg)
  {{$arg}}
@endforeach

```