# Find, All e Paginate

Vamos supor que você criou um controller para pegar todos os posts de um blog.

Como fazer isso?

```php

$posts = Post::all();

```

Mas e se você quiser criar uma páginação?

Vamos lá, basta você digitar:

```php

$itensPorPagina = 15;

$posts = Post::paginate($itensPorPagina);

```

E como procurar por um id específico?

```php

$post = Post::find($post);

```

Mas como eu faço para validar o dado? Um determinado id pode não existir!

Você pode tipar com a model!

Exemplo:

```php

public function getPost(Post $post)
{
  return $post;
}

```

O exemplo acima faz com que, se não existir um post, ele retorne a página padrão `notfound`.