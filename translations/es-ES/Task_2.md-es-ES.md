---
output:
  html_document: defecto
  pdf_document: defecto
---

# Tarea 2: Cómo hacer que su código sea citable con GitHub y Zenodo

Esta tarea está diseñada para estudiantes e investigadores que desean crear y reutilizar proyectos / repositorios basados en GitHub en la literatura académica.

No se olvide que usted puede participar en las discusiones sobre nuestra abierta [**canal Slack**](https://osmooc.herokuapp.com/). ¡Por favor, preséntese en # module5opensource, y cuéntenos un poco sobre quién es usted, su historial y cómo terminó aquí!

Tiempo estimado para completar: 45-60 minutos.

## Tabla de contenido

- [Prefacio](#Foreword)
- [Configurar un repositorio GitHub](#Setup)
- [Elige tu repositorio GitHub](#Choose)
- [Inicia sesión en Zenodo](#Login)
- [Autoriza a GitHub a conectarse con Zenodo](#Authorise)
- [Seleccione el repositorio para archivar](#Archive)
- [Comprobar la configuración del repositorio](#Check)
- [Crear un nuevo lanzamiento](#Release)
- [Obteniendo un DOI](#DOI)
- [Lista de verificación para citar su proyecto](#Checklist)
- [Recursos adicionales](#Resources)

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/Task2.png?raw=true" alt="Flujo de trabajo de la tarea 2" width="600" height="861" style="margin-right: 30px; margin-left: 10px;" onmouseover="this.width='1200'; this.height='1722'" onmouseout="this.width='600'; this.height='861'">
</p>

<p align="center"><i>El flujo de trabajo para la tarea 2. ¡Mantenga esto a mano mientras trabaja en la tarea!</i></p>

  


## Prefacio <a name="Foreword"></a>

Si bien la integración de GitHub y Zenodo hace que sea realmente más fácil trabajar con estas herramientas hoy en día (enero de 2019), es importante destacar que existen alternativas a GitHub (Gitlab, Bitbucket, ...) y alternativas a Zenodo (otros repositorios podrían ser más adecuado para su comunidad, puede preguntar a sus colegas). Por ejemplo, uno puede trabajar con Gitlab y cargar manualmente cada versión nueva a su repositorio universitario, obteniendo un DOI. Los principios (trabajar con un sistema de control de versiones en línea y archivar las versiones principales en un repositorio que proporciona un identificador único persistente) se pueden aplicar en diferentes flujos de trabajo.

## Configurar un repositorio GitHub <a name="Setup"></a>

> **Pro-tip**: Asegúrese de incluir un archivo de LICENCIA y README en su repositorio. Esto indicará a las personas el propósito del proyecto y cómo pueden comprometerse con él en el futuro.

Averigüe cómo configurar un repositorio de GitHub en esta otra guía [Tarea 1: Crear un repositorio de GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) que también forma parte del 'Módulo 5: Software de investigación abierto y código abierto'.

## Elige tu repositorio GitHub <a name="Choose"></a>

Una vez en su página de listados de proyectos de GitHub en [github.com](https://github.com) diríjase a la pestaña 'Repositorios'. Seleccione el repositorio que desea archivar y ábralo.

  


## Inicia sesión en Zenodo <a name="Login"></a>

Ahora dirígete a [zenodo.org](https://zenodo.org). Zenodo es una plataforma donde puede archivar permanentemente su código y otros elementos del proyecto. Zenodo hace esto asignando a los proyectos un **Digital Object Identifier** (DOI), que también ayuda a que el trabajo sea más citable. Esto es diferente a GitHub, que actúa como un lugar donde se realiza el trabajo real en un proyecto, en lugar de su archivo a largo plazo. En GitHub, el contenido puede modificarse, eliminarse, reescribirse y cambiarse de manera irreversible, lo que hace que sea un poco preocupante su uso para fines de referencia más duraderos. Zenodo ofrece más seguridad y permanencia para los resultados de la investigación.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/zenodo.png?raw=true" width="800" /></p>

<p align="center"><i>Regístrate en Zenodo</i></p>

  


Si ya tienes una cuenta Zenodo, esto es fácil. De lo contrario, siga los pasos para crear uno: incluso puede iniciar sesión con su cuenta de GitHub o con el perfil ORCID para simplificar las cosas, ya que Zenodo tiene una integración integrada para ello. Esto podría ser más fácil que crear otra cuenta y perfil de investigación.

  


## Autoriza a GitHub a conectarse con Zenodo <a name="Authorise"></a>

En el sitio web de Zenodo, autorícelo para que se conecte a su cuenta de GitHub en la sección '[Usar GitHub](https://zenodo.org/account/settings/github/)'. Aquí, Zenodo lo redireccionará a GitHub para solicitar permisos para usar '[webhooks](https://developer.github.com/webhooks/)' en sus repositorios. Desea autorizar a Zenodo aquí con los permisos que necesita para formar esos enlaces.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/zenodo_github.png?raw=true" width="800" /></p>

<p align="center"><i>Autoriza a Zenodo a conectarse con GitHub</i></p>

  


Si está tratando de dar acceso a Zenodo a un repositorio organizativo, usted (o un administrador) deberá asegurarse de que Zenodo tenga permisos de acceso de terceros. GitHub enviará un correo electrónico de autorización que necesita confirmación. En este punto, de nuevo en la configuración de su repositorio en GitHub, también debe asegurarse de que el repositorio esté configurado como 'público', no privado.

  


## Seleccione el repositorio para archivar <a name="Archive"></a>

Si ha llegado hasta aquí, esto significa que Zenodo ahora está autorizado para configurar los webhooks del repositorio que necesita para archivar el repositorio y emitir un DOI. Para hacer esto, en el sitio web de Zenodo navegue a la página</a> lista de repositorios de GitHub y simplemente haga clic en el botón 'on' al lado de su repositorio.</p>

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/enabled_repos.png?raw=true" width="800" /></p>

<p align="center"><i>Habilitar los repositorios individuales de GitHub para ser preservados en Zenodo</i></p>

  


## Comprobar la configuración del repositorio <a name="Check"></a>

Ahora ha configurado un nuevo webhook entre Zenodo y su repositorio. En GitHub, haga clic en la configuración de su repositorio y en la pestaña de Webhooks en el menú del lado izquierdo. Esto debería mostrar el nuevo webhook de Zenodo configurado para Zenodo. Tenga en cuenta que la lista de webhook puede tardar un poco en aparecer.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/webhooks.png?raw=true" width="800" /></p>

<p align="center"><i>Compruebe que los webhooks están habilitados para su repositorio de GitHub. Ejemplo aquí usando la estrategia de becas abiertas</i></p>

  


## Crear un nuevo lanzamiento <a name="Release"></a>

La primera vez que archiva un repositorio se conoce como la "primera versión". Cada vez que crea una nueva versión de ese repositorio y la archiva, crea una nueva versión. Esto se puede rastrear en la pestaña 'lanzamientos' de su repositorio en GitHub (centro superior).

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/first_release.png?raw=true" width="800" /></p>

<p align="center"><i>Compruebe que el primer lanzamiento del repositorio fue exitoso. Ejemplo aquí usando la estrategia de becas abiertas</i></p>

  


Para la primera versión archivada de su repositorio, haga clic en 'Crear un nuevo lanzamiento' en Zenodo. Rellene el formulario y proporcione algunos detalles sobre lo que implica el lanzamiento. Para la primera versión, asegúrese de llamarlo v1.0.0, como es la práctica estándar.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/create_release.png?raw=true" width="800" /></p>

<p align="center"><i>Crear una nueva versión. Ejemplo aquí utilizando la Estrategia de becas abiertas, para la cual ya existe una primera versión</i></p>

  


Finalmente, haga clic en 'publicar versión', y su archivo se publicará y versionará en GitHub.

Para ver su lanzamiento en Zenodo, debe visitar la pestaña [Subir](https://zenodo.org/deposit). Para finalizar el archivo, se necesitan algunos detalles más en Zenodo.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/upload_release.png?raw=true" width="800" /></p>

<p align="center"><i>Compruebe que el nuevo lanzamiento ha sido subido. Ejemplo aquí mostrado usando la estrategia de becas abiertas</i></p>

  


## Obteniendo un DOI <a name="DOI"></a>

Esto a veces se conoce como 'acuñación' del DOI y requiere un par de bits adicionales de información sobre el repositorio en Zenodo. En Zenodo, haga clic en la pestaña [Cargar](https://zenodo.org/deposit) en el menú principal, y su repositorio recién cargado debería estar allí. Desplácese por la página y complete la información adicional según sea necesario, los campos obligatorios están marcados con un asterisco rojo y luego haga clic en "Publicar".

**Nota**: Solo después de que se haya agregado esta información adicional, su DOI se activará. También puede tomar poco tiempo para que el DOI se active. Ejemplo de DOI que se muestra a continuación (para la Estrategia de becas abiertas nuevamente).

> **Pro-tip**: copie la URL del DOI en el archivo README de su repositorio de GitHub para facilitar aún más los enlaces cruzados, así como para presentar una credencial DOI claramente resaltada para que los usuarios puedan ver y hacer uso de su DOI. Solo necesita hacer esto una vez con su primer DOI de lanzamiento, ya que actúa como un 'concepto DOI' y está vinculado a todos los DOI de lanzamiento subsiguientes.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1323437.svg)](https://doi.org/10.5281/zenodo.1323437)

La integración GitHub / Zenodo ahora asignará un DOI a cada versión / lanzamiento de un repositorio de proyectos. Esto permite a los usuarios consultar y citar versiones específicas de proyectos. Además, la lista de autores para la cita está determinada automáticamente por los nombres de las cuentas de usuario de GitHub utilizados por el repositorio, lo que significa que nadie queda excluido. Los detalles del autor se pueden editar más adelante en Zenodo. Los DOI utilizados en Zenodo se registran a través del servicio [DataCite](https://www.datacite.org/).

> **Pro-tip**: cree una versión 'legible por humanos' de esta cita en el archivo README de su proyecto. Esto será útil para los investigadores que no estén familiarizados con el uso de DOI para crear citas, y facilitará que otros citen su software y reconozcan su trabajo. Un ejemplo de esto podría ser: Jon Tennant. (2018, 30 de julio). Fundamentos para el desarrollo de estrategias de becas abiertas: primer lanzamiento formal (versión 1.2). Zenodo. <http://doi.org/10.5281/zenodo.1323437>

**¡¡FELICIDADES!!**

Su repositorio GitHub ahora está archivado en Zenodo, y con un DOI que puede ser versionado para reflejar las actualizaciones de la versión del repositorio a través del tiempo. Debería poder ver los detalles de esto en la página de GitHub Zenodo para su repositorio. Esto también significa que sus proyectos archivados pueden ser recogidos por otros servicios de indexación y motores de búsqueda que también usan DOI.

Es necesario proporcionar un archivo a largo plazo y un DOI para su trabajo para que otros puedan citarlo correctamente, ya que esto proporciona metadatos de citas básicas. Para Open Science, es importante poder citar el software que utiliza en su investigación, y este flujo de trabajo integrado permite que eso suceda, en línea con las mejores prácticas para la investigación de citas. Además, esta práctica es importante para elevar el estándar de software (y proyectos relacionados) al de la norma de otros resultados de investigación.

> **Pro-tip**: ¿Su investigación está financiada por una subvención de la UE? Ahora puede conectar directamente su proyecto archivado a su subvención actualizando la sección de subvención de los metadatos en el registro de Zenodo del proyecto. ¡Esto ayuda masivamente a aumentar su descubribilidad!

  


## Lista de verificación para citar su proyecto <a name="Checklist"></a>

¡Así que ahora tiene un repositorio de GitHub archivado de manera sostenible en Zenodo que está listo para ser reutilizado y citado! Antes de continuar, asegúrese de tener:

- [] Vinculó su proyecto GitHub a Zenodo. Si ve una copia completa de su repositorio GitHub en Zenodo, entonces las cosas están funcionando.
- [] La configuración integrada de Zenodo y GitHub funciona muy bien. Por ejemplo, haga que todos los nombres de los autores y el título correcto del proyecto lleguen a Zenodo. Si no, o si los autores solo tienen apodos, puede editar estos detalles en Zenodo.
- [] El proyecto tiene un primer lanzamiento, con un DOI. Debes tener un DOI en tu página de proyectos de Zenodo. Este primer DOI se denomina "concepto DOI" y es el DOI maestro que se vincula a todos los DOI de versiones posteriores. Copie este enlace DOI e insértelo en la página README de sus proyectos de GitHub. Has terminado

### Recursos adicionales <a name="Resources"></a>

[Haciendo que su código sea citable](https://guides.github.com/activities/citable-code/) - Guías GitHub.

**¿Sabes de qué manera se puede mejorar este contenido?**

¡Es hora de tomar tus nuevas habilidades GitHub para una prueba de ejecución! Todo el desarrollo de contenido ocurre principalmente [aquí](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md). Si tiene una mejora sugerida en el contenido, el diseño o cualquier otra cosa, puede hacerlo y luego se convertirá automáticamente en parte del contenido de MOOC después de la verificación de un moderador.

[![Dedicación de dominio público CC0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)