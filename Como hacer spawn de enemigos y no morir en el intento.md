# Introduccion

Hola muy buenas, aquí de nuevo Smulli en este devastador video y esta vez vengo con una estructura algo distinta ya que recibimos bastante feedback por parte de la comunidad de Todo gamedev administrada por nuestro señor y salvador Rhomita y me di cuenta que la forma de organizar y planear nuestros videos no se estaba llevando de la forma más correcta ya que nosotros apuntamos a entretener mas que a enseñar pero aún así buscamos colateralmente enseñar a la vez que os descojonáis de nuestras desgracias ajenas a vuestros asuntos, asi que decidí darle al guión de este video unos grandes cambios de última hora para que no os sea pesado y sea mas a menos disfrutar de la experiencia, asi que voy a dejar de darle a la sin hueso y comenzamos con el video.

## La piscina

---

Empece a trabajar rapidamente en mi sistema de Spawn de enemigos que vienen siendo amables asteroides destructores **(Mostrar meme de meteorito)** y como se que solo será un spawn de enemigos que iré añadiendole más adelante atributos especificos y estados no será de GameObject, si no de una clase estática en especifico.

En vez de hacer uso de la instancia del objeto en la escena y destruirlo con la función destroy, preferí hacer un sistema más eficiente que en vez de destruir las instancias acumulando memoria, las ¡Recicla! **(Mostrar imagen de reciclaje)** Limitando el número de instancias, para ello guardo las instancias iniciales en algo que Unity le llama cola... Y no no va con doble sentido pedazo de mente sucia y para no explayarme tanto en el tema vais a verme sufrir picando código en modo timelapse, con música relejante de fondo y veréis el resultado al final.

Ahora como veis no me sirve cualquier prefab por que no me pide un GameObject si no la clase estática que especificamos.


Aqui solo me faltaba asignarle a la función Spawn que active los asteroides.

Ahora solo quedaba crear un nuevo Vector3 cada vez que Spawneaba y colocarle nuestra posicion de inicio en el eje X el resto los podia dejar con valores constantes.

Para ver mas o menos la posicion en que necesitaba que volvieran a situarse los asteroides simplemente use un objeto vacio y me guie por sus coordenadas en la escena.

¡Y ahí ya aparecen, con una posición aleatoria en el eje X!

## La lluvia

---

Ahora solo necesitaba hacer que cayeran al suelo, para ello simplemente le puse un Vector3 down y use el método translate del transform para que cayeran todos hacia abajo.

Esto está bien cuando quieres que el objeto se mueva a una sola dirección en concreto pero no era lo que quería conseguir y en un futuro me daría problemas, sin embargo para probar su velocidad de movimiento ya estuvo bien, y en un futuro me pondría a hacer que los asteroides apuntasen hacia las estructuras de la colonia.

Para encolarlos y reciclarlos solo tenía que crear una condición preguntando que si el eje Y del asteroide era menor a -10... Em Smulli del pasado dije menor que -10 ¡Smulli! Ay... Ste bato... Ahí ahí está bien ahora todo fluirá como un rio, mmm... O supongo que no ¡Por qué te dije que fuera menor que maldito pen...!.

## Arreglando el movimiento

---

Ahora lo que quise hacer era que los meteoritos no fueran a una sola direccion si no que ellos pudieran determinar a que direccion dir obteniendo el transform de un objeto en la escena, como yo soy una cagada para las mates y la programación en general solo se me ocurrió usar un Vector3 MoveTowards, después hice sprites cuadrados para que simularan ser las estructuras que tu tuvieras que defender de los meteoritos y los convertí en prefab ya que los meteoritos necesitaban moverse hacia un prefab, duplique varios para que sirvieran como ejemplo de varias estructuras que el jugador deberá defender.

Los agregué en las posiciones del array del asteroide y les añadí el tag *colony* y ahora os mostraré como quedó.

Funciona guchi, ahora solo faltaba que pudieran interactuar entre ellos asi que obviamente les puse sus respectivos rigidbodys y box colliders estos últimos marcados como *Triggers*.

De momento la única interacción que tendrán será la de mandar a los asteroides nuevamente a la cola del cementerio.

Eso si recuerden no ser igual de pendejos que yo y acuerdense de poner el OnTriggerEnter2D cuando se trate de colisiones 2D.

## El Disparo

---

Ahora todo lo que me faltaba conseguir era que *Hope* disparase y que tenga un retardo en segundos al disparar, primero hice el respectivo pool de balas y como ya habrían varios pools decidí nombrarlos con unos nombres super descriptivos y almacenarlos en distintos directorios para tenerlo todo mas organizado.

Ahora lo que se me ocurrió para hacer la mecánica de disparo era la de usar una corrutina que se activará cada 0.5 segundos, pero esto no dió los mejores resultados y ya veréis mas adelante por que lo digo.

También los más avispados os fijastéis de que solucione el tema de la autoayuda de Unity y puede que lo enseñe a arreglar en un futuro video por que la verdad que a muchos nos ha pasado que el editor no nos muestra la autoayuda y es un verdadero engorro.

Como veis ya tenía preparada la bala como un prefab, hice un objeto vacio por donde quería que salieran las balas disparadas.

Ahora si tocaba trabajar en el pooler de balas, le agregué una variable tipo transform que obtiene la posición del objeto vacio hijo de *Hope*, basicamente es el mismo pooler que el de los asteroides solo que agregué una condición la cual dice que si la cola de balas llegaba a ser menor que 1 se le permitiría instanciar una más, esto lo hice como precaución para futuras mecánicas que tengo pensadas, ahora vamos a probar.

Hice un nuevo script e hice todo el tema del movimiento de la bala a través de su componente Rigidbody.

**(Poner meme de cumeado)** Esto parece el sueño humedo de una adolescente, pero no es el resultado que esperaba y pasa por la propia corrutina, por suerte descubrí un método mas eficiente sin usar corrutinas y es simplemente usando una condición y funciona espectacular.

Y este fue el resultado, mucho mejor, también me había dado cuenta de que el cañón giraba muy despacio asi que solo le modifique el valor a la variable *speed*, mucho mejor.

Lo siguiente que hice lo mismo que en el caso de los asteroides es crear una condición que cuando la bala supere una cantidad x en el eje Y de su posición vuelva a la cola para ser reciclado.

Bien hasta aqui todo nos vemos en el próximo video por que se me acabó el tiempo, pero si os gustaría seguir viendo el progreso del desarrollo en tiempo real os dejaré el link al repositorio del proyecto en la descripción, ahora os paso con el Smulli al que le gusta despedirse en los videos, os la muestro en modo timelapse.

---

*Despedida*







