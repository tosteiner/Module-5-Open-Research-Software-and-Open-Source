---
output:
  html_document: Standard
  pdf_document: Standard
---

# Aufgabe 1: So richten Sie ein Repository auf GitHub ein

Diese Aufgabe richtet sich an Studenten und Forscher, die ihr erstes Open Source-Projekt (Software oder Nicht-Software) auf GitHub erstellen möchten. GitHub ist ein Ort, an dem Sie neue Forschungsabläufe ausprobieren und ausprobieren können. Es ist wirklich nur der Anfang, um die Voraussetzungen für Ihre eigenen Wege und Ideen zu schaffen.

Vergiss nicht, dass du in unserem offenen [**Slack Channel**](https://osmooc.herokuapp.com/)mitdiskutieren kannst. Bitte stellen Sie sich unter # module5opensource vor und erzählen Sie uns, wer Sie sind, welchen Hintergrund Sie haben und wie Sie hier gelandet sind!

**BITTE BEACHTEN SIE** dass eine Bildschirmaufnahme für diese Aufgabe auch über [YouTube](https://www.youtube.com/watch?v=AnftV9HBPSc&)verfügbar ist.

Geschätzte Zeit bis zur Fertigstellung: 30-45 Minuten.

Geschätzte Zeitersparnis nach Abschluss: Unvorstellbar.

## Inhaltsverzeichnis

* [Fertig machen](#Getting_started) 
  * [Einrichten eines GitHub-Profils](#Profile)
  * [Die GitHub-Sprache](#Language)
  * [Ein neues Repository erstellen](#Create_new)
* [Die grundlegenden Schritte](#Foundation) 
  * [Lizenz auswählen](#License)
  * [Erstellen einer Readme-Datei](#Readme)
  * [Mitwirkende Richtlinien erstellen](#Contributing)
  * [Verhaltenskodex erstellen](#Conduct)
  * [Den Code zitierbar machen](#Citation)
* [Halten Sie Ihre Probleme auf dem neuesten Stand](#Issues)
* [Checkliste zum Starten Ihres Projekts](#Check-list)

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/Task1.png?raw=true" alt="Task 1-Workflow" width="600" height="861" style="margin-right: 30px; margin-left: 10px;" onmouseover="this.width='1200'; this.height='1722'" onmouseout="this.width='600'; this.height='861'">
</p>

<p align="center"><i>Der Workflow für Aufgabe 1. Halten Sie dies bereit, während Sie die Aufgabe abarbeiten!</i></p>

  


## Fertig machen <a name="Getting_started"></a>

Ein 'Repository' ist eigentlich nur ein ausgefallener Name für ein Projekt auf GitHub. GitHub ist ein Online-Ort, an dem Sie Projekte verwalten, Dateien speichern und offen mit anderen zusammenarbeiten können. Dies alles wird durch die Verwendung der Versionskontrolle erreicht, um Projekte während ihres Fortschritts zu verfolgen. Als solches ist GitHub ein leistungsstarkes Tool für Software- und Nicht-Software-Projekte.

Eines der wichtigsten Dinge, die Sie in diesem frühen Stadium berücksichtigen sollten, ist zu überlegen, wie die breitere Community mit Ihrem Projekt interagieren soll. Wenn Sie im Freien arbeiten, möchten Sie sicherstellen, dass sich andere Personen beim Zugriff auf Ihre Arbeit, beim Anzeigen und bei der Arbeit wohl fühlen. Ein Repository so einzurichten, dass die Eintrittsbarrieren gesenkt werden und die Angst, ein Außenseiter zu sein, der erste Schritt zur Aufrechterhaltung eines erfolgreichen Projekts ist.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/octocat.png?raw=true" width="150px" height="125px"/>
</p>

<p align="center"><i>Octocat, GitHubs kleines Maskottchen</i></p>

  


### Einrichten eines GitHub-Profils <a name="Profile"></a>

Um ein GitHub-Profil einzurichten, gehen Sie einfach zur Hauptseite und klicken Sie auf [Sign Up for GitHub](https://github.com/join). Hier können Sie Ihr persönliches Konto mit einem Benutzernamen, einer E-Mail-Adresse und einem Passwort als Standard erstellen.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/github_signup.png?raw=true" width="800" /></p>

<p align="center"><i>Melde dich bei GitHub an</i></p>

  


Der nächste Schritt besteht darin, einen persönlichen Plan aufzustellen. Wählen Sie zunächst einfach den Plan "Unbegrenzte Anzahl öffentlicher Repositorys kostenlos" aus, es sei denn, Sie befassen sich mit dem Datenschutz. Wählen Sie in diesem Fall den privaten Plan aus. Wenn Sie ein Projekt für eine Organisation einrichten möchten, können Sie diese Option ebenfalls auswählen.

  


### Die GitHub-Sprache <a name="Language"></a>

Dies ist möglicherweise der verwirrendste und abstoßendste Aspekt von GitHub. Hier sind einige der am häufigsten verwendeten Begriffe und deren Definitionen:

* **Initialisieren**: Erstellen Sie ein leeres Repository.
* **Checkout**: Erstellen Sie eine Arbeitskopie eines lokalen Repositorys.
* **Klonen**: Kopieren Sie das Repository in ein lokales Verzeichnis auf Ihrem Computer.
* **Gabel**: Erstellen Sie einen persönlichen Ableger eines Repositorys, um parallel daran zu arbeiten.
* **Zweig**: Eine unabhängige und parallele Version eines Repositorys. Änderungen wirken sich nicht auf den Master-Zweig aus.
* **Master**: Der Haupt- und Standardzweig für ein Repository.
* **Bereinigen**: Für den Zweig stehen keine Festschreibungen aus.
* **Phase**: Fügen Sie Aktualisierungen hinzu, die für die Übertragung an eine Zweigstelle bereit sind.
* **Festschreiben**: Eine Revision eines Repositorys, wie eine versionierte Funktion zum Speichern.
* **Commit-Nachricht**: Eine Beschreibung der Änderungen, die mit einem Commit einhergehen.
* **Check**: Eine Statusprüfung.
* **Fetch**: Nichts mit Hunden zu tun. Bezieht sich darauf, die neuesten Änderungen aus einem Online-Repository abzurufen, ohne sie zusammenzuführen.
* **Index**: Der 'Baum', der als Bereitstellungsbereich fungiert.
* **Arbeitsverzeichnis**: Der 'Baum', in dem die Dateien aufbewahrt werden.
* **Kopf**: Der 'Baum', der die zuletzt getätigten Commits anzeigt.
* **Push**: Fügen Sie dem Kopf Ihres Remote-Repository festgeschriebene Änderungen hinzu.
* **Merge**: Kombiniert die in einem Zweig vorgenommenen Änderungen nach Abschluss mit dem Master-Zweig.
* **Pull**: Aktualisieren Sie Ihr Repository, indem Sie die neuesten Commits abrufen und zusammenführen.
* **Pull-Anforderung**: Eine Anforderung zum Zusammenführen eines aktualisierten Zweigs mit dem Master-Zweig.
* **Problem**: Vorgeschlagene Verbesserungen, Aufgaben oder Fragen zu einem Repository.

Wütend! Mach dir keine Sorgen über das Auswendiglernen *alle* davon für jetzt. Wie bei jeder neuen Fähigkeit geht Vertrautheit mit Erfahrung einher.

Sie können wahrscheinlich feststellen, dass einige dieser Vorgänge mit Vorgängen zum Speichern, Kopieren und Einfügen vergleichbar sind, jedoch für einen Softwareverwaltungsprozess geeignet sind. Es gibt eine [paar mehr](https://mirrors.edge.kernel.org/pub/software/scm/git/docs/gitglossary.html) zu, aber dies sollte für die ersten Schritte tun.

Wenn Sie interessiert sind, stammen die meisten dieser Begriffe aus dem zugrunde liegenden [Git-System](https://git-scm.com). Git wurde entwickelt, um Entwicklern das verteilte Verwalten verschiedener Versionen von Quellcode zu ermöglichen, was großartig ist. Es hat viele Funktionen und die Fähigkeit, viele komplexe Dinge zu tun, die von einem [sehr klugen Kerl](https://www.linuxfoundation.org/blog/2015/04/10-years-of-git-an-interview-with-git-creator-linus-torvalds/). Die [Benutzeroberfläche wurde jedoch nicht für neue Benutzer konzipiert,](https://xkcd.com/1597/), daher kann es schwierig sein, sie zu erlernen.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/git.png?raw=true" width="150px"/>
</p>

<p align="center"><i>Unschlagbare Anleitung zur Verwendung von Git. (Quelle: XKCD)</i></p>

  


### Ein neues Repository erstellen <a name="Create_new"></a>

Klicken Sie in Ihrem GitHub-Profil auf "Neues Repository erstellen". Der erste Schritt besteht darin, einen Namen als Marke für Ihr Projekt zu erstellen. Idealerweise sollte es einprägsam sein und einen Hinweis darauf geben, was das Projekt leistet.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/new_repo.png?raw=true" width="800" /></p>

<p align="center"><i>Erstellen Sie ein neues Repository</i></p>

  


Vergewissern Sie sich, dass Namen nicht dupliziert, andere Marken verletzt oder als anstößig eingestuft werden.

  


## Die grundlegenden Schritte <a name="Foundation"></a>

Jedes GitHub-Repository benötigt 4 Schlüsselelemente, um zu beginnen und eine einladende Community aufzubauen:

1. Eine Open Source Lizenz;
2. Eine `README` Datei;
3. Richtlinien beisteuern; und
4. Ein Verhaltenskodex.

Dies sind wichtige Aspekte und Best Practices eines Projekts, damit Benutzer ihre gesetzlichen Rechte, ihre Erwartungen und den Zweck des Projekts verstehen und die Nutzererfahrung insgesamt verbessern können.

Alle vier Dateien sollten sich im Stammverzeichnis Ihres Projekt-Repository befinden. Es ist üblich, für die meisten dieser Dateien Abschriften-Dateiformate (`.md`) zu verwenden (obwohl es sich bei der Lizenzdatei meistens um einfachen Text (`.txt`) handelt) und alle Dateinamen in Großbuchstaben zu schreiben. Verwenden Sie anstelle von Leerzeichen in Dateinamen Unterstriche `_`.

Am Ende sollten Sie also eine grundlegende Dateiauswahl treffen:

1. `LIZENZ.md`
2. `README.md`
3. `BEITRAG.md`
4. `CODE_OF_CONDUCT.md`

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/foundation.png?raw=true" width="800" /></p>

<p align="center"><i>Die grundlegende Repository-Struktur</i></p>

  


### Lizenz auswählen <a name="License"></a>

Die Auswahl einer geeigneten Lizenz unterscheidet Ihr Open Source-Repository von öffentlich verfügbarer Software. Sie sind zwar nicht verpflichtet, eine Lizenz zu wählen, dies garantiert jedoch, dass andere Ihr Projekt innerhalb eines gesetzlichen Rahmens ändern, teilen, wiederverwenden und darauf aufbauen können.

Zunächst möchten Sie [auswählen. Wählen Sie Lizenz](https://choosealicense.com/) , um eine Lizenz zu finden, die Ihren Absichten für das Repository am besten entspricht.

Die drei wichtigsten sind:

* **MIT-Lizenz**: Eine zulässige Lizenz, mit der Personen mit Ihrem Code tun können, was sie wollen, solange sie Ihnen die entsprechende Zuordnung geben, und Sie nicht haftbar machen.
* **Apache License 2.0**: Entspricht den Berechtigungen der MIT-Lizenz, bietet jedoch auch die ausdrückliche Gewährung von Patentrechten von Mitwirkenden an Benutzer.
* **GNU General Public License (GPL) v3**: Eine [Copyleft-](https://en.wikipedia.org/wiki/Copyleft) Lizenz, bei der jeder, der Ihren Code oder ein abgeleitetes Werk weitergibt, verpflichtet ist, die Quelle unter denselben Bedingungen wie die ursprüngliche Lizenz zur Verfügung zu stellen. bietet auch eine ausdrückliche Gewährung von Patentrechten von Mitwirkenden an Benutzer.

Zum Glück haben Sie beim Starten eines neuen Repositorys auf GitHub die Möglichkeit, eine vorhandene Lizenz aus einem Dropdown-Menü auszuwählen. Sie sollten immer (mit sehr wenigen Ausnahmen) eine vorhandene Lizenz verwenden, da dies potenziellen Benutzern und Mitwirkenden angezeigt wird, bevor sie sich entscheiden, Ihre Software zu verwenden oder Beiträge zu leisten.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/license.png?raw=true" width="800" /></p>

<p align="center"><i>Beispiellizenz auswählen</i></p>

  


Wenn sie keine haben, die Sie möchten, können Sie manuell eine hinzufügen, die Sie möchten. Klicken Sie dazu einfach im Repository auf "Neue Datei erstellen" und kopieren Sie einen vorhandenen Lizenztext und fügen Sie ihn ein. Benennen Sie die Datei wie `LICENSE.txt` oder `LICENSE.md` , um dies zu verdeutlichen, und bewahren Sie sie im Hauptverzeichnis auf (dh im Stammverzeichnis). Stellen Sie sicher, dass Sie eine saubere Commit-Nachricht hinzufügen, und Sie sind fertig!

> **Helfende Hand**: Dieses MOOC verwendet eine andere Kombination von Lizenzen für Code-Inhalte und Nicht-Code-Inhalte. Hier finden Sie ein Beispiel für die [MIT-Lizenz](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/LICENSE.md) , die wir für den gesamten Code und die Software anwenden, die im Rahmen der MOOC-Produktion generiert wurden.

  


### Erstellen einer Readme-Datei <a name="Readme"></a>

Wenn Sie Ihr neues Repository initialisieren, sollte es eine Option geben, dies mit einer `README` Datei zu tun. Genau wie Alice im Wunderland tun diese genau das, was sie sagen - sie liefern wichtige Informationen über das Projekt. Dies ist normalerweise das Erste, was externe Autoren sehen, wenn sie in Ihr Repository gelangen. Daher ist es wichtig, sie informativ und einladend zu gestalten.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/readme.png?raw=true" width="800" /></p>

<p align="center"><i>Teil der README-Datei für dieses Modul</i></p>

  


Die Datei hat ursprünglich das Format Markdown (`.md`). Dies ist eine einfache Auszeichnungssprache mit einem Nur-Text-Format. Um einige grundlegende Abschlags, sehen lernen [dieses Spickzettel](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet). Im Moment können wir jedoch nur einfachen Text verwenden.

Es gibt mehrere Dinge, die Sie in Ihre `README` Datei aufnehmen möchten:

* Worum geht es in diesem Projekt und was macht es?
* Warum sollte es die Leute interessieren und warum ist es nützlich?
* Wie kann jemand anfangen, zu dem Projekt beizutragen?
* An wen kann man sich wenden, wenn jemand Hilfe benötigt?
* Ein Link zur Lizenz, den dazugehörigen Richtlinien und dem Verhaltenskodex.
* Eine Beschreibung der Projektstruktur.
* Wer ist beteiligt und welche Rollen haben sie?
* Der aktuelle Status des Projekts.

> **Pro-Tipp**: Wenn sich Ihr Projekt später weiterentwickelt, möchten Sie möglicherweise häufig gestellte Fragen (FAQs) hinzufügen, die auf dem Feedback der Community basieren, oder ein Lernprogramm, mit dem Benutzer besser verstehen, wie Ihr Projekt funktioniert.

Denken Sie daran, dass nicht jeder, der zu Ihrem Projekt kommt, ein Experte ist oder versteht, was Sie tun und warum. Eine gut dokumentierte `README` Datei verbessert das Benutzererlebnis für Personen mit einer Reihe von Vorkenntnissen.

Wenn die Datei `README` im Stammverzeichnis enthalten ist, zeigt GitHub dies automatisch auf der Startseite Ihres Repositorys an. Das heißt, es ist das erste, was die Leute oft sehen, also lass es zählen!

> **Helfende Hand**: Hier finden Sie die `README` Datei, die für dieses [MOOC-Modul](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/README.md). Dazu gehören Informationen zum Status, zur Begründung, zu den Lernergebnissen, zum Entwicklungsteam, zu Schlüsseldokumenten und zur Lizenz zur Unterstützung. Sie können diese Struktur nach Bedarf kopieren und für Ihre eigenen Projekte anpassen.

  


### Mitwirkende Richtlinien erstellen <a name="Contributing"></a>

Mitwirkende Richtlinien sollen potenziellen Mitwirkenden einen kurzen Leitfaden zur Einbindung in Ihr Projekt und Ihre Community vermitteln. Sie möchten sicher gehen, dass Sie willkommen sind, und zeigen, dass Sie darauf bedacht sind, dass sich die Teilnehmer mit Ihrem Projekt befassen. Wenn ein Teilnehmer eine neue Pull-Anfrage öffnet oder eine neue Ausgabe erstellt, wird ihm ein Link zu Ihrer Beitragsdatei angezeigt.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/contributing.png?raw=true" width="800" /></p>

<p align="center"><i>Teil der "BEITRAG" -Richtlinien für dieses Modul</i></p>

  


Der nächste Schritt besteht darin, eine `CONTRIBUTING` Datei zu erstellen. Klicken Sie auf "Neue Datei erstellen" und stellen Sie sicher, dass Sie die Datei wie zuvor im Markdown-Format speichern. In dieser Datei erfahren andere Benutzer, wie sie mit Ihrem Projekt interagieren und an ihm teilnehmen können. Dies ist der erste Schritt zum Aufbau einer Community rund um Ihr Projekt. Machen Sie es ansprechend, prägnant und informativ.

Die Datei `CONTRIBUTING` sollte folgende Informationen enthalten:

* Welche Art von Beiträgen suchen Sie?
* So schlagen Sie Updates oder neue Funktionen vor.
* Interaktion mit dem Projekt mithilfe der Funktionen von GitHub (z. B. dem Pull-Request-Protokoll).
* Wie erstelle ich einen Fehlerbericht oder erstelle ein Problem?
* Das ultimative Ziel, die Vision oder die Roadmap für das Projekt.
* Kontaktaufnahme mit den Projektverantwortlichen.
* Links zu externen Dokumentationen oder Websites.

> **Pro-Tipp**: Beginnen Sie mit einem kurzen Dankeschön, damit sich die Leute die Zeit nehmen, einen Beitrag zu leisten - sie haben auf die Datei geklickt, um schließlich mehr zu erfahren! Wenn Sie andere Erkennungsmethoden in Betracht ziehen, sollten Sie diese auch hier berücksichtigen.

Sie versuchen hier im Wesentlichen, die Menschen dazu zu ermutigen, ihre Zeit freiwillig zu nutzen, um Ihr Projekt voranzutreiben. Seien Sie herzlich und freundlich und zeigen Sie genau, wie die Leute sich engagieren können. Denken Sie beim Verfassen dieses Dokuments unbedingt aus der Benutzerperspektive darüber nach. Wie können Sie die Arbeit erleichtern, wenn Sie Pull-Anforderungen senden und Probleme öffnen, damit das gesamte Projekt reibungsloser abläuft.

> **Helping Hand**: Die [Contributing-Richtlinien](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CONTRIBUTING.md) für dieses MOOC-Modul enthalten einige sehr spezifische Dinge: eine Einführung in die Verwendung von Git und GitHub, Tipps für den Einstieg, Kontaktinformationen, Ändern des Inhalts und Berichterstellungsprobleme, einen Link zu der `README` Datei und Informationen zu den bevorzugten Inhalten und Codestilen. Sie können diese nach Bedarf kopieren und für Ihr eigenes Projekt anpassen.

  


### Verhaltenskodex erstellen <a name="Conduct"></a>

Ein Verhaltenskodex ist wichtig, um die Grundregeln für das erwartete Verhalten und die Teilnahme von Projektmitarbeitern festzulegen. Er ist ein leicht zu verweisendes Dokument, um zu zeigen, dass Ihr Projektteam konstruktive Dialoge ernst nimmt. Daher ist es ein entscheidendes Element für die Schaffung und Aufrechterhaltung einer gesunden Gemeinschaft, die sich konstruktiv und produktiv in einer positiven sozialen Atmosphäre engagiert.

Ein Verhaltenskodex enthält nicht nur Verhaltenserwartungen, sondern beschreibt auch, für wen diese Erwartungen gelten, wann sie gelten, was bei einem Verstoß gegen den Kodex zu tun ist und welche Maßnahmen diesbezüglich erforderlich sind. Daher müssen die Kontaktstellen im Verhaltenskodex klargestellt werden. In der Regel sollte dies privat erfolgen, z. B. als E-Mail-Adresse.

> **Pro-Tipp**: Falls ein Verstoß gegen die Person gemeldet werden muss, die diese Berichte erhält, stellen Sie sicher, dass Sie die Option haben, eine sekundäre Partei zu kontaktieren.

Um einen Verhaltenskodex hinzuzufügen, können Sie durch Hinzufügen einer neuen Abschriftendatei einen eigenen erstellen oder vorhandene Vorlagen verwenden, z. B. den [Contributor Covenant](https://contributor-covenant.org/). Nennen Sie Ihre Datei `CODE_OF_CONDUCT.md`und stellen Sie sicher, dass sie in der `README` Datei sichtbar ist.

> **Helfende Hand**: Dieses MOOC hat auch einen [Verhaltenskodex](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CODE_OF_CONDUCT.md) der auf dem Beitrittsvertrag basiert. Wie Sie sehen können, enthält es Informationen zu den erwarteten Verhaltensstandards, den Verantwortlichkeiten der Community und der Durchsetzung des CoC, einschließlich der Kontaktdaten. Sie können es jederzeit wieder verwenden und an Ihr Projekt anpassen.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/code_of_conduct.png?raw=true" width="800" /></p>

<p align="center"><i>Teil der CODE OF CONDUCT-Datei für dieses Modul, basierend auf dem Contributor Covenant</i></p>

  


Es ist wichtig, den Verhaltenskodex durchzusetzen, da dies zeigt, dass Sie nicht nur den Kodex schätzen, sondern auch den Einfluss respektieren, den er auf Ihre Community hat. Es ist wichtig, jedes Mitglied der Gemeinschaft mit dem Respekt, der Höflichkeit und der Wichtigkeit zu behandeln, die es verdient. Sollte ein Verstoß auftreten oder ein Wiederholungstäter konsequente Verstöße begehen, lesen Sie am besten den [Open Source Guide](https://opensource.guide/code-of-conduct/#enforcing-your-code-of-conduct) , um zu erfahren, wie Sie den Verhaltenskodex durchsetzen können.

  


### Den Code zitierbar machen <a name="Citation"></a>

Wenn Sie Ihren Code von Anfang an zitierfähig machen möchten, sollten Sie die für eine Zitierung erforderlichen Metadaten von Anfang an speichern, indem Sie eine `[codemeta.json](https://codemeta.github.io)` Datei oder eine `[CITATION.cff](https: //citation-file-format.github.io)` Datei. In beiden Fällen können Tools, die derzeit entwickelt werden, automatisch Zitierinformationen erstellen, anstatt Sie zu bitten, diese später in ein Formular einzugeben.

Wenn Sie interessiert sind, bietet [cite.research-software.org](https://cite.research-software.org) weitere Hintergrundinformationen zum Zitieren von Software im akademischen Bereich.

  


## Halten Sie Ihre Probleme auf dem neuesten Stand <a name="Issues"></a>

Probleme sind nicht unbedingt Probleme mit einem Projekt, sondern auch Verbesserungsvorschläge, zukünftige Entwicklungen sowie Kommentare und Rückmeldungen zum durchzuführenden Projekt. Sie können nach Bedarf offen geteilt und mit den Mitwirkenden diskutiert werden, wie in einem Forum.

Wenn Sie ein Projektleiter sind, ist es wichtig, eine Liste von Themen zu führen, die den Mitwirkenden verdeutlicht, welche Aspekte des Projekts Aufmerksamkeit erfordern. Es ist auch wichtig, sich positiv mit möglichst vielen Themen anderer auseinanderzusetzen, um zu zeigen, dass Sie deren Beiträge ernst nehmen.

Wichtige Elemente für Probleme sind:

* Ein informativer Titel und eine Beschreibung;
* Coloud-codierte Labels / Tags zum Kategorisieren und Filtern;
* Meilensteine für die Zuordnung von Problemen zu bestimmten Funktionen oder Projektphasen;
* Die Beauftragten geben an, wer für die Bearbeitung eines Problems verantwortlich ist.
* Kommentare zur Rückmeldung.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/issues.png?raw=true" width="800" /></p>

<p align="center"><i>Der Issue Tracker für das Open Scholarship Strategy Projekt</i></p>

  


Innerhalb von Problemen ist es möglich, @ Erwähnungen zu verwenden, um andere Kontrahenten über das Problem zu informieren und die richtigen Personen auf effektive Weise zu gewinnen. GitHub verfügt über ein internes Benachrichtigungssystem wie Facebook oder Twitter und kann auch E-Mails an Personen senden, die im Issue Tracker erwähnt werden. Dies kann alles für Einzelpersonen in den Benutzereinstellungen angepasst werden.

  


## Checkliste zum Starten Ihres Projekts <a name="Checklist"></a>

Jetzt können Sie Ihr Projekt starten, Werbung schalten und Beiträge erhalten! Bevor Sie fortfahren, stellen Sie sicher, dass Sie:

* [] Das Projekt hat einen einprägsamen und informativen Namen
* [] Project hat eine `LICENSE` Datei, die eine exakte Kopie einer Open Source-Lizenz ist
* [] Vollständige Dokumentation mit den Dateien `README`, `CONTRIBUTING`und `CODE_OF_CONDUCT`
* [] Das Projekt weist mindestens ein eindeutig gekennzeichnetes Problem auf
* [] Jeder in dieser Phase enthaltene Code ist klar strukturiert und mit Anmerkungen versehen

**HERZLICHE GLÜCKWÜNSCHE!**

Sie haben jetzt ein Open Source-Forschungsprojekt gestartet! Hoffentlich wird Ihre Arbeit von nun an der breiteren Community zugute kommen, neue Kooperationen schmieden und neue und fantastische Möglichkeiten für Sie alle schaffen. Überlegen Sie, wie diese Fähigkeiten in zukünftigen Projekten eingesetzt werden können und wie sie in der Vergangenheit möglicherweise auch bei einigen geholfen haben.

Ab sofort liegt es an Ihnen! Einige Ratschläge sind:

* Schreiben Sie sauberen Code.
* Haben Sie ein gut strukturiertes Projekt;
* Machen Sie häufige Commits mit sauberen Nachrichten.
* Halten Sie Projekte gut dokumentiert;
* Klare beitragende Richtlinien haben;
* Nutzen Sie die Beschreibungs- und Tag-Funktionen.
* Verzweigen Sie nicht das Repository einer anderen Person, es sei denn, Sie beabsichtigen, daran zu arbeiten.
* Stellen Sie sicher, dass Sie auch Beiträge für andere Projekte leisten.

**Wissen Sie, wie dieser Inhalt verbessert werden kann?**

Zeit, deine neuen GitHub-Fähigkeiten für einen Testlauf zu nutzen! Alle Inhalte Entwicklung geschieht in erster Linie [hier](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md). Wenn Sie Verbesserungsvorschläge zu Inhalt, Layout oder etwas anderem haben, können Sie diese vornehmen. Nach Überprüfung durch einen Moderator wird sie automatisch Teil des MOOC-Inhalts!

[![CC0 Public Domain Widmung](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)