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
- [Die Open Source Community, Governance und Beiträge](#OS_Community)
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

Einige sehen in der OSS-Bewegung eine Gegenbewegung zu Neoliberalismus und Privatisierung, die sich gegen Vorschriften und Normen bei der Konstruktion und Wiederverwendung von Informationen richtet, und eine potenzielle Transformation des modernen Kapitalismus durch die Bereitstellung von Software in Hülle und Fülle mit minimalem Aufwand. Siehe [Die Free / Open Source Software Bewegung: Widerstand oder Veränderung?](http://www.redalyc.org/html/742/74212712006/) von Panayiota Georgopoulou für mehr zu diesem Thema.

  


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

Es gibt zwei Hauptcamps in der Community der Freien Software: Die **Freie Software Bewegung**und die **OSS Bewegung**. Beide haben unterschiedliche Ideologien, die auf den Benutzerfreiheiten und den praktischen Anwendungen von Software beruhen. Oft wird der Begriff "FLOSS" verwendet, um diese beiden politischen Lager zu versöhnen und bedeutet "Freie / Libre- und Open Source-Software". Libre ist Französisch und Spanisch für "frei" im Kontext der Freiheit.

Das Kernprinzip der Wiederverwendung ist das, was OSS von „Freier Software“ unterscheidet. Freie und Open Source Software (FOSS) ist ein umfassender Begriff zur Beschreibung von Software, die sowohl als freie als auch als Open Source klassifiziert werden kann. Ein gutes Beispiel für FOSS ist das Betriebssystem [Ubuntu Linux](https://www.ubuntu.com/).

Der große Unterschied zwischen Freier Software und OSS besteht darin, dass erstere aktualisierte Versionen unter derselben Lizenz wie das Original vertreiben müssen, während neuere Versionen von OSS unter verschiedenen Lizenzen vertrieben werden können. FOSS vereint das Beste aus beiden Welten.

Diese Definitionen sind inzwischen weit verbreitet, sowohl von internationalen Regierungen als auch von einigen großen Organisationen wie der [Mozilla Foundation](https://www.mozilla.org/en-US/foundation/) und der [Wikimedia Foundation](https://wikimediafoundation.org/wiki/Home). Zu den wichtigsten Organisationen im FLOSS-Bereich gehört das britische [Software Sustainability Institute](https://www.software.ac.uk/), das wertvolle Ressourcen produziert, z. B. die jüngsten [Software Deposit Guidance for Researchers](https://softwaresaved.github.io/software-deposit-guidance/).

### Für einzelne Projekte

Ein typisches Open Source-Projekt hat die folgenden Arten formaler Rollen:

- **Autor**: Es ist die Person, die das Projekt erstellt hat
- **Eigentümer**: Die Person (en), die über Administratorrechte für die Organisation oder das Repository verfügt 
- **Betreuer**: Mitwirkende, die für die Umsetzung der Vision und das Management der organisatorischen Aspekte des Projekts verantwortlich sind. (Sie können auch Autoren oder Eigentümer des Projekts sein.)
- **Mitwirkende**: Der Benutzer, der bereits zu dem Projekt beigetragen hat.
- **Community-Mitglieder**: Personen, die das Projekt nutzen. Sie können aktiv an Gesprächen teilnehmen, neue Themen erstellen oder ihre Meinung zu zukünftigen Projektverbesserungen äußern.

Normalerweise werden Rollen entweder über die Datei `README` , eine Contributors-Datei oder eine separate Teamseite für das Projekt veröffentlicht.

  


## Bestehende Plattformen und Tools für Open Source Software <a name="Platforms"></a>

Virtuelle Umgebungen und Maschinen werden immer beliebter, da sie leistungsstarke Workflow-Funktionen für die Forschung ermöglichen. Viele davon basieren auf OSS (z. B. Betriebssysteme, Programmiersprachen und Datenverarbeitungs-Frameworks). Zu den gängigen Diensten zählen [Google Cloud](https://cloud.google.com/compute/) und [Amazon Web Services](https://aws.amazon.com/), die auch die Speicherung von Datenbanken und die Bereitstellung von Inhalten sowie die Rechenleistung unterstützen. [InsideDNA](https://insidedna.me/) ist eine Computerplattform für reproduzierbare Forschung in den Bereichen Bioinformatik, Genomik und Life Sciences.

Wie bereits erwähnt [über](#What_OSS)stellt Libreoffice eine Open - Source - Alternative zu Microsoft Office. Die beiden sind fast vollständig kompatibel, nur mit verschiedenen Standarddateiformaten. Für Zitiermanager ist [Zotero](https://www.zotero.org/) die beliebteste Open Source-Alternative zu proprietären Plattformen wie Mendeley oder EndNote.

[Zotero](https://www.zotero.org/) verwendet das BibTeX-Format (ausgesprochen "bib-tech"), das auf LaTeX (ausgesprochen "lay-tech") basiert, und verfügt über Browser-Plug-ins, um das Zitiermanagement zu vereinfachen. Durch die Integration mit anderer Software wie LibreOffice ist es jetzt in vielen Fällen möglich, einen vollständigen Open Source-Forschungsworkflow zu haben.

### GitHub <a name="GitHub"></a>

> Wussten Sie, dass dieses gesamte Projekt als offene und kollaborative Community in [GitHub](https://github.com/OpenScienceMOOC/)?

[GitHub](https://github.com/) ist eine beliebte Hosting-Site für Software- und Nicht-Software-Inhalte (häufig als "Notizbücher" bezeichnet) mit zusätzlichen Funktionen für Versionskontrolle, Projektmanagement und -verfolgung sowie für Speicherdienste. GitHub baut auf dem OSS [Git](https://git-scm.com/), mit dem Benutzer remote arbeiten können, um Forschungssoftware und andere nicht auf Software basierende Projekte zu warten, gemeinsam zu nutzen und zusammenzuarbeiten.

Die Versionskontrolle ist im Wesentlichen ein Prozess, der Momentaufnahmen der Dateien in einem Repository erstellt und Änderungen daran nachverfolgt. Es wird aufgezeichnet, wann die Änderungen vorgenommen wurden, was sie waren und wer sie vorgenommen hat. Wenn mehrere Personen gleichzeitig an einer Datei arbeiten, werden überlappende Änderungen erkannt und müssen behoben werden, bevor Sie fortfahren können. Dies bietet einen wesentlich effizienteren und automatisierten Prozess als das manuelle Speichern und Aufzeichnen von Änderungen während der Projektentwicklung. Außerdem werden die unvermeidlichen Listen verwirrender benannter Dateiversionen vermieden ...

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/xkcd.png?raw=true" width="200" /></p>

<p align="center"><i>GitHub hilft uns, suboptimale Dateinamenskonventionen zu vermeiden (Quelle: XKCD)</i></p>

  


Eine der beliebtesten und nützlichsten Funktionen von GitHub ist der [Issue-Tracker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/issues), mit dem die OSS-Entwicklung organisiert wird. Über den obigen Link gelangen Sie zum Issue Tracker für die Entwicklung dieses Moduls! Wenn Sie der Meinung sind, dass sich hier etwas verbessern lässt, oder wenn Sie etwas kommentieren möchten, kann jeder dort ein Problem hinzufügen oder dazu beitragen!

Andere ähnliche Projekt-Hosting-Dienste umfassen [BitBucket](https://bitbucket.org/), [GitLab](https://about.gitlab.com/)und [Launchpad](https://launchpad.net/). Wenn die kürzlich erfolgte Akquisition von GitHub durch Microsoft Sie etwas abschreckt, sind dies großartige Alternativen.

Wir wissen jedoch auch, dass GitHub eine recht hohe Lernkurve aufweisen kann. Aus diesem Grund lernen Sie in der ersten praktischen Aufgabe für dieses MOOC, wie Sie Ihr erstes GitHub-Projekt-Repository einrichten!

**[WEITER ZU AUFGABE 1: Erstellen Sie Ihr erstes GitHub-Repository](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)**

  


## Open Source Software für Forschungszwecke <a name="Research"></a>

Insbesondere in der wissenschaftlichen Forschung ist der Einsatz und die Entwicklung von Open Source-Software praktisch zur Norm geworden. Hierfür gibt es eine Reihe von Gründen, die über die allgemeine Akzeptanz von OSS hinausgehen, beispielsweise bei Verbrauchern, der Industrie oder der Regierung. Zu diesen Gründen gehören:

- Zunehmend sind in Analysesoftware implementierte Algorithmen ein wesentlicher Bestandteil der in wissenschaftlichen Veröffentlichungen beschriebenen Methoden. Insofern widerspricht es einem strengen Peer Review, wenn diese Algorithmusimplementierungen für Außenstehende nicht zugänglich sind.

- Die wissenschaftliche Zusammenarbeit erstreckt sich häufig über mehrere Institutionen und verteilte Forschungsnetzwerke, in denen Geheimhaltung und Befehlshierarchie nicht in einer Weise aufrechterhalten werden, die für die Entwicklung geschlossener Quellen "notwendig" ist.

- Viele Computeranalysen werden in virtualisierten Umgebungen (z. B. institutionellen, nationalen oder internationalen Cloud-Infrastrukturen) ausgeführt und auf Mehrbenutzerservern gehostet. Kommerzielle Closed-Source-Software lässt eine solche Verwendung häufig nicht zu.

- Die OSS-Entwicklung beruht häufig auf Freiwilligen. In Zeiten knapper Haushaltsmittel für die wissenschaftliche Forschung ist dies ein klarer Vorteil.

Aus diesen und anderen Gründen werden Open Source-Tools in der wissenschaftlichen Forschung sehr häufig verwendet. Dies schließt den Einsatz in Bereichen ein, in denen viele Forscher selbst Amateurentwickler sind und auf Tools wie [R](https://www.r-project.org/) für statistische Analysen und Skripterstellung zurückgreifen, die im letzten Jahrzehnt kommerzielle Software für statistische Analysen wie SPSS oder JMP in einem fast vollständig verdrängt haben viele Felder. In Bereichen wie der Bioinformatik, in denen die Ausgabe von DNA-Sequenzierungsplattformen häufig in Dateien verarbeitet wird, sind Allzweck-Skriptsprachen wie [Python](https://www.python.org/) und häufig verwendete Bibliotheken (wie [Biopython](http://biopython.org)) von entscheidender Bedeutung Teil des Toolkits vieler Forscher.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/python.png?raw=true" width="400" /></p>

<p align="center"><i>Python</i></p>

  


Tools wie R und Python sind im Wesentlichen Software zum Schreiben von Software. Obwohl die Programmierung immer häufige Aktivität unter den Forschern ist natürlich nicht *jeder* Wissenschaftler tut dies. Ein Schritt weg von der Programmierung ist die Verkettung der Ein- und Ausgänge verschiedener Analysetools in längeren Workflows. Als ein Beispiel aus der Genomik ist es ein sehr häufiger Arbeitsablauf, mit Sequenzen mit hohem Durchsatz zu beginnen und dann i) grundlegende Qualitätskontrollprüfungen durchzuführen; ii) die gelesenen Werte gegen ein Referenzgenom abbilden; iii) Identifizieren Sie die Punkte, an denen die neuen Daten von der Referenz abweichen. Diese Schritte werden routinemäßig als Workflow ausgeführt, in dem für jeden der drei Schritte eine andere ausführbare Open Source-Datei in einer Linux-Befehlszeilenumgebung ausgeführt wird. Obwohl dies wohl keine Open-Source-Softwareentwicklung ist, werden Open-Source-Artefakte (z. B. Linux-Shell-Skripte) verwendet und produziert, für die die in diesem Modul beschriebenen Prinzipien gelten.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/r.png?raw=true" width="200" /></p>

<p align="center"><i>R</i></p>

  


Schließlich wird OSS auch in der wissenschaftlichen Forschung aus Gründen verwendet, die denen, die die Einführung von OSS in einer breiteren Gesellschaft vorantreiben, genauer entsprechen, nämlich, dass es billig ist. Einzelpersonen oder Organisationen könnten sich beispielsweise dafür entscheiden, von Microsoft Office zu LibreOffice zu wechseln, um Manuskripte zu schreiben oder Tabellenkalkulationen zu verarbeiten, da letztere kostenlos sind (sowohl in [**'Freibier'**](https://www.youtube.com/watch?v=dQw4w9WgXcQ) als auch in 'Redefreiheit'). Ebenso kann die Auswahl eines Wechsels von ArcGIS zu [QGIS](https://www.qgis.org/en/site/) für die Analyse von geografischen Informationen einfach aus Kostengründen erfolgen.   


## Erste Schritte mit OSS - FAQ <a name="FAQ"></a>

**Ich verwende X [zB Matlab, STATA, Excel] und möchte auf etwas Offeneres umsteigen. Was sind die nächsten Schritte?**

Selbst wenn Sie proprietäre Software verwenden, können Sie in der Regel Ihren Quellcode / Ihre Dokumente usw. weitergeben. *Der beste erste Schritt ist, alles zu teilen, was Sie können*.

**Großartig! Ich kann sie in mein neues Github-Repo legen.**

Wenn es dir jetzt reicht, großartig! Wenn nicht für die meisten proprietären Softwareprodukte, gibt es Open Source-Entsprechungen. Probieren Sie es aus und sehen Sie, was Sie denken.

| Geschlossen                                                                                                 | Öffnen                                                                                                                                                                           |
| ----------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Matlab                                                                                                      | Python, Julia                                                                                                                                                                    |
| STATA / SPSS                                                                                                | R                                                                                                                                                                                |
| MS Office                                                                                                   | LibreOffice                                                                                                                                                                      |
| Mathematica                                                                                                 | JupyterLab                                                                                                                                                                       |
| Testen Sie Ihre neuen [Pull Request -PR-](https://help.github.com/articles/about-pull-requests/) Skills ... | ... indem Sie hier Ihr eigenes Beispiel [hinzufügen](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md) |

**Cool! Aber wenn ich den Wechsel mache, stecke ich fest: Es dauert ewig, ein neues Tool / ohne Support / mit Buggy-Software zu erlernen.**

Gute Frage! Die Antwort ist, es kommt darauf an. Das Beste, was Sie tun können, ist, jemanden zu finden, der zuvor den Wechsel vorgenommen hat, und aus seinen Erfahrungen zu lernen. Oder führen Sie einfach eine Google-Suche durch! Einige OSS sind viel besser als ihre geschlossenen Gegenstücke, andere nicht, daher lohnt es sich, sorgfältig zu wählen.

## Gute Software zur Wiederverwendung machen <a name="Reuse"></a>

Die wahrscheinlichste Person, die Ihre Software in Zukunft wiederverwenden möchte, ist ... Sie! Während das Teilen immer besser ist als das Nicht-Teilen, können Sie durch entsprechende Dokumentation Ihr eigenes Leben und das anderer einfacher gestalten. Die Dokumentation kann verschiedene Dinge enthalten, z. B. hilfreiche Kommentare und Anmerkungen im Code, die erklären, warum eine bestimmte Aktion ausgeführt wurde und nicht, was erreicht werden soll.

Einer der kritischsten Aspekte dabei ist eine informative `README` Datei, die zu fast jedem OSS-Projekt und manchmal sogar zu mehreren gehört. Es kann eine gute Praxis sein, eine solche Datei in jedes Verzeichnis aufzunehmen, die eine Liste von Dateien, ein Inhaltsverzeichnis und den Zweck des Verzeichnisses enthält. Die `README` Datei ist in der Regel nur einfacher Text oder eine Abschrift (wie alle für das MOOC!) Und kann wichtige Informationen zur Installation und Ausführung von Software, frühere Abhängigkeiten und Anforderungen sowie Lernprogramme oder Anleitungen enthalten Beispiele.

> **Wussten Sie, dass ...** Der Begriff `README` wird manchmal spielerisch der berühmten Szene in Lewis Carrolls Alice im Wunderland zugeschrieben, in der Alice mit magischen Knabbereien konfrontiert wird, die mit "Eat Me" und "Drink Me" gekennzeichnet sind. Potent.

Ziel ist es, ausreichende Informationen bereitzustellen, um die Wiederverwendung und Reproduzierbarkeit der Computerumgebung zu maximieren, sodass Personen ohne Projekterfahrung problemlos auf die Software zugreifen und sie erneut verwenden können ([Sandve et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)). Indem Sie die Eintrittsbarrieren senken, erhöhen Sie die Wahrscheinlichkeit, dass andere Ihre Arbeit wiederverwenden können, was eines der obersten Ziele von OSS ist ([Ince et al., 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)).

Eine Erweiterung davon, die dazu beitragen kann, die Dinge für die zukünftige Wiederverwendung noch einfacher zu machen, ist die Containertechnologie. Container sind wie ein in der Zeit eingefrorenes Ökosystem, in dem der Code, die Daten und alle anderen Abhängigkeiten in den gegenwärtigen funktionierenden Versionen perfekt erhalten, verpackt und gespeichert werden. Dies bedeutet, dass in Zukunft jeder die Analysen erneut ausführen kann. Als solche sind sie in der Regel gut für die Wiederverwendung geeignet. Dies kann jedoch dazu führen, dass andere Benutzer Änderungen vornehmen oder verstehen, da im Quellcode und seinen Abhängigkeiten häufig viele Details verborgen sind. Häufige Beispiele für die Implementierung von Containern in der Forschung sind [Rocker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf) (ein Docker-Container für die R-Sprache), [Binder](https://mybinder.readthedocs.io/en/latest/)und [Code Ocean](https://codeocean.com/).

**Nachhaltige Software ist gute Software.**

  


## 10 einfache Regeln für reproduzierbare Computerforschung

Die 10 einfachen Regeln zur besseren Reproduzierbarkeit von Computerrecherchen, basierend auf [Sandve et al., (2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF), lauten:

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

<p align="center"><i>Infografik adaptiert von Sandve et al., (2013). Laden Sie dieses Dokument herunter und drucken Sie es aus, damit Sie es während Ihrer Recherche immer zur Hand haben!</i></p>

  


Wenn Sie diese Schritte zusammen mit den Prozessen in [**Aufgabe 1**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) und [**Aufgabe 2**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)ausführen, sollte es Ihnen gut gehen!

  


## Open Source Lizenzierung <a name="Licensing"></a>

Eine Open Source-Lizenz ist eine Art von Lizenz, die speziell für Software und Code entwickelt wurde, um die rechtlichen Bedingungen für die Weitergabe und Wiederverwendung zu erläutern. Wie bereits erwähnt [über](#What_OSS)ist die Zugabe eines geeigneten Lizenz , welche Software von OSS öffentlich geteilt differenziert. Zum Beispiel ist das weit verbreitete [MATLAB](https://www.mathworks.com/products/matlab.html) proprietäre Software, und [Octave](https://www.gnu.org/software/octave/) ist eine offen lizenzierte alternative Programmiersprache.

Derzeit gibt es mehr als 1.400 einzigartige Open Source-Lizenzen. Diese Komplexität resultiert aus der Schwierigkeit, die Unterschiede zwischen den rechtlichen Auswirkungen verschiedener Lizenzen zu verstehen.

Einige der gebräuchlichsten Lizenzen umfassen:

- [Berkeley Software Distribution ("BSD")](https://en.wikipedia.org/wiki/BSD_licenses),
- [Apache](https://www.apache.org/licenses/LICENSE-2.0),
- [MIT-Stil (Massachusetts Institute of Technology)](https://opensource.org/licenses/MIT)oder
- [GNU General Public License ("GPL")](https://www.gnu.org/licenses/gpl-3.0.en.html).

Sie müssen nicht alle rechtlichen Details kennen, aber es ist gut zu wissen, welche Optionen Ihnen zur Verfügung stehen.

Es gibt zwei Möglichkeiten, wie Beiträge zu einem Projekt lizenziert werden:

1. *Ausdrücklich*, wobei der einzelne Beitrag unabhängig vom Hauptprojekt eine eindeutig gekennzeichnete Lizenz hat; oder
2. *Implizit*, wobei der Beitrag unter den ursprünglichen Lizenzcode des Hauptprojekts fällt.

Zum Glück ist die Auswahl einer Open Source-Lizenz dank benutzerfreundlicher Tools wie [Choose A License](https://choosealicense.com/)relativ einfach. Jede dieser Lizenzen ermöglicht es anderen Benutzern, Ihre Arbeit zu nutzen, zu kopieren, zu verteilen und darauf aufzubauen, und gleichzeitig sicherzustellen, dass die Urheber für ihre Arbeit angemessen anerkannt werden. Hier ist der Schlüssel die Auswahl einer geeigneten Lizenz für Ihre Arbeit, je nachdem, was andere damit machen möchten oder nicht.

  


## Software-Zitat <a name="Citation"></a>

Zitate stellen eine der wichtigsten Wechselwirkungen in der wissenschaftlichen Forschung dar und bilden die Grundlage für unsere Referenzierungs- und Metriksysteme. In der Regel wird dies mithilfe einer permanenten eindeutigen Kennung durchgeführt, beispielsweise einer [Digital Object Identifiers](https://en.wikipedia.org/wiki/Digital_object_identifier) (DOI). Ein DOI ist eine permanente Kennung, die im [Handle-System](https://en.wikipedia.org/wiki/Handle_System)implementiert ist und je nach Verwendungszweck einem gemeinsamen Standard entspricht, z. B. zur Identifizierung akademischer Informationen. Eine solche Identifizierung ist entscheidend für die Verfolgung der Genealogie und Herkunft der Forschung, für die Reproduzierbarkeit sowie für die angemessene Anerkennung derjenigen, die die Software erstellt haben. Wichtig ist, dass Software als legitimes Ergebnis wissenschaftlicher Forschung betrachtet werden sollte, und Zitate werden immer häufiger als Hinweis darauf verwendet.

Im Jahr 2016 haben [Smith et al., 2016](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) im Rahmen der FORCE11 Software Citation Working Group ein Forschungspapier über die Prinzipien des Software Citation verfasst. Ebenso wie Sie Software zitieren möchten, die Sie im Rahmen guter Forschungspraktiken verwendet haben, ist es wichtig, dass Ihre Forschung auch leicht zitierbar ist. Wenn Sie Software zitieren, die für Ihre eigene Forschung verwendet wird, sollten Sie mindestens Folgendes angeben:

- Die Namen der Autoren,
- Softwaretitel,
- Versionsnummer und
- Der eindeutige Bezeichner / Locator (DOI oder URL).

Die sechs Prinzipien der Software-Zitierung von [Smith et al. (2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) werden hier bereitgestellt:

- **Wichtigkeit**: Software sollte als legitimes und zitierfähiges Forschungsprodukt betrachtet werden. Softwarezitate sollten in der wissenschaftlichen Dokumentation dieselbe Bedeutung haben wie Zitate anderer Forschungsprodukte wie Veröffentlichungen und Daten. Sie sollten in die Metadaten der zitierenden Arbeit aufgenommen werden, beispielsweise in die Referenzliste eines Zeitschriftenartikels, und nicht weggelassen oder getrennt werden. Software sollte auf der gleichen Grundlage zitiert werden wie jedes andere Forschungsprodukt, z. B. ein Papier oder ein Buch. Das heißt, Autoren sollten die entsprechenden Softwareprodukte genauso zitieren, wie sie die entsprechenden Papiere zitieren.

- **Anrechnung und Zuschreibung**: Softwarezitate sollen die wissenschaftliche Anrechnung und die normative, rechtliche Zuschreibung für alle Mitwirkenden an der Software erleichtern, wobei zu berücksichtigen ist, dass ein einziger Stil oder Mechanismus der Zuschreibung möglicherweise nicht für alle Software anwendbar ist.

- **Eindeutige Identifizierung**: Ein Software-Zitat sollte eine Methode zur Identifizierung enthalten, die maschinenlesbar, global eindeutig, interoperabel und von mindestens einer Community der entsprechenden Domain-Experten und vorzugsweise von Forschern der allgemeinen Öffentlichkeit anerkannt ist.

- **Persistenz**: Eindeutige Kennungen und Metadaten, die die Software und ihre Anordnung beschreiben, sollten bestehen bleiben - auch über die Lebensdauer der von ihnen beschriebenen Software hinaus.

- **Barrierefreiheit**: Softwarezitate sollten den Zugriff auf die Software selbst und die zugehörigen Metadaten, Dokumentationen, Daten und sonstigen Materialien erleichtern, die sowohl für den Menschen als auch für die Maschine erforderlich sind, um die referenzierte Software sachkundig zu nutzen.

- **Spezifität**: Softwarezitate sollten die Identifizierung und den Zugriff auf die spezifische Version der verwendeten Software erleichtern. Die Identifizierung der Software sollte so spezifisch wie nötig sein, z. B. mithilfe von Versionsnummern, Versionsnummern oder Varianten wie Plattformen.

Hinweis: Anweisungen zum Zitieren Ihrer Software finden Sie in den Abschnitten [**Verwenden von GitHub und Zenodo**](#GitHub_Zenodo) und [**Aufgabe 2: Verknüpfen von GitHub und Zenodo**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md).

  


## Mit GitHub und Zenodo <a name="GitHub_Zenodo"></a>

[GitHub](#GitHub) ist ein beliebtes Tool für die Projektverwaltung, Inhaltsspeicherung und Versionskontrolle. Beachten Sie, dass GitHub selbst kein OSS ist. Git ist jedoch das Werkzeug, auf dem es basiert. Git wurde entwickelt, um die Quellcodedateien und deren Aktualisierungen für ein Softwareprojekt zu verwalten. Es kann jedoch auch auf andere Nicht-Software-Projekte ausgeweitet werden. Zum Beispiel diese [MOOC](https://github.com/OpenScienceMOOC/)!

Die Erforschung von GitHub ist jedoch nur der erste Schritt. Es ist ebenso wichtig, es dauerhaft und wiederverwendbar zu machen, weshalb es nützlich sein kann, einen Digital Object Identifier (DOI) zu verwenden. Der einfachste Weg, dies zu tun, ist ein Service namens [Zenodo](https://zenodo.org/), ein kostenloses und Open-Source-Repository für mehrere Disziplinen, das von OpenAIRE und CERN erstellt wurde und verwendet werden kann, um einzelnen GitHub-Repositories eine DOI zuzuweisen. Es gibt einen [GitHub-Leitfaden](https://guides.github.com/activities/citable-code/) , der die Details erklärt, bei denen GitHub-Repositorys direkt mit Zenodo verknüpft werden, sodass Zenodo beim Erstellen formaler Releases für ihre Software eine solche Version der Software erstellt und archiviert.

Es ist nichts Besonderes, Zenodo zum Erstellen von DOIs zu verwenden, außer die **kostenlos ist**; Es können auch andere allgemeine Repositorys wie [DataCite DOI Fabrica](https://doi.datacite.org/)oder Ihre eigenen institutionellen Repositorys wie [Caltech's](https://www.library.caltech.edu/news/enhanced-software-preservation-now-available-caltechdata).

Viele Forscher haben möglicherweise Angst, unvollständigen, fehlerhaften oder fehlerhaften Code weiterzugeben. In der OSS-Community ist eine solche Praxis des Austauschs von 'rohem' Code jedoch weit verbreitet. Das offene Teilen von Code ermöglicht es anderen, ihn wiederzuverwenden und zu verbessern sowie sich eingehender mit der damit verbundenen Forschung zu befassen. Dies ist einer der grundlegenden Aspekte der Peer-Collaboration, die am besten durch den traditionellen Prozess der Peer-Review von Forschungsmanuskripten veranschaulicht werden kann.

Aufgabe 2 führt Sie durch den Prozess der Verknüpfung eines GitHub-Repositorys mit Zenodo zur Archivierung.

> **Wussten Sie schon ...** Alle für dieses MOOC erstellten Inhalte sind als Teil einer Community in [Zenodo](https://zenodo.org/communities/open-science-mooc/)verfügbar?

**[WEITER ZU AUFGABE 2: Verbinden von GitHub und Zenodo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)**

  


## Zusammenarbeit und Mitwirkung durch Open Source <a name="Collaborating"></a>

Oft wird OSS in einer öffentlichen, dezentralen und kollaborativen Weise zwischen mehreren Mitwirkenden entwickelt. Ziel ist es, die Vielfalt und den Umfang eines Projekts und seine Gestaltung zu verbessern, um mehr Nutzen und Nachhaltigkeit zu erzielen. Ein solcher Ansatz wurde von Eric Raymond, einem frühen Befürworter der OSS, mit einem Basarmodell verglichen. Eines der wichtigsten Leitprinzipien dabei ist das der **Peer Production**, die sich auf selbstorganisierte Gemeinschaften stützt, um die Entwicklung von Inhalten zu regulieren, die auf ein gemeinsames Ziel oder Ergebnis abgestimmt sind.

OSS-Projekte stützen sich in hohem Maße auf die freiwillige Zusammenarbeit, die häufig einen ständigen Zustrom von Neuankömmlingen nach sich zieht, um produktiv und nachhaltig zu werden ([Steinmacher et al., 2014](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)). Die Schaffung der richtigen sozialen Atmosphäre für ein Projekt und ein einladendes Umfeld für das Engagement sind häufig entscheidend für eine erfolgreiche Zusammenarbeit in OSS.

  


## Wohin soll es von hier aus gehen? <a name="Future_OSS"></a>

Hoffentlich sehen Sie jetzt die Bedeutung von Software als Eckpfeiler der modernen Wissenschaft und die Bedeutung, die OSS dabei spielt.

Die **Lernergebnisse** daraus sollten sein:

1. Sie werden nun in der Lage sein, die Merkmale von OSS und einige der ethischen, rechtlichen, wirtschaftlichen und forschungsbezogenen Argumente dafür und dagegen zu definieren.

2. Basierend auf Community-Standards können Sie nun die Qualitätsanforderungen für das Teilen und Wiederverwenden von offenem Code beschreiben.

3. Sie können nun eine Reihe von Recherchetools verwenden, die OSS verwenden.

4. Sie können jetzt Code, der für den persönlichen Gebrauch entwickelt wurde, in Code umwandeln, der für andere zugänglich und wieder verwendbar ist.

5. Softwareentwickler können ihre Software zitierfähig machen, und Software-Benutzer können die von ihnen verwendete Software zitieren.

  


**BONUSAUFGABE**

Wenn Sie [Aufgabe 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) und [Aufgabe 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), haben wir auch eine **BONUS-AUFGABE** für Sie, wenn Sie Ihre Fähigkeiten weiterentwickeln möchten. [Aufgabe 3](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md) führt Sie ein Stück tiefer in die Integration von Git in einen typischen Forschungsworkflow ein, indem es Ihnen zeigt, wie Sie es in R Studio integrieren. Es wird empfohlen, dass Sie die ersten 2 Aufgaben abgeschlossen haben, bevor Sie mit dieser fortfahren.

Ihre Open Source-Reise hört hier jedoch nicht auf! Dies war nur der Anfang und es gibt einige unglaubliche Ressourcen, wenn Sie mehr tun oder lernen möchten:

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

*Diese Referenzen hier sind nur der Anfang. Sie enthalten einige der nützlichsten allgemeinen Übersichten über die Open Source-Landschaft in der Forschung. Wenn Sie jedoch etwas finden möchten, das spezifischer für Ihr eigenes Forschungsgebiet ist, können Sie diesen Pfad erkunden!*

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

**Wissen Sie, wie dieser Inhalt verbessert werden kann?**

Zeit, deine neuen GitHub-Fähigkeiten für einen Testlauf zu nutzen! Alle Inhalte Entwicklung geschieht in erster Linie [hier](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md). Wenn Sie Verbesserungsvorschläge zu Inhalt, Layout oder etwas anderem haben, können Sie diese vornehmen. Nach Überprüfung durch einen Moderator wird sie automatisch Teil des MOOC-Inhalts!

[![CC0 Public Domain Widmung](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)