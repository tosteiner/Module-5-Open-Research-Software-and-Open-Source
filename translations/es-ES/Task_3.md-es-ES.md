---
output:
  html_document: defecto
  pdf_document: defecto
---

# Tarea 3: Cómo integrar Git con R Studio

Esta tarea está diseñada para estudiantes e investigadores que desean implementar un sistema de control de versiones dentro de un flujo de trabajo estándar basado en R. Esto se puede aplicar a una variedad de tareas de desarrollo de software, análisis de datos y gestión de proyectos. Tu futuro investigador te agradecerá la conveniencia.

No se olvide que usted puede participar en las discusiones sobre nuestra abierta [**canal Slack**](https://osmooc.herokuapp.com/). ¡Por favor, preséntese en # module5opensource, y cuéntenos un poco sobre quién es usted, su historial y cómo terminó aquí!

Tiempo estimado para completar: 30 minutos.

Estime el ahorro de tiempo una vez completado: Virtualmente infinito

**NOTA** Una versión de guía de video de esta tarea ahora está disponible en [YouTube](https://www.youtube.com/watch?v=Q-6jfjSAspA).

## Tabla de contenido

* [Empezando](#Getting_started) 
  * [Git](#Git)
  * [Estudio r](#Rstudio)
* [Paso uno: Descarga todas las cosas.](#one)
* [Paso dos: Configurar Git dentro de RStudio](#two)
* [Paso tres: ¿Por qué acabo de hacer eso?](#three)
* [Paso cuatro: El matrimonio perfecto entre Git y R](#four)
* [Paso cinco: Obtener contenido con contenido](#five)
* [Paso seis: Un compromiso valiente.](#six)
* [Paso siete: PUSH!](#seven)

## Empezando <a name="Getting_started"></a>

¡Felicidades por haber llegado tan lejos! Si estás leyendo esto, has sobrevivido a las solicitudes de extracción, a los ganchos web, y probablemente puedas incluso decirnos qué significa la F en FOSS (*no* Frustración ...). Es de esperar que hayas superado cualquier escepticismo o renuencia. hacia los beneficios de GitHub y Open Source Software, y están listos para dar el siguiente paso.

Antes de comenzar esta tarea, asegúrese de que ya ha completado [Tareas 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) y [Tarea 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), para que esté más familiarizado con GitHub y algunas prácticas estándar de código abierto.

Esta tarea le enseñará cómo integrar el software de control de versiones, Git, con el popular entorno de codificación, RStudio. Y sí, es Git como en gif o Dios, no Jit como en la forma incorrecta de pronunciar las cosas.

Si usted es uno de esos investigadores que piensa que el tener código distribuido en varios discos duros que están a punto de interrumpirse, Dropbox, Google Drive o cualquier otro software no especializado, esta tarea es solo para usted. Si alguna vez ha experimentado el proceso de adormecimiento mental de tener múltiples versiones 'finales' de un documento rebotando entre diferentes coautores, esto también es para usted.

Todos nosotros somos culpables de este tipo de cosas de vez en cuando, pero hay maneras de hacerlo que son mejores para usted, para el futuro y para aquellos que podrían beneficiarse de su trabajo.

  


### Conseguir git <a name="Git"></a>

Entonces, ¿qué es Git y en qué se diferencia de GitHub? Git es un sistema de control de versiones, que le permite guardar y rastrear copias de su trabajo con sello de tiempo durante el proceso de desarrollo. También funciona con elementos no codificados, como este MOOC, la mayoría de los cuales se escribieron en markdown en RStudio y se integraron con un flujo de trabajo Git / GitHub.

Esto es importante, ya que todas las investigaciones pasan por cambios y, a veces, queremos saber cuáles fueron esas cosas. ¿Borraste un texto que ahora crees que es importante? El control de versiones guardará eso para ti. ¿Funcionó su código perfectamente en el pasado, pero ahora está lleno de errores? Control de versiones. Es una excelente manera de evitar ese estado caótico en el que tiene varias copias del mismo archivo, pero sin una convención de nombres de archivos estúpida y molesta. `FINAL_Revised_2.2_supervisor_edits_ver1.7_scream.txt` será cosa del pasado.

GitHub es la plataforma que le permite compartir sin problemas el código de su área de trabajo (por ejemplo, una computadora portátil) para ser alojado en un espacio en línea. Entonces, algo así como la interfaz pública de GitHub. Las ventajas de Git / GitHub son:

1. Tienes la oportunidad de guardar copias de todo tu trabajo a través del tiempo;
2. Puede comparar el trabajo a través de diferentes copias a través del tiempo, lo que ayuda a detectar errores o errores;
3. Otras personas pueden colaborar abiertamente con tu trabajo;
4. Tiene una copia local y en línea de su trabajo que permanece sincronizada;
5. Es totalmente transparente en cuanto a quién hizo una contribución, por qué la hicieron y cuándo; y
6. Puede tener varias personas trabajando en el mismo proyecto a la vez en paralelo.

Si bien esto fue diseñado principalmente para el código fuente, debería ser instantáneamente obvio cómo esto se convierte en una herramienta poderosa para prácticamente todos los flujos de trabajo de investigación.

  


### RStudio <a name="Rstudio"></a>

RStudio es un entorno de codificación popular para los investigadores que usan el lenguaje de programación estadística, R. Viene con un editor de texto, por lo que no tiene que instalar otro y alternar entre ellos. También incluye una interfaz gráfica de usuario (GUI) para Git y GitHub, que utilizaremos aquí.

¿No es agradable cuando las brillantes herramientas de código abierto se integran perfectamente así? Esto debería ayudar a que su uso diario de Git sea mucho más sencillo.

Si en algún momento necesita instalar nuevos paquetes para R, simplemente use el siguiente comando:

`install.packages ("NOMBRE DEL PAQUETE", dependencias = VERDADERO)`

Reemplazando `NOMBRE DEL PAQUETE` con el, er, nombre del paquete. Algunos ejemplos con los que puede jugar que pueden ser útiles incluyen `knitr`, `devtools` o `ggplot2`.

  


## Paso uno: Descarga todas las cosas. <a name="one"></a>

1. Ya deberías tener una cuenta de GitHub si has seguido las tareas anteriores. Si no, [regístrate aquí](https://github.com/). ¡Repositorios ilimitados gratis para todos!
2. Descarga e instala la última versión de [R](https://www.r-project.org/). También disponible para [Mac](https://cloud.r-project.org/) y [Linux](https://cloud.r-project.org/bin/linux/).
3. Descarga e instala la última versión de [Rstudio](https://www.rstudio.com/products/rstudio/#Desktop). Oh, hey, lo parece Open Source! Silbido.
4. Descarga e instala la última versión de [Git](https://gitforwindows.org/). **Asegúrese de seleccionar "Usar Git desde el símbolo del sistema de Windows" durante la instalación.**

> **Pro-tip**: para actualizar todos sus paquetes R en uno, simplemente ejecute el siguiente código `paquetes <code> actualización (preguntar = FALSO, checkBuilt = VERDADERO)`

Por ahora, simplemente elija todas las opciones predeterminadas habituales para cada instalación. Dependiendo de qué sistema operativo (por ejemplo, Mac, Windows, Linux), esto podría ser diferente para cada uno de ustedes. Por ahora, y por el resto de esta tarea, nos limitaremos a hacer las cosas de la manera más sencilla de Windows (pero también proporcionaremos algunas instrucciones para usar la línea de comandos).

Para usuarios de Linux o Debian, simplemente use el siguiente comando para instalar Git:

`sudo apt-get install git-core`

Para usuarios de Mac, [este enlace](http://git-scm.com/download/mac), o compre una nueva computadora portátil con un sistema operativo diferente.

Si lo desea, también puede descargar la versión [local de GitHub](https://desktop.github.com/) y usarla a través de la sencilla GUI. Está disponible en Windows, Mac y Linux, y puede hacer su vida un poco más fácil, especialmente si desea usar una plataforma diferente para RStudio.

> **Pro-tip:** Verás cuando instalas Git dice '¿Usar Git Bash como shell para proyectos Git?' Este es el lugar donde puede usar la línea de comandos para acceder a Git desde fuera de RStudio. Es una bestia poderosa. Pruebe los siguientes dos comandos para comenzar:

`git config --global user.name 'SU NOMBRE DE USUARIO'`   
`git config --global user.email 'YOUR EMAIL'`   


## Paso dos: Configurar Git dentro de RStudio <a name="two"></a>

Correcto, eso es lo más fácil. Luego, ingrese a RStudio, y en las pestañas en la parte superior vaya a Ir a **Herramientas> Opciones globales> Git / SVN**. SVN es solo otro sistema de control de versiones como Git, y no tenemos que preocuparnos por eso aquí.

En el lugar donde dice *ejecutable Git*, agregue la ruta aquí al archivo git.exe que acaba de descargar en el paso anterior. Asegúrese de que la casilla aquí que dice **Habilitar la interfaz de control de versión para proyectos de RStudio** esté marcada. Esto ahora ha vinculado el control de versiones a proyectos futuros en RStudio, para proporcionar una dimensión adicional realmente poderosa al trabajo colaborativo o en solitario.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/git_svn.png?raw=true" width="400px"/>
</p>

<p align="center"><i>La ventana de Opciones Globales dentro de RStudio</i></p>

  


Luego, presione el botón en esta ventana que dice *Crear RSA Clave*, esta es una clave privada que se usa para la autenticación entre diferentes sistemas y le evita tener que escribir su contraseña una y otra vez. Aquí, aparecerá una nueva ventana con una clave pública, que desea copiar en su portapapeles.

Dirígete a GitHub, ve a la configuración de tu perfil, y a la pestaña *SSH y GPG keys*. Haga clic en *Nueva clave SSH*. Aquí, pegue la clave de RStudio y llámelo algo imaginativo como 'RStudio'.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/ssh_key.png?raw=true" width="800px"/>
</p>

<p align="center"><i>Dentro de GitHub, donde querrá ingresar la clave que acaba de generar en RStudio</i></p>

  


Bien, ahora, aferrate a tus extremos, vamos a entrar en la línea de comandos. No se preocupe si nunca ha usado el shell antes porque es muy similar a usar R, o cualquier otro sistema de codificación. Sin embargo, la principal diferencia aquí es que, en lugar de llamar a funciones como en R, se llaman comandos.

De nuevo en RStudio, vaya a **Herramientas> Shell**, y se abrirá una ventana del símbolo del sistema. Si ya jugaste con el Git Bash anterior, ya deberías haber hecho este paso. Ingrese los siguientes dos comandos:

`git config --global user.name 'SU NOMBRE DE USUARIO'`   
`git config --global user.email 'YOUR EMAIL'`   


Esperemos que no sea necesario decir que sustituya su propio nombre de usuario y correo electrónico de GitHub aquí. Puede acceder a esto en cualquier momento con solo encontrar el 'Shell' dentro de Windows. O bien, si hace clic con el botón derecho en cualquier carpeta de su escritorio que esté vinculada a un repositorio de GitHub, puede abrir el Shell al instante y eliminar.

Lo que esta etapa ha hecho es configurar Git, que es un software que se ejecuta en su escritorio, a GitHub, que es un sitio web de repositorio.

Reinicie R Studio. Menos mal, eso fue duro. Siguiente.

  


## Paso tres: ¿Por qué acabo de hacer eso? <a name="three"></a>

Bien, mantén la respiración, vamos a hacer una pausa aquí solo para aprender algunos comandos básicos de Git. Algunas de las claves que podrías hacer con el aprendizaje son:

* **Agregar**: aquí es donde envía los archivos al área de preparación antes de confirmarlos.

* **Commit** Esto es como "guardar" su trabajo creando una nueva versión o copia.

* **Push**: así es como envía archivos desde su proyecto local al repositorio en línea.

* **Pull**: Esta es la forma en que obtiene los archivos de su repositorio en línea a su proyecto local.

De vuelta en RStudio, escriba lo siguiente en el Terminal</em>*, o abriendo un nuevo Shell:</p> 

`git añadir.`

No hará nada por el momento, pero en el futuro agregará todos los archivos en su directorio de trabajo actual (eso es lo que hace el `` ) a la preparación lista para un compromiso.

  


## Paso cuatro: El matrimonio perfecto entre Git y R <a name="four"></a>

Ahora, en la Tarea 1, deberías haber aprendido cómo construir tu primer repositorio de GitHub. Si no lo has hecho, podemos esperar aquí mientras haces eso. Si ya lo tiene, o tiene un repositorio de GitHub, podemos continuar.

Entonces, deberías tener un repositorio en GitHub, completo con un archivo `README` , un archivo `LICENCIA` y algunos otros bits y bobs.

Lo que vamos a hacer ahora, es integrar ese repositorio con Git. Estable ahora.

1. En primer lugar, vaya a **Proyecto> Crear proyecto> Control de versiones> Git**.
2. De vuelta en GitHub, debería ver un poco donde hay una URL https: //. Ese es el enlace a su repositorio, y le da la opción de clonarlo en su escritorio. Por ahora, simplemente copie ese enlace, vuelva a RStudio y péguelo en la 'URL del repositorio' como se indica.
3. Dale al proyecto un nombre de directorio, como prueba, Jim o lo que quieras.
4. A continuación, busque el lugar en su escritorio donde desea que este proyecto viva, su subdirectorio.
5. Haga clic en 'Crear proyecto', y deje que la magia se haga!

Lo que acaba de hacer fue decirle a RStudio que asocie un nuevo proyecto en R con un repositorio específico en GitHub.

## **Paso cuatro: Alternativa**

Si aún no ha construido su primer repositorio en GitHub, aquí podemos hacer algo ligeramente diferente. En RStudio, haga clic en *Nuevo proyecto* y luego en *Nuevo directorio*. Llámelo como desee y cambie el directorio según sea necesario, asegúrese de marcar *Crear un repositorio git*y luego hacer clic en *Crear Proyecto*. Esto crea un archivo `.Rproj` , que puede administrar de la manera habitual a través de RStudio, incluyendo la adición de `archivos README.md`y `LICENSE.md` como se explica en la Tarea 1.

## Paso cinco: Obtener contenido con contenido <a name="five"></a>

¿Recuerdas ese archivo `README` que creamos hace un tiempo? Bueno, es hora de escribirlo. Pensando en la Tarea 1, hubo algunas cosas específicas que dijimos que hacen un buen archivo de `README`. ¿Recuerdas qué fue alguno de ellos? Solo para refrescar tu memoria, estas fueron:

* ¿De qué se trata este proyecto y qué hace?
* ¿Por qué debería importarle a la gente y por qué es útil?
* ¿Cómo puede alguien comenzar a contribuir al proyecto?
* A quién se puede contactar en caso de que alguien necesite ayuda.
* Un enlace a la licencia, pautas de contribución y código de conducta.
* Una descripción de la estructura del proyecto.
* Quién está involucrado, y cuáles son sus roles.
* El estado actual del proyecto.

Entonces, en RStudio, abra ese archivo e intente agregar solo un poco de información sobre esto para su proyecto. Si está haciendo esto para un proyecto real, intente y hágalo útil. Si solo estás jugando un poco por ahora, puedes agregar lo que quieras.

Recuerde que su archivo `README` está en formato markdown (.md). Para un repaso de algunos de los usos simples de reducción del precio de sintaxis, que mira esto [cheatsheet útil](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/markdown.png?raw=true" width="600px"/>
</p>

<p align="center"><i>Captura de pantalla de lo que este módulo se ve en markdown, durante el desarrollo. Meta.</i></p>

  


## Paso seis: Un compromiso valiente. <a name="six"></a>

De acuerdo, ahora debería tener un archivo `README` bien editado. Ahora vamos a 'confirmar' esto al proyecto usando Git. Este es básicamente el equivalente a guardar esta versión de su proyecto, con un registro de los cambios realizados. Las confirmaciones sucesivas producen un historial que se puede examinar más adelante, lo que le permite trabajar con confianza.

Hay algunas maneras de hacer esto.

1. Vaya a **Herramientas> Control de versiones> Confirmar**
2. En el panel de entorno en RStudio, debería haber una nueva pestaña 'Git'. Práctico.
3. En el panel de la consola, ahora debería haber un nuevo 'Terminal', mediante el cual puede ejecutar las líneas de comando de Git.

Sigamos con la segunda opción por ahora. Este panel de Git le muestra qué archivos se han cambiado e incluye botones para los comandos de Git más importantes que vimos anteriormente.

Seleccione el archivo `README` en la ventana de Git, que se mostrará automáticamente si ha realizado ediciones en él. Esto agrega ese archivo al área de "preparación", que es algo así como el espacio de guardado previo para su trabajo. Haga clic en 'Confirmar' y aparecerá una nueva ventana.

Aquí, tienes la oportunidad de revisar tus cambios y escribir un buen mensaje de confirmación. Escriba algo breve, pero informativo sobre los cambios que ha realizado en esta versión o instantánea de su trabajo. Desea que esta información sea suficiente para que, si usted u otra persona miran hacia atrás, sabrán por qué cometieron este compromiso y los cambios asociados con él. Estas son como redes de seguridad para su proyecto en caso de que necesite retirarse por alguna razón.

> **Pro-tip**: Aquí verá una lista de todos los cambios que ha realizado desde su último compromiso. Las líneas eliminadas más antiguas están en rojo, y las líneas recién agregadas están en verde. Verifique dos veces para asegurarse de que las ediciones que ha realizado son las que deseaba realizar. Esto es realmente útil para detectar errores tipográficos, ediciones parciales y cualquier otro pequeño error que pueda haber introducido accidentalmente. Seguridad primero.

**Nota** Si es ciego al color y no puede ver qué líneas se han agregado o eliminado, puede usar los números de línea en las dos columnas a la izquierda de la ventana como guía. Aquí, el número en la primera columna identifica la versión anterior, y el número en la segunda columna identifica la nueva versión.

Ahora, cuando haga clic en "Confirmar", aparecerá otra ventana que le indicará cuántos archivos ha cambiado y la cantidad de líneas dentro de ese archivo que ha cambiado. Cierra esa pequeña ventana hacia abajo.

  


## Paso siete: PUSH! <a name="seven"></a>

Haga clic en el botón *Push* en la parte superior derecha de la nueva ventana. Una nueva ventana aparecerá ahora. Lo que está haciendo es sincronizar los archivos modificados en su repositorio local con el archivo `README` a la versión en línea del proyecto en GitHub.

Para hacer esto desde el Shell, use el siguiente comando:

`git push -u maestro de origen`

Algunas veces aquí se le solicitará que agregue su nombre de usuario y contraseña de GitHub, lo que debe hacer si se le solicita.

Cierra esa ventana, y la siguiente. Vaya a su proyecto en GitHub, actualice y compruebe que el archivo `README` aún está allí en toda su gloria recién editada. Debería ver el mensaje de confirmación que hizo junto al archivo también.

  


**OPCIONAL AVANZADO / PASO IMPRESIONANTE**

Muy bien, así que acabas de enviar contenido a tu primer repo, ¡increíble! Ahora pongámoslo en práctica para un proyecto real. Como en el que estás participando ahora. Probemos esto:

1. Vaya al repositorio de este proyecto en [GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source)

2. Bifurca el repositorio a tu propia cuenta de GitHub. La URL para esto debe ser: `https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source.git`

3. Diríjase a RStudio, vaya a **Archivo> Nuevo proyecto**, elija *Version Control*, seleccione *Git*y luego pegue la URL del repositorio bifurcado que se encuentra en su copia del repositorio. Ahora tiene su propia copia versionada de todo este módulo. Ordenado. Guarde esto en algún lugar de su máquina local.

4. Ahora, debe decirle a Git que existe una versión diferente de este proyecto. Abra el *Shell*e ingrese el comando: `git remoto agregar hacia arriba https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source`

5. Lo que acaba de hacer fue nombrar la rama original aquí `aguas arriba`, solo para mantener las cosas simples por ahora. Ahora, cree un nuevo **rama** para documentar sus cambios independientemente de la rama principal. Ingrese el comando: `git checkout -b propuesto-cambios maestro`

6. Acaba de crear una nueva rama llamada `cambios propuestos` donde ahora puede editar todo el contenido y los archivos para deleite de su corazón. Con suerte, la estructura de este proyecto es lo suficientemente simple para que usted pueda navegar. Todos los archivos sin procesar del MOOC se pueden encontrar en la carpeta `content_development` , y esto es `Task_3.md`.

7. Si se desplaza hasta la parte inferior de `Tarea_3.md`, debería ver un lugar donde pueda editar su nombre y afiliación. Agregue estos y luego siga el procedimiento de confirmación detallado anteriormente. Si ve algo más que también necesita ser editado, ¡siéntase libre de agregarlo también!

8. Ahora, desea reenviar los cambios a la rama original. Use el siguiente comando en su *Shell*: `git push origin propuestos-cambios`

9. Vuelve a GitHub y encuentra tu tenedor aquí. Haga clic en el pequeño botón verde y cree una solicitud de extracción. Esto es esencialmente una revisión para integrar los cambios realizados en la sucursal original para este proyecto MOOC.

10.     Los propietarios a cargo del proyecto MOOC ahora recibirán una notificación de esto, lo revisarán y lo confirmarán si todo salió según lo planeado. Lo revisaremos y, si todo salió bien, su nombre aparecerá ahora por toda la eternidad como alguien que completó esta tarea avanzada.
      

11.     ¡Tómate una taza de té, café o vino para celebrar!
      

**FELICIDADES**

Acaba de integrar Git con R Studio e hizo su primer cambio a un proyecto de versión controlada. Su vida ahora nunca será la misma, y su flujo de trabajo de investigación probablemente será más rápido, ágil y colaborativo que nunca. Buena suerte volviendo a Word.

Lo bueno es que esto no tiene que ser usado solo para el código. Puede usarlo para texto sin formato, markdown, html y, bueno, código R. Las posibilidades son ilimitadas: lo que acaba de aprender es una nueva forma de gestión de proyectos de colaboración abierta que funciona para una enorme variedad de tareas.

De ahora en adelante, todo depende de ti! Algunos consejos son:

* Hacer confirmaciones frecuentes. Trata a Git como a tu cachorro, ya que requiere atención constante y especial. Solo una palmadita en la cabeza de vez en cuando es suficiente para mantenerlo satisfecho, pero será más feliz con un servicio sostenido.

* La mejor manera de hacerlo es comprometerse cada vez que trabaje en un problema específico. Por ejemplo, escribir un párrafo, ejecutar un análisis o corregir un error.

* Empuje a menudo. No permita que esos compromisos se acumulen, de lo contrario, corre más riesgo de entrar en conflictos de combinación. Ya que estas pueden ser una pesadilla, solo asegúrate de presionar con frecuencia.

* Tire a menudo. Si otros están trabajando de forma remota en el mismo proyecto, querrá estar al día con sus cambios. Asegúrate de introducir con frecuencia los cambios de GitHub para asegurarte de que todos estén sincronizados.

* Experimenta y explora! Esta tarea realmente solo araña la superficie, y existen muchas funciones, herramientas y formas diferentes en las que se puede utilizar. En realidad, depende de usted averiguar cómo utilizar esta información para mejorar su flujo de trabajo de investigación y, en última instancia, colaborar en una investigación mejor, más abierta y confiable.

* Para obtener más información acerca de los problemas, ramas, conflictos de fusión, tiran de las solicitudes, y otros aspectos avanzados de usar Git y rstudio, echa un vistazo a esta [guía impresionante](http://r-pkgs.had.co.nz/git.html) por Hadley Wickham.

  


**¿Sabes de qué manera se puede mejorar este contenido?**

¡Es hora de tomar tus nuevas habilidades GitHub para una prueba de ejecución! Todo el desarrollo de contenido ocurre principalmente [aquí](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md). Si tiene una mejora sugerida en el contenido, el diseño o cualquier otra cosa, puede hacerlo y luego se convertirá automáticamente en parte del contenido de MOOC después de la verificación de un moderador.

## Lista de participantes que completaron la versión AVANZADA de esta tarea

* Brendan Palmer, CRF-C, University College Cork
* Lisa Matthias, Freie Universität Berlin
* Hollie Marshall, Universidad de Leicester 
* Eric D. Wilkey, Western University, Canadá
* José-Raúl Canay-Pazos, Universidad de Santiago de Compostela, España
* Encarnación Martínez Álvarez, España
* Alberto Albz Marocchino, Italia
* Iratxe Rubio, Centro Vasco para el Cambio Climático BC3
* Gabriele Orlandi, Escuela de Estudios Avanzados en Ciencias Sociales (EHESS) de París, Francia
* Hande Sodacı, Turquía
* Luke W. Johnston, Universidad de Aarhus, Dinamarca
* Philippe Joly, WZB y HU-Berlín
* Paul Griffiths, NCAS y U. Cambridge
* Harin Lee, Goldsmiths, Universidad de Londres
* Luis Camacho, Universidad Católica, Perú
* Tom Cridford, Imperial College de Londres
* Nithiya Streethran, Universidad de Stavanger 

[![Dedicación de dominio público CC0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)