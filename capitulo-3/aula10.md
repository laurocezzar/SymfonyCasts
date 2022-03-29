---
description: 'Banco de Dados: Usando parâmetros de consulta'
---

# Aula10

* Usamos _`$_POST`_ para obter dados enviados em um formulário e _`$_SERVER`_ para descobrir se esta é uma solicitação _`GET`_ ou _`POST`_.
* Os parâmetros de consulta são acessados pelo método _`$_GET.`_Podemos adicionar mais valores na URL adicionando um sinal & entre cada um:

![](../.gitbook/assets/exmplo\_GET.png)

{% hint style="info" %}
Os parâmetros de consulta sempre começam com um _**`?`**_ e então cada par chave-valor é separado por um _**`&`**_ depois.
{% endhint %}

![Gerando uma chave ID de $\_GET](../.gitbook/assets/obtendoID\_GET.png)
