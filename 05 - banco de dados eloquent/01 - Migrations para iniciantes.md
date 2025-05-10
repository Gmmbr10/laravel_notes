# Migrations para iniciantes

Migrations são 'mapas' das tabelas do seu banco de dados.

Para criar uma tabela devemos criar usamos o seguinte comando:

```bash

php artisan make:migration create_nomeTabela_table

```

Logo será criado um arquivo na pasta `database/migrations` do seu migration.

Para criar a tabela, dentro desse arquvo você pode criar as colunas da seguinte forma:
`$table->tipoDeDado('nome_coluna');`

Exemplo:

```php

$table->id();
// coluna comum
$table->string('title');
// chave estrangeira
$table->foreignId('nome_coluna')->references('id')->on('outra_tabela')->cascadeOnDelete();
$table->timestamps();

```

## E como criar a tabela?

Basta rodar o comando abaixo:

```bash

php artisan migrate

```