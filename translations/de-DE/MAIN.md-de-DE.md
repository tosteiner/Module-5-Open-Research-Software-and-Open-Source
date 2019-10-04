---
output:
  html_document: Standard
  pdf_document: Standard
---

# Modul 5: Open Research Software und Open Source

## Inhaltsverzeichnis

- [Einführung](#Introduction)
- [Was ist Open Source Software?](#What_OSS)
- [Prinzipien von Open Source Software](#Principles)
- [The Open Source community and its governance](#OS_Community)
- [Bestehende Plattformen und Tools für Open Source Software](#Platforms)
- [Open Source Software für Forschungszwecke](#Research)
- [Erste Schritte mit OSS - FAQ](#FAQ)
- [Gute Software zur Wiederverwendung machen](#Reuse)
- [Open Source Lizenzierung](#Licensing)
- [Software-Zitat](#Citation)
- [Mit GitHub und Zenodo](#GitHub_Zenodo)
- [Zusammenarbeit durch Open Source](#Collaborating)
- [Wohin soll es von hier aus gehen?](#Future_OSS)

**BITTE BEACHTEN SIE** dass eine Audioversion davon über [Soundcloud](https://soundcloud.com/open-science-mooc/module-5-open-source-and-open-research-software) und [YouTube](https://www.youtube.com/watch?v=BHrOEmKk5zM) zum Herunterladen verfügbar ist.

## Einführung <a name="Introduction"></a>

Willkommen zu **Modul 5** des Open Science MOOC: **Open Research Software und Open Source**.

Dieses Modul wurde [in the open](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source) in Zusammenarbeit mit einem internationalen Team von [Open Source-Afficianados](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/README.md#development-team-). Alles, was Sie hier sehen, wurde offen durch interaktives Feedback und die Zusammenarbeit mit der breiteren Community entwickelt. Es umfasst eine Reihe von Videos, Infografiken, textbasiertes Lesen und praktische Aufgaben, in die Sie sich hineinversetzen können.

Vergiss nicht, dass du in unserem offenen [**Slack Channel**](https://osmooc.herokuapp.com/)mitdiskutieren kannst. Bitte stellen Sie sich unter # module5opensource vor und erzählen Sie uns, wer Sie sind, welchen Hintergrund Sie haben und wie Sie hier gelandet sind!

### Für wen ist dieses Modul?

Dieses Modul richtet sich in erster Linie an Computerforscher mit und ohne Hochschulabschluss sowie angehende Datenwissenschaftler und andere Forscher, die analytischen Code oder Software verwenden. In einer modernen Forschungsumgebung sind damit so ziemlich alle abgedeckt, die einen Computer für ihre Arbeit verwenden.

> "Ein Artikel über das Rechenergebnis ist Werbung, kein Stipendium. Das eigentliche Stipendium ist die vollständige Softwareumgebung, Code und Daten, die das Ergebnis hervorgebracht haben. "- J. Buckheit und DL Donoho, 1995.

Software und Technologie untermauern einen Großteil der modernen Forschung, die heutzutage auf die eine oder andere Weise fast unweigerlich rechenintensiv ist - Suchmaschinen, Plattformen für soziale Netzwerke, Analysesoftware und digitales Publishing. Mit dieser Tatsache steigt die Nachfrage nach anspruchsvollerer Open Source-Software, verbunden mit der zunehmenden Bereitschaft der Forscher, offen an neuen Tools zusammenzuarbeiten.

Die Stärke von Open Source besteht darin, dass die Hindernisse für die Zusammenarbeit und Akzeptanz gesenkt werden, sodass sich Ideen und Technologien schneller verbreiten können. In diesem Modul werden die erforderlichen Tools vorgestellt, um Software in etwas zu verwandeln, auf das offen zugegriffen und von anderen wiederverwendet werden kann.

<img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/open_research_software_open_source.png?raw=true" width="800" />

<p align="center"><i>Bild von Patrick Hochstenbach (CC0 1.0 Universal)</i></p>

  


### **Spezifische Lernziele für dieses Modul**:

1. Lernen Sie die Eigenschaften offener Software kennen. verstehen , die **ethischen, rechtlichen, wirtschaftlichen und Forschung Auswirkungen Argumente für und gegen Open Source Software**, und weiter die Qualitätsanforderungen der offenen Code verstehen.

2. Sie können Code, der für den persönlichen Gebrauch erstellt wurde, in offenen Code umwandeln, auf den andere zugreifen können.

3. Verwenden Sie Software (Tools), die offene Inhalte verwendet und eine breitere Zusammenarbeit fördert.

  


## Was ist Open Source Software? <a name="What_OSS"></a>

Nahezu alle modernen wissenschaftlichen Forschungsabläufe basieren auf einer Reihe von Softwaretools, die entweder auf unterschiedlichen Datensätzen mit unterschiedlichen Parametern und iterativ auf verschiedene Arten (Data Science) angewendet werden oder auf unterschiedlichen Eingaben und unter Verwendung von Modellen und Methoden zur Vorhersage eines bestimmten Ausgabezustands ( Computerwissenschaft). Open Source Software (OSS) ist eine Computersoftware, in der der vollständige Quellcode unter einer bestimmten Lizenz verfügbar ist, die es anderen Benutzern ermöglicht, auf diesen Code für beliebige Zwecke zuzugreifen, ihn anzuzeigen, zu ändern und weiterzugeben. Da für OSS eine solche Lizenz erforderlich ist, ist diese in der Regel weiterhin kostenlos. Diese explizite Lizenzierung unterscheidet OSS auch von freier Software. Die Wiederverwendung von OSS zur Analyse, Simulation und Visualisierung für Forschungszwecke ist im Vergleich zu proprietärer Software in der Regel einfacher und flexibler. Unabhängig davon, ob wir es wissen oder nicht, verwenden wir OSS häufig bereits als Teil unserer eigenen Forschungsabläufe.

OSS fügt sich in das umfassendere Schema von Open Science ein, da es dazu beiträgt, die gesamte Forschungsumgebung, einschließlich der Software, die die Forschungsergebnisse erstellt hat, vollständig zugänglich und wiederverwendbar zu machen. Als solches bildet es eine notwendige Komponente für die Best Practices ([Jiménez et al., 2018](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Jim%C3%A9nez%20et%20al.%2C%202018.pdf)) und die Wiederholbarkeit und Reproduzierbarkeit der Forschung (sowohl persönlich als auch durch andere) sowie für andere Komponenten wie den Datenaustausch ([Stodden, 2010)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Stodden%2C%202010.pdf)).

In einigen Fällen kann die Weitergabe von Quellcode sogar von der Akzeptanz der zugehörigen Forschungsmanuskripte abhängig gemacht werden ([Shamir et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Shamir%20et%20al.%2C%202013.pdf)). Es wird auch allgemein angenommen, dass die Auswirkungen auf die Forschung zunehmen ([Vandwalle, 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Vandewalle%2C%202012.pdf)).

Einige der allgemeinen Vorteile für Entwickler sind:

- Erhöhte Entwicklerloyalität und -ermächtigung;

- Geringere Kosten für Dienstleistungen und Marketing;

- Verstärktes Branding von Dienstleistungen und Produkten;

- Produktion hochwertiger Software zu geringeren Kosten;

- Flexibilität und schnelle Innovation;

- Anpassung und modulare Integration;

- Erhöhte Zuverlässigkeit und Unabhängigkeit; und

- Basierend auf offenen Standards, die für alle verfügbar sind.

Die Hauptvorteile für Forscher (Benutzer) sind daher: **geringere Kosten**, **erhöhte Transparenz**, **erhöhte Sicherheit und Stabilität**, **kein "Einschließen" des Anbieters mit erhöhter Benutzerkontrolle**und **insgesamt höhere Qualität**. Durch die gemeinsame Nutzung von OSS können Forscher ihre Bemühungen honorieren, beispielsweise durch direktes Zitieren von Software [(Smith et al., 2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf).

Zu den häufig verwendeten OSS gehören der Internetbrowser [Mozilla Firefox](https://www.mozilla.org/en-US/firefox/) und die vollständige Office-Suite [LibreOffice](https://www.libreoffice.org/). LibreOffice ähnelt dem beliebten Microsoft Office, einschließlich eines Textverarbeitungsprogramms, eines Tabellenkalkulations-Managers und einer Folienpräsentationssoftware, ist jedoch völlig kostenlos und Open Source.

Einige sehen in der OSS-Bewegung eine Gegenbewegung zu Neoliberalismus und Privatisierung, die sich gegen Vorschriften und Normen bei der Konstruktion und Wiederverwendung von Informationen richtet, und eine potenzielle Transformation des modernen Kapitalismus durch die Bereitstellung von Software in Hülle und Fülle mit minimalem Aufwand. See [The free/open source software movement: Resistance or change?](https://doi.org/10.15448/1984-7289.2009.1.5569) by Panayiota Georgopoulou for more on this topic.

  


## Prinzipien von Open Source Software <a name="Principles"></a>

Die [Open Source Initiative](https://opensource.org/), einer der Pioniere von OSS, bietet die folgende [Definition](https://en.wikipedia.org/wiki/The_Open_Source_Definition#Definition):

*Keine Sorge, Sie müssen sich das alles nicht merken, aber es ist gut, die Prinzipien zu kennen, von denen OSS kommt.*

- **Kostenlose Weiterverteilung**: Die Lizenz darf keine Partei daran hindern, die Software als Bestandteil einer aggregierten Softwareverteilung zu verkaufen oder weiterzugeben, die Programme aus verschiedenen Quellen enthält. Für diesen Verkauf ist für die Lizenz keine Lizenzgebühr oder sonstige Gebühr erforderlich.
    
    - **Quellcode**: Das Programm muss Quellcode enthalten und die Verteilung im Quellcode sowie in kompilierter Form ermöglichen. Wenn eine Form eines Produkts nicht mit Quellcode vertrieben wird, muss es ein gut bekanntes Mittel geben, um den Quellcode für nicht mehr als einen angemessenen Vervielfältigungspreis zu erhalten, vorzugsweise zum kostenfreien Herunterladen über das Internet. Der Quellcode muss die bevorzugte Form sein, in der ein Programmierer das Programm ändern würde. Absichtlich verschleierter Quellcode ist nicht erlaubt. Zwischenformulare wie die Ausgabe eines Präprozessors oder Übersetzers sind nicht zulässig.
    
    - **Abgeleitete Werke**: Die Lizenz muss Änderungen und abgeleitete Werke zulassen und die Weitergabe unter denselben Bedingungen wie die Lizenz der Originalsoftware zulassen.
    
    - **Integrität des Quellcodes des Autors**: Die Lizenz darf die Weitergabe von Quellcode in geänderter Form nur einschränken, wenn die Lizenz die Weitergabe von "Patch-Dateien" mit dem Quellcode zum Zweck der Änderung des Programms zum Zeitpunkt der Erstellung zulässt. Die Lizenz muss die Weitergabe von Software, die aus geändertem Quellcode erstellt wurde, ausdrücklich gestatten. Die Lizenz erfordert möglicherweise abgeleitete Werke, die einen anderen Namen oder eine andere Versionsnummer als die ursprüngliche Software tragen.
    
    - **Keine Diskriminierung von Personen oder Gruppen**: Die Lizenz darf keine Person oder Personengruppe diskriminieren.
    
    - **Keine Diskriminierung von Handlungsfeldern**: Die Lizenz darf niemanden daran hindern, das Programm in einem bestimmten Handlungsfeld zu nutzen. Beispielsweise darf es das Programm nicht daran hindern, in einem Unternehmen oder für die genetische Forschung verwendet zu werden.
    
    - **Verteilung der Lizenz**: Die mit dem Programm verbundenen Rechte müssen für alle gelten, an die das Programm weitergegeben wird, ohne dass diese Parteien eine zusätzliche Lizenz ausführen müssen.
    
    - **Lizenz darf nicht produktspezifisch sein**: Die mit dem Programm verbundenen Rechte dürfen nicht davon abhängen, ob das Programm Teil einer bestimmten Softwareverteilung ist. Wenn das Programm aus dieser Distribution extrahiert und im Rahmen der Lizenzbedingungen des Programms verwendet oder verbreitet wird, sollten alle Parteien, an die das Programm weitergegeben wird, die gleichen Rechte haben, die im Zusammenhang mit der ursprünglichen Softwareverteilung gewährt werden.
    
    - **Lizenz darf andere Software nicht einschränken**: Die Lizenz darf keine Einschränkungen für andere Software enthalten, die zusammen mit der lizenzierten Software vertrieben wird. Beispielsweise darf die Lizenz nicht darauf bestehen, dass alle anderen auf demselben Medium verteilten Programme Open-Source-Software sein müssen.
    
    - **Lizenz muss technologieneutral sein.**: Die Bereitstellung der Lizenz darf nicht auf einer bestimmten Technologie oder einem bestimmten Schnittstellentyp beruhen.

Nun, das alles könnte ein wenig kompliziert sein, um sich zu erinnern. Es kann jedoch als *wodurch die Software für zukünftige Arbeiten so weit wie möglich wiederverwendbar wird und gleichzeitig frei verfügbar ist*.

  


## Eine Open Source Checkliste

Es gibt eine Reihe vorhandener Plattformen und Tools, die OSS und die Zusammenarbeit unterstützen. Das [Open Science Training Handbook](https://open-science-training-handbook.gitbook.io/book/) enthält eine Checkliste zur Bewertung der Offenheit vorhandener Forschungssoftware auf der Grundlage der obigen Open Source-Definition:

- [] Ist die Software zum Herunterladen und Installieren verfügbar?

- [] Kann die Software problemlos auf verschiedenen Plattformen installiert werden?

- [] Hat die Software Nutzungsbedingungen?

- [] Steht der Quellcode zur Einsicht zur Verfügung?

- [] Ist der vollständige Verlauf des Quellcodes über einen öffentlich zugänglichen Versionsverlauf zur Einsicht verfügbar?

- [] Sind die Abhängigkeiten der Software (Hardware und Software) richtig beschrieben? Benötigen diese Abhängigkeiten nur einen relativ geringen Aufwand, um sie zu erhalten und zu verwenden?

Überprüfen, überprüfen, überprüfen, fertig! Simples.

  


## Die Open Source Community und ihre Governance <a name="OS_Community"></a>

There are two main camps within the free/libre and open source software (FLOSS) community: The **free software movement**, and the **open source software movement** (OSS). Beide haben unterschiedliche Ideologien, die auf den Benutzerfreiheiten und den praktischen Anwendungen von Software beruhen. The term 'FLOSS' is used as a overaching neutral term to refer to both; libre being French and Spanish for 'free' in the context of freedom.

In a similar way that people active in the open science movement are heterogeneous in their assumptions and aims, different opinions exist in the FLOSS community as well. Recalling module 1, two of the schools of thought in open science were the *Pragmatic school* and the *Democratic school*. While the former is driven by the assumption that research could be more efficient if scientists worked together, the latter wants to set straight an unequal distribution of knowledge. They probably both end up sharing their research, but each with different intentions.

This is roughly comparable to the OSS and the free software movement: The latter evolved around 1983 to protect what they call the four essential freedoms of a program's user. These include the freedom to run, copy, distribute, study, change and improve a program. Software that respects these freedoms with an appropriate license is considered 'free'. The four freedoms are seen as vital for a society as a whole in the sense that they only enable sharing, cooperation and ultimately freedom in general. In this sense the free software movement is a social movement that creates an ethical imperative.

The open source software movement, which splintered off in 1998, focuses on the practical advantages and does not campaign for principles. It is concerned with developing high-quality software, for which everyone's ability to obtain, modify and contribute back the source code is considered highly beneficial.

Among multiple conclusions they arrive at, access to a program's source code is a shared one. Software thus may be considered *free*, *open source*, or both, according to agreed-on definitions by the Free Software Foundation ([FSF](https://www.gnu.org/philosophy/free-sw.html)) and the Open Source Initiative ([OSI](https://opensource.org/osd)). The FSF argues that free software is a subset of OSS, with only a [fraction](https://www.gnu.org/philosophy/free-open-overlap.html) being open source but nonfree.

Thus, highlighting a particular license status of software in use—open source or free—is mostly about different philosophies, not about software not having the other status as well. Each movement has its share of problems explaining their term: *free* means more than being gratis and *open source* means more than having access to the source code. The [FSF](https://www.gnu.org/philosophy/open-source-misses-the-point.html) and the European counterpart [FSFE](https://fsfe.org/documents/whyfs.html) provide more information on this topic.

### Für einzelne Projekte

A typical open source project has the following types of formal roles:

- **Autor**: Es ist die Person, die das Projekt erstellt hat
- **Eigentümer**: Die Person (en), die über Administratorrechte für die Organisation oder das Repository verfügt 
- **Betreuer**: Mitwirkende, die für die Umsetzung der Vision und das Management der organisatorischen Aspekte des Projekts verantwortlich sind. (Sie können auch Autoren oder Eigentümer des Projekts sein.)
- **Mitwirkende**: Der Benutzer, der bereits zu dem Projekt beigetragen hat.
- **Community-Mitglieder**: Personen, die das Projekt nutzen. Sie können aktiv an Gesprächen teilnehmen, neue Themen erstellen oder ihre Meinung zu zukünftigen Projektverbesserungen äußern.

Typically, roles are made public through either the `README` file, a Contributors file, or a separate team page for the project.

  


## Bestehende Plattformen und Tools für Open Source Software <a name="Platforms"></a>

Virtual environments and machines are becoming increasingly popular as high-powered research workflow enablers, and many of these are built upon OSS (e.g., operating systems, programming languages, and data processing frameworks). Popular services include [Google Cloud](https://cloud.google.com/compute/) and [Amazon Web Services](https://aws.amazon.com/), which also assist with database storage and content delivery, as well as computational power. [InsideDNA](https://insidedna.me/) is a computing platform for reproducible research in bioinformatics, genomics and the life sciences.

As mentioned [above](#What_OSS), LibreOffice provides an Open Source alternative to Microsoft Office. The two are almost completely compatible, just with different default file formats. For citation managers, [Zotero](https://www.zotero.org/) is the most popular Open Source alternative to proprietary platforms such as Mendeley or EndNote.

[Zotero](https://www.zotero.org/) uses the BibTeX (pronounced 'bib-tech') format, based on LaTeX (pronounced 'lay-tech'), and has browser plugins to make citation management simple. By integrating this with other software such as LibreOffice, it is now possible to have a fully Open Source research workflow in many cases.

### GitHub <a name="GitHub"></a>

> Wussten Sie, dass dieses gesamte Projekt als offene und kollaborative Community in [GitHub](https://github.com/OpenScienceMOOC/)?

[GitHub](https://github.com/) is a popular hosting site for both software and non-software content (often called 'notebooks'), with added capabilities for version control, project management and tracking, and storage services. GitHub is built on top of the OSS [Git](https://git-scm.com/), which enables users to work remotely to maintain, share, and collaborate on research software and other non-software based projects.

Version control is essentially a process that takes snapshots of the files in a repository, and tracks modifications to them. It records when the changes were made, what they were, and who did them. If several people are working on one file at once, any overlapping changes are detected, and must be resolved prior to continuing. This provides a much more streamlined and automated process than manually saving and recording changes as projects develop. It also avoids the inevitable lists of confusing named file versions...

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/xkcd.png?raw=true" width="200" /></p>

<p align="center"><i>GitHub helps us to avoid, er, sub-optimal file naming conventions (source: XKCD)</i></p>

  


One of the more popular and useful functions of GitHub is the [issue tracker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/issues), which is used to organise OSS development. The above link takes you to the issue tracker for the development of this module! If you think there is something here that can improved, or you want to comment on, anyone can add or contribute to an issue there!

Other similar project hosting services include [BitBucket](https://bitbucket.org/), [GitLab](https://about.gitlab.com/), and [Launchpad](https://launchpad.net/). If the recent acquisition of GitHub by Microsoft is a bit off-putting to you, these are great alternatives.

However, we also know that GitHub can have quite a high learning curve. Which is why the first practical task for this MOOC will teach you how to set up your first GitHub project repository!

**[GO TO TASK 1: Building your first GitHub repository](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)**

  


## Open Source Software für Forschungszwecke <a name="Research"></a>

Especially in scientific research, Open Source Software usage and development has become practically the norm. There's a number of reasons for this beyond those that apply to the general acceptance of OSS by, for example, consumers, industry, or government. Among these reasons are:

- Zunehmend sind in Analysesoftware implementierte Algorithmen ein wesentlicher Bestandteil der in wissenschaftlichen Veröffentlichungen beschriebenen Methoden. Insofern widerspricht es einem strengen Peer Review, wenn diese Algorithmusimplementierungen für Außenstehende nicht zugänglich sind.

- Die wissenschaftliche Zusammenarbeit erstreckt sich häufig über mehrere Institutionen und verteilte Forschungsnetzwerke, in denen Geheimhaltung und Befehlshierarchie nicht in einer Weise aufrechterhalten werden, die für die Entwicklung geschlossener Quellen "notwendig" ist.

- Viele Computeranalysen werden in virtualisierten Umgebungen (z. B. institutionellen, nationalen oder internationalen Cloud-Infrastrukturen) ausgeführt und auf Mehrbenutzerservern gehostet. Kommerzielle Closed-Source-Software lässt eine solche Verwendung häufig nicht zu.

- Die OSS-Entwicklung beruht häufig auf Freiwilligen. In Zeiten knapper Haushaltsmittel für die wissenschaftliche Forschung ist dies ein klarer Vorteil.

For these and other reasons, Open Source tools are very commonly used in scientific research. This includes usage in fields where many researchers are amateur developers themselves and rely on tools such as [R](https://www.r-project.org/) for statistical analysis and scripting, which, in the last decade, has almost completely displaced commercial software for statistical analysis such as SPSS or JMP in a lot of fields. In fields such as bioinformatics, that involve a lot of file handling of the outputs of DNA sequencing platforms, general purpose scripting languages such as [Python](https://www.python.org/) and commonly used libraries built on top of it (such as [biopython](http://biopython.org)) have become a vital part of the toolkit of many researchers.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/python.png?raw=true" width="400" /></p>

<p align="center"><i>Python</i></p>

  


Tools such as R and Python are essentially software for writing software. Although programming is an increasingly common activity among researchers, of course not *every* scientist does this. One step away from programming is the chaining together of the inputs and outputs of various analysis tools in longer workflows. As an example from genomics, a very common workflow is to start out with high-throughput sequencing reads and then i) do basic quality control checks; ii) map the reads against a reference genome; iii) identify the points where the new data are at variance with the reference. These steps are routinely executed as a workflow where a different Open Source executable is run in a Linux command-line environment for each of the three steps. Although this is arguably not quite open source software development, it does involve the usage and production of open source artifacts (such as Linux shell scripts) for which the principles that we discuss in this module are applicable.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/r.png?raw=true" width="200" /></p>

<p align="center"><i>R</i></p>

  


Lastly, OSS is also used in scientific research for reasons that more closely mirror those that drive the adoption of OSS in wider society, namely that it is cheap. For example, individuals or organizations might decide to switch from Microsoft Office to LibreOffice for manuscript writing or spreadsheet processing because the latter is free (both as in [**'free beer'**](https://www.youtube.com/watch?v=dQw4w9WgXcQ) and 'free speech'). Likewise, the choice to switch from ArcGIS to [QGIS](https://www.qgis.org/en/site/) for the analysis of geographic information might be prompted simply by cost considerations.   


## Erste Schritte mit OSS - FAQ <a name="FAQ"></a>

**I'm using X[e.g. Matlab,STATA,Excel] and I want to transition to something more open. What are the next steps?**

Even if you are using proprietary software, you can usually still share your source code/documents etc. *The best first step is sharing whatever you can*.

**Great! I can put them in my new github repo.**

If that's enough for you for now great! If not for most pieces of proprietary software there are Open Source equivalents. Have a go with one and see what you think.

| Geschlossen                                                                                             | Öffnen                                                                                                                                                            |
| ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Matlab                                                                                                  | Python, Julia                                                                                                                                                     |
| STATA / SPSS                                                                                            | R                                                                                                                                                                 |
| MS Office                                                                                               | LibreOffice                                                                                                                                                       |
| Mathematica                                                                                             | JupyterLab                                                                                                                                                        |
| Max/MSP                                                                                                 | PureData                                                                                                                                                          |
| Test out your new [Pull Request -PR-](https://help.github.com/articles/about-pull-requests/) Skills ... | ... by adding your own example [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md) |

**Cool! But if I make the switch will I be stuck: taking ages to learn a new tool/ without support /with buggy software.**

Good question! The answer is it depends. The best thing to do is find someone who's made the switch before and learn from their experience. Or just do a Google search! Some OSS is much better than their closed counterparts, some aren't, so it's worth choosing carefully.

## Gute Software zur Wiederverwendung machen <a name="Reuse"></a>

The most likely person who might want to re-use your software in the future is...you! So while sharing is always better than not sharing, you can make your own life, and that of others, much easier through appropriate documentation. Documentation can include several things, such as including helpful comments and annotations in the code that help to explain why a particular action was performed, rather than what it is intended to achieve.

One of the most critical aspects of this is including an informative `README` file, that accompanies almost every OSS project, and some times even more than one. It can be a good practice to include one such file in every directory, that includes a list of files, a table of contents, and what the purpose of the directory is. The `README` file is typically just plain text or markdown (again, such as all of the ones for the MOOC!), and can include critical information for how to install and run software, previous dependencies and requirements, as well as tutorials or examples.

> **Wussten Sie, dass ...** Der Begriff `README` wird manchmal spielerisch der berühmten Szene in Lewis Carrolls Alice im Wunderland zugeschrieben, in der Alice mit magischen Knabbereien konfrontiert wird, die mit "Eat Me" und "Drink Me" gekennzeichnet sind. Potent.

The purpose here is to provide sufficient information to maximise the re-use and reproducibility of the computational environment, such that someone with no experience with the project can easily access and re-use the software ([Sandve et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)). By lowering the barriers to entry, you increase the chances of others being able to re-use your work, which is one of the ultimate goals of OSS ([Ince et al., 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)).

An extension of this that can help to make things even easier for future re-use is 'container' technology. Containers are like an ecosystem frozen in time, where the code, the data, any other dependencies, are all perfectly preserved, packaged and saved in the present functioning versions. This means that anyone in the future any one can come in and run the analyses again. As such, they are generally good for re-use, but this can come at the sacrifice of modification or understanding by others, as often a lot of details can be hidden within the source code and its dependencies. Common examples of container implementation in research include [Rocker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf) (a Docker container for the R language), [Binder](https://mybinder.readthedocs.io/en/latest/), and [Code Ocean](https://codeocean.com/).

**Sustainable software is good software.**

  


## 10 einfache Regeln für reproduzierbare Computerforschung

The 10 simple rules for making computational research more reproducible, based on [Sandve et al., (2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF), are:

1. Verfolgen Sie für jedes Ergebnis, wie es hergestellt wurde.
2. Vermeiden Sie manuelle Datenmanipulationsschritte.
3. Archivieren Sie die genauen Versionen aller verwendeten externen Programme.
4. Versionskontrolle aller benutzerdefinierten Skripte.
5. Erfassen Sie alle Zwischenergebnisse, wenn möglich, in standardisierten Formaten.
6. Beachten Sie für Analysen, die Zufälligkeiten enthalten, die zugrunde liegenden zufälligen Seeds.
7. Speichern Sie Rohdaten immer hinter Plots.
8. Generieren Sie hierarchische Analyseausgaben, damit Ebenen mit zunehmenden Details untersucht werden können.
9. Verbinden Sie Textaussagen mit den zugrunde liegenden Ergebnissen.
10. Bieten Sie öffentlichen Zugriff auf Skripts, Ausführungen und Ergebnisse.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/simple_rules.png?raw=true" width="800" /></p>

<p align="center"><i>Infographic adapted from Sandve et al., (2013). Feel free to download this and print it out to keep handy during your research!</i></p>

  


If you follow these steps, along with the processes in [**Task 1**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [**Task 2**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), you should be fine!

  


## Open Source Lizenzierung <a name="Licensing"></a>

An Open Source license is a type of license designed specifically for software and code that make it explicit what the legal conditions for sharing and re-use are. As mentioned [above](#What_OSS), the addition of a suitable license is what differentiates publicly shared software from OSS. For example, the widely used [MATLAB](https://www.mathworks.com/products/matlab.html) is proprietary software, and [Octave](https://www.gnu.org/software/octave/) is an openly licensed alternative programming language.

There are currently more than 1,400 unique Open Source licenses, a complexity born from the difficulty in understanding the differences between the legal implications across different license.

Some of the more common licenses include:

- [Berkeley Software Distribution ("BSD")](https://en.wikipedia.org/wiki/BSD_licenses),
- [Apache](https://www.apache.org/licenses/LICENSE-2.0),
- [MIT-Stil (Massachusetts Institute of Technology)](https://opensource.org/licenses/MIT)oder
- [GNU General Public License ("GPL")](https://www.gnu.org/licenses/gpl-3.0.en.html).

You don't need to know all the legal itty gritty behind all of these, but it is good to at least know what options are avaiilable to you.

There are two ways in which contributions to a project become licensed:

1. *Ausdrücklich*, wobei der einzelne Beitrag unabhängig vom Hauptprojekt eine eindeutig gekennzeichnete Lizenz hat; oder
2. *Implizit*, wobei der Beitrag unter den ursprünglichen Lizenzcode des Hauptprojekts fällt.

Thankfully, the process of selecting an Open Source license is relatively trivial, thanks to user-friendly tools such as [Choose A License](https://choosealicense.com/) or [Public License Selector](https://ufal.github.io/public-license-selector/). Each of these licenses allows other users to use, copy, distribute, and build upon your work, often while ensuring that the creators are appropriately recognised for their work. Here, the key is selecting an appropriate license for your work, depending on what you want, or do not want, others to do with it.

  


## Software-Zitat <a name="Citation"></a>

Citations provide one of the most important interactions in scholarly research, forming the basis of our referencing and metrics systems. Typically, this is performed thanks to the assistance of a permanent unique identifier such as a [Digital Object Identifiers](https://en.wikipedia.org/wiki/Digital_object_identifier) (DOI). A DOI is a persistent identifier, implemented in the [Handle System](https://en.wikipedia.org/wiki/Handle_System), that meets a common standard, depending on the purpose, such as for identifying academic information. Such identification is critical for tracking the genealogy and provenance of research, for reproducibility, as well as for giving appropriate credit to those who have created the software. Importantly, software should be considered a legitimate output from scholarly research, and citation is becoming an increasingly common way to indicate that.

In 2016, [Smith et al., 2016](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) wrote a research paper about the principles of software citation as part of the FORCE11 Software Citation Working Group. In the same way that you would want to cite software that you have used as part of good research practices, it is important to make your research easily citable too. When citing any software used for your own research, you should include at minimum:

- Die Namen der Autoren,
- Softwaretitel,
- Versionsnummer und
- Der eindeutige Bezeichner / Locator (DOI oder URL).

The six principles of software citation by [Smith et al., (2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) are provided here:

- **Wichtigkeit**: Software sollte als legitimes und zitierfähiges Forschungsprodukt betrachtet werden. Softwarezitate sollten in der wissenschaftlichen Dokumentation dieselbe Bedeutung haben wie Zitate anderer Forschungsprodukte wie Veröffentlichungen und Daten. Sie sollten in die Metadaten der zitierenden Arbeit aufgenommen werden, beispielsweise in die Referenzliste eines Zeitschriftenartikels, und nicht weggelassen oder getrennt werden. Software sollte auf der gleichen Grundlage zitiert werden wie jedes andere Forschungsprodukt, z. B. ein Papier oder ein Buch. Das heißt, Autoren sollten die entsprechenden Softwareprodukte genauso zitieren, wie sie die entsprechenden Papiere zitieren.

- **Anrechnung und Zuschreibung**: Softwarezitate sollen die wissenschaftliche Anrechnung und die normative, rechtliche Zuschreibung für alle Mitwirkenden an der Software erleichtern, wobei zu berücksichtigen ist, dass ein einziger Stil oder Mechanismus der Zuschreibung möglicherweise nicht für alle Software anwendbar ist.

- **Eindeutige Identifizierung**: Ein Software-Zitat sollte eine Methode zur Identifizierung enthalten, die maschinenlesbar, global eindeutig, interoperabel und von mindestens einer Community der entsprechenden Domain-Experten und vorzugsweise von Forschern der allgemeinen Öffentlichkeit anerkannt ist.

- **Persistenz**: Eindeutige Kennungen und Metadaten, die die Software und ihre Anordnung beschreiben, sollten bestehen bleiben - auch über die Lebensdauer der von ihnen beschriebenen Software hinaus.

- **Barrierefreiheit**: Softwarezitate sollten den Zugriff auf die Software selbst und die zugehörigen Metadaten, Dokumentationen, Daten und sonstigen Materialien erleichtern, die sowohl für den Menschen als auch für die Maschine erforderlich sind, um die referenzierte Software sachkundig zu nutzen.

- **Spezifität**: Softwarezitate sollten die Identifizierung und den Zugriff auf die spezifische Version der verwendeten Software erleichtern. Die Identifizierung der Software sollte so spezifisch wie nötig sein, z. B. mithilfe von Versionsnummern, Versionsnummern oder Varianten wie Plattformen.

Note: For instructions on 'how to make your software citable' see the section [**Using GitHub and Zenodo**](#GitHub_Zenodo) below and [**Task 2: Linking GitHub and Zenodo**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md).

  


## Mit GitHub und Zenodo <a name="GitHub_Zenodo"></a>

[GitHub](#GitHub) is a popular tool for project management, content storage, and version control. Note that GitHub itself is not OSS. However, Git, the tool which it is based on, is. Git is designed to help manage the source code files, and the updates to them, for a software-related project. However, it can also be extended to other non-software projects; for example, this [MOOC](https://github.com/OpenScienceMOOC/)!

However, getting research onto GitHub is just the first step. It is equally important to make it persistent and re-usable, which is why having a Digital Object Identifier (DOI) associated with it can be useful. The simplest way to do this is through a service called [Zenodo](https://zenodo.org/), which is a free and open source multi-disciplinary repository created by OpenAIRE and CERN, and can be used to assign a DOI to individual GitHub repositories. There is a [GitHub Guide](https://guides.github.com/activities/citable-code/) that explains the details, which involve linking GitHub repositories directly through to Zenodo so that when developers create formal releases for their software, Zenodo creates and archives a that version of the software.

There's nothing special about using Zenodo for creating DOIs, other than its **free of cost**; other general repositories can also be used, such as [DataCite DOI Fabrica](https://doi.datacite.org/), or your own institutional repositories such as [Caltech's](https://www.library.caltech.edu/news/enhanced-software-preservation-now-available-caltechdata).

A lot of researchers might typically be afraid of sharing code which is incomplete, buggy, or imperfect. However, in the OSS community, such a practice of sharing 'raw' code is fairly commonplace. Sharing code openly enables others to re-use and improve it, as well as to engage in a deeper way with any research associated with it. This is one of the fundamental aspects of peer-collaboration, perhaps best exemplified by the traditional process of research manuscript peer review.

Task 2 will guide you through the process of linking a GitHub repository to Zenodo for archiving.

> **Wussten Sie schon ...** Alle für dieses MOOC erstellten Inhalte sind als Teil einer Community in [Zenodo](https://zenodo.org/communities/open-science-mooc/)verfügbar?

**[GO TO TASK 2: Linking GitHub and Zenodo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)**

  


## Zusammenarbeit und Mitwirkung durch Open Source <a name="Collaborating"></a>

Often, OSS is developed in a public, decentralised, collaborative manner between multiple contributors. The purpose of this is to enhance the diversity and scope of a project and its design, in order to become more beneficial and sustainable. Such an approach was famously likened to a 'bazaar' model by Eric Raymond, an early OSS proponent. One of the major guiding principles of this is that of **peer production**, which relies on self-organised communities to regulate the development of content, co-ordinated towards a shared goal or outcome.

OSS projects rely heavily on volunteer collaboration, which often entails a constant flux of newcomers in order to become productive and sustainable ([Steinmacher et al., 2014](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)). Creating the right social atmosphere for a project, and a welcoming engagement environment, are often critical to successful collaboraitons in OSS.

  


## Wohin soll es von hier aus gehen? <a name="Future_OSS"></a>

Hopefully now you have come to see the importance of software as a cornerstone of modern science, and the importance that OSS plays in this.

The **learning outcomes** from this should be:

1. Sie werden nun in der Lage sein, die Merkmale von OSS und einige der ethischen, rechtlichen, wirtschaftlichen und forschungsbezogenen Argumente dafür und dagegen zu definieren.

2. Basierend auf Community-Standards können Sie nun die Qualitätsanforderungen für das Teilen und Wiederverwenden von offenem Code beschreiben.

3. Sie können nun eine Reihe von Recherchetools verwenden, die OSS verwenden.

4. Sie können jetzt Code, der für den persönlichen Gebrauch entwickelt wurde, in Code umwandeln, der für andere zugänglich und wieder verwendbar ist.

5. Softwareentwickler können ihre Software zitierfähig machen, und Software-Benutzer können die von ihnen verwendete Software zitieren.

  


**BONUS TASK**

If you have completed [Task 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [Task 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), we also have a **BONUS TASK** for you, if you want to take your skills a step further. [Task 3](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md) will take you a step deeper into integrating Git into a typical research workflow by showing you how to integrate it with R Studio. It is recommended that you have completed the first 2 tasks before proceeding with this one.

However, your Open Source journey does not stop here! This was just the beginning, and there are some incredible resources out there if you would like to do or learn more:

- Wenn Sie sich davon besonders inspiriert fühlen, können Sie das [Science Code Manifesto](http://sciencecodemanifesto.org/), das auf den fünf Prinzipien Code, Copyright, Zitation, Credit und Curation basiert.

- Um Ihr eigenes Projekt zu starten und zu entwickeln, bietet das Programm [Open Source Guides](https://opensource.guide/) eine Reihe praktischer Anleitungen und Fähigkeiten, mit denen Sie Ihre OSS-Projekte starten und vorantreiben können.

- Für einen detaillierten Blick auf OSS-basierte Forschungsworkflows ist das Handbuch [Open Science, Open Data, Open Source](https://pfern.github.io/OSODOS/gitbook/) von Pedro L. Fernandes und Rutger A. Vos eine der wichtigsten Online-Ressourcen.

- Für softwarebasierte Artikel gibt es auch mehr formalisierte Veranstaltungsorte, darunter [The Journal of Open Research Software](https://openresearchsoftware.metajnl.com/) und [The Journal of Open Source Software](https://joss.theoj.org/). Eine Liste solcher Veranstaltungsorte ist ebenfalls [verfügbar](https://www.software.ac.uk/which-journals-should-i-publish-my-software).

- Das [PLOS Open Source Toolkit](https://channels.plos.org/open-source-toolkit) bietet ein globales Forum für die Forschung und Anwendung von Open Source-Hardware und -Software.

- Das [NumFOCUS](http://www.numfocus.org) ist eine gemeinnützige Organisation, die erstklassige, innovative Open-Source-Wissenschaftssoftware unterstützt und fördert. Einige der von ihnen geförderten Projekte umfassen:
    
    - [IPython](http://ipython.org) und [Jupyter Notebook](https://jupyter.org) Initiativen.
    
    - [rOpenSci](http://ropensci.org), das die Open Source R-Statistikumgebung für transparente und reproduzierbare Forschung fördert.
    
    - Um mehr praktische Erfahrungen mit OSS zu sammeln, veranstaltet die Community von [Software Carpentry](https://software-carpentry.org/) regelmäßig Workshops zur Verbesserung der laborbasierten Computerfähigkeiten ([Wilson et al., 2017](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Wilson%20et%20al.%2C%202017.pdf)).

  


### Weitere Lektüre <a name="Reading"></a>

*These references here are just the beginning. They include some of the most useful general overviews of the Open Source landscape in research. However, if you want to be find something more specific to your own research field, then that path is there for you to explore!*

- Die Zukunft der Forschung in der Entwicklung von Free / Open Source-Software [(Scacchi, 2010)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Scacchi%2C%202010.pdf).

- Die wissenschaftliche Methode in der Praxis: Reproduzierbarkeit in den Computerwissenschaften [(Stodden, 2010)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Stodden%2C%202010.pdf).

- Der Fall für offene Computerprogramme [(Ince et al., 2012)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf).

- Aktuelle Themen und Forschungstrends zu Open-Source-Software-Communities [(Martinez-Torres und Diaz-Fernandez, 2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Martinez-Torres%20and%20Diaz-Fernandez%2C%202013.pdf).

- Zehn einfache Regeln für reproduzierbare Computerforschung [(Sandve et al., 2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF).

- Eine systematische Literaturübersicht über die von Newcomern konfrontiert Barrieren - Source - Software - Projekte zu öffnen [(Steinmacher et al., 2014)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf).

- Wissensaustausch in Open Source-Software-Communities: Motivation und Management [(Iskoujina und Roberts, 2015)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Iskoujina%20and%20Roberts%2C%202015.pdf).

- Software-Zitierprinzipien [(Smith et al., 2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf).

- Eine Einführung in Rocker: Docker Container für R [(Boettiger und Eddelbuettel, 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf).

- Gute Praktiken im wissenschaftlichen Rechnen [(Wilson et al., 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Wilson%20et%20al.%2C%202017.pdf).

- Vier einfache Empfehlungen zur Förderung von Best Practices in der Forschungssoftware [(Jiménez et al., 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Jim%C3%A9nez%20et%20al.%2C%202018.pdf).

  


### Entwicklungsteam <a name="Development_team"></a>

- [Alex Morley](https://twitter.com/alex__morley), Open Sourceror, Universität Oxford, Großbritannien.
- [Kevin Moerman](https://twitter.com/KMMoerman), Open Sourceror, MIT, USA.
- [Tania Allard](https://twitter.com/ixek), Open Sourceress, Datenbeschwörerin, Universität Leeds, Großbritannien.
- [Simon Worthington](https://twitter.com/mrchristian99), Book Liberationist, TIB, Deutschland.
- [Paola Masuzzo](https://twitter.com/pcmasuzzo), Open Source Batman, Italien.
- [Ivo Grigorov](https://twitter.com/OAforClimate), Open Source Robin, Dänemark.
- [Rutger Vos](https://twitter.com/rvosa), Open Sourceror, Naturalis Biodiversity Center, Niederlande.
- [Julien Colomb](https://twitter.com/j_colomb), Open Ninja, Berlin.
- [Jon Tennant](https://twitter.com/protohedgehog), Dinosaur Whisperer.

**Know a way this content can be improved?**

Time to take your new GitHub skills for a test-run! All content development primarily happens [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md). If you have a suggested improvement to the content, layout, or anything else, you can make it and then it will automatically become part of the MOOC content after verification from a moderator!

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)