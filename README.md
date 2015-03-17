#PartituraDB

O PartituraDB é uma API com um CRUD comum para os bancos NoSQL.

Para isso vamos definir inicialmente qual será nossa API básica que todos os bancos devem implementar:

```js
{ 
  "DB": "mongo"
, "create": "insert"
, "retrieve": "find"
, "get": "findOne"
, "save": "update"
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

##API

###Create - Insert

Função que irá inserir um objeto passado como parâmetro.

```js
function insert(JSON, callback(err, data));
// JSON é o objeto a ser inserido
```




