# Node.js - Aula 03 - Exercício
**User:** [daniofilho](https://github.com/daniofilho)

**Autor:** Dânio Filho

**Date:** 1452720577119

# 1. Por que quando requisitamos ao nosso servidor de Query String, **com o Chrome**, ele executa 2 requisições, sendo a última "vazia"?

O Chrome, além da requisição que foi solicitada, ele realiza uma requisição de um favicon. Como não passamos isso, ele retorna vazio.

# 2. Qual a **DIFERENÇA** entre o **GET** e o **POST**?

** GET **

O GET foi feito para se enviar pedidos para receber informações de uma url, e é usado para enviar parâmetros via URL. Ele possui uma limitação de caracteres em seu envio de 1024 caracteres, o que torna o conteúdo bem limitado.

** POST **

Já o POST foi feito para enviar informações e não apenas consulta-las (como é o caso do GET). Os parâmetros não são enviados via url e o limite do POST é "ilimitado", sendo esse limite sendo apenas definido via servidor, o que geralmente garante o POST de bastante informação sem problema nenhum.

# 3. Crie um Pokemon na nossa API com o seu nome, depois modifique seu nome pelo seu user do Github, colocando aqui a resposta de cada passo.

~~~ js

//Criando o "Pokemon"

STATUS: 201
HEADERS: {"server":"Cowboy","connection":"close","x-powered-by":"Express","access-control-allow-origin":"*","content-type":"application/json; charset=utf-8","content-length":"78","etag":"W/\"4e-GtkDpHj2/UkF+JW96KfJcQ\"","date":"Wed, 13 Jan 2016 21:49:14 GMT","via":"1.1 vegur"}
Dados finalizados:  {"__v":0,"name":"Danio Filho","type":"aluno","_id":"5696c65a2f90f71100f42eca"}

//Removendo

STATUS: 202
HEADERS: {"server":"Cowboy","connection":"close","x-powered-by":"Express","access-control-allow-origin":"*","content-type":"application/json; charset=utf-8","content-length":"108","etag":"W/\"6c-BsH4onU2gQgfl729cawThQ\"","date":"Wed, 13 Jan 2016 21:52:44 GMT","via":"1.1 vegur"}
Dados finalizados:  {"data":{"ok":1,"nModified":1,"n":1,"lastOp":"6239393325560889345","electionId":"565e25d106dca622271891c4"}}

~~~

# 4. Depois faça o DELETE, criando o script para tal, colocndo aqui a resposta.

~~~ js

//Excluindo

STATUS: 204
HEADERS: {"server":"Cowboy","content-length":"0","connection":"close","x-powered-by":"Express","access-control-allow-origin":"*","date":"Wed, 13 Jan 2016 21:53:47 GMT","via":"1.1 vegur"}
Dados finalizados:

~~~

# 5. Escolha uma API externa e crie um script para fazer um GET nela mostrando o resultado em HTML.

~~~ js
//API
host: 'pokeapi.co',
path: '/api/v1/type/?limit=10&offset=1'

//Retorno
STATUS: 200
HEADERS: {"server":"nginx/1.1.19","date":"Wed, 13 Jan 2016 23:35:29 GMT","content-type":"application/json","transfer-encoding":"chunked","connection":"close","vary":"Accept","x-frame-options":"SAMEORIGIN","cache-control":"s-maxage=360, max-age=360"}
<ul>
<li>Fighting</li>
<li>Flying</li>
<li>Poison</li>
<li>Ground</li>
<li>Rock</li>
<li>Bug</li>
<li>Ghost</li>
<li>Steel</li>
<li>Fire</li>
<li>Water</li>
</ul>
~~~
