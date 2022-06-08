# Introducción

---

En el anterior video creamos el arte del proyecto, lo llevamos todo a nuestro proyecto creado en Unity, instalamos los paquetes y dependencias para que nuestro juego fuera más decente, configuramos la iluminación y nuestros modelos de tablero y fichas.

Hoy pequeño insecto **(Meme de vegeta)** te enseñaré a asignar la posición de las fichas con ayuda de un raycast, a crear las celdas donde se moverán nuestras fichas y crear un sistema de victoria.

## Creando el GameManager

---

Crearé un nuevo script y lo llamaré *GameManager* y haré que tenga una referencia estática de si misma, añadiré un objeto vacío dentro de la escena y le pondremos el script a este pendejo de aquí sin vida que será nuestro *GameManager* dentro de la escena del juego. 

Seguidamente lo abriré en el editor y escribiré una propiedad a la que llamaré *Turn* para ser lo más descriptivo posible, para que se pueda mostrar el turno de a que jugador le toca el turno, ahora dejaré el script a un lado y volveré a Unity por que nos faltan hacer 2 scripts de mucha importancia para completar el flujo de juego.

## Creando las celdas y la tabla

---

Llamaré a nuestros 2 hermosos scripts *TableCC* y *CellCC*, abriremos *TableCC* en una nueva pestaña dentro del editor y pondré en el interior de la clase una propiedad que almacene los Prefabs de las fichas con respecto a cada jugador.

Escribiré un método llamado *GetToken* que nos retornará el prefab correspondiente al jugador que nos pasen por parámetro en la propiedad Turn que hice antes.

Después abriré *CellCC* para escribir código ya que aquí es donde haremos las comprobaciones de los objetos que esten ubicada en cada celda del tablero, escribiré una propiedad que almacene el tipo de ficha que se encuentre en la celda **(Mostrar imagen de la princesa zelda)** y añadiré una excepción en el caso de que esté vacía, añadiré un método de tipo público al que nombraré *SetToken*, haré un pequeño enfases en recordaros que los nombres de los métodos, variables, clases y básicamente cualquier objeto con el que trabajemos debe ser lo más descriptivo posible para evitar catástrofes futuras.

En este método haremos que se asigne el prefab de la ficha a la propiedad que creamos anteriormente, preguntaremos a la tabla para obtener el token correspondiente a tipo de entrada y lo moveré un poquitin hacia arriba para que no traspase el suelo, nuevo nivel de realismo compas...


Me desplazo al script de nuestra tabla y crearé un método *GetToken* que me retornará el prefab correspondiente al jugador que me pase por parametro.

Me desplazo nuevamente al script de las celdas. Ufff man... Me estoy cambiando mas de scripts que un europeo de sexo... 

-Smulli: ¡Qué nos funan wey!
 
-TK: Pero si el chiste lo escribiste tu en el guión hijo de su puta madre, ¡Quédese en el armario pinche esclavo!

-Smulli: Si señol...

Anyway, Añadiré un nuevo método de tipo público *CheckToken* que nos retorne si el tipo de ficha es igual al que está almacenando, haré una excepción de que si no hay nada en la celda, nos retorne falso.

En el método *SetToken* al asignar la ficha le colocaré una excepción para añadir un método de comprobación de victoria que veremos más adelante.

Seguiré creando una propiedad que almacene las posiciones X y Y de las celdas en una matriz en el script de nuestra tabla como no.

Para que me genere todas las celdas del tablero de forma automática escribiré un método nuevo al que llamaré *GenBoard* y le pediré que las almacene en la propiedad correspondiente.

Y finalmente haré otro método que nos pida las coordenadas de la última ficha colocada y el tipo, este método se va a encargar de comprobar todas las fichas que haya en línea recta, si encuentra 4 encadenadas, llamará a la función *Win* del *GameManager*.

Llamo el método *GenBoard* en el método *Start* para que lo llame justo al ejecutar el primer frame del juego. 

## Completando el flujo del juego

---

En mi script *GameManager* haré que la clase de nuestro script de la tabla quede referenciada en nuestro script del *GameManager* y propiamente le pondré un nombre descriptivo para evitar confundirme con mi propio código.

Crearé a continuación el método *Win* que pudimos ver previamente, que nos permitirá detonar el sistema de victoria dependiendo de si se cumplen o no las condiciones, este hará que se muestre en pantalla un texto de victoria o de derrota.

Excelente ya casi tengo terminado el flujo normal del juego me faltan los últimos retoques añadir un método *NextTurn* para avanzar de turno y colocaré al método *SetToken* de nuestro script de celdas una llamada al método *NextTurn* del *GameManager*.

Y listo con todo esto ya tendremos nuestro 5 en raya casi terminado, ahora solo falta implementar el puto online ¡FUUUUUCK!

**-Despedida-**