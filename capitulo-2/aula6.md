---
description: Vídeo Curso Symfony Casts
---

# Aula6

Atividade 1

1. Reorganize a lógica de economia de brinquedos em uma nova função chamada `save_toys()`.
2. Certifique-se de chamar esta função para manter as coisas funcionando!

{% code title="new_toy.php" %}
```php
<?php
require __DIR__.'/lib/functions.php';

if ($_SERVER['REQUEST_METHOD'] == 'POST') {
    $name = $_POST['name'];
    $description = $_POST['description'];

    $toys = get_great_pet_toys();
    $toys[] = ['name' => $name, 'description' => $description];
    save_toys($toys);
}
?>

<form action="/new_toy.php" method="POST">
    <input type="text" name="name" />
    <textarea name="description"></textarea>

    <button type="submit">Add toy</button>
</form>
```
{% endcode %}

{% code title="functions.php" %}
```php
<?php
function get_great_pet_toys()
{
    $contents = file_get_contents(__DIR__.'/../toys.json');
    $toys = json_decode($contents, true);

    return $toys;
}

function save_toys(array $toys)
{
    $json = json_encode($toys, JSON_PRETTY_PRINT);
    file_put_contents(__DIR__.'/../toys.json', $json);
}
```
{% endcode %}

{% code title="toys.json" %}
```json
[
    {
        "name": "Bacon Bone",
        "description": "What could be better?"
    },
    {
        "name": "Tennis Ball",
        "description": "Throw, fetch, throw, fetch, throw, fetch..."
    },
    {
        "name": "Frisbee",
        "description": "Go Deep!"
    }
]
```
{% endcode %}
