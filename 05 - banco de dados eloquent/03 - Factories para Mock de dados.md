# Factories para Mock de dados

Factories são scripts para criar dados falsos em seu sistema, para facilitar os testes do nosso sistema.

Dentro da pasta `database`, temos uma pasta chamada `factories`. Nela estão presentes as nossas factories.

Caso precise alterar um nome de coluna, ou adicionar coluna, você deve abrir o arquivo factory e ir no método `definition()`.

Para criar um dado falso, podemos usar o `php artisan tinker`. Ele abrirá um executador de comandos php dentro do nosso terminal.

Dentro dele você executa o seguinte comando:

```bash

Tabela::factory()->create();

```

Com isso, você vai conseguir criar dados falsos.