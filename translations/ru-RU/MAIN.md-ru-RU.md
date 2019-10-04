---
output:
  html_document: по умолчанию
  pdf_document: по умолчанию
---

# Модуль 5: Открытое программное обеспечение для исследований и Open Source

## Оглавление

- [Вступление](#Introduction)
- [Что такое программное обеспечение с открытым исходным кодом](#What_OSS)
- [Принципы открытого программного обеспечения](#Principles)
- [The Open Source community and its governance](#OS_Community)
- [Существующие платформы и инструменты для программного обеспечения с открытым исходным кодом](#Platforms)
- [Программное обеспечение с открытым исходным кодом, используемое в исследованиях](#Research)
- [Начало работы с OSS - FAQ](#FAQ)
- [Создание хорошего программного обеспечения для повторного использования](#Reuse)
- [Лицензирование Open Source](#Licensing)
- [Цитирование программного обеспечения](#Citation)
- [Использование GitHub и Zenodo](#GitHub_Zenodo)
- [Сотрудничество через открытый исходный код](#Collaborating)
- [Куда пойти отсюда](#Future_OSS)

**ПОЖАЛУЙСТА, ОБРАТИТЕ ВНИМАНИЕ** что аудио версия этого доступна для загрузки через [Soundcloud](https://soundcloud.com/open-science-mooc/module-5-open-source-and-open-research-software) и [YouTube](https://www.youtube.com/watch?v=BHrOEmKk5zM).

## Вступление <a name="Introduction"></a>

Добро пожаловать в **Модуль 5** Open Science MOOC: **Open Research Software и Open Source**.

Этот модуль был разработан [в открытом](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source) в сотрудничестве с международной командой [Open Source Afficianados](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/README.md#development-team-). Все, что вы видите здесь, было разработано в открытой форме благодаря интерактивной обратной связи и сотрудничеству со стороны более широкого сообщества. Он включает в себя серию видео, инфографику, текстовое чтение и практические задания, в которые вы можете погрузиться.

Не забудьте присоединиться к обсуждению на нашем открытом канале [**Slack**](https://osmooc.herokuapp.com/). Пожалуйста, представьтесь на # module5opensource и расскажите нам немного о том, кто вы, свое прошлое и как вы оказались здесь!

### Для кого этот модуль?

Этот модуль предназначен в первую очередь для специалистов в области вычислительной техники на уровне выпускников и студентов, а также для начинающих исследователей данных и любых других исследователей, использующих аналитический код или программное обеспечение. В современной исследовательской среде это касается практически любого, кто использует компьютер для своей работы.

> «Статья о вычислительном результате - реклама, а не стипендия. Фактическая стипендия - это полная программная среда, код и данные, которые дали результат ». - J. Buckheit и DL Donoho, 1995.

Программное обеспечение и технологии лежат в основе большинства современных исследований, которые в настоящее время почти неизбежно являются вычислительными в той или иной мере - поисковыми системами, платформами социальных сетей, аналитическим программным обеспечением и цифровыми публикациями. При этом существует все более возрастающая потребность в более совершенном программном обеспечении с открытым исходным кодом, которое сопровождается растущей готовностью исследователей открыто сотрудничать в разработке новых инструментов.

Сила Open Source заключается в том, что он снижает барьеры для сотрудничества и принятия, что позволяет быстрее распространять идеи и технологии. В этом модуле будут представлены необходимые инструменты, необходимые для превращения программного обеспечения в нечто, что может быть открыто доступно и повторно использовано другими.

<img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/open_research_software_open_source.png?raw=true" width="800" />

<p align="center"><i>Изображение Patrick Hochstenbach (CC0 1.0 Universal)</i></p>

  


### **Конкретные цели обучения для этого модуля**:

1. Узнать характеристики открытого программного обеспечения; понимать **этические, правовые, экономические и научные аргументы воздействия и против Open Source Software**и более глубокого понимания требований к качеству открытого кода.

2. Уметь превращать код, созданный для личного использования, в открытый код, доступный для других.

3. Используйте программное обеспечение (инструменты), которое использует открытый контент и поощряет более широкое сотрудничество.

  


## Что такое программное обеспечение с открытым исходным кодом <a name="What_OSS"></a>

Практически все современные рабочие процессы научных исследований опираются на целый ряд программных инструментов, работающих на разных наборах данных с разными параметрами и применяемых итеративно различными способами (наука о данных) или работающих на разных входных данных и использующих модели и методы для прогнозирования некоторого выходного состояния ( вычислительная наука). Программное обеспечение с открытым исходным кодом (OSS) - это компьютерное программное обеспечение, в котором полный исходный код доступен по специальной лицензии, которая позволяет другим пользователям получать доступ, просматривать, изменять и распространять этот код для любых целей. Поскольку OSS требует такую лицензию, по умолчанию она обычно остается бесплатной. Это явное лицензирование также отличает OSS от свободного программного обеспечения. Повторное использование OSS для анализа, моделирования и визуализации для исследований также обычно проще и более гибко по сравнению с проприетарным программным обеспечением. Часто, знаем ли мы это или нет, мы уже используем OSS как часть наших собственных исследовательских рабочих процессов.

OSS вписывается в более широкую схему Open Science, поскольку помогает сделать полную исследовательскую среду, включая программное обеспечение, которое дало результаты исследований, полностью доступными и многократно используемыми. Как таковой, он формирует необходимый компонент для лучших практик ([Jiménez et al., 2018](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Jim%C3%A9nez%20et%20al.%2C%202018.pdf)) и воспроизводимости и воспроизводимости исследований (как лично, так и другими), наряду с другими компонентами, такими как обмен данными ([Stoden, 2010](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Stodden%2C%202010.pdf))

В некоторых случаях совместное использование исходного кода может даже быть условным для принятия соответствующих исследовательских рукописей ([Shamir et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Shamir%20et%20al.%2C%202013.pdf)). Также считается, что это увеличивает влияние исследований ([Vandwalle, 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Vandewalle%2C%202012.pdf))

Некоторые из общих преимуществ для разработчиков включают в себя:

- Повышение лояльности разработчиков и расширение прав и возможностей;

- Снижение затрат на услуги и маркетинг;

- Усиление брендинга услуг и продуктов;

- Производство высококачественного программного обеспечения с меньшими затратами;

- Гибкость и быстрые инновации;

- Кастомизация и модульная интеграция;

- Повышенная надежность и независимость; а также

- На основе открытых стандартов, доступных каждому.

Таким образом, основными преимуществами для исследователей (пользователей) являются: **меньшие затраты**, **повышенная прозрачность**, **повышенная безопасность и стабильность**, **отсутствие привязки к поставщику с повышенным контролем пользователя**и **общее более высокое качество** Кроме того, совместное использование OSS позволяет исследователям получать кредит за их усилия, например, путем прямого цитирования программного обеспечения [(Smith et al., 2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf).

Обычно используются ОСС включает [Mozilla Firefox](https://www.mozilla.org/en-US/firefox/) Интернет - браузер и [LibreOffice](https://www.libreoffice.org/) полный офисный пакет. LibreOffice похож на популярный Microsoft Office, включая текстовый процессор, менеджер электронных таблиц и программное обеспечение для слайд-презентаций, но является полностью бесплатным и открытым исходным кодом.

Некоторые считают, что движение OSS представляет собой противодействие неолиберализму и приватизации посредством игнорирования нормативных актов и норм в области конструирования и повторного использования информации, а также потенциальной трансформации современного капитализма за счет обеспечения доступности программного обеспечения с минимальными усилиями. See [The free/open source software movement: Resistance or change?](https://doi.org/10.15448/1984-7289.2009.1.5569) by Panayiota Georgopoulou for more on this topic.

  


## Принципы открытого программного обеспечения <a name="Principles"></a>

[Инициатива Open Source](https://opensource.org/), один из пионеров ОСС, предлагает следующее : [определения](https://en.wikipedia.org/wiki/The_Open_Source_Definition#Definition):

*Не волнуйтесь, вам не нужно запоминать все это, но хорошо знать принципы, из которых исходит OSS.*

- **Бесплатное распространение**: Лицензия не должна ограничивать какие-либо стороны от продажи или передачи программного обеспечения как компонента совокупного распространения программного обеспечения, содержащего программы из нескольких различных источников. Лицензия не требует лицензионного платежа или других сборов за такую продажу.
    
    - **Исходный код**: программа должна включать исходный код и разрешать распространение в исходном коде, а также в скомпилированной форме. В тех случаях, когда какая-либо форма продукта не распространяется с исходным кодом, должны быть широко обнародованные средства получения исходного кода по разумной цене, предпочтительно не превышающей разумную стоимость, с бесплатной загрузкой через Интернет. Исходный код должен быть предпочтительной формой, в которой программист может изменить программу. Умышленно запутанный исходный код не допускается. Промежуточные формы, такие как выходные данные препроцессора или переводчика, не допускаются.
    
    - **Производные работы**: Лицензия должна разрешать модификации и производные работы, а также разрешать их распространение на тех же условиях, что и лицензия исходного программного обеспечения.
    
    - **Целостность исходного кода автора**Лицензия может ограничивать распространение исходного кода в измененной форме, только если лицензия допускает распространение «файлов исправлений» с исходным кодом с целью изменения программы во время сборки. Лицензия должна явно разрешать распространение программного обеспечения, созданного из измененного исходного кода. Лицензия может требовать, чтобы производные работы носили другое имя или номер версии от исходного программного обеспечения.
    
    - **Нет дискриминации в отношении лиц или групп**: Лицензия не должна быть дискриминационной по отношению к какому-либо лицу или группе лиц.
    
    - **Нет дискриминации по отношению к сферам деятельности**Лицензия не должна ограничивать использование программы в определенной области деятельности. Например, оно не может ограничивать использование программы в бизнесе или ее использование для генетических исследований.
    
    - **Распространение лицензии**Права, прилагаемые к программе, должны распространяться на всех, кому программа распространяется, без необходимости выполнения дополнительной лицензии этими сторонами.
    
    - **Лицензия не должна быть специфичной для продукта**Права, приложенные к программе, не должны зависеть от того, входит ли программа в конкретный дистрибутив программного обеспечения. Если программа извлекается из этого дистрибутива и используется или распространяется в соответствии с условиями лицензии на программу, все стороны, которым распространяется программа, должны иметь те же права, что и те, которые предоставляются вместе с оригинальным дистрибутивом программного обеспечения.
    
    - **Лицензия не должна ограничивать другое программное обеспечение**Лицензия не должна накладывать ограничения на другое программное обеспечение, которое распространяется вместе с лицензионным программным обеспечением. Например, лицензия не должна настаивать на том, чтобы все другие программы, распространяемые на том же носителе, были с открытым исходным кодом.
    
    - **Лицензия должна быть нейтральной в отношении технологии**Предоставление лицензии не может основываться ни на какой отдельной технологии или стиле интерфейса.

Теперь все это может быть немного сложным для запоминания. Однако его можно суммировать как *что делает программное обеспечение максимально пригодным для повторного использования в будущих работах и в то же время свободно доступным*.

  


## Контрольный список с открытым исходным кодом

Существует ряд существующих платформ и инструментов, которые поддерживают OSS и совместную работу. [Open Science Training Handbook](https://open-science-training-handbook.gitbook.io/book/) содержит контрольный список, который можно использовать для оценки «открытости» существующего исследовательского программного обеспечения на основе приведенного выше определения открытого источника:

- [] Доступно ли программное обеспечение для загрузки и установки?

- [] Может ли программное обеспечение быть легко установлено на разных платформах?

- [] Есть ли у программного обеспечения условия на использование?

- [] Доступен ли исходный код для проверки?

- [] Доступна ли полная история исходного кода для проверки через общедоступную историю версий?

- [] Правильно ли описаны зависимости программного обеспечения (аппаратного и программного обеспечения)? Эти зависимости требуют только разумно минимального количества усилий для получения и использования?

Проверьте, проверьте, проверьте, сделано! Simples.

  


## Сообщество Open Source и его управление <a name="OS_Community"></a>

There are two main camps within the free/libre and open source software (FLOSS) community: The **free software movement**, and the **open source software movement** (OSS). Оба имеют различные идеологии, основанные на свободах пользователей и практическом применении программного обеспечения. The term 'FLOSS' is used as a overaching neutral term to refer to both; libre being French and Spanish for 'free' in the context of freedom.

In a similar way that people active in the open science movement are heterogeneous in their assumptions and aims, different opinions exist in the FLOSS community as well. Recalling module 1, two of the schools of thought in open science were the *Pragmatic school* and the *Democratic school*. While the former is driven by the assumption that research could be more efficient if scientists worked together, the latter wants to set straight an unequal distribution of knowledge. They probably both end up sharing their research, but each with different intentions.

This is roughly comparable to the OSS and the free software movement: The latter evolved around 1983 to protect what they call the four essential freedoms of a program's user. These include the freedom to run, copy, distribute, study, change and improve a program. Software that respects these freedoms with an appropriate license is considered 'free'. The four freedoms are seen as vital for a society as a whole in the sense that they only enable sharing, cooperation and ultimately freedom in general. In this sense the free software movement is a social movement that creates an ethical imperative.

The open source software movement, which splintered off in 1998, focuses on the practical advantages and does not campaign for principles. It is concerned with developing high-quality software, for which everyone's ability to obtain, modify and contribute back the source code is considered highly beneficial.

Among multiple conclusions they arrive at, access to a program's source code is a shared one. Software thus may be considered *free*, *open source*, or both, according to agreed-on definitions by the Free Software Foundation ([FSF](https://www.gnu.org/philosophy/free-sw.html)) and the Open Source Initiative ([OSI](https://opensource.org/osd)). The FSF argues that free software is a subset of OSS, with only a [fraction](https://www.gnu.org/philosophy/free-open-overlap.html) being open source but nonfree.

Thus, highlighting a particular license status of software in use—open source or free—is mostly about different philosophies, not about software not having the other status as well. Each movement has its share of problems explaining their term: *free* means more than being gratis and *open source* means more than having access to the source code. The [FSF](https://www.gnu.org/philosophy/open-source-misses-the-point.html) and the European counterpart [FSFE](https://fsfe.org/documents/whyfs.html) provide more information on this topic.

### Для индивидуальных проектов

A typical open source project has the following types of formal roles:

- **Автор**: Это человек, который создал проект
- **Владелец**: лицо / лица, которые имеют административную собственность на организацию или хранилище 
- **Сопровождающие**Участники, ответственные за управление видением и управление организационными аспектами проекта. (Они также могут быть авторами или владельцами проекта.)
- **Участники**: Пользователь, который уже внес свой вклад в проект.
- **Участники сообщества**: Люди, которые используют проект. Они могут быть активными в разговорах, создавать новые проблемы или высказать свое мнение о будущих улучшениях проекта.

Typically, roles are made public through either the `README` file, a Contributors file, or a separate team page for the project.

  


## Существующие платформы и инструменты для программного обеспечения с открытым исходным кодом <a name="Platforms"></a>

Virtual environments and machines are becoming increasingly popular as high-powered research workflow enablers, and many of these are built upon OSS (e.g., operating systems, programming languages, and data processing frameworks). Popular services include [Google Cloud](https://cloud.google.com/compute/) and [Amazon Web Services](https://aws.amazon.com/), which also assist with database storage and content delivery, as well as computational power. [InsideDNA](https://insidedna.me/) is a computing platform for reproducible research in bioinformatics, genomics and the life sciences.

As mentioned [above](#What_OSS), LibreOffice provides an Open Source alternative to Microsoft Office. The two are almost completely compatible, just with different default file formats. For citation managers, [Zotero](https://www.zotero.org/) is the most popular Open Source alternative to proprietary platforms such as Mendeley or EndNote.

[Zotero](https://www.zotero.org/) uses the BibTeX (pronounced 'bib-tech') format, based on LaTeX (pronounced 'lay-tech'), and has browser plugins to make citation management simple. By integrating this with other software such as LibreOffice, it is now possible to have a fully Open Source research workflow in many cases.

### GitHub <a name="GitHub"></a>

> Знаете ли вы, что весь этот проект был построен как совместная работа сообщества в [GitHub](https://github.com/OpenScienceMOOC/)?

[GitHub](https://github.com/) is a popular hosting site for both software and non-software content (often called 'notebooks'), with added capabilities for version control, project management and tracking, and storage services. GitHub is built on top of the OSS [Git](https://git-scm.com/), which enables users to work remotely to maintain, share, and collaborate on research software and other non-software based projects.

Version control is essentially a process that takes snapshots of the files in a repository, and tracks modifications to them. It records when the changes were made, what they were, and who did them. If several people are working on one file at once, any overlapping changes are detected, and must be resolved prior to continuing. This provides a much more streamlined and automated process than manually saving and recording changes as projects develop. It also avoids the inevitable lists of confusing named file versions...

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/xkcd.png?raw=true" width="200" /></p>

<p align="center"><i>GitHub helps us to avoid, er, sub-optimal file naming conventions (source: XKCD)</i></p>

  


One of the more popular and useful functions of GitHub is the [issue tracker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/issues), which is used to organise OSS development. The above link takes you to the issue tracker for the development of this module! If you think there is something here that can improved, or you want to comment on, anyone can add or contribute to an issue there!

Other similar project hosting services include [BitBucket](https://bitbucket.org/), [GitLab](https://about.gitlab.com/), and [Launchpad](https://launchpad.net/). If the recent acquisition of GitHub by Microsoft is a bit off-putting to you, these are great alternatives.

However, we also know that GitHub can have quite a high learning curve. Which is why the first practical task for this MOOC will teach you how to set up your first GitHub project repository!

**[GO TO TASK 1: Building your first GitHub repository](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)**

  


## Программное обеспечение с открытым исходным кодом, используемое в исследованиях <a name="Research"></a>

Especially in scientific research, Open Source Software usage and development has become practically the norm. There's a number of reasons for this beyond those that apply to the general acceptance of OSS by, for example, consumers, industry, or government. Among these reasons are:

- Все чаще алгоритмы, внедряемые в программное обеспечение для анализа, составляют неотъемлемую часть методов, описанных в научных публикациях. Как таковой, он полностью расходится с тщательным экспертным обзором, если эти реализации алгоритма закрыты для посторонних.

- Научное сотрудничество чаще всего охватывает несколько учреждений и распределенных исследовательских сетей, где секретность и командная иерархия не поддерживаются таким образом, который «необходим» для разработки с закрытыми исходными кодами.

- Многие вычислительные анализы проводятся в виртуализированных средах (таких как институциональные, национальные или международные «облачные» инфраструктуры) и размещаются на многопользовательских серверах. Коммерческое программное обеспечение с закрытым исходным кодом часто запрещает такое использование.

- Развитие OSS часто зависит от добровольцев. Во времена бюджетных ограничений для научных исследований это явное преимущество.

For these and other reasons, Open Source tools are very commonly used in scientific research. This includes usage in fields where many researchers are amateur developers themselves and rely on tools such as [R](https://www.r-project.org/) for statistical analysis and scripting, which, in the last decade, has almost completely displaced commercial software for statistical analysis such as SPSS or JMP in a lot of fields. In fields such as bioinformatics, that involve a lot of file handling of the outputs of DNA sequencing platforms, general purpose scripting languages such as [Python](https://www.python.org/) and commonly used libraries built on top of it (such as [biopython](http://biopython.org)) have become a vital part of the toolkit of many researchers.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/python.png?raw=true" width="400" /></p>

<p align="center"><i>Python</i></p>

  


Tools such as R and Python are essentially software for writing software. Although programming is an increasingly common activity among researchers, of course not *every* scientist does this. One step away from programming is the chaining together of the inputs and outputs of various analysis tools in longer workflows. As an example from genomics, a very common workflow is to start out with high-throughput sequencing reads and then i) do basic quality control checks; ii) map the reads against a reference genome; iii) identify the points where the new data are at variance with the reference. These steps are routinely executed as a workflow where a different Open Source executable is run in a Linux command-line environment for each of the three steps. Although this is arguably not quite open source software development, it does involve the usage and production of open source artifacts (such as Linux shell scripts) for which the principles that we discuss in this module are applicable.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/r.png?raw=true" width="200" /></p>

<p align="center"><i>R</i></p>

  


Lastly, OSS is also used in scientific research for reasons that more closely mirror those that drive the adoption of OSS in wider society, namely that it is cheap. For example, individuals or organizations might decide to switch from Microsoft Office to LibreOffice for manuscript writing or spreadsheet processing because the latter is free (both as in [**'free beer'**](https://www.youtube.com/watch?v=dQw4w9WgXcQ) and 'free speech'). Likewise, the choice to switch from ArcGIS to [QGIS](https://www.qgis.org/en/site/) for the analysis of geographic information might be prompted simply by cost considerations.   


## Начало работы с OSS - FAQ <a name="FAQ"></a>

**I'm using X[e.g. Matlab,STATA,Excel] and I want to transition to something more open. What are the next steps?**

Even if you are using proprietary software, you can usually still share your source code/documents etc. *The best first step is sharing whatever you can*.

**Great! I can put them in my new github repo.**

If that's enough for you for now great! If not for most pieces of proprietary software there are Open Source equivalents. Have a go with one and see what you think.

| Закрыто                                                                                                 | открыто                                                                                                                                                           |
| ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Matlab                                                                                                  | Питон, Юлия                                                                                                                                                       |
| STATA / SPSS                                                                                            | р                                                                                                                                                                 |
| Майкрософт офис                                                                                         | LibreOffice                                                                                                                                                       |
| Mathematica                                                                                             | JupyterLab                                                                                                                                                        |
| Max/MSP                                                                                                 | PureData                                                                                                                                                          |
| Test out your new [Pull Request -PR-](https://help.github.com/articles/about-pull-requests/) Skills ... | ... by adding your own example [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md) |

**Cool! But if I make the switch will I be stuck: taking ages to learn a new tool/ without support /with buggy software.**

Good question! The answer is it depends. The best thing to do is find someone who's made the switch before and learn from their experience. Or just do a Google search! Some OSS is much better than their closed counterparts, some aren't, so it's worth choosing carefully.

## Создание хорошего программного обеспечения для повторного использования <a name="Reuse"></a>

The most likely person who might want to re-use your software in the future is...you! So while sharing is always better than not sharing, you can make your own life, and that of others, much easier through appropriate documentation. Documentation can include several things, such as including helpful comments and annotations in the code that help to explain why a particular action was performed, rather than what it is intended to achieve.

One of the most critical aspects of this is including an informative `README` file, that accompanies almost every OSS project, and some times even more than one. It can be a good practice to include one such file in every directory, that includes a list of files, a table of contents, and what the purpose of the directory is. The `README` file is typically just plain text or markdown (again, such as all of the ones for the MOOC!), and can include critical information for how to install and run software, previous dependencies and requirements, as well as tutorials or examples.

> **Знаете ли вы ...** Термин `README` иногда игриво приписывают известной сцене в «Приключениях Алисы в стране чудес» Льюиса Кэрролла, в которой Алиса сталкивается с волшебными жаворонками, помеченными надписями «Съешь меня» и «Выпей меня». Могучий.

The purpose here is to provide sufficient information to maximise the re-use and reproducibility of the computational environment, such that someone with no experience with the project can easily access and re-use the software ([Sandve et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)). By lowering the barriers to entry, you increase the chances of others being able to re-use your work, which is one of the ultimate goals of OSS ([Ince et al., 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)).

An extension of this that can help to make things even easier for future re-use is 'container' technology. Containers are like an ecosystem frozen in time, where the code, the data, any other dependencies, are all perfectly preserved, packaged and saved in the present functioning versions. This means that anyone in the future any one can come in and run the analyses again. As such, they are generally good for re-use, but this can come at the sacrifice of modification or understanding by others, as often a lot of details can be hidden within the source code and its dependencies. Common examples of container implementation in research include [Rocker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf) (a Docker container for the R language), [Binder](https://mybinder.readthedocs.io/en/latest/), and [Code Ocean](https://codeocean.com/).

**Sustainable software is good software.**

  


## 10 простых правил для воспроизводимых вычислительных исследований

The 10 simple rules for making computational research more reproducible, based on [Sandve et al., (2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF), are:

1. Для каждого результата следите за тем, как он был получен.
2. Избегайте ручных операций с данными.
3. Архивируйте точные версии всех используемых внешних программ.
4. Контроль версий всех пользовательских скриптов.
5. Запишите все промежуточные результаты, когда это возможно, в стандартизированных форматах.
6. Для анализа, который включает случайность, отметьте основные случайные семена.
7. Всегда храните необработанные данные за графиками.
8. Генерация результатов иерархического анализа, позволяющая проверять слои с возрастающей детализацией.
9. Соедините текстовые заявления с основными результатами.
10. Предоставить публичный доступ к сценариям, прогонам и результатам.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/simple_rules.png?raw=true" width="800" /></p>

<p align="center"><i>Infographic adapted from Sandve et al., (2013). Feel free to download this and print it out to keep handy during your research!</i></p>

  


If you follow these steps, along with the processes in [**Task 1**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [**Task 2**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), you should be fine!

  


## Лицензирование Open Source <a name="Licensing"></a>

An Open Source license is a type of license designed specifically for software and code that make it explicit what the legal conditions for sharing and re-use are. As mentioned [above](#What_OSS), the addition of a suitable license is what differentiates publicly shared software from OSS. For example, the widely used [MATLAB](https://www.mathworks.com/products/matlab.html) is proprietary software, and [Octave](https://www.gnu.org/software/octave/) is an openly licensed alternative programming language.

There are currently more than 1,400 unique Open Source licenses, a complexity born from the difficulty in understanding the differences between the legal implications across different license.

Some of the more common licenses include:

- [Berkeley Software Distribution ("BSD")](https://en.wikipedia.org/wiki/BSD_licenses),
- [Апач](https://www.apache.org/licenses/LICENSE-2.0),
- [стиле MIT (Массачусетский технологический институт)](https://opensource.org/licenses/MIT), или
- [Стандартная общественная лицензия GNU («GPL»)](https://www.gnu.org/licenses/gpl-3.0.en.html).

You don't need to know all the legal itty gritty behind all of these, but it is good to at least know what options are avaiilable to you.

There are two ways in which contributions to a project become licensed:

1. *Явно*, при этом индивидуальный вклад имеет четко обозначенную лицензию, независимую от основного проекта; или же
2. *Неявно*, согласно которому вклад подпадает под исходный лицензионный код основного проекта.

Thankfully, the process of selecting an Open Source license is relatively trivial, thanks to user-friendly tools such as [Choose A License](https://choosealicense.com/) or [Public License Selector](https://ufal.github.io/public-license-selector/). Each of these licenses allows other users to use, copy, distribute, and build upon your work, often while ensuring that the creators are appropriately recognised for their work. Here, the key is selecting an appropriate license for your work, depending on what you want, or do not want, others to do with it.

  


## Цитирование программного обеспечения <a name="Citation"></a>

Citations provide one of the most important interactions in scholarly research, forming the basis of our referencing and metrics systems. Typically, this is performed thanks to the assistance of a permanent unique identifier such as a [Digital Object Identifiers](https://en.wikipedia.org/wiki/Digital_object_identifier) (DOI). A DOI is a persistent identifier, implemented in the [Handle System](https://en.wikipedia.org/wiki/Handle_System), that meets a common standard, depending on the purpose, such as for identifying academic information. Such identification is critical for tracking the genealogy and provenance of research, for reproducibility, as well as for giving appropriate credit to those who have created the software. Importantly, software should be considered a legitimate output from scholarly research, and citation is becoming an increasingly common way to indicate that.

In 2016, [Smith et al., 2016](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) wrote a research paper about the principles of software citation as part of the FORCE11 Software Citation Working Group. In the same way that you would want to cite software that you have used as part of good research practices, it is important to make your research easily citable too. When citing any software used for your own research, you should include at minimum:

- Имя автора (ов),
- Название программного обеспечения,
- Номер версии и
- Уникальный идентификатор / локатор (DOI или URL).

The six principles of software citation by [Smith et al., (2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) are provided here:

- **Важность**: Программное обеспечение должно считаться законным и ценным продуктом исследований. Цитаты программного обеспечения должны иметь такое же значение в научных записях, как и цитаты других исследовательских продуктов, таких как публикации и данные; они должны быть включены в метаданные цитирующей работы, например, в список литературы в журнальной статье, и не должны быть пропущены или разделены. Программное обеспечение должно цитироваться на той же основе, что и любой другой исследовательский продукт, такой как статья или книга, то есть авторы должны ссылаться на соответствующий набор программных продуктов так же, как они ссылаются на соответствующий набор документов.

- **Кредит и указание авторства**Цитирование программного обеспечения должно облегчать предоставление ученым должного и нормативного юридического указания на всех участников программного обеспечения, признавая, что единый стиль или механизм присвоения могут быть неприменимы ко всему программному обеспечению.

- **Уникальная идентификация**Ссылка на программное обеспечение должна включать в себя метод идентификации, который является машинным, глобально уникальным, совместимым и распознается по крайней мере сообществом экспертов в соответствующей области, и предпочтительно исследователями из широкой общественности.

- **Постоянство**: Уникальные идентификаторы и метаданные, описывающие программное обеспечение и его расположение, должны сохраняться - даже после срока службы программного обеспечения, которое они описывают.

- **Доступность**Ссылки на программное обеспечение должны облегчать доступ к самому программному обеспечению и к связанным с ним метаданным, документации, данным и другим материалам, необходимым как для людей, так и для машин, для осознанного использования упомянутого программного обеспечения.

- **Специфика**: Цитирование программного обеспечения должно облегчать идентификацию и доступ к конкретной версии программного обеспечения, которая использовалась. Идентификация программного обеспечения должна быть настолько конкретной, насколько это необходимо, например, использовать номера версий, номера редакций или варианты, такие как платформы.

Note: For instructions on 'how to make your software citable' see the section [**Using GitHub and Zenodo**](#GitHub_Zenodo) below and [**Task 2: Linking GitHub and Zenodo**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md).

  


## Использование GitHub и Zenodo <a name="GitHub_Zenodo"></a>

[GitHub](#GitHub) is a popular tool for project management, content storage, and version control. Note that GitHub itself is not OSS. However, Git, the tool which it is based on, is. Git is designed to help manage the source code files, and the updates to them, for a software-related project. However, it can also be extended to other non-software projects; for example, this [MOOC](https://github.com/OpenScienceMOOC/)!

However, getting research onto GitHub is just the first step. It is equally important to make it persistent and re-usable, which is why having a Digital Object Identifier (DOI) associated with it can be useful. The simplest way to do this is through a service called [Zenodo](https://zenodo.org/), which is a free and open source multi-disciplinary repository created by OpenAIRE and CERN, and can be used to assign a DOI to individual GitHub repositories. There is a [GitHub Guide](https://guides.github.com/activities/citable-code/) that explains the details, which involve linking GitHub repositories directly through to Zenodo so that when developers create formal releases for their software, Zenodo creates and archives a that version of the software.

There's nothing special about using Zenodo for creating DOIs, other than its **free of cost**; other general repositories can also be used, such as [DataCite DOI Fabrica](https://doi.datacite.org/), or your own institutional repositories such as [Caltech's](https://www.library.caltech.edu/news/enhanced-software-preservation-now-available-caltechdata).

A lot of researchers might typically be afraid of sharing code which is incomplete, buggy, or imperfect. However, in the OSS community, such a practice of sharing 'raw' code is fairly commonplace. Sharing code openly enables others to re-use and improve it, as well as to engage in a deeper way with any research associated with it. This is one of the fundamental aspects of peer-collaboration, perhaps best exemplified by the traditional process of research manuscript peer review.

Task 2 will guide you through the process of linking a GitHub repository to Zenodo for archiving.

> **Знаете ли вы ...** Весь контент, созданный для этого MOOC, доступен как часть сообщества в [Zenodo](https://zenodo.org/communities/open-science-mooc/)?

**[GO TO TASK 2: Linking GitHub and Zenodo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)**

  


## Сотрудничество и участие через открытый исходный код <a name="Collaborating"></a>

Often, OSS is developed in a public, decentralised, collaborative manner between multiple contributors. The purpose of this is to enhance the diversity and scope of a project and its design, in order to become more beneficial and sustainable. Such an approach was famously likened to a 'bazaar' model by Eric Raymond, an early OSS proponent. One of the major guiding principles of this is that of **peer production**, which relies on self-organised communities to regulate the development of content, co-ordinated towards a shared goal or outcome.

OSS projects rely heavily on volunteer collaboration, which often entails a constant flux of newcomers in order to become productive and sustainable ([Steinmacher et al., 2014](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)). Creating the right social atmosphere for a project, and a welcoming engagement environment, are often critical to successful collaboraitons in OSS.

  


## Куда пойти отсюда <a name="Future_OSS"></a>

Hopefully now you have come to see the importance of software as a cornerstone of modern science, and the importance that OSS plays in this.

The **learning outcomes** from this should be:

1. Теперь вы сможете определить характеристики OSS и некоторые этические, правовые, экономические и исследовательские аргументы за и против.

2. Основываясь на стандартах сообщества, вы теперь сможете описать требования к качеству совместного использования и повторного использования открытого кода.

3. Теперь вы сможете использовать ряд исследовательских инструментов, использующих OSS.

4. Теперь вы сможете преобразовывать код, предназначенный для их личного использования, в код, который доступен и может использоваться другими пользователями.

5. Разработчики программного обеспечения смогут сделать свое программное обеспечение доступным, а пользователи программного обеспечения будут знать, как цитировать используемое ими программное обеспечение.

  


**BONUS TASK**

If you have completed [Task 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [Task 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), we also have a **BONUS TASK** for you, if you want to take your skills a step further. [Task 3](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md) will take you a step deeper into integrating Git into a typical research workflow by showing you how to integrate it with R Studio. It is recommended that you have completed the first 2 tasks before proceeding with this one.

However, your Open Source journey does not stop here! This was just the beginning, and there are some incredible resources out there if you would like to do or learn more:

- Если вы чувствуете , особенно вдохновленный этим, вы можете одобрить [Science Code Манифеста](http://sciencecodemanifesto.org/), которая основана на пяти принципах кода, авторское право, цитаты, кредита и курирование.

- Для запуска и разработки собственного проекта программа [Open Source Guides](https://opensource.guide/) предлагает ряд практических руководств и навыков, которые помогут запустить и продвинуть ваши проекты OSS.

- Для подробного ознакомления с научными рабочими процессами на основе OSS руководство « [Open Science, Open Data, Open Source](https://pfern.github.io/OSODOS/gitbook/) » Педро Л. Фернандес и Рутгер А. Вос является одним из лучших онлайн-ресурсов.

- Более формализованный журнал центры существуют также для программного обеспечения на основе статей, в том числе [Журнал открытых исследований программного обеспечения](https://openresearchsoftware.metajnl.com/) и [Журнал Open Source Software](https://joss.theoj.org/). Список таких мест также [доступно](https://www.software.ac.uk/which-journals-should-i-publish-my-software).

- [PLOS Open Source Toolkit](https://channels.plos.org/open-source-toolkit) предоставляет глобальный форум для исследований и приложений аппаратного и программного обеспечения с открытым исходным кодом.

- The [NumFOCUS](http://www.numfocus.org) - некоммерческая организация, которая поддерживает и продвигает инновационное научное программное обеспечение с открытым исходным кодом мирового класса. Некоторые из проектов, которые они спонсируют, включают:
    
    - [IPython](http://ipython.org) и [инициативы Jupyter Notebook](https://jupyter.org).
    
    - [rOpenSci](http://ropensci.org), которая поддерживает открытую статистическую среду R для прозрачных и воспроизводимых исследований.
    
    - Чтобы получить больше практического опыта работы с OSS, сообщество [Software Carpentry](https://software-carpentry.org/) проводит регулярные семинары для улучшения навыков компьютерных вычислений ([Wilson et al., 2017](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Wilson%20et%20al.%2C%202017.pdf)).

  


### дальнейшее чтение <a name="Reading"></a>

*These references here are just the beginning. They include some of the most useful general overviews of the Open Source landscape in research. However, if you want to be find something more specific to your own research field, then that path is there for you to explore!*

- Будущее исследований в области разработки свободного / открытого программного обеспечения [(Scacchi, 2010)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Scacchi%2C%202010.pdf).

- Научный метод на практике: воспроизводимость в вычислительных науках [(Stoden, 2010)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Stodden%2C%202010.pdf).

- Случай для открытых компьютерных программ [(Ince et al., 2012)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf).

- Текущие проблемы и направление исследований по открытому исходному коду программного обеспечения сообщество [(Martinez-Торрес и Диас-Fernandez, 2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Martinez-Torres%20and%20Diaz-Fernandez%2C%202013.pdf).

- Десять простых правил для воспроизводимых вычислительных исследований [(Sandve et al., 2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF).

- Систематический обзор литературы о барьерах, с которыми сталкиваются новички в проектах программного обеспечения с открытым исходным кодом [(Steinmacher et al., 2014)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf).

- Обмен знаниями в сообществах программного обеспечения с открытым исходным кодом: мотивация и управление [(Iskoujina and Roberts, 2015)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Iskoujina%20and%20Roberts%2C%202015.pdf).

- Принципы цитирования программного обеспечения [(Smith et al., 2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf).

- Введение в Rocker: контейнеры Docker для R [(Boettiger and Eddelbuettel, 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf).

- Достаточно хорошие практики в научных вычислениях [(Wilson et al., 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Wilson%20et%20al.%2C%202017.pdf).

- Четыре простых рекомендации для поощрения лучших практик в области программного обеспечения для исследований [(Jiménez et al., 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Jim%C3%A9nez%20et%20al.%2C%202018.pdf).

  


### Команда разработчиков <a name="Development_team"></a>

- [Алекс Морли](https://twitter.com/alex__morley), Open Sourceror, Оксфордский университет, Великобритания.
- [Кевин Моерман](https://twitter.com/KMMoerman), Open Sourceror, MIT, США.
- [Таня Аллард](https://twitter.com/ixek), Open Sourceress, Data Enchantress, Университет Лидса, Великобритания.
- [Саймон Уортингтон](https://twitter.com/mrchristian99), Книга Освободителя, TIB, Германия.
- [Паола Масуццо](https://twitter.com/pcmasuzzo), Бэтмен с открытым исходным кодом, Италия.
- [Ivo Grigorov](https://twitter.com/OAforClimate), Open Source Robin, Дания.
- [Rutger Vos](https://twitter.com/rvosa), Open Sourceror, Центр биоразнообразия Naturalis, Нидерланды.
- [Julien Colomb](https://twitter.com/j_colomb), Open Ninja, Берлин.
- [Джон Теннант](https://twitter.com/protohedgehog), Динозавр Шепот.

**Know a way this content can be improved?**

Time to take your new GitHub skills for a test-run! All content development primarily happens [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md). If you have a suggested improvement to the content, layout, or anything else, you can make it and then it will automatically become part of the MOOC content after verification from a moderator!

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)