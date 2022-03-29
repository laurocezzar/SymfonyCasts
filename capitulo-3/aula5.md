---
description: Conversando com Banco de Dados em PHP
---

# Aula5

* Conectando com o Banco de Dados:

```php
$pdo = new PDO('mysql:dbname=air_pup;host=localhost', 'root', null);
$result = $pdo->query('SELECT * FROM pet');
$rows = $result->fetchAll();
```
