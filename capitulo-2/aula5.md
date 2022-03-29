---
description: Vídeo Curso Symfony Casts
---

# Aula5

Atividade 2



1. Preencha a lógica necessária `aboutUs.php`para redirecionar para `/about.php`.

{% code title="aboutUs.php" %}
```php
<?php
http_response_code(301);
header('Location: /about.php');
```
{% endcode %}

{% code title="about.php" %}
```php
<h1>Yea! About us!</h1>
```
{% endcode %}
