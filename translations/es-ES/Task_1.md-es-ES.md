---
output:
  html_document: defecto
  pdf_document: defecto
---

# Tarea 1: Cómo configurar un repositorio en GitHub

Esta tarea está diseñada para estudiantes e investigadores que desean crear su primer proyecto de código abierto (software o no software) en GitHub. GitHub es un lugar para que vengas a jugar y experimentar con nuevos flujos de trabajo de investigación, y es realmente solo el comienzo para ayudar a preparar el escenario para tus propios caminos e ideas.

No se olvide que usted puede participar en las discusiones sobre nuestra abierta [**canal Slack**](https://osmooc.herokuapp.com/). ¡Por favor, preséntese en # module5opensource, y cuéntenos un poco sobre quién es usted, su historial y cómo terminó aquí!

**NOTA** que hay una grabación para esta tarea pantalla también está disponible a través de [YouTube](https://www.youtube.com/watch?v=AnftV9HBPSc&).

Tiempo estimado para completar: 30-45 minutos.

Estimar el ahorro de tiempo una vez completado: Inimaginable ..

## Tabla de contenido

* [Empezando](#Getting_started) 
  * [Configurando un perfil de GitHub](#Profile)
  * [El lenguaje GitHub](#Language)
  * [Creando un nuevo repositorio](#Create_new)
* [Los pasos fundacionales](#Foundation) 
  * [Elegir una licencia](#License)
  * [Creando un archivo README](#Readme)
  * [Creación de lineamientos contribuyentes.](#Contributing)
  * [Creando un código de conducta.](#Conduct)
  * [Haciendo citable tu código](#Citation)
* [Manteniendo sus problemas al día.](#Issues)
* [Lista de verificación para lanzar tu proyecto](#Check-list)

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/Task1.png?raw=true" alt="Flujo de trabajo de la tarea 1" width="600" height="861" style="margin-right: 30px; margin-left: 10px;" onmouseover="this.width='1200'; this.height='1722'" onmouseout="this.width='600'; this.height='861'">
</p>

<p align="center"><i>El flujo de trabajo para la Tarea 1. ¡Mantenga esto a mano mientras trabaja en la tarea!</i></p>

  


## Empezando <a name="Getting_started"></a>

Un 'repositorio' es realmente un nombre elegante para un proyecto en GitHub. GitHub es un lugar en línea donde puede administrar proyectos, almacenar archivos y colaborar abiertamente con otros. Todo esto se logra utilizando el control de versiones para rastrear los proyectos a medida que avanzan. Como tal, GitHub es una herramienta poderosa para proyectos de software y no software.

Una de las cosas más importantes a considerar en esta etapa temprana es pensar cómo quiere que la comunidad en general interactúe con su proyecto. Mientras trabaja abiertamente, desea asegurarse de que los demás se sientan cómodos para acceder, ver y participar en su trabajo. Configurar un repositorio de manera que disminuya las barreras de entrada, y el temor de ser un "forastero" es el primer paso para mantener un proyecto exitoso.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/octocat.png?raw=true" width="150px" height="125px"/>
</p>

<p align="center"><i>Octocat, la pequeña mascota de GitHub</i></p>

  


### Configurando un perfil de GitHub <a name="Profile"></a>

Para configurar un perfil de GitHub, simplemente diríjase a la página principal y haga clic en [Registrarse en GitHub](https://github.com/join). Aquí, puede crear su cuenta personal, con un nombre de usuario, correo electrónico y contraseña como estándar.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/github_signup.png?raw=true" width="800" /></p>

<p align="center"><i>Registrarse en GitHub</i></p>

  


El siguiente paso es configurar un plan personal. Por ahora, simplemente seleccione el plan 'Repositorios públicos ilimitados de forma gratuita', a menos que esté preocupado por la privacidad, en cuyo caso seleccione el plan privado. Si pretende configurar un proyecto para una organización, también puede seleccionar esa opción.

  


### El lenguaje GitHub <a name="Language"></a>

Este es posiblemente el aspecto más confuso y desagradable de GitHub. Estos son algunos de los términos más utilizados y sus definiciones:

* **Inicializar**: Crear un repositorio vacío.
* **Checkout**: Crear una copia de trabajo de un repositorio local.
* **Clon**: copie el repositorio en un directorio local en su computadora.
* **Bifurcación**: cree una división personal de un repositorio para trabajar en él en paralelo.
* **Rama**: Una versión independiente y paralela de un repositorio. Los cambios no afectan la rama maestra.
* **Master**: la rama principal y predeterminada de un repositorio.
* **Limpio**: No hay confirmaciones pendientes en la rama.
* **Etapa**: agregue actualizaciones listas para comprometerse en una rama.
* **Commit**: Una revisión de un repositorio, como una función de 'guardar' versionada.
* **Mensaje**confirmación </strong> : una descripción de los cambios que acompañan a una confirmación.
* **Comprobación**: Una comprobación de estado.
* **Fetch**: Nada que ver con los perros. Se refiere a obtener los últimos cambios de un repositorio en línea sin fusionarlos.
* **Índice**: El 'árbol' que actúa como área de preparación.
* **Directorio de trabajo**: el 'árbol' donde se guardan los archivos.
* **Cabeza**: el 'árbol' que indica las últimas confirmaciones realizadas.
* **Push**: Agregue cambios comprometidos al encabezado de su repositorio remoto.
* **Fusión**: Combinando los cambios realizados en una rama con la rama maestra al finalizar.
* **Pull**: Actualiza tu repositorio al buscar y fusionar las confirmaciones más recientes.
* **Solicitud de extracción**: una solicitud para combinar una rama actualizada en la rama maestra.
* **Problema**: mejoras, tareas o preguntas sugeridas relacionadas con un repositorio.

¡Uf! No te preocupes por memorizar *todos* de estos por ahora. Como cualquier nueva habilidad, la familiaridad viene con la experiencia.

Probablemente pueda ver cómo algunos de estos son bastante similares a cosas como guardar, copiar, pegar, operaciones de flujo de trabajo estándar, pero adaptadas para un proceso de administración de software. También hay un [más](https://mirrors.edge.kernel.org/pub/software/scm/git/docs/gitglossary.html) , pero esto debería hacer para comenzar.

Si está interesado, la mayoría de estos términos provienen del sistema subyacente [Git](https://git-scm.com). Git fue creado para permitir a los desarrolladores administrar diferentes versiones de código fuente de manera distribuida, lo cual es genial. Tiene un montón de características y la capacidad de hacer un montón de cosas complejas, escrito por un [chico muy inteligente](https://www.linuxfoundation.org/blog/2015/04/10-years-of-git-an-interview-with-git-creator-linus-torvalds/). Sin embargo, la interfaz de usuario [no fue diseñada teniendo en cuenta a los nuevos usuarios](https://xkcd.com/1597/), por lo que puede ser difícil de aprender.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/git.png?raw=true" width="150px"/>
</p>

<p align="center"><i>Guía inmejorable para usar Git. (Fuente: XKCD)</i></p>

  


### Creando un nuevo repositorio <a name="Create_new"></a>

En su perfil de GitHub, haga clic en 'Crear nuevo repositorio'. El primer paso es crear un nombre como la marca para su proyecto. Idealmente, debería ser memorable y dar alguna indicación de lo que hace el proyecto.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/new_repo.png?raw=true" width="800" /></p>

<p align="center"><i>Crear un nuevo repositorio</i></p>

  


Asegúrese de no duplicar nombres, infringir otras marcas comerciales o nombrarlos como algo que pueda considerarse ofensivo.

  


## Los pasos fundacionales <a name="Foundation"></a>

Cualquier repositorio de GitHub requiere 4 elementos clave para comenzar y comenzar a desarrollar una comunidad acogedora:

1. Una licencia de código abierto;
2. Un archivo de `README`;
3. Guías de contribución; y
4. Un código de conducta.

Estos son aspectos críticos y mejores prácticas de cualquier proyecto para que los usuarios entiendan sus derechos legales, sus expectativas, el propósito del proyecto y para mejorar la experiencia general del usuario.

Los cuatro de estos archivos deben mantenerse en el directorio raíz de su repositorio de proyectos. Es una convención usar formatos de archivo de marca descendente (`.md`) para la mayoría de estos archivos (aunque el archivo de licencia es a menudo texto sin formato (`.txt`)), y poner en mayúscula todos los nombres de archivo. En lugar de espacios en los nombres de archivos, asegúrese de usar guiones bajos `_`.

Así que deberías terminar con una selección de archivos de base como esta:

1. `LICENCIA.md`
2. `README.md`
3. `CONTRIBUYENDO.md`
4. `CODE_OF_CONDUCT.md`

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/foundation.png?raw=true" width="800" /></p>

<p align="center"><i>La estructura básica del repositorio.</i></p>

  


### Elegir una licencia <a name="License"></a>

Elegir una licencia adecuada es lo que diferenciará su repositorio de código abierto del software disponible públicamente. Si bien no está obligado a elegir una licencia, hacerlo garantiza que otros podrán modificar, compartir, reutilizar y desarrollar su proyecto dentro de un marco legal.

Para empezar, desea verificar [Elija una licencia](https://choosealicense.com/) para encontrar la licencia que mejor se adapte a sus intenciones para el repositorio.

Los tres principales para elegir son:

* **Licencia**MIT: una licencia permisiva que le permite a las personas hacer lo que quieran con su código, siempre que le proporcionen las atribuciones adecuadas y no lo responsabilicen.
* **Apache License 2.0**: permisos similares a la licencia MIT, pero también proporciona una concesión expresa de derechos de patente de los contribuyentes a los usuarios.
* **GNU General Public License (GPL) v3**: una licencia [copyleft](https://en.wikipedia.org/wiki/Copyleft) que requiere que cualquiera que redistribuya su código, o un trabajo derivado, haga que la fuente esté disponible bajo los mismos términos que la licencia original; También proporciona una concesión expresa de los derechos de patente de los contribuyentes a los usuarios.

Afortunadamente, cuando inicia un nuevo repositorio en GitHub, se le ofrece la opción de seleccionar una licencia existente de un menú desplegable. Siempre debe (con muy pocas excepciones) usar una licencia existente, ya que esto es lo que verán los posibles usuarios y contribuyentes antes de que decidan usar o contribuir a su software.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/license.png?raw=true" width="800" /></p>

<p align="center"><i>Elegir una licencia de ejemplo</i></p>

  


Si no tienen la que desea, puede agregarla manualmente. Para hacer esto, simplemente haga clic en 'Crear nuevo archivo' en el repositorio, y copie y pegue un texto de licencia existente. Nombre el archivo como `LICENSE.txt` o `LICENSE.md` para que quede claro, y manténgalo en la carpeta principal del repositorio (es decir, la raíz). Asegúrate de agregar un mensaje de confirmación limpio, ¡y listo!

> **Helping hand**: este MOOC utiliza una combinación diferente de licencias para contenido de código y contenido sin código. Aquí puede encontrar un ejemplo de la licencia [MIT](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/LICENSE.md) que aplicamos para todo el código y el software generado como parte de la producción de MOOC.

  


### Creando un archivo README <a name="Readme"></a>

Cuando inicie su nuevo repositorio, debería haber una opción para hacerlo con un archivo `README`. Al igual que Alicia en el país de las maravillas, estos hacen exactamente lo que dicen: proporcionan información clave sobre el proyecto. Estos son, por lo general, lo primero que verán los colaboradores externos cuando lleguen a su repositorio, por lo que es clave que sean informativos y de bienvenida.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/readme.png?raw=true" width="800" /></p>

<p align="center"><i>Parte del archivo README para este módulo</i></p>

  


El archivo estará originalmente en formato markdown (`.md`). Este es un lenguaje de marcado ligero con un formato de texto plano. Para aprender algo de reducción básica, vea [esta hoja](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)trucos </a> . Pero por ahora, solo podemos usar texto plano.

Hay varias cosas que querrá incluir en su archivo `README`:

* ¿De qué se trata este proyecto y qué hace?
* ¿Por qué debería importarle a la gente y por qué es útil?
* ¿Cómo puede alguien comenzar a contribuir al proyecto?
* A quién se puede contactar en caso de que alguien necesite ayuda.
* Un enlace a la licencia, pautas de contribución y código de conducta.
* Una descripción de la estructura del proyecto.
* Quién está involucrado, y cuáles son sus roles.
* El estado actual del proyecto.

> **Pro-tip**: Más adelante, a medida que se desarrolle su proyecto, es posible que desee agregar preguntas frecuentes basadas en los comentarios de la comunidad o un tutorial para ayudar a los usuarios a comprender cómo funciona su proyecto.

Recuerde que no todos los que vengan a su proyecto serán expertos, ni comprenderán qué es lo que están haciendo y por qué. Tener un archivo `README` bien documentado mejorará la experiencia del usuario para las personas con un rango de conocimientos previos.

Cuando el archivo `README` se incluye en el directorio raíz, GitHub lo mostrará automáticamente en la página de inicio de su repositorio. Esto significa que es lo primero que las personas verán a menudo, ¡así que haz que cuente!

> **Helping hand**: Aquí puede encontrar el archivo `README` utilizado para este [módulo MOOC](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/README.md). Esto incluye información sobre el estado, la justificación, los resultados de aprendizaje, el equipo de desarrollo, los documentos clave y la licencia para ayudar. Puede copiar y adaptar esta estructura para sus propios proyectos según sea necesario.

  


### Creación de lineamientos contribuyentes. <a name="Contributing"></a>

Las pautas de contribución están diseñadas para comunicar a los contribuyentes potenciales una breve guía sobre cómo interactuar con su proyecto y su comunidad. Desea asegurarse de ser acogedor e indicar que desea que los participantes se comprometan con su proyecto. Cada vez que un participante abre una nueva solicitud de extracción o crea un nuevo problema, verá un enlace a su archivo de contribución.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/contributing.png?raw=true" width="800" /></p>

<p align="center"><i>Parte de las pautas de 'CONTRIBUYENDO' para este módulo</i></p>

  


Siguiendo con los nombres de todos los archivos de mayúsculas, el siguiente paso es crear un archivo `CONTRIBUYENDO`. Haga clic en 'Crear nuevo archivo' y asegúrese de guardarlo en formato de reducción como antes. Este archivo le dirá a otros usuarios cómo pueden participar y participar en su proyecto. Este es el primer paso hacia el establecimiento de una comunidad alrededor de su proyecto, por lo que debe ser atractivo, conciso e informativo.

El archivo `CONTRIBUYENDO` debe incluir información sobre:

* ¿Qué tipo de contribuciones estás buscando?
* Como sugerir actualizaciones o nuevas funcionalidades.
* Cómo interactuar con el proyecto utilizando las funciones de GitHub (por ejemplo, el protocolo de solicitud de extracción).
* Cómo presentar un informe de error o crear un problema.
* El objetivo final, la visión o la hoja de ruta para el proyecto.
* Cómo contactar con los responsables del proyecto.
* Enlaces a cualquier documentación externa o sitios web.

> **Pro-tip**: Considere comenzar con una breve nota de agradecimiento para las personas que se toman el tiempo de considerar contribuir. ¡Han hecho clic en el archivo para obtener más información después de todo! Si tiene en mente otros métodos de reconocimiento, asegúrese de incluirlos aquí también.

Aquí, esencialmente estás tratando de alentar a las personas a que ofrezcan su tiempo como voluntarios para avanzar en tu proyecto. Asegúrese de ser acogedor y amigable, y sea preciso sobre cómo las personas pueden participar. Al escribir esto, asegúrese de pensarlo desde la perspectiva del usuario: ¿cómo puede hacer su vida más fácil al enviar solicitudes de extracción y abrir problemas para que todo el proyecto funcione sin problemas?

> **Helping hand**: Las [pautas de Contribución](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CONTRIBUTING.md) para este módulo MOOC incluyen algunas cosas muy específicas: una introducción al uso de Git y GitHub, consejos para comenzar, información de contacto, cómo modificar el contenido y los problemas de reporte, un enlace a los `Archivo README` , e información sobre los estilos de código y contenido preferidos. Siéntase libre de copiar y adaptar esto para su propio proyecto según sea necesario.

  


### Creando un Código de Conducta <a name="Conduct"></a>

Un código de conducta es importante para establecer las reglas básicas para el comportamiento esperado y la participación de los contribuyentes del proyecto, y es un documento de fácil referencia para mostrar que su equipo de proyecto toma en serio los diálogos constructivos. Por lo tanto, es un elemento crítico para crear y mantener una comunidad saludable que se involucre de manera constructiva y productiva dentro de una atmósfera social positiva.

Un código de conducta no solo proporciona expectativas de comportamiento, sino que también describe a quién se aplican esas expectativas, cuándo se aplican, qué hacer en caso de que se produzca una violación del código y cuáles serán los elementos de acción para esto. Como tales, los puntos de contacto deben quedar claros en el código de conducta. Por lo general, esto debe hacerse de manera privada, como una dirección de correo electrónico.

> **Pro-tip**: En caso de que se deba informar una violación sobre la persona que recibe esos informes, asegúrese de incluir una opción para comunicarse con una parte secundaria.

Para agregar un código de conducta, puede crear su propio desde cero agregando un nuevo archivo de rebajas, o usar plantillas existentes, como el [Pacto](https://contributor-covenant.org/)Colaborador. Nombre su archivo `CODE_OF_CONDUCT.md`, y asegúrese de que esté visible en el archivo `README`.

> **Helping hand**: Este MOOC también tiene un [Código de conducta](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CODE_OF_CONDUCT.md) basado en el Pacto de contribuyentes. Como puede ver, incluye información sobre los estándares de comportamiento esperados, las responsabilidades de los miembros de la comunidad y el cumplimiento del CoC, incluidos los detalles de contacto. Siéntase libre de nuevo para reutilizarlo y adaptarlo a su proyecto como mejor le parezca.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/code_of_conduct.png?raw=true" width="800" /></p>

<p align="center"><i>Parte del archivo de CÓDIGO DE CONDUCTA para este módulo, basado en el Pacto de contribuidor</i></p>

  


Asegurarse de hacer cumplir el código de conducta es importante, ya que muestra que no solo valora el código, sino que respeta la influencia que tiene en su comunidad. Es importante tratar a cada miembro de la comunidad con el respeto, la cortesía y la importancia que merecen. En caso de producirse una violación o un reincidente hace violaciónes consistentes, lo mejor para referirse a la es [Guía Open Source](https://opensource.guide/code-of-conduct/#enforcing-your-code-of-conduct) para ver cómo hacer cumplir el código de conducta.

  


### Haciendo citable tu código <a name="Citation"></a>

Si desea que su código sea citable desde el principio, debe almacenar los metadatos necesarios para una cita desde el inicio, creando un archivo `[codemeta.json](https://codemeta.github.io)` o un archivo `[CITATION.cff](https: //citation-file-format.github.io)` archivos. Ambos permitirán que las herramientas que se están desarrollando actualmente creen automáticamente información de citas, en lugar de pedirle que la escriba en un formulario más adelante.

Si está interesado, [cite.research-software.org](https://cite.research-software.org) proporciona más información de fondo sobre citas de software en la academia.

  


## Manteniendo sus problemas al día. <a name="Issues"></a>

Los problemas no son necesariamente problemas con un proyecto, sino también sugerencias de mejora, cosas que se desarrollarán en el futuro y comentarios y comentarios sobre el proyecto que se debe realizar. Pueden compartirse abiertamente y discutirse con los colaboradores según sea necesario, como un foro.

Si usted es un líder de proyecto, es importante mantener una lista de problemas que deje en claro a los contribuyentes qué aspectos del proyecto necesitan atención. También es importante comprometerse con tantos temas como sea posible de otros de una manera positiva, para demostrar que toma en serio sus contribuciones.

Los elementos clave para los problemas incluyen:

* Un título informativo y descripción;
* Etiquetas / etiquetas codificadas por colores para ayudar a clasificar y filtrar;
* Hitos para asociar problemas con características específicas o fases del proyecto;
* Los asignados indican quién es responsable de trabajar en un problema;
* Comentarios para proporcionar comentarios.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/issues.png?raw=true" width="800" /></p>

<p align="center"><i>El rastreador de problemas para el proyecto Open Scholarship Strategy.</i></p>

  


Dentro de los problemas, es posible usar @ menciones para notificar a otros colaboradores sobre el tema y para que las personas adecuadas se involucren de manera efectiva. GitHub tiene un sistema interno de notificaciones, como Facebook o Twitter, y también puede enviar correos electrónicos a las personas que se mencionan en el rastreador de problemas. Todo esto se puede personalizar para individuos dentro de la configuración del usuario.

  


## Lista de verificación para lanzar tu proyecto <a name="Checklist"></a>

¡Ahora está listo para lanzar su proyecto, comenzar a publicarlo y obtener contribuciones! Antes de continuar, asegúrese de tener:

* [] El proyecto tiene un nombre memorable e informativo
* [] El proyecto tiene un `LICENCIA` archivo que es una copia exacta de una licencia de código abierto
* [] Documentación completa que incluye archivos de `README`, `CONTRIBUYENDO`y `CODE_OF_CONDUCT`
* [] El proyecto tiene al menos un tema claramente etiquetado
* [] Cualquier código incluido en esta etapa está claramente estructurado y anotado

**¡FELICIDADES!**

¡Ya has lanzado un proyecto de investigación Open Source! Con suerte, de aquí en adelante, su trabajo actuará para beneficiar a la comunidad en general, forjar nuevas colaboraciones y crear nuevas y fantásticas oportunidades para todos ustedes. Pruebe y piense en las formas en que estas habilidades se pueden aplicar a proyectos futuros, y cómo podrían haber ayudado en el pasado.

De ahora en adelante, todo depende de ti! Algunos consejos son:

* Escribir código limpio;
* Tener un proyecto bien estructurado;
* Hacer confirmaciones frecuentes con mensajes limpios;
* Mantener los proyectos bien documentados;
* Tener directrices claras de contribución;
* Hacer uso de las funciones de descripción y etiqueta;
* No bifurques el repositorio de otra persona a menos que quieras trabajar en él;
* Asegúrate de contribuir también a los proyectos de otras personas.

**¿Sabes de qué manera se puede mejorar este contenido?**

¡Es hora de tomar tus nuevas habilidades GitHub para una prueba de ejecución! Todo el desarrollo de contenido ocurre principalmente [aquí](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md). Si tiene una mejora sugerida en el contenido, el diseño o cualquier otra cosa, puede hacerlo y luego se convertirá automáticamente en parte del contenido de MOOC después de la verificación de un moderador.

[![Dedicación de dominio público CC0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)