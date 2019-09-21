---
output:
  html_document: defecto
  pdf_document: defecto
---

# Módulo 5: Open Research Software y Open Source

## Contenidos del módulo

- [Introducción](#Introduction)
- [Qué es el software de código abierto](#What_OSS)
- [Principios del software de código abierto](#Principles)
- [La comunidad de código abierto, la gobernanza y las contribuciones.](#OS_Community)
- [Plataformas y herramientas existentes para software de código abierto](#Platforms)
- [Software de código abierto utilizado en la investigación.](#Research)
- [Comenzando con OSS - Preguntas frecuentes](#FAQ)
- [Haciendo buen software para su reutilización.](#Reuse)
- [Licencia de código abierto](#Licensing)
- [Citación de software](#Citation)
- [Usando GitHub y Zenodo](#GitHub_Zenodo)
- [Colaborando a través de Open Source](#Collaborating)
- [A dónde ir desde aquí](#Future_OSS)

**NOTA** una versión en audio de esto está disponible para descargar a través de [Soundcloud](https://soundcloud.com/open-science-mooc/module-5-open-source-and-open-research-software) y [de YouTube](https://www.youtube.com/watch?v=BHrOEmKk5zM).

## Introducción <a name="Introduction"></a>

Bienvenido al **Módulo 5** de Open Science MOOC: **Open Research Software y Open Source**.

Este módulo se ha desarrollado mediante la "Open" colaboración de un equipo internacional "Open Source" [aficionados](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/README.md#development-team-). Todo lo que ve aquí se ha desarrollado a través de "open" comentarios interactivos y la colaboración de la comunidad en general. Comprende una serie de videos, infografías, lectura basada en texto y tareas prácticas a las que puedes hincar el diente.

No te olvides que puedes participar en las discusiones en nuestro [**canal Slack**](https://osmooc.herokuapp.com/). ¡Por favor, preséntate en # module5opensource, y cuéntanos un poco sobre quién eres, tu trayectoria académica y cómo terminastes aquí!

### ¿Para quién es este módulo?

Este módulo está diseñado principalmente para investigadores computacionales a nivel de licenciatura y posgrado, así como para científicos iniciándose en datos y cualquier otro investigador que utilice un código o software analítico. En un entorno de investigación de hoy en día, esto cubre casi completamente a cualquiera que use una computadora para su trabajo.

> "Un artículo sobre el resultado computacional es publicidad, no beca. La beca actual es el entorno de software completo, el código y los datos que produjeron el resultado ". - J. Buckheit y DL Donoho, 1995.

El software y la tecnología sustentan gran parte de la investigación moderna, que ahora es casi inevitablemente computacional de una u otra forma: motores de búsqueda, plataformas de redes sociales, software analítico y publicación digital. Con esto, existe una demanda cada vez mayor de software de código abierto más sofisticado, combinado con una creciente disposición de los investigadores a colaborar abiertamente en nuevas herramientas.

El poder de Open Source radica en que reduce las barreras para la colaboración y la adopción, lo que permite que las ideas y la tecnología se propaguen más rápidamente. Este módulo presentará las herramientas necesarias para transformar el software en algo que otros puedan acceder y reutilizar abiertamente.

<img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/open_research_software_open_source.png?raw=true" width="800" />

<p align="center"><i>Imagen de Patrick Hochstenbach (CC0 1.0 Universal)</i></p>

  


### **Objetivos específicos de aprendizaje para este Módulo**:

1. Aprende las características del software abierto; entender los **argumentos de impacto éticas, legales, económicos y de investigación favor y en contra del software Open Source**, y para entender mejor los requisitos de calidad de código abierto.

2. Ser capaz de convertir el código hecho para uso personal en un código abierto al que otros puedan acceder.

3. Use software (herramientas) que utiliza contenido abierto y fomenta una colaboración más amplia.

  


## ¿Qué es el software de código abierto? <a name="What_OSS"></a>

Prácticamente todos los flujos de trabajo de investigación científica moderna se basan en una gama de herramientas de software, ya sea que operan en diferentes conjuntos de datos, con diferentes parámetros, y se aplican de manera iterativa de varias maneras (ciencia de datos) o que operan en diferentes entradas y utilizan modelos y métodos para predecir algún estado de salida ( Ciencia computacional). El software de código abierto (OSS) es un software de computadora en el que el código fuente completo está disponible bajo una licencia específica que permite a otros usuarios acceder, ver, modificar y redistribuir ese código para cualquier propósito. Debido a que OSS requiere una licencia de este tipo, por lo general se mantiene de forma gratuita de forma predeterminada. Esta licencia explícita es también lo que diferencia a OSS del software libre. Reutilizar OSS para análisis, simulación y visualización para investigación también suele ser más fácil y más flexible en comparación con el software propietario. A menudo, ya sea que lo sepamos o no, ya estamos usando OSS como parte de nuestros propios flujos de trabajo de investigación.

OSS encaja en el esquema más amplio de Open Science, ya que ayuda a hacer que el entorno de investigación completo, incluido el software que produjo los resultados de la investigación, sea totalmente accesible y reutilizable. Como tal, constituye un componente necesario para las mejores prácticas ([Jiménez et al., 2018](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Jim%C3%A9nez%20et%20al.%2C%202018.pdf)) y la repetibilidad y reproducibilidad de la investigación (tanto personalmente como por otros), junto con otros componentes, como el intercambio de datos ([Stodden, 2010](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Stodden%2C%202010.pdf)).

En algunos casos, el intercambio de código fuente puede incluso ser condicional para la aceptación de manuscritos de investigación asociados ([Shamir et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Shamir%20et%20al.%2C%202013.pdf)). También se percibe generalmente que aumenta el impacto de la investigación ([Vandwalle, 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Vandewalle%2C%202012.pdf)).

Algunas de las ventajas comunes para los desarrolladores incluyen:

- Mayor lealtad y empoderamiento del desarrollador;

- Menores costos de servicios y marketing;

- Incremento en la marca de servicios y productos;

- Producción de software de alta calidad a un menor costo;

- Flexibilidad e innovación rápida;

- Personalización e integración modular;

- Mayor confiabilidad e independencia; y

- Basado en estándares abiertos disponibles para todos.

Como tal, las principales ventajas para los investigadores (usuarios) incluyen **costos más bajos**, **transparencia incrementada**, **mayor seguridad y estabilidad**, **no hay 'dependencia' del proveedor con mayor control del usuario**y **general mayor calidad**. Además, compartir OSS permite a los investigadores recibir crédito por sus esfuerzos, por ejemplo a través de la cita de software directa [(Smith et al., 2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf).

El OSS de uso común incluye el navegador</a> Internet Mozilla Firefox </a> y la suite de oficina completa [LibreOffice](https://www.libreoffice.org/). LibreOffice es similar al popular Microsoft Office, que incluye un procesador de textos, administrador de hojas de cálculo y software de presentación de diapositivas, pero es completamente gratuito y de código abierto.</p> 

Algunos consideran que el movimiento OSS representa un movimiento contrario al neoliberalismo y la privatización, a través del desafío a las regulaciones y normas en la construcción y reutilización de la información, y una transformación potencial del capitalismo moderno al hacer que el software esté disponible abundantemente con el mínimo esfuerzo. Ver [El movimiento de software de fuente abierta / libre: ¿Resistencia o cambio?](http://www.redalyc.org/html/742/74212712006/) por Panayiota Georgopoulou para más información sobre este tema.

  


## Principios del software de código abierto <a name="Principles"></a>

El [Open Source Initiative](https://opensource.org/), uno de los pioneros de la OSS, ofrece las siguientes [definición](https://en.wikipedia.org/wiki/The_Open_Source_Definition#Definition):

*No se preocupe, no necesita memorizar todo esto, pero es bueno saber los principios de los que proviene OSS.*

- **Redistribución gratuita**: La licencia no debe restringir a ninguna parte la venta o la entrega del software como un componente de una distribución de software agregada que contiene programas de varias fuentes diferentes. La licencia no requerirá una regalía u otra tarifa por dicha venta.
    
    - **Código fuente**: el programa debe incluir el código fuente y debe permitir la distribución en el código fuente y en el formato compilado. Cuando alguna forma de un producto no se distribuye con el código fuente, debe haber un medio bien publicitado para obtener el código fuente por un costo de reproducción no superior a lo preferible, descargándolo a través de Internet sin cargo. El código fuente debe ser la forma preferida en la que un programador modificaría el programa. El código fuente deliberadamente ofuscado no está permitido. No se permiten formularios intermedios, como la salida de un preprocesador o traductor.
    
    - **Trabajos derivados**: La licencia debe permitir modificaciones y trabajos derivados, y debe permitir que se distribuyan bajo los mismos términos que la licencia del software original.
    
    - **Integridad del código fuente del autor**: la licencia puede restringir la distribución del código fuente en forma modificada solo si la licencia permite la distribución de "archivos de parches" con el código fuente con el fin de modificar el programa en el momento de la compilación. La licencia debe permitir explícitamente la distribución de software creado a partir del código fuente modificado. La licencia puede requerir trabajos derivados para llevar un nombre o número de versión diferente del software original.
    
    - **No discriminación contra personas o grupos**: La licencia no debe discriminar a ninguna persona o grupo de personas.
    
    - **No discriminación contra Fields of Endeavour**: La licencia no debe restringir a nadie para hacer uso del programa en un campo específico de esfuerzo. Por ejemplo, es posible que no impida que el programa se utilice en una empresa o que se utilice para investigación genética.
    
    - **Distribución de la licencia**: Los derechos adjuntos al programa deben aplicarse a todos aquellos a quienes se redistribuye el programa sin la necesidad de que las partes ejecuten una licencia adicional.
    
    - **licencia no debe ser específica para un producto**: Los derechos adjuntos al programa no deben depender de que el programa sea parte de una distribución de software en particular. Si el programa se extrae de esa distribución y se utiliza o distribuye dentro de los términos de la licencia del programa, todas las partes a quienes se redistribuye el programa deben tener los mismos derechos que los otorgados en conjunto con la distribución de software original.
    
    - **licencia no debe restringir otro software**: la licencia no debe imponer restricciones a otro software que se distribuye junto con el software con licencia. Por ejemplo, la licencia no debe insistir en que todos los demás programas distribuidos en el mismo medio deben ser software de código abierto.
    
    - **licencia debe ser tecnológica-Neutral**: ninguna disposición de la licencia puede basarse en ninguna tecnología individual o estilo de interfaz.

Ahora, todo esto puede ser un poco complejo para recordar. Sin embargo, se puede resumir en *hace que el software sea tan reutilizable como sea posible para futuros trabajos, mientras que también está disponible de forma gratuita*.

  


## Una lista de verificación de código abierto

Hay una serie de plataformas y herramientas existentes que admiten OSS y colaboración. El [Ciencia Abierta Manual de Entrenamiento](https://open-science-training-handbook.gitbook.io/book/) proporciona una lista de control que se utilizará para la evaluación de la 'apertura' de software de investigación existente, basado en la definición de código abierto más arriba:

- [] ¿El software está disponible para descargar e instalar?

- [] ¿Se puede instalar fácilmente el software en diferentes plataformas?

- [] ¿El software tiene condiciones de uso?

- [] ¿El código fuente está disponible para inspección?

- [] ¿El historial completo del código fuente está disponible para inspección a través de un historial de versiones públicamente disponible?

- [] ¿Se describen correctamente las dependencias del software (hardware y software)? ¿Estas dependencias requieren solo una cantidad de esfuerzo razonablemente mínima para obtener y usar?

Cheque, cheque, cheque, hecho! Simples.

  


## La comunidad Open Source y su gobierno. <a name="OS_Community"></a>

Hay dos campos principales dentro de la comunidad de software libre: el **movimiento de software libre**y el movimiento **OSS**. Ambos tienen diferentes ideologías basadas en las libertades de los usuarios y las aplicaciones prácticas del software. A menudo, el término 'FLOSS' se usa para reconciliar estos dos campos políticos, y significa 'Software libre / libre y de código abierto'; Libre de ser francés y español para 'gratis' en el contexto de la libertad.

El principio básico de la reutilización es lo que separa a OSS del 'Software libre'. El software libre y de código abierto (FOSS, por sus siglas en inglés) es un término inclusivo para describir un software que puede clasificarse como libre y de código abierto. Un buen ejemplo de FOSS es el sistema operativo [Ubuntu Linux](https://www.ubuntu.com/).

La gran diferencia entre el software libre y el OSS es que el primero debe distribuir versiones actualizadas con la misma licencia que el original, mientras que las versiones más recientes de OSS se pueden distribuir con diferentes licencias. FOSS combina lo mejor de ambos mundos.

Estas definiciones ahora se han adoptado ampliamente, tanto por los gobiernos internacionales como por algunas organizaciones grandes como [Mozilla Foundation](https://www.mozilla.org/en-US/foundation/) y [Wikimedia Foundation](https://wikimediafoundation.org/wiki/Home). Las principales organizaciones de software libre en el espacio incluyen el Reino Unido [Software Sostenibilidad Instituto](https://www.software.ac.uk/), que producen recursos valiosos, tales como su reciente [Software fuerte orientación para investigadores](https://softwaresaved.github.io/software-deposit-guidance/).

### Para proyectos individuales

Un proyecto típico de código abierto tiene los siguientes tipos de roles formales:

- **Autor**: Es la persona que creó el proyecto.
- **Propietario**: la persona o personas que tienen propiedad administrativa sobre la organización o el repositorio 
- **Mantenedores**: Colaboradores que son responsables de dirigir la visión y gestionar los aspectos organizativos del proyecto. (También pueden ser autores o dueños del proyecto.)
- **Colaboradores**: El usuario que ya ha contribuido al proyecto.
- **Miembros de la comunidad**: Personas que usan el proyecto. Pueden participar activamente en las conversaciones, crear nuevos problemas o expresar su opinión sobre las futuras mejoras del proyecto.

Normalmente, los roles se hacen públicos a través del archivo `README` , un archivo de contribuyentes o una página de equipo separada para el proyecto.

  


## Plataformas y herramientas existentes para software de código abierto <a name="Platforms"></a>

Las máquinas y los entornos virtuales se están volviendo cada vez más populares como habilitadores de flujo de trabajo de investigación de gran potencia, y muchos de ellos se basan en OSS (por ejemplo, sistemas operativos, lenguajes de programación y marcos de procesamiento de datos). Los servicios más populares incluyen [Google Cloud](https://cloud.google.com/compute/) y [Amazon Web Services](https://aws.amazon.com/), que también ayudan con el almacenamiento de la base de datos y la entrega de contenido, así como la potencia computacional. [InsideDNA](https://insidedna.me/) es una plataforma informática para la investigación reproducible en bioinformática, genómica y ciencias de la vida.

Como se mencionó [arriba de](#What_OSS), LibreOffice proporciona una alternativa de código abierto a Microsoft Office. Los dos son casi completamente compatibles, solo que con diferentes formatos de archivo predeterminados. Para los administradores de citas, [Zotero](https://www.zotero.org/) es la alternativa de código abierto más popular para plataformas propietarias como Mendeley o EndNote.

[Zotero](https://www.zotero.org/) usa el formato BibTeX (pronunciado 'bib-tech'), basado en LaTeX (pronunciado 'lay-tech'), y tiene complementos de navegador para simplificar la gestión de citas. Al integrar esto con otro software como LibreOffice, ahora es posible tener un flujo de trabajo de investigación de código abierto completo en muchos casos.

### GitHub <a name="GitHub"></a>

> ¿Sabía que este proyecto completo se construyó como un esfuerzo comunitario abierto y colaborativo en [GitHub](https://github.com/OpenScienceMOOC/)?

[GitHub](https://github.com/) es un sitio de hospedaje popular para software y contenido que no es software (a menudo llamado 'notebooks'), con capacidades adicionales para el control de versiones, gestión y seguimiento de proyectos y servicios de almacenamiento. GitHub se basa en el OSS [Git](https://git-scm.com/), que permite a los usuarios trabajar de forma remota para mantener, compartir y colaborar en software de investigación y otros proyectos no basados en software.

El control de versiones es esencialmente un proceso que toma instantáneas de los archivos en un repositorio y les hace un seguimiento de las modificaciones. Registra cuándo se hicieron los cambios, cuáles fueron y quién los hizo. Si varias personas están trabajando en un archivo a la vez, se detectan cambios superpuestos y deben resolverse antes de continuar. Esto proporciona un proceso mucho más simplificado y automatizado que guardar y registrar manualmente los cambios a medida que se desarrollan los proyectos. También evita las inevitables listas de confusas versiones de archivos nombrados ...

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/xkcd.png?raw=true" width="200" /></p>

<p align="center"><i>GitHub nos ayuda a evitar, er, convenciones de nombres de archivos por debajo del nivel óptimo (fuente: XKCD)</i></p>

  


Una de las funciones más populares y útiles del GitHub es el [de seguimiento de incidencias](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/issues), que se utiliza para organizar el desarrollo de software libre. ¡El enlace anterior lo lleva al rastreador de problemas para el desarrollo de este módulo! Si cree que hay algo aquí que puede mejorar, o si desea comentar, ¡cualquiera puede agregar o contribuir a un problema allí!

Otros servicios de alojamiento de proyectos similares incluyen [BitBucket](https://bitbucket.org/), [GitLab](https://about.gitlab.com/)y [Launchpad](https://launchpad.net/). Si la reciente adquisición de GitHub por parte de Microsoft es un poco desagradable para usted, estas son excelentes alternativas.

Sin embargo, también sabemos que GitHub puede tener una curva de aprendizaje bastante alta. ¡Es por eso que la primera tarea práctica de este MOOC le enseñará cómo configurar su primer repositorio de proyectos GitHub!

**[IR A LA TAREA 1: Construyendo tu primer repositorio de GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)**

  


## Software de código abierto utilizado en la investigación. <a name="Research"></a>

Especialmente en la investigación científica, el uso y desarrollo de software de código abierto se ha convertido prácticamente en la norma. Hay varias razones para esto más allá de aquellas que se aplican a la aceptación general de OSS por, por ejemplo, los consumidores, la industria o el gobierno. Entre estas razones están:

- Cada vez más, los algoritmos implementados en el software de análisis forman una parte integral de los métodos descritos en publicaciones académicas. Como tal, está completamente en desacuerdo con la rigurosa revisión por pares si estas implementaciones de algoritmos están cerradas a personas externas.

- La colaboración científica a menudo abarca múltiples instituciones y redes de investigación distribuidas donde el secreto y la jerarquía de comando no se mantienen de una manera que sea 'necesaria' para el desarrollo de código cerrado.

- Muchos análisis computacionales se ejecutan en entornos virtualizados (como infraestructuras institucionales, nacionales o internacionales de "nube") y se alojan en servidores multiusuario. El software comercial de código cerrado a menudo no permite tal uso.

- El desarrollo de OSS a menudo se basa en voluntarios. En una época de restricciones presupuestarias para la investigación científica, esta es una clara ventaja.

Por estas y otras razones, las herramientas de código abierto son muy utilizadas en la investigación científica. Esto incluye el uso en campos donde muchos investigadores son desarrolladores aficionados y confían en herramientas como [R](https://www.r-project.org/) para el análisis estadístico y la creación de scripts, que, en la última década, ha desplazado casi por completo el software comercial para el análisis estadístico, como SPSS o JMP en un muchos campos En campos como la bioinformática, que involucra una gran cantidad de manejo de archivos de las salidas de las plataformas de secuenciación de ADN, los lenguajes de programación de propósito general como [Python](https://www.python.org/) y las bibliotecas de uso común construidas sobre ella (como [biopython](http://biopython.org)) se han convertido en un elemento vital. Parte del conjunto de herramientas de muchos investigadores.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/python.png?raw=true" width="400" /></p>

<p align="center"><i>Pitón</i></p>

  


Herramientas como R y Python son esencialmente software para escribir software. Aunque la programación es una actividad cada vez más común entre los investigadores, por supuesto, no *cada* científico hace esto. Un paso lejos de la programación es el encadenamiento de las entradas y salidas de varias herramientas de análisis en flujos de trabajo más largos. Como ejemplo de la genómica, un flujo de trabajo muy común es comenzar con lecturas de secuenciación de alto rendimiento y luego i) hacer verificaciones básicas de control de calidad; ii) mapear las lecturas contra un genoma de referencia; iii) identificar los puntos donde los nuevos datos están en desacuerdo con la referencia. Estos pasos se ejecutan rutinariamente como un flujo de trabajo en el que se ejecuta un ejecutable de código abierto diferente en un entorno de línea de comandos de Linux para cada uno de los tres pasos. Si bien este no es un desarrollo de software de código abierto, sí implica el uso y la producción de artefactos de código abierto (como los scripts de shell de Linux) para los cuales se aplican los principios que analizamos en este módulo.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/r.png?raw=true" width="200" /></p>

<p align="center"><i>R</i></p>

  


Por último, la OSS también se utiliza en la investigación científica por razones que reflejan más de cerca las que impulsan la adopción de la OSS en la sociedad en general, a saber, que es barata. Por ejemplo, los individuos u organizaciones pueden decidir cambiar de Microsoft Office a LibreOffice para la escritura de manuscritos o el procesamiento de hojas de cálculo porque este último es gratis (tanto como en [**'cerveza gratis'**](https://www.youtube.com/watch?v=dQw4w9WgXcQ) y 'libertad de expresión'). Del mismo modo, la elección de cambiar de ArcGIS a [QGIS](https://www.qgis.org/en/site/) para el análisis de la información geográfica puede deberse simplemente a consideraciones de costo.   


## Comenzando con OSS - Preguntas frecuentes <a name="FAQ"></a>

**Estoy usando X [por ejemplo, Matlab, STATA, Excel] y quiero hacer la transición a algo más abierto. ¿Cuáles son los siguientes pasos?**

Incluso si está utilizando software propietario, generalmente puede compartir su código fuente / documentos, etc. *El mejor primer paso es compartir lo que puedas*.

**¡Genial! Puedo ponerlos en mi nuevo repositorio de github.**

Si eso es suficiente para ti por ahora genial! Si no fuera por la mayoría de las piezas de software propietario, hay equivalentes de código abierto. Prueba uno y ve lo que piensas.

| Cerrado                                                                                               | Abierto                                                                                                                                                            |
| ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Matlab                                                                                                | Python, Julia                                                                                                                                                      |
| STATA / SPSS                                                                                          | R                                                                                                                                                                  |
| MS Office                                                                                             | LibreOffice                                                                                                                                                        |
| Matemática                                                                                            | JupyterLab                                                                                                                                                         |
| Prueba tu nuevo [Pull Request -PR-](https://help.github.com/articles/about-pull-requests/) Skills ... | ... añadiendo su propio ejemplo [aquí](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md) |

**¡Guay! Pero si hago el cambio, me quedo atascado: me demoraré en aprender una nueva herramienta / sin soporte / con software defectuoso.**

¡Buena pregunta! La respuesta es, depende. Lo mejor que puedes hacer es encontrar a alguien que haya hecho el cambio antes y aprender de su experiencia. O simplemente hacer una búsqueda en Google! Algunos OSS son mucho mejores que sus contrapartes cerradas, otros no, por lo que vale la pena elegir cuidadosamente.

## Haciendo buen software para su reutilización. <a name="Reuse"></a>

La persona más probable que quiera reutilizar su software en el futuro es ... ¡usted! Entonces, mientras que compartir siempre es mejor que no compartir, puedes hacer tu propia vida y la de los demás, mucho más fácil a través de la documentación apropiada. La documentación puede incluir varias cosas, como incluir comentarios útiles y anotaciones en el código que ayudan a explicar por qué se realizó una acción en particular, en lugar de lo que se pretende lograr.

Uno de los aspectos más críticos de esto es incluir un archivo informativo `README` , que acompaña a casi todos los proyectos OSS, y algunas veces incluso más de uno. Puede ser una buena práctica incluir un archivo de este tipo en cada directorio, que incluya una lista de archivos, una tabla de contenido y cuál es el propósito del directorio. El archivo `README` normalmente es solo texto sin formato o de reducción (de nuevo, como todos los de MOOC!), Y puede incluir información crítica sobre cómo instalar y ejecutar software, dependencias y requisitos anteriores, así como tutoriales o ejemplos

> **¿Sabías que ...** El término `README` se atribuye algunas veces a la famosa escena de Alicia en el País de las Maravillas de Alicia de Lewis Carroll, en la que Alicia se enfrenta a bocadillos mágicos etiquetados con "Eat Me" y "Drink Me". Potente.

El propósito aquí es proporcionar información suficiente para maximizar la reutilización y reproducibilidad del entorno informático, de modo que alguien sin experiencia en el proyecto pueda acceder y reutilizar fácilmente el software ([Sandve et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)). Al reducir las barreras de entrada, aumenta las posibilidades de que otros puedan reutilizar su trabajo, que es uno de los objetivos finales de OSS ([Ince et al., 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)).

Una extensión de esto que puede ayudar a hacer las cosas aún más fáciles para una futura reutilización es la tecnología de "contenedor". Los contenedores son como un ecosistema congelado en el tiempo, donde el código, los datos y cualquier otra dependencia están perfectamente conservados, empaquetados y guardados en las versiones actuales de funcionamiento. Esto significa que cualquiera en el futuro, cualquiera puede entrar y ejecutar los análisis nuevamente. Como tales, generalmente son buenos para ser reutilizados, pero esto puede venir al sacrificio de la modificación o comprensión por parte de otros, ya que a menudo se pueden ocultar muchos detalles dentro del código fuente y sus dependencias. Los ejemplos comunes de implementación de contenedores en investigación incluyen [Rocker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf) (un contenedor Docker para el lenguaje R), [Binder](https://mybinder.readthedocs.io/en/latest/)y [Code Ocean](https://codeocean.com/).

**El software sostenible es un buen software.**

  


## 10 reglas simples para la investigación computacional reproducible

Las 10 reglas simples para hacer que la investigación computacional sea más reproducible, basada en [Sandve et al., (2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF), son:

1. Para cada resultado, mantenga un registro de cómo se produjo.
2. Evitar los pasos manuales de manipulación de datos.
3. Archiva las versiones exactas de todos los programas externos utilizados.
4. Control de versiones de todos los scripts personalizados.
5. Registre todos los resultados intermedios, cuando sea posible en formatos estandarizados.
6. Para los análisis que incluyen aleatoriedad, tenga en cuenta las semillas aleatorias subyacentes.
7. Siempre almacene los datos en bruto detrás de las parcelas.
8. Genere resultados de análisis jerárquicos, lo que permite inspeccionar capas de cada vez más detalles.
9. Conecte declaraciones textuales a los resultados subyacentes.
10. Proporcionar acceso público a scripts, ejecuciones y resultados.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/simple_rules.png?raw=true" width="800" /></p>

<p align="center"><i>Infografía adaptada de Sandve et al., (2013). ¡Siéntase libre de descargar esto e imprimirlo para tenerlo a mano durante su investigación!</i></p>

  


Si sigue estos pasos, junto con los procesos en [**Tarea 1**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) y [**Tarea 2**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), ¡debería estar bien!

  


## Licencia de código abierto <a name="Licensing"></a>

Una licencia de código abierto es un tipo de licencia diseñada específicamente para software y código que lo hace explícito cuáles son las condiciones legales para compartir y reutilizar. Como se mencionó [arriba](#What_OSS), la adición de una licencia adecuada es lo que diferencia el software compartido públicamente de OSS. Por ejemplo, el ampliamente utilizado [MATLAB](https://www.mathworks.com/products/matlab.html) es un software propietario, y [Octave](https://www.gnu.org/software/octave/) es un lenguaje de programación alternativo con licencia abierta.

Actualmente hay más de 1,400 licencias únicas de código abierto, una complejidad que nace de la dificultad de entender las diferencias entre las implicaciones legales en diferentes licencias.

Algunas de las licencias más comunes incluyen:

- [Berkeley Software Distribution ("BSD")](https://en.wikipedia.org/wiki/BSD_licenses),
- [apache](https://www.apache.org/licenses/LICENSE-2.0),
- [MIT-style (Instituto de Tecnología de Massachusetts)](https://opensource.org/licenses/MIT), o
- [GNU General Public License ("GPL")](https://www.gnu.org/licenses/gpl-3.0.en.html).

No es necesario que sepa todo lo que hay detrás de todo esto, pero es bueno saber al menos qué opciones están disponibles para usted.

Hay dos formas en que las contribuciones a un proyecto se licencian:

1. *Explícitamente*, donde la contribución individual tiene una licencia claramente indicada, independiente del proyecto principal; o
2. *Implícitamente*, por lo que la contribución cae bajo el código de licencia original del proyecto principal.

Afortunadamente, el proceso de selección de una licencia de código abierto es relativamente trivial, gracias a herramientas fáciles de usar como [Choose A License](https://choosealicense.com/). Cada una de estas licencias permite que otros usuarios utilicen, copien, distribuyan y desarrollen su trabajo, a menudo a la vez que se aseguran de que los creadores sean reconocidos adecuadamente por su trabajo. Aquí, la clave es seleccionar una licencia adecuada para su trabajo, dependiendo de lo que quiera o no quiera que otros hagan con él.

  


## Cita del software <a name="Citation"></a>

Las citas proporcionan una de las interacciones más importantes en la investigación académica, formando la base de nuestros sistemas de referencia y métricas. Por lo general, esto se realiza gracias a la asistencia de un identificador único permanente, como un [Digital Object Identifiers](https://en.wikipedia.org/wiki/Digital_object_identifier) (DOI). Un DOI es un identificador persistente, implementado en el [Handle System](https://en.wikipedia.org/wiki/Handle_System), que cumple con un estándar común, según el propósito, por ejemplo, para identificar información académica. Dicha identificación es crítica para rastrear la genealogía y la procedencia de la investigación, para la reproducibilidad, así como para dar el crédito apropiado a aquellos que han creado el software. Es importante destacar que el software debe considerarse un resultado legítimo de la investigación académica, y las citas se están convirtiendo en una forma cada vez más común de indicar eso.

En 2016, [Smith et al., 2016](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) escribieron un artículo de investigación sobre los principios de la citación de software como parte del Grupo de trabajo de citación de software FORCE11. De la misma manera que querría citar el software que ha utilizado como parte de las buenas prácticas de investigación, es importante que su investigación también sea fácilmente citable. Al citar cualquier software utilizado para su propia investigación, debe incluir como mínimo:

- El nombre del autor,
- Título del software,
- Número de versión, y
- El identificador / localizador único (DOI o URL).

Los seis principios de la cita del software de [Smith et al., (2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) se proporcionan aquí:

- **Importancia**: el software debe considerarse un producto de investigación legítimo y citable. A las citas de software se les debe otorgar la misma importancia en el registro académico que las citas de otros productos de investigación, como publicaciones y datos; deben incluirse en los metadatos del trabajo de citación, por ejemplo, en la lista de referencia de un artículo de una revista, y no deben omitirse ni separarse. El software debe citarse sobre la misma base que cualquier otro producto de investigación, como un papel o un libro, es decir, los autores deben citar el conjunto adecuado de productos de software tal como citan el conjunto apropiado de documentos.

- **Crédito y atribución**: las citas de software deben facilitar el otorgamiento de créditos académicos y normativos, atribución legal a todos los contribuyentes al software, reconociendo que un solo estilo o mecanismo de atribución puede no ser aplicable a todo el software.

- **Identificación única**: una cita de software debe incluir un método de identificación que sea accionable por máquina, globalmente único, interoperable y reconocido por al menos una comunidad de los expertos de dominio correspondientes, y preferiblemente por investigadores del público en general.

- **Persistencia**: los identificadores únicos y los metadatos que describen el software y su disposición deben persistir, incluso más allá de la vida útil del software que describen.

- **Accesibilidad**: las citas de software deben facilitar el acceso al mismo software ya sus metadatos, documentación, datos y otros materiales necesarios para que tanto los humanos como las máquinas puedan hacer un uso informado del software al que se hace referencia.

- **Especificidad**: las citas de software deben facilitar la identificación y el acceso a la versión específica del software que se utilizó. La identificación del software debe ser tan específica como sea necesario, como el uso de números de versión, números de revisión o variantes, como plataformas.

Nota: Para obtener instrucciones sobre 'cómo hacer que su software sea citable', consulte la sección [**Uso de GitHub y Zenodo**](#GitHub_Zenodo) continuación y [**Tarea 2: Vinculación de GitHub y Zenodo**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md).

  


## Usando GitHub y Zenodo <a name="GitHub_Zenodo"></a>

[GitHub](#GitHub) es una herramienta popular para la gestión de proyectos, el almacenamiento de contenido y el control de versiones. Tenga en cuenta que GitHub en sí no es OSS. Sin embargo, Git, la herramienta en la que se basa, es. Git está diseñado para ayudar a administrar los archivos de código fuente, y las actualizaciones a ellos, para un proyecto relacionado con el software. Sin embargo, también puede extenderse a otros proyectos que no sean software; Por ejemplo, este [MOOC](https://github.com/OpenScienceMOOC/)!

Sin embargo, investigar sobre GitHub es solo el primer paso. Es igualmente importante hacerlo persistente y reutilizable, por lo que puede ser útil tener un Identificador de objeto digital (DOI) asociado. La forma más sencilla de hacerlo es a través de un servicio llamado [Zenodo](https://zenodo.org/), que es un repositorio multidisciplinario gratuito y de código abierto creado por OpenAIRE y CERN, y se puede usar para asignar un DOI a repositorios individuales de GitHub. Hay un [Guía GitHub](https://guides.github.com/activities/citable-code/) que explica los detalles, que implican la vinculación de los repositorios de GitHub directamente a través de Zenodo de modo que cuando los desarrolladores a crear comunicados formales para su software, Zenodo crea y archivos que una versión del software.

No hay nada especial en el uso de Zenodo para crear DOI, aparte de su **gratuito**; También se pueden usar otros repositorios generales, como [DataCite DOI Fabrica](https://doi.datacite.org/), o sus propios repositorios institucionales, como [Caltech's](https://www.library.caltech.edu/news/enhanced-software-preservation-now-available-caltechdata).

Muchos investigadores normalmente temen compartir un código incompleto, defectuoso o imperfecto. Sin embargo, en la comunidad OSS, tal práctica de compartir código 'en bruto' es bastante común. Compartir el código abiertamente permite a otros reutilizarlo y mejorarlo, así como a involucrarse de una manera más profunda en cualquier investigación asociada con él. Este es uno de los aspectos fundamentales de la colaboración entre pares, tal vez mejor ejemplificado por el proceso tradicional de investigación de pares de revisión manuscrita.

La tarea 2 lo guiará a través del proceso de vinculación de un repositorio de GitHub a Zenodo para su archivo.

> **¿Sabía que ...** Todo el contenido producido para este MOOC está disponible como parte de una comunidad en [Zenodo](https://zenodo.org/communities/open-science-mooc/)?

**[IR A LA TAREA 2: Vinculación de GitHub y Zenodo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)**

  


## Colaborando y contribuyendo a través de Open Source. <a name="Collaborating"></a>

A menudo, OSS se desarrolla de manera pública, descentralizada y colaborativa entre múltiples contribuyentes. El propósito de esto es mejorar la diversidad y el alcance de un proyecto y su diseño, para que sea más beneficioso y sostenible. Este enfoque fue famoso en comparación con un modelo de "bazar" por Eric Raymond, uno de los primeros defensores de la OSS. Uno de los principales principios rectores de esto es el de **Peer Production**, que se basa en comunidades auto-organizadas para regular el desarrollo de contenido, coordinado hacia un objetivo o resultado compartido.

Los proyectos de OSS dependen en gran medida de la colaboración de voluntarios, que a menudo conlleva un flujo constante de recién llegados para ser productivos y sostenibles ([Steinmacher et al., 2014](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)). La creación de la atmósfera social adecuada para un proyecto, y un entorno de compromiso acogedor, a menudo son críticos para el éxito de las colaboraciones en OSS.

  


## A dónde ir desde aquí <a name="Future_OSS"></a>

Esperemos que ahora haya llegado a ver la importancia del software como una piedra angular de la ciencia moderna, y la importancia que OSS juega en esto.

Los **resultados de aprendizaje** de esto deberían ser:

1. Ahora podrá definir las características de OSS y algunos de los argumentos de impacto ético, legal, económico y de investigación a favor y en contra.

2. De acuerdo con los estándares de la comunidad, ahora podrá describir los requisitos de calidad para compartir y reutilizar el código abierto.

3. Ahora podrá utilizar una gama de herramientas de investigación que utilizan OSS.

4. Ahora podrá transformar el código diseñado para su uso personal en un código accesible y reutilizable por otros.

5. Los desarrolladores de software podrán hacer que su software sea citable, y los usuarios de software sabrán cómo citar el software que utilizan.

  


**TAREA DE BONIFICACIÓN**

Si ha completado [Tarea 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) y [Tarea 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), también tenemos **TAREA BONUS** para usted, si desea llevar sus habilidades un paso más allá. [Tarea 3](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md) lo llevará más allá en la integración de Git en un flujo de trabajo de investigación típico al mostrarle cómo integrarlo con R Studio. Se recomienda que haya completado las 2 primeras tareas antes de continuar con esta.

Sin embargo, su viaje de código abierto no se detiene aquí! Esto fue solo el comienzo, y hay algunos recursos increíbles por ahí si desea hacer o aprender más:

- Si se siente particularmente inspirado por esto, puede respaldar el Manifiesto</a>Código de Ciencia , que se basa en los cinco principios de código, derechos de autor, citas, crédito y curación.</p></li> 
    
    - Para iniciar y desarrollar su propio proyecto, el programa [Guías de código abierto](https://opensource.guide/) ofrece una gama de guías prácticas y habilidades para ayudar a lanzar y avanzar sus proyectos OSS.
    
    - Para un examen detallado de los flujos de trabajo de investigación basada en OSS, el [Ciencia Abierta, Open Data, Open Source](https://pfern.github.io/OSODOS/gitbook/) mano-guía por Pedro L. Fernandes y Rutger A. Vos es uno de los mejores recursos en línea.
    
    - También existen sitios de revistas más formalizados para artículos basados en software, incluidos [The Journal of Open Research Software](https://openresearchsoftware.metajnl.com/) y [The Journal of Open Source Software](https://joss.theoj.org/). Una lista de tales lugares es también [disponible](https://www.software.ac.uk/which-journals-should-i-publish-my-software).
    
    - El kit</a> herramientas de fuente abierta [PLOS ](https://channels.plos.org/open-source-toolkit) proporciona un foro global para la investigación y aplicaciones de hardware y software de fuente abierta.
    
    - El [NumFOCUS](http://www.numfocus.org) es una organización sin fines de lucro que respalda y promueve software científico de código abierto, innovador y de clase mundial. Algunos de los proyectos que patrocinan incluyen:
        
        - [IPython](http://ipython.org) y [Jupyter Notebook](https://jupyter.org) iniciativas.
        
        - [rOpenSci](http://ropensci.org), que promueve el entorno estadístico de código abierto R para una investigación transparente y reproducible.
        
        - Para obtener más experiencia práctica con OSS, la comunidad [Software Carpentry](https://software-carpentry.org/) organiza talleres regulares para mejorar las habilidades informáticas basadas en el laboratorio ([Wilson et al., 2017](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Wilson%20et%20al.%2C%202017.pdf)).</ul> 
    
      
    
    
    ### Otras lecturas <a name="Reading"></a>
    
    *Estas referencias aquí son solo el comienzo. Incluyen algunas de las descripciones generales más útiles del panorama de código abierto en la investigación. Sin embargo, si desea encontrar algo más específico para su propio campo de investigación, entonces ese camino está ahí para que lo explore.*
    
    - El futuro de la investigación en el desarrollo de software libre / de código abierto [(Scacchi, 2010)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Scacchi%2C%202010.pdf).
    
    - El método científico en la práctica: reproducibilidad en las ciencias computacionales [(Stodden, 2010)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Stodden%2C%202010.pdf).
    
    - El caso de los programas informáticos abiertos [(Ince et al., 2012)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf).
    
    - Problemas actuales y tendencias de investigación en comunidades de software de código abierto [(Martínez-Torres y Díaz-Fernández, 2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Martinez-Torres%20and%20Diaz-Fernandez%2C%202013.pdf).
    
    - Diez reglas simples para la investigación computacional reproducible [(Sandve et al., 2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF).
    
    - Una revisión sistemática de la literatura sobre las barreras que enfrentan los recién llegados a los proyectos de software de código abierto [(Steinmacher et al., 2014)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf).
    
    - Intercambio de conocimientos en comunidades de software de código abierto: motivaciones y gestión [(Iskoujina y Roberts, 2015)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Iskoujina%20and%20Roberts%2C%202015.pdf).
    
    - Principios de citación de software [(Smith et al., 2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf).
    
    - Una introducción a los contenedores Rocker: Docker para R [(Boettiger y Eddelbuettel, 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf).
    
    - Buenas prácticas en computación científica [(Wilson et al., 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Wilson%20et%20al.%2C%202017.pdf).
    
    - Cuatro recomendaciones simples para fomentar las mejores prácticas en software de investigación [(Jiménez et al., 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Jim%C3%A9nez%20et%20al.%2C%202018.pdf).
    
      
    
    
    ### Equipo de desarrollo <a name="Development_team"></a>
    
    - [Alex Morley](https://twitter.com/alex__morley), Open Sourceror, Universidad de Oxford, Reino Unido.
    - [Kevin Moerman](https://twitter.com/KMMoerman), Open Sourceror, MIT, EE. UU.
    - [Tania Allard](https://twitter.com/ixek), Open Sourceress, Encantadora de datos, Universidad de Leeds, Reino Unido.
    - [Simon Worthington](https://twitter.com/mrchristian99), Libro Liberacionista, TIB, Alemania.
    - [Paola Masuzzo](https://twitter.com/pcmasuzzo), Open Source Batman, Italia.
    - [Ivo Grigorov](https://twitter.com/OAforClimate), Open Source Robin, Dinamarca.
    - [Rutger Vos](https://twitter.com/rvosa), Open Sourceror, Naturalis Biodiversity Center, Países Bajos.
    - [Julien Colomb](https://twitter.com/j_colomb), Open Ninja, Berlín.
    - [Jon Tennant](https://twitter.com/protohedgehog), Dinosaur Whisperer.
    
    **¿Sabes de qué manera se puede mejorar este contenido?**
    
    ¡Es hora de tomar tus nuevas habilidades GitHub para una prueba de ejecución! Todo el desarrollo de contenido ocurre principalmente [aquí](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md). Si tiene una mejora sugerida en el contenido, el diseño o cualquier otra cosa, puede hacerlo y luego se convertirá automáticamente en parte del contenido de MOOC después de la verificación de un moderador.
    
    [![Dedicación de dominio público CC0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)