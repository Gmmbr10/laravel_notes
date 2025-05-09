# Templates e Layouts

Nós podemos padronizar as páginas do nosso sistema, mas de que maneira podemos fazer isso?

Usando as diretivas.

Primeiro criamos o arquivo de layout/template do nosso site. Após isso, nos lugares que queremos adicionar o conteúdo, nós colocamos `@yield('nome-da-sessao')`.

Exemplo:

```php

<header></header>

<main>
  @yield('nome-da-sessao','conteudo a ser carregado caso não tenha a sessão')
</main>

<footer></footer>

```

Já no arquivo que temos o conteúdo, nós fazemos o seguinte:

```php

@extends('template')

@section('nome-da-sessao')

  conteúdo da sessao

@endsection

```

## Como criar componentes fixos e dinâmicos ao mesmo tempo?

De vez em quando, podemos passar uma logo diferenciada em relação a outras páginas. Mas como fazemos isso e ainda assim mantemos modelo padrão?

Simples:

```php

@yield('logo',View::make('pasta.arquivo'))

```