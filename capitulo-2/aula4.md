---
description: Vídeo Curso Symfony Casts
---

# Aula4

* _<mark style="background-color:blue;">file\_put\_contents</mark> =_ Escreve dados em um arquivo.

Atividade 1

1. Busque os brinquedos de animais de estimação existentes com a função`get_great_pet_toys().`
2. Adicione o novo brinquedo à matriz
3. Em seguida, salve o JSON de volta para`toys.json`
4. Para provar que está funcionando, leia o arquivo novamente com `file_get_contents()`e `var_dump()`a string JSON.
5. Preencha o formulário com `Fluffy Pig Stuffed Animal`e qualquer descrição para experimentar!

{% code title="new_toy.php" %}
```php
<?php
require __DIR__.'/lib/functions.php';

if ($_SERVER['REQUEST_METHOD'] == 'POST') {
    $name = $_POST['name'];
    $description = $_POST['description'];

    $toys = get_great_pet_toys();
    $toys[] = ['name' => $name, 'description' => $description];
    $json = json_encode($toys, JSON_PRETTY_PRINT);
    file_put_contents('toys.json', $json);

    var_dump(file_get_contents('toys.json'));
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
