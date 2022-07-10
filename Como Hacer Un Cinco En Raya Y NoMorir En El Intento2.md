# Introducción

Hoy te mostraré las últimas fases del desarrollo del 5 en raya y añ a asignar la posición de las fichas con ayuda de un raycast, a crear las celdas donde se moverán nuestras fichas y crear un sistema de victoria.

## Creando el GameManager

---

En el anterior video creé el arte del proyecto y configuré el proyecto en Unity, en esta ocasión toca hacer el GameManager para eso creé un nuevo script y lo llamé *GameManager* , añadí un objeto vacío dentro de la escena y le puse el script. 

Seguidamente empecé a escribir una propiedad dentro del *GameManager* a la que llamé *Turn*, en esta propiedad escribiré el código que servirá para mostrar por pantalla el turno al que le corresponde a cada jugador.

## Creando las celdas y la tabla

---

Empecé a trabajar en el comportamiento de la tabla y las celdas asi que hice 2 scripts que funcionarán como sus respectivos controladores, principalmente la tabla se ocupará de generar las celdas y las celdas se ocuparán del comportamiento de las fichas que colisionen con ellas, dentro de *TableCC* puse una propiedad que almacene los prefabs de las fichas.

Seguidmente hice un método que me retornará el prefab correspondiente al jugador que pase por parámetro en la propiedad Turn del *GameManager*.

En el script de las celdas creé una propiedad que almacene el tipo de ficha que se encuentre colisionando con ella, seguidamente hice un nuevo método donde le digo que me asigne el prefab de la ficha a la propiedad que creé anteriormente y puse una excepción por si resultase que la celda estuviera vacía, moví el objeto de la celda un poquitin hacia arriba para que no traspasase el suelo, ya estoy a unos pasos menos de terminar el juego pero aún quedaban muchas cositas que hacer.

Continuo creando un nuevo método de tipo público que me retorne si el tipo de ficha es igual al que está almacenando en la prpiedad y le añadí una excepción donde le diré que si no hay nada en la celda, nos retorne falso.

En el método *SetToken* al asignar la ficha le añadí una excepción para llamar a un método de comprobación de victoria que veremos más adelante.

Creé una propiedad que almacene las posiciones X y Y de las celdas en una matriz en el script de nuestra tabla como no.

Ahora falta que las celdas se generen de forma automática y se vayan colocando en orden sobre la tabla, para que las genere escribí un método nuevo al que le pedí que la almacenase en una propiedad.

Para que me genere todas las celdas del tablero de forma automática creé un método nuevo que nos las empezará a generar y le pediré que las almacene en la propiedad correspondiente, la pongo en el Start para que se generen en el primer frame del juego.

Y finalmente haré otro método que pida las coordenadas de la última ficha colocada y el tipo, este método se va a encargar de comprobar todas las fichas que haya en línea recta, si encuentra 4 encadenadas llamará a la función  *Win* del *GameManager*.

## Completando el flujo del juego

---

En el script del *GameManager* haré que la clase de nuestro script de la tabla quede referenciada en nuestro script del *GameManager* y propiamente le pondré un nombre descriptivo para evitar confundirme con mi propio código.

Creé a continuación la función *Win* que mencione previamente, que me permitirá detonar el sistema de victoria dependiendo de si se cumplen o no las condiciones, este hará que se muestre en pantalla un texto de victoria o de derrota.

Excelente ya casi tengo terminado el flujo normal del juego me faltan los últimos retoques, asi que continuo añadiendo un método para avanzar de turno y añadiré al método *SetToken* de nuestro script de celdas una llamada al método para avanzar de turno.

Y listo con todo esto ya tendremos nuestro 5 en raya casi terminado, ahora solo falta implementar el puto online ¡FUUUUUCK!

**-Despedida-**