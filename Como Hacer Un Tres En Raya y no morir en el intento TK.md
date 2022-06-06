Empecemos con lo basico.

## Creando los Recursos para el Proyecto.

---

1. En el programa de Blender (pobre), hacemos unas fichas rapidas con las formas basicas por defecto.

2. Descargamos texturas "gratuitas" (pobre) de internet.

3. Utlizamos el programa llamado Materialize (Pobre) para generar las texturas de Normal, Altura (Height) y Oclusion ambiental (SOMBRAS).

4. Configurar los materiales en Blender y exportar todo y meter a una carpeta para despues deslizarlo sueavemente al proyecto de unity.

5. lo mismo hacer para el tablero.

## Creando el proyecto..

---

1. Crear un nuevo proyecto en la version 2021 LTS.
2. Selecionar la plantilla 3D URP Core.
3. Cagarte en Unity porque no descarga la plantilla.
4. Usar la version estandar de 3d de plantilla.
5. Olvidarte de ponerle nombre al proyecto.
6. Clickar en el boton crear.

## Instalando paquetes y dependencias.

---

1. Ir a la Asset Store de Unity (ni modo que al market place de Unreal).
2. Buscar el asset llamado Pun 2 de Photon.
3. Seleccionar el gratuito (because pobreza) y añadirlo a mis assets. 

4. Dentro del Proyecto de Unity: Windows -> Package Manager.

5. Antes de instalar los paquetes, debemos ir a Photon.com, registrarse y crear un proyecto de tipo PUN (Photon Unity Network).

6. Instalar los paquetes:
    - Pun2.
    - Cinemachine.
    - TimeLine.
    - TextMeshPro.

7. Meter toda la mierda de los paquetes en una carpeta llamada "Dependencias", para que no molesten.

## Configurando la iluminacion de la Escena

---

en la escena que usaremos de plantilla se deben realizar ciertas configuraciones para que el juego no se vea como tú, cuando te acabas de despertar de una cruda.

1. Windows > Rendering > Lightning > Environment

    + Desactivar y bajar la intencidad de las luces de ambiente a 0.

2. Quitar la directional light que no sierve para una mierta y añadir 2 luces Puntuales a cada lado de la escena.

3. Poner el color y la intensidad que mas te agrade a las luces puntuales, para esto puedes añadir los objetos que acabamos de crear.

4. Presionar reiteradamente el CTR + S por si en algun momento el Unity (Crashea).

## Configurando el Tablero y las Fichas.

---

1. Añadir el tablero a la escena.

2. Colocar un Mesh Collider.

3. Crear un cubo que ocupe el mismo tamaño que las celdas del modelo del tablero.

4. Marcar el Collider del cubo como Trigger y colocarlo en una layer distinta al que llamaremos "Celdas".

5. Renombrar el Cubo a Celula y hacerlo un Prefab arrastrandolo a la pestaña de proyecto.

6. Agregar una Ficha a la Escena.

7. Colocar un Mesh Collider.

8. Guardarlo Como Ficha.

9. Hacer del Prefab ficha variantes para las piesas, asi cuando tengamos que editarlos, podemos recurir directamente al padre y se actualizarán en resto.

## Creando el click.

---

1. Crear un script nuevo (CursorCC).

2. Hacer que en el Update detecte si el click Izquierdo del Raton es pulsado (Input.ButtonDown())

3. Si esta pulsando el boton y el **GameManager** indica que es nuestro turno, Lanzaremos un raycast cuyo origen es la camara principal y la direccion es la que obtendremos del input del cursor.

4. si el raycast colisiona con una ficha de momento lanzaremos un Log dicidendo el Nombre del objecto con el que chocamos.

## Creando la Celda.

---

1. Crear un script nuevo (CellCC).

2. añadir una propiedad que almacene el tipo de ficha que contiene (añadir una excepción para cuando este vacia).
3. añadir un método púlbico (**SetToken**) que asigne una ficha a la propiedad que tenemos creada, preguntaremos a la tabla para obtener el token correspondiente a tipo de entrada y lo movemos un poco hacia arriba para que no traspase el suelo.

4. Añadir un método público (**CheckToken**) que nos devuelva si el tipo de ficha que estamos comprobando es igual al que tenemos almacenado, sino tenemos nada almacenado, retornará falso.

5. En el método **SetToken** al asignar la ficha colocaremos una excepción para añadir un metodo de comprobacion de victoria que veremos más adelante.

6. Colocar en **SetToken** una llamada al método **NextTurn** del **GameManager**. 

## Creando la Tabla.

---

1. Crear un nuevo Script (TableCC).

1. Creamos una Propiedad que alacene los Prefabs las fichas con respecto a cada jugador.

1. Crear un método (**GetToken**) que nos retornará el prefab correspondiente al jugador que nos pasen por parametro.

1. Crear una Propiedad que almacene todas las celdas (CellCC) dentro en una matris de 2. **[x,y]**

1. Crear un método **GenBoard** que nos genere todas las celdas (CellCC) del tablero de forma automatica y nos las almacene el la Propiedad correspondiente.

1. Crear un método **CheckWin** que nos pida las coordenadas de la ultima ficha colocada y el tipo, este se va a encargar de comprobar todas las fichas que haya en line recta, si encuentra 4 encadenadas, este Activara la funcion **Win** del **GameManager**

1. en el Metodo Start, añadimos la llamada a **GenBoard**.

## Creando el GameManager

---

1. Crear un script **GameManager**

1. Hacer una referencia estatica a si mismo **Singleton**

1. Crear una Propiedad **Turn** que nos almacene el turno del jugador en el que estamos.

1. Crear una Propiedad **Table** que almacene una referencia al **TableCC**, asi poder acceder de manera facil al tablero.

1. Crear un método **Win** que nos permita detonar el sistema de Victoria que muestre una pantalla de victoria o derrota dependiendo del jugador que gano.

1. Crear un método **NextTurn** para avanzar el turno en uno.

Listo ya tenemos el X0 Funcionando, ahora a implementar el Online (FUCK)

## Añadiendo PUN al Proyecto.

---

1. Crear un script(LobbyCC) que nos conecte con el lobby.

2. al Conectarnos correctamente con el lobby este debera activarnos el menu de busqueda de Salas.

3. Crear un script (RoomCC) que nos gestione las conecciones con la Sala u con

## Creando Lobby.

---
1.

## Creando Sala de Juego.

---

## Añadiendo Multiplayer al GameLoop.