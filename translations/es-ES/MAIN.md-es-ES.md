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
- [The Open Source community and its governance](#OS_Community)
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

> "Un artículo sobre el resultado computacional es publicidad, no erudición. La actual erudición es el entorno de software completo, el código y los datos que produjeron el resultado ". - J. Buckheit y DL Donoho, 1995.

El software y la tecnología sustentan gran parte de la investigación moderna, que ahora es casi inevitablemente computacional de una u otra forma: motores de búsqueda, plataformas de redes sociales, software analítico y publicación digital. Con esto, existe una demanda cada vez mayor de software de código abierto más sofisticado, combinado con una creciente disposición de los investigadores a colaborar abiertamente en nuevas herramientas.

El poder del Código Abierto radica en que reduce las barreras para la colaboración y la adopción, lo que permite que las ideas y la tecnología se propaguen más rápidamente. Este módulo presentará las herramientas necesarias para transformar el software en algo que otros puedan acceder y reutilizar abiertamente.

<img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/open_research_software_open_source.png?raw=true" width="800" />

<p align="center"><i>Imagen de Patrick Hochstenbach (CC0 1.0 Universal)</i></p>

  


### **Objetivos específicos de aprendizaje para este Módulo**:

1. Aprender las características del software abierto; entender los **argumentos éticos, legales, económicos y de impacto en la investigación a favor y en contra del Software de Código Abierto **, además de entender mejor los requisitos de calidad de código abierto.

2. Ser capaz de convertir el código hecho para uso personal en un código abierto al que otros puedan acceder.

3. Usar software (herramientas) que utiliza contenido abierto y fomenta una colaboración más amplia.

  


## ¿Qué es el Software de Código Abierto? <a name="What_OSS"></a>

Prácticamente todos los flujos de trabajo de investigación científica moderna se basan en una gama de herramientas de software, ya sea que operen en diferentes conjuntos de datos con diferentes parámetros y se apliquen de manera iterativa de varias maneras (ciencia de datos) o que operan en diferentes entradas y utilizan modelos y métodos para predecir algún estado de salida ( Ciencia computacional). El software de código abierto (OSS) es un software de computadora en el que el código fuente completo está disponible bajo una licencia específica que permite a otros usuarios acceder, ver, modificar y redistribuir ese código para cualquier propósito. Debido a que OSS requiere una licencia de este tipo, por lo general se mantiene de forma gratuita de forma predeterminada. Esta licencia explícita es también lo que diferencia a OSS del software libre. Reutilizar OSS para análisis, simulación y visualización para investigación también suele ser más fácil y más flexible en comparación con el software propietario. A menudo, ya sea que lo sepamos o no, ya estamos usando OSS como parte de nuestros propios flujos de trabajo de investigación.

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

Algunos consideran que el movimiento OSS representa un movimiento contrario al neoliberalismo y la privatización, a través del desafío a las regulaciones y normas en la construcción y reutilización de la información, y una transformación potencial del capitalismo moderno al hacer que el software esté disponible abundantemente con el mínimo esfuerzo. See [The free/open source software movement: Resistance or change?](https://doi.org/10.15448/1984-7289.2009.1.5569) by Panayiota Georgopoulou for more on this topic.

  


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

There are two main camps within the free/libre and open source software (FLOSS) community: The **free software movement**, and the **open source software movement** (OSS). Ambos tienen diferentes ideologías basadas en las libertades de los usuarios y las aplicaciones prácticas del software. The term 'FLOSS' is used as a overaching neutral term to refer to both; libre being French and Spanish for 'free' in the context of freedom.

In a similar way that people active in the open science movement are heterogeneous in their assumptions and aims, different opinions exist in the FLOSS community as well. Recalling module 1, two of the schools of thought in open science were the *Pragmatic school* and the *Democratic school*. While the former is driven by the assumption that research could be more efficient if scientists worked together, the latter wants to set straight an unequal distribution of knowledge. They probably both end up sharing their research, but each with different intentions.

This is roughly comparable to the OSS and the free software movement: The latter evolved around 1983 to protect what they call the four essential freedoms of a program's user. These include the freedom to run, copy, distribute, study, change and improve a program. Software that respects these freedoms with an appropriate license is considered 'free'. The four freedoms are seen as vital for a society as a whole in the sense that they only enable sharing, cooperation and ultimately freedom in general. In this sense the free software movement is a social movement that creates an ethical imperative.

The open source software movement, which splintered off in 1998, focuses on the practical advantages and does not campaign for principles. It is concerned with developing high-quality software, for which everyone's ability to obtain, modify and contribute back the source code is considered highly beneficial.

Among multiple conclusions they arrive at, access to a program's source code is a shared one. Software thus may be considered *free*, *open source*, or both, according to agreed-on definitions by the Free Software Foundation ([FSF](https://www.gnu.org/philosophy/free-sw.html)) and the Open Source Initiative ([OSI](https://opensource.org/osd)). The FSF argues that free software is a subset of OSS, with only a [fraction](https://www.gnu.org/philosophy/free-open-overlap.html) being open source but nonfree.

Thus, highlighting a particular license status of software in use—open source or free—is mostly about different philosophies, not about software not having the other status as well. Each movement has its share of problems explaining their term: *free* means more than being gratis and *open source* means more than having access to the source code. The [FSF](https://www.gnu.org/philosophy/open-source-misses-the-point.html) and the European counterpart [FSFE](https://fsfe.org/documents/whyfs.html) provide more information on this topic.

### Para proyectos individuales

A typical open source project has the following types of formal roles:

- **Autor**: Es la persona que creó el proyecto.
- **Propietario**: la persona o personas que tienen propiedad administrativa sobre la organización o el repositorio 
- **Mantenedores**: Colaboradores que son responsables de dirigir la visión y gestionar los aspectos organizativos del proyecto. (También pueden ser autores o dueños del proyecto.)
- **Colaboradores**: El usuario que ya ha contribuido al proyecto.
- **Miembros de la comunidad**: Personas que usan el proyecto. Pueden participar activamente en las conversaciones, crear nuevos problemas o expresar su opinión sobre las futuras mejoras del proyecto.

Typically, roles are made public through either the `README` file, a Contributors file, or a separate team page for the project.

  


## Plataformas y herramientas existentes para software de código abierto <a name="Platforms"></a>

Virtual environments and machines are becoming increasingly popular as high-powered research workflow enablers, and many of these are built upon OSS (e.g., operating systems, programming languages, and data processing frameworks). Popular services include [Google Cloud](https://cloud.google.com/compute/) and [Amazon Web Services](https://aws.amazon.com/), which also assist with database storage and content delivery, as well as computational power. [InsideDNA](https://insidedna.me/) is a computing platform for reproducible research in bioinformatics, genomics and the life sciences.

As mentioned [above](#What_OSS), LibreOffice provides an Open Source alternative to Microsoft Office. The two are almost completely compatible, just with different default file formats. For citation managers, [Zotero](https://www.zotero.org/) is the most popular Open Source alternative to proprietary platforms such as Mendeley or EndNote.

[Zotero](https://www.zotero.org/) uses the BibTeX (pronounced 'bib-tech') format, based on LaTeX (pronounced 'lay-tech'), and has browser plugins to make citation management simple. By integrating this with other software such as LibreOffice, it is now possible to have a fully Open Source research workflow in many cases.

### GitHub <a name="GitHub"></a>

> ¿Sabía que este proyecto completo se construyó como un esfuerzo comunitario abierto y colaborativo en [GitHub](https://github.com/OpenScienceMOOC/)?

[GitHub](https://github.com/) is a popular hosting site for both software and non-software content (often called 'notebooks'), with added capabilities for version control, project management and tracking, and storage services. GitHub is built on top of the OSS [Git](https://git-scm.com/), which enables users to work remotely to maintain, share, and collaborate on research software and other non-software based projects.

Version control is essentially a process that takes snapshots of the files in a repository, and tracks modifications to them. It records when the changes were made, what they were, and who did them. If several people are working on one file at once, any overlapping changes are detected, and must be resolved prior to continuing. This provides a much more streamlined and automated process than manually saving and recording changes as projects develop. It also avoids the inevitable lists of confusing named file versions...

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/xkcd.png?raw=true" width="200" /></p>

<p align="center"><i>GitHub helps us to avoid, er, sub-optimal file naming conventions (source: XKCD)</i></p>

  


One of the more popular and useful functions of GitHub is the [issue tracker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/issues), which is used to organise OSS development. The above link takes you to the issue tracker for the development of this module! If you think there is something here that can improved, or you want to comment on, anyone can add or contribute to an issue there!

Other similar project hosting services include [BitBucket](https://bitbucket.org/), [GitLab](https://about.gitlab.com/), and [Launchpad](https://launchpad.net/). If the recent acquisition of GitHub by Microsoft is a bit off-putting to you, these are great alternatives.

However, we also know that GitHub can have quite a high learning curve. Which is why the first practical task for this MOOC will teach you how to set up your first GitHub project repository!

**[GO TO TASK 1: Building your first GitHub repository](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)**

  


## Software de código abierto utilizado en la investigación. <a name="Research"></a>

Especially in scientific research, Open Source Software usage and development has become practically the norm. There's a number of reasons for this beyond those that apply to the general acceptance of OSS by, for example, consumers, industry, or government. Among these reasons are:

- Cada vez más, los algoritmos implementados en el software de análisis forman una parte integral de los métodos descritos en publicaciones académicas. Como tal, está completamente en desacuerdo con la rigurosa revisión por pares si estas implementaciones de algoritmos están cerradas a personas externas.

- La colaboración científica a menudo abarca múltiples instituciones y redes de investigación distribuidas donde el secreto y la jerarquía de comando no se mantienen de una manera que sea 'necesaria' para el desarrollo de código cerrado.

- Muchos análisis computacionales se ejecutan en entornos virtualizados (como infraestructuras institucionales, nacionales o internacionales de "nube") y se alojan en servidores multiusuario. El software comercial de código cerrado a menudo no permite tal uso.

- El desarrollo de OSS a menudo se basa en voluntarios. En una época de restricciones presupuestarias para la investigación científica, esta es una clara ventaja.

For these and other reasons, Open Source tools are very commonly used in scientific research. This includes usage in fields where many researchers are amateur developers themselves and rely on tools such as [R](https://www.r-project.org/) for statistical analysis and scripting, which, in the last decade, has almost completely displaced commercial software for statistical analysis such as SPSS or JMP in a lot of fields. In fields such as bioinformatics, that involve a lot of file handling of the outputs of DNA sequencing platforms, general purpose scripting languages such as [Python](https://www.python.org/) and commonly used libraries built on top of it (such as [biopython](http://biopython.org)) have become a vital part of the toolkit of many researchers.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/python.png?raw=true" width="400" /></p>

<p align="center"><i>Python</i></p>

  


Tools such as R and Python are essentially software for writing software. Although programming is an increasingly common activity among researchers, of course not *every* scientist does this. One step away from programming is the chaining together of the inputs and outputs of various analysis tools in longer workflows. As an example from genomics, a very common workflow is to start out with high-throughput sequencing reads and then i) do basic quality control checks; ii) map the reads against a reference genome; iii) identify the points where the new data are at variance with the reference. These steps are routinely executed as a workflow where a different Open Source executable is run in a Linux command-line environment for each of the three steps. Although this is arguably not quite open source software development, it does involve the usage and production of open source artifacts (such as Linux shell scripts) for which the principles that we discuss in this module are applicable.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/r.png?raw=true" width="200" /></p>

<p align="center"><i>R</i></p>

  


Lastly, OSS is also used in scientific research for reasons that more closely mirror those that drive the adoption of OSS in wider society, namely that it is cheap. For example, individuals or organizations might decide to switch from Microsoft Office to LibreOffice for manuscript writing or spreadsheet processing because the latter is free (both as in [**'free beer'**](https://www.youtube.com/watch?v=dQw4w9WgXcQ) and 'free speech'). Likewise, the choice to switch from ArcGIS to [QGIS](https://www.qgis.org/en/site/) for the analysis of geographic information might be prompted simply by cost considerations.   


## Comenzando con OSS - Preguntas frecuentes <a name="FAQ"></a>

**I'm using X[e.g. Matlab,STATA,Excel] and I want to transition to something more open. What are the next steps?**

Even if you are using proprietary software, you can usually still share your source code/documents etc. *The best first step is sharing whatever you can*.

**Great! I can put them in my new github repo.**

If that's enough for you for now great! If not for most pieces of proprietary software there are Open Source equivalents. Have a go with one and see what you think.

| Cerrado                                                                                                 | Abierto                                                                                                                                                           |
| ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Matlab                                                                                                  | Python, Julia                                                                                                                                                     |
| STATA / SPSS                                                                                            | R                                                                                                                                                                 |
| MS Office                                                                                               | LibreOffice                                                                                                                                                       |
| Matemática                                                                                              | JupyterLab                                                                                                                                                        |
| Max/MSP                                                                                                 | PureData                                                                                                                                                          |
| Test out your new [Pull Request -PR-](https://help.github.com/articles/about-pull-requests/) Skills ... | ... by adding your own example [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md) |

**Cool! But if I make the switch will I be stuck: taking ages to learn a new tool/ without support /with buggy software.**

Good question! The answer is it depends. The best thing to do is find someone who's made the switch before and learn from their experience. Or just do a Google search! Some OSS is much better than their closed counterparts, some aren't, so it's worth choosing carefully.

## Haciendo buen software para su reutilización. <a name="Reuse"></a>

The most likely person who might want to re-use your software in the future is...you! So while sharing is always better than not sharing, you can make your own life, and that of others, much easier through appropriate documentation. Documentation can include several things, such as including helpful comments and annotations in the code that help to explain why a particular action was performed, rather than what it is intended to achieve.

One of the most critical aspects of this is including an informative `README` file, that accompanies almost every OSS project, and some times even more than one. It can be a good practice to include one such file in every directory, that includes a list of files, a table of contents, and what the purpose of the directory is. The `README` file is typically just plain text or markdown (again, such as all of the ones for the MOOC!), and can include critical information for how to install and run software, previous dependencies and requirements, as well as tutorials or examples.

> **¿Sabías que ...** El término `README` se atribuye algunas veces a la famosa escena de Alicia en el País de las Maravillas de Alicia de Lewis Carroll, en la que Alicia se enfrenta a bocadillos mágicos etiquetados con "Eat Me" y "Drink Me". Potente.

The purpose here is to provide sufficient information to maximise the re-use and reproducibility of the computational environment, such that someone with no experience with the project can easily access and re-use the software ([Sandve et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)). By lowering the barriers to entry, you increase the chances of others being able to re-use your work, which is one of the ultimate goals of OSS ([Ince et al., 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)).

An extension of this that can help to make things even easier for future re-use is 'container' technology. Containers are like an ecosystem frozen in time, where the code, the data, any other dependencies, are all perfectly preserved, packaged and saved in the present functioning versions. This means that anyone in the future any one can come in and run the analyses again. As such, they are generally good for re-use, but this can come at the sacrifice of modification or understanding by others, as often a lot of details can be hidden within the source code and its dependencies. Common examples of container implementation in research include [Rocker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf) (a Docker container for the R language), [Binder](https://mybinder.readthedocs.io/en/latest/), and [Code Ocean](https://codeocean.com/).

**Sustainable software is good software.**

  


## 10 reglas simples para la investigación computacional reproducible

The 10 simple rules for making computational research more reproducible, based on [Sandve et al., (2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF), are:

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

<p align="center"><i>Infographic adapted from Sandve et al., (2013). Feel free to download this and print it out to keep handy during your research!</i></p>

  


If you follow these steps, along with the processes in [**Task 1**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [**Task 2**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), you should be fine!

  


## Licencia de código abierto <a name="Licensing"></a>

An Open Source license is a type of license designed specifically for software and code that make it explicit what the legal conditions for sharing and re-use are. As mentioned [above](#What_OSS), the addition of a suitable license is what differentiates publicly shared software from OSS. For example, the widely used [MATLAB](https://www.mathworks.com/products/matlab.html) is proprietary software, and [Octave](https://www.gnu.org/software/octave/) is an openly licensed alternative programming language.

There are currently more than 1,400 unique Open Source licenses, a complexity born from the difficulty in understanding the differences between the legal implications across different license.

Some of the more common licenses include:

- [Berkeley Software Distribution ("BSD")](https://en.wikipedia.org/wiki/BSD_licenses),
- [apache](https://www.apache.org/licenses/LICENSE-2.0),
- [MIT-style (Instituto de Tecnología de Massachusetts)](https://opensource.org/licenses/MIT), o
- [GNU General Public License ("GPL")](https://www.gnu.org/licenses/gpl-3.0.en.html).

You don't need to know all the legal itty gritty behind all of these, but it is good to at least know what options are avaiilable to you.

There are two ways in which contributions to a project become licensed:

1. *Explícitamente*, donde la contribución individual tiene una licencia claramente indicada, independiente del proyecto principal; o
2. *Implícitamente*, por lo que la contribución cae bajo el código de licencia original del proyecto principal.

Thankfully, the process of selecting an Open Source license is relatively trivial, thanks to user-friendly tools such as [Choose A License](https://choosealicense.com/) or [Public License Selector](https://ufal.github.io/public-license-selector/). Each of these licenses allows other users to use, copy, distribute, and build upon your work, often while ensuring that the creators are appropriately recognised for their work. Here, the key is selecting an appropriate license for your work, depending on what you want, or do not want, others to do with it.

  


## Cita del software <a name="Citation"></a>

Citations provide one of the most important interactions in scholarly research, forming the basis of our referencing and metrics systems. Typically, this is performed thanks to the assistance of a permanent unique identifier such as a [Digital Object Identifiers](https://en.wikipedia.org/wiki/Digital_object_identifier) (DOI). A DOI is a persistent identifier, implemented in the [Handle System](https://en.wikipedia.org/wiki/Handle_System), that meets a common standard, depending on the purpose, such as for identifying academic information. Such identification is critical for tracking the genealogy and provenance of research, for reproducibility, as well as for giving appropriate credit to those who have created the software. Importantly, software should be considered a legitimate output from scholarly research, and citation is becoming an increasingly common way to indicate that.

In 2016, [Smith et al., 2016](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) wrote a research paper about the principles of software citation as part of the FORCE11 Software Citation Working Group. In the same way that you would want to cite software that you have used as part of good research practices, it is important to make your research easily citable too. When citing any software used for your own research, you should include at minimum:

- El nombre del autor,
- Título del software,
- Número de versión, y
- El identificador / localizador único (DOI o URL).

The six principles of software citation by [Smith et al., (2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) are provided here:

- **Importancia**: el software debe considerarse un producto de investigación legítimo y citable. A las citas de software se les debe otorgar la misma importancia en el registro académico que las citas de otros productos de investigación, como publicaciones y datos; deben incluirse en los metadatos del trabajo de citación, por ejemplo, en la lista de referencia de un artículo de una revista, y no deben omitirse ni separarse. El software debe citarse sobre la misma base que cualquier otro producto de investigación, como un papel o un libro, es decir, los autores deben citar el conjunto adecuado de productos de software tal como citan el conjunto apropiado de documentos.

- **Crédito y atribución**: las citas de software deben facilitar el otorgamiento de créditos académicos y normativos, atribución legal a todos los contribuyentes al software, reconociendo que un solo estilo o mecanismo de atribución puede no ser aplicable a todo el software.

- **Identificación única**: una cita de software debe incluir un método de identificación que sea accionable por máquina, globalmente único, interoperable y reconocido por al menos una comunidad de los expertos de dominio correspondientes, y preferiblemente por investigadores del público en general.

- **Persistencia**: los identificadores únicos y los metadatos que describen el software y su disposición deben persistir, incluso más allá de la vida útil del software que describen.

- **Accesibilidad**: las citas de software deben facilitar el acceso al mismo software ya sus metadatos, documentación, datos y otros materiales necesarios para que tanto los humanos como las máquinas puedan hacer un uso informado del software al que se hace referencia.

- **Especificidad**: las citas de software deben facilitar la identificación y el acceso a la versión específica del software que se utilizó. La identificación del software debe ser tan específica como sea necesario, como el uso de números de versión, números de revisión o variantes, como plataformas.

Note: For instructions on 'how to make your software citable' see the section [**Using GitHub and Zenodo**](#GitHub_Zenodo) below and [**Task 2: Linking GitHub and Zenodo**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md).

  


## Usando GitHub y Zenodo <a name="GitHub_Zenodo"></a>

[GitHub](#GitHub) is a popular tool for project management, content storage, and version control. Note that GitHub itself is not OSS. However, Git, the tool which it is based on, is. Git is designed to help manage the source code files, and the updates to them, for a software-related project. However, it can also be extended to other non-software projects; for example, this [MOOC](https://github.com/OpenScienceMOOC/)!

However, getting research onto GitHub is just the first step. It is equally important to make it persistent and re-usable, which is why having a Digital Object Identifier (DOI) associated with it can be useful. The simplest way to do this is through a service called [Zenodo](https://zenodo.org/), which is a free and open source multi-disciplinary repository created by OpenAIRE and CERN, and can be used to assign a DOI to individual GitHub repositories. There is a [GitHub Guide](https://guides.github.com/activities/citable-code/) that explains the details, which involve linking GitHub repositories directly through to Zenodo so that when developers create formal releases for their software, Zenodo creates and archives a that version of the software.

There's nothing special about using Zenodo for creating DOIs, other than its **free of cost**; other general repositories can also be used, such as [DataCite DOI Fabrica](https://doi.datacite.org/), or your own institutional repositories such as [Caltech's](https://www.library.caltech.edu/news/enhanced-software-preservation-now-available-caltechdata).

A lot of researchers might typically be afraid of sharing code which is incomplete, buggy, or imperfect. However, in the OSS community, such a practice of sharing 'raw' code is fairly commonplace. Sharing code openly enables others to re-use and improve it, as well as to engage in a deeper way with any research associated with it. This is one of the fundamental aspects of peer-collaboration, perhaps best exemplified by the traditional process of research manuscript peer review.

Task 2 will guide you through the process of linking a GitHub repository to Zenodo for archiving.

> **¿Sabía que ...** Todo el contenido producido para este MOOC está disponible como parte de una comunidad en [Zenodo](https://zenodo.org/communities/open-science-mooc/)?

**[GO TO TASK 2: Linking GitHub and Zenodo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)**

  


## Colaborando y contribuyendo a través de Open Source. <a name="Collaborating"></a>

Often, OSS is developed in a public, decentralised, collaborative manner between multiple contributors. The purpose of this is to enhance the diversity and scope of a project and its design, in order to become more beneficial and sustainable. Such an approach was famously likened to a 'bazaar' model by Eric Raymond, an early OSS proponent. One of the major guiding principles of this is that of **peer production**, which relies on self-organised communities to regulate the development of content, co-ordinated towards a shared goal or outcome.

OSS projects rely heavily on volunteer collaboration, which often entails a constant flux of newcomers in order to become productive and sustainable ([Steinmacher et al., 2014](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)). Creating the right social atmosphere for a project, and a welcoming engagement environment, are often critical to successful collaboraitons in OSS.

  


## A dónde ir desde aquí <a name="Future_OSS"></a>

Hopefully now you have come to see the importance of software as a cornerstone of modern science, and the importance that OSS plays in this.

The **learning outcomes** from this should be:

1. Ahora podrá definir las características de OSS y algunos de los argumentos de impacto ético, legal, económico y de investigación a favor y en contra.

2. De acuerdo con los estándares de la comunidad, ahora podrá describir los requisitos de calidad para compartir y reutilizar el código abierto.

3. Ahora podrá utilizar una gama de herramientas de investigación que utilizan OSS.

4. Ahora podrá transformar el código diseñado para su uso personal en un código accesible y reutilizable por otros.

5. Los desarrolladores de software podrán hacer que su software sea citable, y los usuarios de software sabrán cómo citar el software que utilizan.

  


**BONUS TASK**

If you have completed [Task 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [Task 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), we also have a **BONUS TASK** for you, if you want to take your skills a step further. [Task 3](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md) will take you a step deeper into integrating Git into a typical research workflow by showing you how to integrate it with R Studio. It is recommended that you have completed the first 2 tasks before proceeding with this one.

However, your Open Source journey does not stop here! This was just the beginning, and there are some incredible resources out there if you would like to do or learn more:

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
    
    *These references here are just the beginning. They include some of the most useful general overviews of the Open Source landscape in research. However, if you want to be find something more specific to your own research field, then that path is there for you to explore!*
    
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
    
    **Know a way this content can be improved?**
    
    Time to take your new GitHub skills for a test-run! All content development primarily happens [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md). If you have a suggested improvement to the content, layout, or anything else, you can make it and then it will automatically become part of the MOOC content after verification from a moderator!
    
    [![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)