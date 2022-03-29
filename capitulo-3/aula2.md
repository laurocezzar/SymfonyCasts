---
description: Consultas, Bancos de Dados e Tabelas
---

# Aula2

*   Conectar em um Banco de Dados:

    * `mysql -h` servidor `--port=3306 -u` usuario `-p;`


* Exibir Base de Dados existentes:
  * `SHOW DATABASES;`
* Criar um Banco de Dados:
  * `CREATE DATABASE air_pup;`
* Selecionar uma Base de Dados específica:
  * `USE air_pup;`
* Criar tabela em uma Base de Dados:

```
CREATE TABLE pet (
    id int(11) AUTO_INCREMENT;
    name varchar(255);
    breed varchar(100);
    PRIMARY KEY (id);
    ) ENGINE=InnoDB;
```

{% code title="Exibir tabelas" %}
```
SHOW TABLES;
```
{% endcode %}
