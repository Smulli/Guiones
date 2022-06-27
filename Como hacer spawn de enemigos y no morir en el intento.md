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

Bien ahora si probé y todo parecía funcionar a la perfección al menos hasta el próximo video por que se me acabó el tiempo, pero si os gustaría seguir viendo el progreso del desarrollo en tiempo real os dejaré el link al repositorio del proyecto en la descripción, ahora os paso con el Smulli al que le gusta despedirse en los videos.

---

*Despedida*







