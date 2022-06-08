# Saludo

Hola muy buenas estamos aquí en una nueva serie para el canal, en donde podréis aprender y repasar algunos conceptos tanto de programación como de modelaje a la par que también saber que se está cociendo dentro de las entrañas de nuestra prospera comunidad de desarrolladores humildes.

## La propuesta

---

Algunos se preguntaran que clase de droga del averno es Project Hope, bueno pues para decepción vuestra Project Hope no es ninguna droga si no un juego que estoy desarrollando de forma individual querido yonki **(Mostrar man tomando drogas)** en el que podrás controlar tu propio sistema de defensa planetario, y se te ordenará la protección de unas colonia stituadas en varios planetas que funcionaran como niveles del juego y habrá que defenderlas de una lluvia de asteroides con ayuda de un cañón que protege el centro de la colonia de amenazas orbitales llamado “Hope”, el juego se centra en mecánicas shoot em’up arcade de la vieja escuela estilo Missile Command un juego que seguramente lo conocerá tu tataratatara abuelo de la época del catapum **(Mostrar viejo suggar daddy)**, tendrá un ciclo infinito por rondas en la que la dificultad se ve aumentada a medida que vayas subiendo de rondas, para enfrentar las amenazas podrás mejorar a Hope con multitud de armas destruyendo los asteroides dorados, pero si los asteroides acaban arrasando todas las estructuras de la colonia el juego finalizará con un game over.

Bueno pues teniendo en cuenta la propuesta genérica de valor que tiene, voy a proceder a hablaros en que motor de desarrollo se realizará Project Hope, como se realizará el arte y posteriormente en siguientes episodios os mostraré su proceso de desarrollo tanto programando, como realizando arte y como componiendo música y efectos de sonido, pero si esta es la parte que más te llega a interesar del video y te sientes bastamente decepcionado pensando que en este vídeo no va a haber una chufa de desarrollo déjame decirte que estás muy errado querido amigo simionte, ya que al final de este vídeo te mostraré como programo la rotación de nuestro largo y erecto cañón.

## Unity (como no)

---

Bueno pues como en el 99,9% de juegos desarrollados por desarrolladores humildes alfa el juego se formará desde lo más bajo como una pieza de arte que solo tu madre podría apreciar vagamente y colocarlo en la parte más inferior del portón de la nevera **(Mostrar imágen de dibujo mal hecho en nevera)**, hasta ser una obra de arte moderno en el motor de Unity, lo cual saber donde trabajaré en este proyecto a estas alturas no debería sorprender absolutamente a nadie, pero por si hay algún que otro despistado que no se haya pispado del palo que vamos tenemos un bonito vídeo en donde enseñamos el proceso de instalación de Unity y del que estoy seguro no te decepcionará dejar tus prejuicios de rarito de Godot y probar esta maravilla del software de creación de videojuegos.

## El Arte
---

Bueno pues como sabe todo el mundo el arte es indispensable para helarte de frío y vivir en una esquina durmiendo en cajas de cartón a menos de que seas uno de los pocos modeladores o diseñadores de niveles que quedan en la industría que no haya sido sustituidos por inteligencias artificiales que hacen el trabajo sin cobrar **(Mostrar meme de artista en la calle)** ... Quiero decir, olvidad lo que acabo de decir amables y exitosos artistas 3D vosotros sois los que más aportáis a la industria y eso nadie lo duda **(Mostrar imagen de turba enfurecida)** nada es mas indispensable que crear buen arte, es absolutamente necesario para cualquier juego a día de hoy que se considere como un proyecto digerible, asi que a lo largo y ancho de esta serie de video vlogs de desarrollo me veréis mucho utilizar Blender, Gimp y otros programas que nos servirán para hacer todo tipo de magnificencias y de paso os mostraré atajos y trucos que he ido aprendiendo con la experiencia en el uso de estos softwares, sin duda no me estoy autocalifico como un experto pero para que el que más seguramente serán muy agradecidos.

## Movimiento del personaje

---

Bueno pues lo prometido es deuda en este vídeo veréis algo de lujurioso desarrollo del juego, no os asustéis ni de coña esta aberración será el arte del juego y algunos habréis deducido con gran acierto que solo se trata de un nivel de prueba en donde se establecen las mecánicas base y se pulen antes de ponerse a trabajar en el arte, en este caso vamos a añadir el movimiento a nuestro suculento y jugoso cañón, así que básicamente lo que pensé en un juego que simplemente haces rotar y disparas el cañón no fue especialmente complicado de pensar, solo tenemos que crear una variable de punto flotante que será nuestro ángulo y un evento en el que le diremos que cuando el usuario haga click o toque la pantalla de su móvil, el cañón obtendrá la posición del mouse en el eje X, pero  tenemos un grave problema en donde el cañón no deja de rotar así que lo que haremos es anclar 2 rotaciones una mínima y otra máxima para que así nuestro cañón no parezca un molino de agua fuera de control **(Mostrar vídeo de molino perdiendo el control)**. 

Crearé otras 2 variables en donde almacenaremos la rotación mínima y la rotación máxima en este caso de -40 y 40 y a continuación dentro del evento escribiremos una función matemática, no te preocupes mi IQ también es de -60 **(Mostrar a alguien nervioso)**, así que no te asustes compadre que sirve la leche del tazón de cereales **(Mostrar cereales)** antes de ponerlos en el tazón no usaremos matemáticas, solo usaré una función que me permitirá anclar la rotación del cañón con estas 2 variables que cree antes.

Y como ves ahora nuestro cañoncete solo rota en 40 y en menos -40 así que espero que aprender para que sirve esta función te haya resultado útil y no olvides querido amigo que lo puedes aplicar en cualquier tipo de transform.

## Despedida

---

Y como siempre no te olvides comentar que te ha parecido el video y de darle tu fabuloso likesito, la IA de youtube estará eternamente agradecida contigo, siguenos en nuestro twitter y en el canal de Twitch de nuestro querido overlord, nos vemos en otra ocasión compas ¡chao!

