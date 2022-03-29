---
description: Vídeo Curso Symfony Casts
---

# Aula2

Atividade 2 - Crie um formulário HTML que envie uma solicitação POST /new\_toy.php e forneça 2 campos: um campo input de texto chamado name e um campo textarea chamado description. Recarregue para verificar seu formulário!

```php
<?php require 'layout/header.php'; ?>
<div class="container">
	<div class="row">
		<div class="col-xs-3">
			<h1>Add your Toys!</h1>

			<form action="/new_toy.php" method="POST">
				<div class="form-group">
					<label for="toy-name" class="control-label">Toy Name</label>
					<input type="text" name="name" id="toy-name" class="form-control" />
				</div>
				<div class="form-group">
					<label for="toy-description">Description</label>
					<textarea id="toy-description" name="description" rows="3" cols="33" maxlength="500">Digite aqui...</textarea>
				</div>
				<button type="submit" class="btn btn-primary">
					<span class="glyphicon glyphicon-heart"></span>
					Add
				</button>
			</form>
		</div>
	</div>
</div>
<?php require 'layout/footer.php'; ?>
```

