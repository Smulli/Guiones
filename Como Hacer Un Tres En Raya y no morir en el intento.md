## Saludo

---

¿Siempre deseaste hacer tu propio OXO? Y no, no me refiero al OXXO que está en cada esquina de tu pueblo, me refiero al clásico de los clásicos, el juego que lo inicio todo, ¡El tres en raya con brillitos!

Pues sí mi estimado, hoy aprenderás a desarrollar tu propio 3 **(Mostrar meme de 3 tachado sustituido con un 5)**, **(añadir sonido de Smulli gritando 5!)** en raya con gráficos 3D hermosos y una iluminación NoPor que te hará replantearte tu sexualidad por las monas chinas o pensar de ir a terapia... A todo esto por si fuera poco le agregaré componente online para que así tú y tus amigos tengáis algo más para entreteneros que viendo memes del Xokas hasta las 3 en punto de la mañana.

¡Bueno, pues empezemos con el video!

Modelando assets del proyecto: Empezaremos creando nuestros hermosos modelos para nuestro 3 en raya **(sonido de Smulli chillado 5!)**. Y para esta tarea tendremos el privilegio de usar la que seguro es la herramienta por excelencia de modelaje 3D para gente humilde ¡Blender! Borraré el cubito por defecto de Blender, luego crearé otro y lo volveré a borrar. No sé because cubito por defecto de Blender... Blender lo pone para que lo borremos... Es la perra de Blender por defecto... Y eso... Y ahora si me pondré a Modelar unas fichas rápidamente con geometría básica y como buenas personas humildes que somos no usaré mi tiempo en hacerme mis propias texturas si no que lo emplearé en descargar las de alguien que ya lo haya hecho por mi y claro está si son gratuitas mejor que mejor, si no ni en pedo.

Utilizaré el Materialize el Substance Painter humilde, para generar las texturas de normal, mapa de altura, y oclusión ambiental que le añideré a nuestros lindos modelos.

Me moveré a Blender y después a la pestaña de Shading para configurar los materiales y dentro de exportar crearé una carpeta donde almacenaré el fbx del modelo y después de haber creado el proyecto agarraré esta carpeta y la introduciré suave y ricolinamente **(Tono sexy)** dentro de la carpeta de assets del proyecto.

## Creando el proyecto

---

Crearé un nuevo proyecto en Unity y seleccionaré la plantilla 3D URP Core.

Posteriormente procederé a cagarme en Unity por no descargar la pinche plantilla y usar la plantilla 3D de Unity estándar con mi corazón desecho por tantos sueños rotos... **(Mostrar man llorando)**.

Posteriormente procederé a cagarme en Unity por no descargar la pinche plantilla y usar la plantilla 3D de Unity estándar con mi corazón desecho por tantos sueños rotos... **(Mostrar man llorando)**.

Lo crearé olvidándome por completo de que todas las cosas de este mundo necesitan un nombre y le daré al botón de crear.

## Instalando paquetes y dependencias

---

**(Mostrar imagen de 2 years later...)** Después de esperar 2 años, 24 meses, 730 días, 17.520 pajas, para que me abriese el puto Unity comenzaré por instalar una serie de paquetes que nos resultaran de gran ayuda para el 3 en raya **(Sonido de Smulli ¡5!)** que vamos a hacer... Smulli que sí... Ya se que es ¡5! **(Sonido de Smulli diciendo por el culo te la inco!)**. 

Procedo a ir a la Market Place de Unreal para Unity, buscaré el asset llamado PUN2 de Photon, seleccionaré obviamente la versión para humildes y lo añadiré a mis assets, que lo podremos encontrar con facilidad dentro de *Windows -> Package Manager*, pero antes de instalar nada debemos registrarnos en photonengine.com y crear un proyecto de tipo PUN que por sus siglas significa Photon Unity Network.

Continuo instalando 3 paquetes más de vital importancia para que nuestro proyecto obtenga unos resultados notables, y son: CineMachine, TimeLine y TextMeshPro.

Crearé una carpeta llamada dependencias dentro del proyecto que lo usaré como basurero para toda la mierda instalada de los paquetes para que así no molesten.

## Configurando la iluminación de la escena

---

En la escena que usaremos de plantilla se deben realizar ciertas configuraciones, para que el juego no se vea como tú, cuando te acabas de despertar de una cruda.

Nos dirijiremos a la pestaña *Windows > Rendering > Lighting > Environment* y nos aparecerá una ventana bien chingonas para mejorar la iluminación de nuestra escena pero por el momento centrémonos en desactivar y bajar la intensidad de las luces de ambiente a 0.

Después quitaré la Directional Light de la escena ya que no la quieren ni para iluminar el corazón de tu ex y como sustitución añadiré 2 luces puntuales a cada lado de la escena, a continuación pongan el color y la intensidad que mas les agrade, para esto puedes añadir a la escena los objetos que importamos desde Blender y ver como queda.

Recuerda que es importante que reiteradamente en alguna ocasión presiones el comándo Ctrl + S para guardar el proyecto por si Unity decidiese trollearnos con un rico crasheo.

## Configurando el Tablero y las Fichas

---

Añado mi tablero a la escena importado de Blender, por que como buen artista que soy me gusta hacer todos mis assets desde 0 excepto cuando me da flojera modelarlos o texturizarlos, le colocaré un Mesh Collider, Crearé un cubo y ajustaré su escala para que tenga el mísmo tamaño que las celdas del tablero, marcaremos el collider del cubo como Trigger y lo colocaré en una layer distinta a la que llamaremos Celdas, renombraré el cubo como Cell y lo arrastraré a la pestaña de proyecto para convertirlo en prefab **(Mostrar meme de Cell sintió el verdadero terror)** Agregaré una ficha a la escena y le colocaré un Mesh Collider, la guardaré como otro prefab, y haré variantes de la misma "para las piesas", así para cuando tengamos que editarlas, podremos recurrir directamente al padre y se actualizarán el resto.

## Despedida

---

Espero que hayan seguido bien los pasos y recuerden suscribirse a este canal para ver más de mi contenido, comenten que les ha parecido el vídeo me ayudará mucho a seguir haciendolos, no te olvides de tu pulgarcito, por último puedes seguirme en mi cuenta de Twitter y también en Twitch, allí hago directos ricolinos y puedes verme picar código como un loco haciendo cosas chulas, me despido compas y nos vemos en el siguiente ¡chaoooo!