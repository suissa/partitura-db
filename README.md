#PartituraDB

O PartituraDB é uma API com um CRUD comum para os bancos NoSQL.

Para isso vamos definir inicialmente qual será nossa API básica que todos os bancos devem implementar:

```js
{ 
  "DB": "mongo"
, "create": "insert"
, "retrieve": "find"
, "get": "findOne"
, "update": "update"
, "delete": "remove"
}

```

E qual vai ser a definição dos parâmetros dessas funções?

```js
var Partitura = require('Partitura');
// os métodos inicialmente não serão encadeados
Partitura
  .insert(JSON, callback(err, data))
  .find(JSON, callback(err, data)) 
  .findOne(JSON, callback(err, data))
  .update(JSON, callback()) 
  .update(JSON_QUERY, JSON_UPDATE ,callback(err, data)) 
  .remove(JSON, callback(err,data))
```

##API - CRUD

###Callbacks

Para usar o padrão do Node.js todo o *callback* deve aceitar 2 parâmetros:

- err: objeto retornado ao ERRO
- data: objeto retornado ao SUCESSO

Caso o *callback* seja de **sucesso** deve-se retornar `null` como primeiro parâmetro.

###Create - Insert

Função que irá inserir um objeto passado como parâmetro.

```js
function insert(JSON, callback(err, data));
// JSON é o objeto a ser inserido
```

###Retrieve - Find
Função que irá listar os objetos buscados pela query no primeiro parâmetro..

```js
function insert(JSON, callback(err, data));
// JSON é o objeto a ser inserido
```

###Update - Update
Função que irá inserir um objeto passado como parâmetro.

```js
function insert(JSON, callback(err, data));
// JSON é o objeto a ser inserido
```

###Delete - Remove
Função que irá inserir um objeto passado como parâmetro.

```js
function insert(JSON, callback(err, data));
// JSON é o objeto a ser inserido
```




