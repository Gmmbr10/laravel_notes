# Eloquent básico

Eloquent é um ORM do Laravel.

Ele será um facilitador de consulta ao banco de dados.

No lugar de você escrever:

`select * from users`

Você vai escrever:

`User::all()`

Esse é um simples exemplo, mas ele deixa muito visível a facilidade que ele trará.

Todos os comandos são baseados no model. O nosso model pode ser criado com o comando:

```bash

php artisan make:model Tabela

```

Dentro do arquivo `model` temos algumas propriedades. Por exemplo:

```php

protected $table = 'nome_tabela';

// usado para definir quais são as colunas da tabela
protected $fillable = [
  'colunas',
  'colunas',
  'colunas',
];

// usado para definir tipos de dados mais específicos como boolean, entre outros
protected $casts = [
  'coluna' => 'tipo_de_dado'
];

```