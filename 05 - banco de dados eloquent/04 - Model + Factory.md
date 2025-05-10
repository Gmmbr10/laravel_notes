# Model + Factory

O nosso model é a configuração da tabela.

Para saber mais acesse a [Aula 02 - Eloquent básico](./02%20-%20Eloquent%20básico.md) ou a [documentação oficial](https://laravel.com/docs/)

E para criar um factory, rodamos o seguinte código:

```bash

php artisan make:factory TabelaFactory

```

Dentro do arquivo do factory da tabela, colocamos dentro do método `definition` as colunas e um faker, se precisar usar um id de outra tabela, podemos criar uma função anônima e usar o factory daquela tabela.

Exemplo:

```php

protected function definition(){
  return [
    'user_id' => function() {
      return User::factory()->create()->id
    }
  ];
}

```