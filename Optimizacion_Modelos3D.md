# Guión: Optimización de Modelos 3D: Claves para Mejorar el Rendimiento en tus Videojuegos

*Pregunta*: ¿Alguna vez te preguntaste si tus modelos 3D están realmente optimazados para tu proyecto de animación, render o videojuego? ¿Podrías estar desperdiciando recursos valiosos en detalles innecesarios que no mejoran la experiencia del jugador?

*Introducción* : En el mundo de los videojuegos 3D como es en el caso que más nos atañe, la optimización de los modelos es esencial para garantizar el rendimiento fluido y evitar errores. 

A continuación, te presentamos cinco consejos clave para optimizar tus modelos 3D y mejorar la eficiencia de tus proyectos.

**Reducir el número de polígonos innecesarios** : Los polígonos que no son visibles para el jugador pueden ser eliminados sin afectar a la calidad visual del juego. Esto puede mejorar el rendimiento general en el juego y reducir el tiempo de carga.

¿Qué significa reducir el tiempo de carga en nuestros videojuegos? Muy simple, menos polígonos significan menos datos que deben ser cargados desde el disco duro o descargados desde un servidor, lo que se traduce en tiempos de carga más cortos ya que nuestro modelo pesa menos de un giga.

Esto mejorará la experiencia de nuestros jugadores, ya que no les harás esperar mucho tiempo para poder comenzar a jugar y lo podría hacer accesible a más consumidores ya que mejora la compatibilidad con hardware de menor rango.

Un caso muy curioso que se viene a la cabeza es el de los peatones de Cities Skylines 2, que le modelaron hasta el aspecto más irrelevante para un juego de su género, la dentadura de los modelos que la gente que pasea y hace su vida en la ciudad, esto provoco varias quejas ya que la mayor parte de la culpa de lo mal optimizado que estaba el juego era por culpa de detalles tan obvios como estos. 

Y ahora si pasando al siguiente punto.

**Unificar texturas en un solo material** : En lugar de tener múltiples materiales y texturas, puedes combinarlos en un solo archivo. Esto puede simplificar mucho el proceso de renderizado.

También mejora el consumo de memoria, puede facilitarte el proceso de desarrollo de tu proyecto y otorgar una mayor coherencia visual.

Este aspecto es importante por que al utilizar un material para instancias del modelo similares entre si, puede lograr una apariencia más consistente y uniforme en todo el juego. 

Algunos desarrolladores encuentran el equilibrio entre la clidad visual que proporcionan los materiales adicionales y el impacto que tienen hacia el rendimiento.

Sin embargo la forma mas estandarizada en la industria es el uso de materiales PBR, Phisically Based Rendering, para lograr un aspecto realista con una gestión más eficiente de recursos.

**Usar modelos LOD(Level-Of-Detail)** : Los modelos LOD permiten que el juego muestre diferentes niveles de detalle dependiendo de la distancia del jugador al objeto. Esto puede mejorar el rendimiento al reducir la cantidad de detalle de un objeto en la lejanía.

Y como siempre usar distintos LOD para tu juego trae otros varios aspectos positivos consigo, tiempos de carga más rápidos, mayor escalabilidad, mayor eficiencia de recursos, etc... 

**Simplificar el Rigging** : Un rigging más simple implementando el mínimo uso de huesos y datos como constraits y la distribución del peso en los mísmos, puede reducir la complejidad de los modelos. 

Es importante mantener el rigging lo más simple posible sin sacrificar la calidad de animaciones.

**Limitar el uso de físicas** : Limitar el uso de físicas en tiempo real es muy importante de cara al rendimiento general de nuestro proyecto.

Las físicas en tiempo real pueden requerir de una gran cantidad de recursos de la CPU, la GPU y la RAM, lo que puede afectar el rendimiento del juego.

Al limitar el uso de físicas, se pueden reducir demanda de procesamiento y lograr un rendimiento fluido y estable.
