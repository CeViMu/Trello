# Trello
Actividad de la semana 4 de Launch X

# Explorando la API REST trello
1) Primero necesitamos crear una cuenta en la página  https://trello.com/
2) Para poder interactuar con esta API se necesita un api key y un token que se solicitan aquí: https://trello.com/app-key . Estos valores son muy importantes y hay que guardarlos
3) Exploremos ahora la documentación de la API REST Trello que se encuentra aquí: https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-group-boards
4) Dentro de la documentación veremos los siguientes puntos:
- Cómo crear un nuevo board.
- Cómo obtener la información de un board a partir de su ID
- Cómo obtener la lista de cards de un board
- Cómo crear una nueva card en un board
5) Para hacer esta exploración tenemos la coleccion de postman con métodos, esta debe ser importada a Postman para hacer uso de ella.

A continuación se presentan los resultados de la exploración de los puntos anteriores.

## Crear un nuevo board
1) La petición que usaremos en Postman es POST Create board:  
![image](https://github.com/CeViMu/Trello/blob/main/images/CreateBoard.png)
2) En Postman hay una sección de params que se tiene que llenar con la información del api key en el campo key y el token en Token.  
![image](https://github.com/CeViMu/Trello/blob/main/images/params.png)
3) Damos click en Send  
4) Vamos a nuestro tablero de Trello y verificamos que se haya creado un nuevo board.  
![image](https://github.com/CeViMu/Trello/blob/main/images/newboard.png)
5) En el response que se obtiene en Postman, hay un campo id que corresponde al ID del tablero que se creó, este ID debe ser guardado.  
![image](https://github.com/CeViMu/Trello/blob/main/images/id.png)

## Obtener la lista de cards de un board
1) La petición que usaremos ahora es:
![image](https://github.com/CeViMu/Trello/blob/main/images/getList.png)
2) En la sección de Postman de params agregamos el API KEY y TOKEN, además tenemos que modificar la url que aparece en Postman, después de /1/boards/ quitamos el valor que esta ahí y ponemos el ID del board creado en la sección anterior.
![image](https://github.com/CeViMu/Trello/blob/main/images/GetListIm.png)
3) Damos click en Send
4) Verificamos que la información recibida corresponda a la lista de columnas que aparecen en el tablero.
![image](https://github.com/CeViMu/Trello/blob/main/images/ListCol.png)
5) De esta parte tomamos el primer ID que usaremos en la seguiente sección.

## Cómo crear una nueva card en un board
1) La petición a usar : 
![image](https://github.com/CeViMu/Trello/blob/main/images/CreateCard.png)
2) Los parámetros que se necesitan para esta petición son el Token, name (que es el nombre que le daremos a la card nueva) y el ID que guardamos en la sección anterior.
![image](https://github.com/CeViMu/Trello/blob/main/images/CardByID.png)
3) Damos click en Send
4) Verificamos que se haya creado una nueva card en Trello
![image](https://github.com/CeViMu/Trello/blob/main/images/newcard.png)

