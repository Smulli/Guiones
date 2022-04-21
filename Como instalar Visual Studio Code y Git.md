## Introducción:

---

Hola muy buenas estamos aquí de nuevo en este devastador video para aprender cosas que ya todo el mundo en este punto debería saber, sin embargo nunca está de más repasar algunos conceptos que definitivamente la gran mayoría ya habréis olvidado.

Pues en este video os enseñaré a como instalar debidamente nuestro editor de código completamente gratuito. **(Mostrar logo de Visual Studio Code)** ,para que podáis comenzar a programar vuestras aberraciones ya bien sea construidas desde cero en el editor o bien hechas con las propias librerias que nuestro querido amigo Unity nos brinda.

De paso también os enseñaré a como guardar vuestros proyectos en la nube para que así, si algún día se os peta el disco duro o cualquier asunto turbio que tenga que ver con vuestro pc ardiendo. **(Mostrar imagen de pc ardiendo)**, no lo tengáis que lamentar al no tener un respaldo de vuestro proyecto a buen recaudo.

## Instalación de Visual Studio Code:

---

Estupendo pues lo primero que haremos es descargar nuestro fabuloso editor de código, no os preocupéis, os dejaré los enlaces en la descripción para que no os perdáis en esta travesía, lo descargaremos directamente haciendo click en este botón de aquí y automáticamente comenzará la descarga, en mi caso será para Windows pero por si sois un poco raritos y os consideráis altamente uniks y detergentes. **(Mostrar imagen de Harley Queen)**, por el hecho de no haber accedido. **(Mostrar logo de Windows)**, a tocar un Windows ni con un palo, podéis hacer click en la flechita de al lado del botón para ver cual de las versiones os puede venir mejor para vuestro sistema operativo.

Une vez descargado ejecutamos el instalador y como en cualquier programa le daremos siguiente hasta que nos deje instalar definitivamente el editor. **(Mostrar el editor después de la instalación)**.

## Explicación de Git

---

Bien ahora pasaremos a la herramienta de control de versiones que sin duda alguna nos salvará el culo en caso de que nuestro pc haga la inmolación. **(Mostrar otra imágen de pc ardiendo)** y así podamos salvaguardar nuestro proyecto en la nube y recuperarlo en cualquier momento y desde cualquier dispositivo.

Git es un programa de control de versiones ¿Y eso qué pallaringas quiere decir? Que es un software el cual nos permitirá guardarlos como dije antes, en un repositorio en la nube que hayamos creado previamente que en el caso de Git sería en los de GitHub, esto no solo será útil por si nuestro pc decide morir si no que también puede llegar a ser especialmente útil en situaciones en donde eliminemos los ficheros y archivos del proyecto por error. **(Mostrar imagen de programador enfurecido)**, o si llegaramos a complicar demasiado nuestro proyecto o cometemos alguna cagada, básicamente vas a poder restablecerlo a una versión más antigua si es que la llegaste a alojar antes por supuesto, asi que por eso es muy importate que después de cada actualización que nosotros consideremos como estable nos acordemos de guardarlo mediante Git en dicho repositorio, esto puede parecer algo muy pesado y que le daría flojera hasta a tu perro. **(Mostrar imagen de perro perezoso)**, pero creedme cuando os digo que es muy sencillo de hacer y que lo vais a agradecer un montón el hecho de acostumbraros a hacerlo. **(Mostrar imagen de vault boy)**.

## Instalación de Git

---

Perfecto ahora que entendimos que es Git llega el momento de su instalación, es realmente fácil nos venimos al sitio web de Git y como previamente en la instalación de Visual instalaremos la versión que más se adecue a nuestro Sistema Operativo, le damos siguiente a todo hasta finalizar la instalación.

## Configuración de Git

---

Ahora la forma de usar Git puede abrumar a muchos ya que no es un programa que no tiene ninguna característica visual mas allá de los comandos que usaremos para trabajar con él. 

Pero que no os asuste ver una ventana completamente negra con unas letras de colores ya que es realmente fácil de usar. **(Mostrar imagen de un michi)**, bueno pues lo primero que tenemos que hacer es ir a nuestro perfil de GitHub y crear un nuevo repositorio, para ello le damos a este botón verde de aquí, le damos un nombre, una descripción si así lo queremos y así al resto de opciones os lo dejo a vuestro sabio criterio, le damos al botón y así ya tendremos nuestro precioso repositorio de GitHub creado en donde algunos de vosotros a lo mejor lo usaréis como basurero personal. **(Mostrar imagen de basura en África)**, pero la gran mayoría lo usará para lo que fue concebido.

Lo segundo que deberemos hacer es crear un token de acceso personal o PAT para los amigos, ya que Git nos lo pedirá más tarde posiblemente para subir los archivos, básicamente este token funcionará como una password de toda la vida de tu cuenta y os preguntaréis no puedo usar la password de mi cuenta al momento de iniciar sesión en Git? Pues eso tendría lógica. **(Mostrar imagen de estrategia)** lo que pasa es que GitHub decidió eliminar esa característica para brindar mayor seguridad al usuario así que en vez de introducir tu password regular tendremos que iniciar sesión con dicho token, os dejaré el enlace en la descripción de una página bastante completa de GitHub en donde os enseñaran a crear vuestro propio token de acceso personal, sigamos con el resto del vídeo por que si no se hará excesivamente largo.

Ya teniendo nuestro token de acceso personal a continuación iniciaremos sesión en nuestra cuenta de GitHub desde Git, para ello escribiremos los siguientes comandos:

```
git config --global user.name "USERNAME"
```

 * Aquí iría nuestro username de nuestra cuenta de GitHub".

```
git config --global user.email "EMAIL"
```

 * Nuestro email asociado a nuestra cuenta.

```
git config --global github.user "USERNAME"
```

 * y con este comando introduciremos nuestra clave del token que hayamos creado, importante guardar en un sitio seguro la clave de este token ya que si desaparece después no la podremos recuperar:

```
git config --global github.token "OUR TOKEN"
```
## Clonación de un repositorio

---

Lo siguiente que haremos es clonar nuestro repositorio de GitHub para poder subir nuestros archivos, vamos a crear una carpeta donde guardaremos el repositorio de forma local le damos click derecho en la ventana de nuestro fichero y le damos a la opción "Git Bash here" y listo Git ahora se encuentra ubicado en nuestra carpeta totalmente vacía pero que no lo estará por mucho tiempo, ahora lo que tenemos que escribir es el comando:

```
git clone
```

, aquí paramos de escribir y nos dirijimos nuevamente a nuestro repositorio en GitHub, le damos en este botoncito de aquí y empezaras a ver muchas cosas que pulsar pero tranquilo de momento solo céntrate en copiar este código de aquí y pegarlo al lado del comando git clone, lo puedes hacer mediante atajos de teclado con Shift + Insert o con click derecho pegar, una vez hayáis descargado la información de nuestro repositorio aparecerá en nuestro pc en forma de carpeta, ubicaremos nuestro Git en dicha carpeta como hago eso? Pues simplemente escribimos el comando cd y escribimos el nombre del repositorio tal cual como lo vemos en la carpeta y así Git se moverá al interior de nuestro repositorio para confirmar que esto sea cierto escribimos el comando ls y Git nos otorgará todo lo que contiene dicha carpeta.

Bien ahora crearé un archivo txt normal y corriente le añadiremos texto y le pondremos un nombre y con esto es más que suficiente para enseñaros un claro ejemplo, para comprobar las actualizaciones y cambios que le hayamos hecho a nuestro repositorio basta con que vayamos a Git y escribamos el comando:

```
git status
```

, aquí nos aparecerá información muy precisa de nuestros cambios y avances ahora para subirlo únicamente tenemos que escribir 3 sencillos comandos, escribiremos primero:

```
git add .
```
, posteriormente deberemos hacer un comentario de lo que estamos subiendo al repositorio importantísimo ya sea para dejar una advertencia o información clave a tu yo del futuro o estás trabajando con un equipo siempre tienes que brindar información de los cambios que has realizado para que vuestros proyectos no se conviertan en infiernos laborales, para ello escribiremos:

```
git commit
```

seguido de un:

```
-m
```

mensaje y ahora entre comillas escribiremos a que se debe esta actualización o cambio que hayamos realizado y definitivamente para poder subirlo a GitHub escribiremos lo siguiente, para esto es importante que nos encontremos en la rama main de nuestro repositorio o cualquier alguna que nosotros hayamos creado o esto no funcionará, escribimos:

```
git push origin main
```

le damos a enter y automáticamente empezará con la subida lógicamente dependiendo de la cantidad de cosas que le queramos subir al repo, tardará más o menos tiempo, fabuloso ahora nos dirijiremos a nuestro repositorio de GitHub y veremos como nuestro archivo de prueba se ha subido correctamente con su commit y cotenido. **(Reproducir sonido de Yaaay!)**

## Despedida

---

Espero que no os hayáis perdido por el camino que hemos recorrido juntos y recordad suscribiros a este hermoso canal para ver más del contenido que estamos desarrollando para vosotros, comentad que os ha parecido el vídeo no te olvides de tu likesito, por último podéis seguirnos a nuestra cuenta de Twitter como TheSecretTK y seguir los directos en el canal de Twitch de nuestro queridísimo overlord, allí le podéis ver hacer un montón de burradas ricolinas que de seguro no decepcionara a más de uno, nos vemos en el siguiente ¡chaoooo!




