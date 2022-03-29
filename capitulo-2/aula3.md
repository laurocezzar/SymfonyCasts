---
description: Vídeo Curso Symfony Casts
---

# Aula3

Atividade 1

1 - Defina o nome enviado para uma variavel `$name` e a descrição para uma variável `$description`.

2 - Em seguida, execute `var_dump()` em ambas as variáveis ​​para ver o que está sendo enviado.

3 - Clique Check para carregar o formulário. Ignore os erros desagradáveis ​​de índice indefinido : vamos corrigi-los em breve!

4 - Preencha o campo de nome com `Fluffy Pig Stuffed Animal` e o campo de descrição com `Your dog will destroy it!`.

5 - Envie o formulário para ver seus valores despejados!

{% code title="new_toy.php" %}
```php
<?php
$name = $_POST['name'];
$description = $_POST['description'];
var_dump($name, $description);
?>

<form action="/new_toy.php" method="POST">
    <input type="text" name="name" value="Fluffy Pig Stuffed Animal"/>
    <textarea name="description">Your dog will destroy it!</textarea>

    <button type="submit">Add toy</button>
</form>
```
{% endcode %}

Atividade 2

1. Adicione uma declaração `if` em torno de nossa lógica para que ela seja executada apenas quando o usuário enviar o formulário (ou seja, fizer uma solicitação `POST)`.

{% code title="new_toy.php" %}
```php
<?php
$name = $_POST['name'];
$description = $_POST['description'];

if ($_SERVER['REQUEST_METHOD'] == 'POST') {

	if (isset($_POST['name'])) {
		$name = $_POST['name'];
	} else {
		$name = '';
	}
}
?>

<form action="/new_toy.php" method="POST">
    <input type="text" name="name" />
    <textarea name="description"></textarea>

    <button type="submit">Add toy</button>
</form>
```
{% endcode %}

Atividade 4

1. Despeje a variável `$_SERVER` e execute seu código para descobrir qual chave armazena informações sobre qual navegador você está usando. (seu código será avaliado errado no início, mas não se preocupe!)
2. _Dica:_ As informações do navegador são uma string grande e longa que (neste exemplo) será incluída `Mozilla`nela.
3. Imprima as informações do navegador na tag `h3`.

{% code title="new_toy.php" %}
```php
<h3>
    <?php echo $_SERVER['HTTP_USER_AGENT']; ?>
</h3>
```
{% endcode %}
