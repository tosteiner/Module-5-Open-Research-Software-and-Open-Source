---
output:
  html_document: Standard
  pdf_document: Standard
---

# Aufgabe 3: So integrieren Sie Git in R Studio

Diese Aufgabe richtet sich an Studenten und Forscher, die ein Versionskontrollsystem in einem standardmäßigen R-basierten Workflow implementieren möchten. Dies kann auf eine Reihe von Aufgaben in den Bereichen Softwareentwicklung, Datenanalyse und Projektmanagement angewendet werden. Ihr zukünftiges Forschungsunternehmen wird sich bei Ihnen für die Bequemlichkeit bedanken.

Vergiss nicht, dass du in unserem offenen [**Slack Channel**](https://osmooc.herokuapp.com/)mitdiskutieren kannst. Bitte stellen Sie sich unter # module5opensource vor und erzählen Sie uns, wer Sie sind, welchen Hintergrund Sie haben und wie Sie hier gelandet sind!

Geschätzte Bearbeitungszeit: 30 Minuten

Geschätzte Zeitersparnis nach Abschluss: Praktisch unendlich

**HINWEIS** Eine Video-Guide-Version dieser Aufgabe ist jetzt auf [YouTube](https://www.youtube.com/watch?v=Q-6jfjSAspA)verfügbar.

## Inhaltsverzeichnis

* [Fertig machen](#Getting_started) 
  * [Git](#Git)
  * [R Studio](#Rstudio)
* [Schritt eins: Laden Sie alle Dinge herunter](#one)
* [Schritt zwei: Konfigurieren Sie Git in RStudio](#two)
* [Schritt drei: Warum habe ich das gerade getan?](#three)
* [Schritt vier: Die perfekte Ehe zwischen Git und R](#four)
* [Schritt fünf: Inhalte mit Inhalten erhalten](#five)
* [Schritt sechs: Eine mutige Verpflichtung](#six)
* [Schritt sieben: DRÜCKEN!](#seven)

## Fertig machen <a name="Getting_started"></a>

Herzlichen Glückwunsch, dass Sie es so weit gebracht haben! Wenn Sie dies lesen, haben Sie Pull-Requests und Web-Hooks überlebt und können uns wahrscheinlich sogar sagen, wofür das F in FOSS steht (** Frustration ...). Hoffentlich haben Sie jede Skepsis oder Zurückhaltung überwunden auf die Vorteile von GitHub und Open Source Software zu und sind bereit, den nächsten Schritt zu tun.

Bevor Sie mit dieser Aufgabe beginnen, vergewissern Sie sich, dass Sie [Aufgabe 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) und [Aufgabe 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), damit Sie mit GitHub und einigen Standard-Open-Source-Methoden besser vertraut sind.

In dieser Übung lernen Sie, wie Sie die Versionskontrollsoftware Git in die beliebte Codierungsumgebung RStudio integrieren. Und ja, es ist Git wie in gif oder Gott, nicht Jit wie in der falschen Art, Dinge auszusprechen.

Wenn Sie zu den Forschern gehören, die der Meinung sind, dass sich der Code auf mehrere Festplatten verteilt, die darauf warten, beschädigt zu werden, Dropbox, Google Drive oder eine andere nicht spezialisierte Software, ist diese Aufgabe nur für Sie. Wenn Sie jemals den irrsinnigen Prozess erlebt haben, mehrere "endgültige" Versionen eines Papiers zu haben, die zwischen verschiedenen Co-Autoren hin und her springen, ist dies auch für Sie.

Von Zeit zu Zeit sind wir alle an solchen Dingen schuld, aber es gibt Möglichkeiten, die für Sie, Ihre Zukunft und diejenigen, die von Ihrer Arbeit profitieren könnten, besser sind.

  


### Git bekommen <a name="Git"></a>

Was ist Git und wie unterscheidet es sich von GitHub? Git ist ein Versionskontrollsystem, mit dem Sie zeitgestempelte Kopien Ihrer Arbeit während des gesamten Entwicklungsprozesses speichern und verfolgen können. Es funktioniert auch mit Nicht-Code-Elementen wie diesem MOOC, von denen der größte Teil in Markdown in RStudio geschrieben und in einen Git / GitHub-Workflow integriert wurde.

Dies ist wichtig, da jede Forschung Veränderungen durchläuft und wir manchmal wissen möchten, was diese Dinge waren. Haben Sie einen Text gelöscht, den Sie jetzt für wichtig halten? Die Versionskontrolle speichert das für Sie. Hat Ihr Code in der Vergangenheit perfekt funktioniert, ist er jetzt aber unglaublich fehlerhaft? Versionskontrolle. Dies ist eine großartige Möglichkeit, um diesen chaotischen Zustand zu vermeiden, in dem Sie mehrere Kopien derselben Datei haben, jedoch ohne eine dumme und lästige Konvention zur Benennung von Dateien. `FINAL_Revised_2.2_supervisor_edits_ver1.7_scream.txt` der Vergangenheit an.

GitHub ist die Plattform, mit der Sie Code nahtlos von Ihrem Arbeitsbereich (z. B. Laptop) aus freigeben können, um ihn in einem Online-Bereich zu hosten. So ähnlich wie die öffentliche Schnittstelle zu GitHub. Die Vorteile von Git / GitHub sind:

1. Sie können Kopien aller Ihrer Arbeiten im Laufe der Zeit aufbewahren.
2. Sie können die Arbeit anhand verschiedener Kopien im Laufe der Zeit vergleichen, um Fehler oder Fehler zu erkennen.
3. Andere Personen können offen mit Ihrer Arbeit zusammenarbeiten.
4. Sie haben sowohl eine lokale als auch eine Online-Kopie Ihrer Arbeit, die synchron bleiben.
5. Es ist völlig transparent, wer einen Beitrag geleistet hat, warum und wann er geleistet wurde. und
6. Sie können mehrere Personen gleichzeitig an einem Projekt arbeiten lassen.

Obwohl dies in erster Linie für Quellcode gedacht war, sollte sofort klar sein, wie dies ein leistungsstarkes Werkzeug für praktisch alle Forschungsworkflows wird.

  


### RStudio <a name="Rstudio"></a>

RStudio ist eine beliebte Codierungsumgebung für Forscher, die die statistische Programmiersprache R verwenden. Es wird mit einem Texteditor geliefert, sodass Sie keinen weiteren installieren und zwischen diesen wechseln müssen. Es enthält auch eine grafische Benutzeroberfläche (GUI) für Git und GitHub, die wir hier verwenden werden.

Ist es nicht schön, wenn sich so brillante Open Source-Tools nahtlos integrieren lassen? Dies sollte Ihnen helfen, den täglichen Gebrauch von Git zu vereinfachen.

Wenn Sie zu irgendeinem Zeitpunkt neue Pakete für R installieren müssen, verwenden Sie einfach den folgenden Befehl:

`install.packages ("PACKAGE NAME", Abhängigkeiten = TRUE)`

Ersetzen von `PAKETNAME` durch den Namen des Pakets. Einige Beispiele, mit denen Sie spielen können, könnten nützlich sein: `knitr`, `devtools` oder `ggplot2`.

  


## Schritt eins: Laden Sie alle Dinge herunter <a name="one"></a>

1. Sie sollten bereits ein GitHub-Konto haben, wenn Sie die vorherigen Aufgaben ausgeführt haben. Wenn nicht, [anmelden](https://github.com/). Kostenlose unbegrenzte Repositories für alle!
2. Laden Sie die neueste Version von [R](https://www.r-project.org/)herunter und installieren Sie sie. Auch für [Mac](https://cloud.r-project.org/) und [Linux](https://cloud.r-project.org/bin/linux/)verfügbar.
3. Laden Sie die neueste Version von [Rstudio](https://www.rstudio.com/products/rstudio/#Desktop)herunter und installieren Sie sie. Oh, hey, sieht nach Open Source aus! Swish.
4. Laden Sie die neueste Version von [Git](https://gitforwindows.org/)herunter und installieren Sie sie. **Stellen Sie sicher, dass Sie während der Installation "Git von der Windows-Eingabeaufforderung verwenden" auswählen.**

> **Pro-Tipp**: Um alle R-Pakete in einem zu aktualisieren, führen Sie einfach den folgenden Code `update.packages aus (ask = FALSE, checkBuilt = TRUE)`

Wählen Sie vorerst einfach alle üblichen Standardoptionen für jede Installation aus. Je nach Betriebssystem (z. B. Mac, Windows, Linux) kann dies für jeden von Ihnen unterschiedlich sein. Im Moment und für den Rest dieser Aufgabe werden wir die Dinge auf einfache Windows-Art erledigen (aber auch einige Anweisungen für die Verwendung der Befehlszeile bereitstellen).

Verwenden Sie für Linux- oder Debian-Benutzer einfach den folgenden Befehl, um Git zu installieren:

`sudo apt-get installiert git-core`

Für Mac - Anwender [Link](http://git-scm.com/download/mac), oder einen neuen Laptop mit einem anderen Betriebssystem erwerben.

Wenn Sie möchten, können Sie auch die lokale Version [von GitHub](https://desktop.github.com/) herunterladen und über die einfache Benutzeroberfläche verwenden. Es ist für Windows, Mac und Linux verfügbar und kann Ihnen das Leben ein wenig erleichtern, insbesondere wenn Sie eine andere Plattform als RStudio verwenden möchten.

> **Pro-Tipp:** Sie sehen, wenn Sie Git installieren: "Git Bash als Shell für Git-Projekte verwenden?" Hier können Sie über die Befehlszeile von außerhalb von RStudio auf Git zugreifen. Es ist ein mächtiges Tier. Probieren Sie die folgenden zwei Befehle aus, um zu beginnen:

`git config --global benutzername 'IHR BENUTZERNAME'`   
`git config --global benutzername 'IHR EMAIL'`   


## Schritt zwei: Konfigurieren Sie Git in RStudio <a name="two"></a>

Richtig, das ist das leichte Stück. Rufen Sie als Nächstes RStudio auf und klicken Sie in den Registerkarten oben auf Gehe zu **Extras> Globale Optionen> Git / SVN**. SVN ist nur ein weiteres Versionskontrollsystem wie Git, und darüber brauchen wir uns hier keine Gedanken zu machen.

Fügen Sie an der Stelle, an der *Git executable*steht, den Pfad hier zur Datei git.exe hinzu, die Sie gerade im vorherigen Schritt heruntergeladen haben. Vergewissern Sie sich, dass das Kontrollkästchen **Versionskontrollschnittstelle für RStudio-Projekte aktivieren** aktiviert ist. Dies hat nun die Versionskontrolle mit zukünftigen Projekten in RStudio verknüpft, um eine wirklich leistungsstarke zusätzliche Dimension für die Zusammenarbeit oder die Einzelarbeit bereitzustellen.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/git_svn.png?raw=true" width="400px"/>
</p>

<p align="center"><i>Das Fenster "Globale Optionen" in RStudio</i></p>

  


Klicken Sie anschließend in diesem Fenster auf die Schaltfläche *RSA-Schlüssel erstellen*Dies ist ein privater Schlüssel, der für die Authentifizierung zwischen verschiedenen Systemen verwendet wird, und erspart Ihnen die wiederholte Eingabe Ihres Kennworts. Hier öffnet sich ein neues Fenster mit einem öffentlichen Schlüssel, den Sie in Ihre Zwischenablage kopieren möchten.

Gehen Sie zu GitHub, gehen Sie zu Ihren Profileinstellungen und zur Registerkarte *SSH- und GPG-Schlüssel*. Klicken Sie auf *Neuer SSH-Schlüssel*. Fügen Sie hier den Schlüssel aus RStudio ein und nennen Sie ihn etwas Fantasievolles wie "RStudio".

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/ssh_key.png?raw=true" width="800px"/>
</p>

<p align="center"><i>In GitHub, wo Sie den Schlüssel eingeben möchten, den Sie gerade in RStudio generiert haben</i></p>

  


OK, jetzt halt deine Ärsche fest, wir gehen in die Befehlszeile. Machen Sie sich keine Sorgen, wenn Sie die Shell noch nie zuvor verwendet haben, da sie der Verwendung von R oder einem anderen Codierungssystem sehr ähnlich ist. Der Hauptunterschied besteht darin, dass Sie, anstatt Funktionen wie in R aufzurufen, Befehle aufrufen.

Gehen Sie also zurück in RStudio zu **Tools> Shell**und es wird ein Eingabeaufforderungsfenster geöffnet. Wenn Sie oben bereits mit Git Bash gespielt haben, sollten Sie diesen Schritt bereits ausgeführt haben. Geben Sie die folgenden zwei Befehle ein:

`git config --global benutzername 'IHR BENUTZERNAME'`   
`git config --global benutzername 'IHR EMAIL'`   


Hoffentlich muss nicht gesagt werden, dass Sie hier Ihren eigenen GitHub-Benutzernamen und Ihre E-Mail-Adresse einsetzen müssen. Sie können jederzeit darauf zugreifen, indem Sie die 'Shell' in Windows suchen. Wenn Sie mit der rechten Maustaste auf einen Ordner auf Ihrem Desktop klicken, der mit einem GitHub-Repo verknüpft ist, können Sie die Shell sofort öffnen und mit Bash away versehen.

In dieser Phase wurde Git (Software, die auf Ihrem Desktop ausgeführt wird) für GitHub (eine Repository-Website) konfiguriert.

Starten Sie R Studio neu. Puh, das war hart. Nächster.

  


## Schritt drei: Warum habe ich das gerade getan? <a name="three"></a>

OK, atme durch, wir machen hier eine Pause, um ein paar grundlegende Git-Befehle zu lernen. Einige der wichtigsten Dinge, die Sie mit dem Lernen tun könnten, sind:

* **Add**: Hierüber senden Sie Dateien an den Staging-Bereich, bevor Sie festgeschrieben werden.

* **Commit** Dies ist wie das 'Speichern' Ihrer Arbeit durch Erstellen einer neuen Version oder Kopie.

* **Push**: So senden Sie Dateien aus Ihrem lokalen Projekt an das Online-Repository.

* **Pull**: So bringen Sie Dateien aus Ihrem Online-Repository in Ihr lokales Projekt.

Geben Sie in RStudio Folgendes in das *Terminal*oder öffnen Sie eine neue Shell:

`Git hinzufügen.`

Derzeit wird eigentlich nichts unternommen, aber in Zukunft werden alle Dateien in Ihrem aktuellen Arbeitsverzeichnis (das ist es, was die `` tut) zur Bereitstellung für ein Commit hinzugefügt.

  


## Schritt vier: Die perfekte Ehe zwischen Git und R <a name="four"></a>

In Aufgabe 1 sollten Sie nun gelernt haben, wie Sie Ihr erstes GitHub-Repository erstellen. Wenn Sie das nicht getan haben, können wir hier warten, während Sie das tun. Wenn Sie bereits ein GitHub-Repository haben oder über ein solches verfügen, können wir fortfahren.

Sie sollten also ein Repository auf GitHub haben, das eine `README` Datei, eine `LICENSE` Datei und einige andere Informationen enthält.

Was wir jetzt tun werden, ist das Repository in Git zu integrieren. Jetzt fest.

1. Gehen Sie zunächst zu **Projekt> Projekt erstellen> Versionskontrolle> Git**.
2. Zurück auf GitHub sollten Sie ein bisschen sehen, wo es eine https: // URL gibt. Dies ist der Link zu Ihrem Repository und bietet Ihnen die Möglichkeit, es auf Ihrem Desktop zu klonen. Kopieren Sie zunächst diesen Link, wechseln Sie zurück zu RStudio und fügen Sie ihn wie angegeben in die 'Repository-URL' ein.
3. Geben Sie dem Projekt einen Verzeichnisnamen wie test, Jim oder was auch immer Sie möchten.
4. Suchen Sie als Nächstes auf Ihrem Desktop nach dem Ort, an dem das Projekt gespeichert werden soll, dh nach dem Unterverzeichnis.
5. Klicken Sie auf "Projekt erstellen" und lassen Sie die Magie erledigen!

Sie haben gerade RStudio angewiesen, ein neues Projekt in R mit einem bestimmten Repository auf GitHub zu verknüpfen.

## **Schritt vier: Alternative**

Wenn Sie Ihr erstes Repository noch nicht auf GitHub erstellt haben, können wir hier etwas anderes tun. Klicken Sie in RStudio auf *Neues Projekt* und dann auf *Neues Verzeichnis*. Nennen Sie es, wie Sie möchten, und ändern Sie das Verzeichnis nach Bedarf. Kreuzen Sie *Create a git repository*an und klicken Sie dann auf *Create Project*. Dadurch wird eine `.Rproj` Datei erstellt, die Sie auf die in RStudio übliche Weise verwalten können, einschließlich des Hinzufügens von `README.md`und `LICENSE.md` Dateien, wie in Aufgabe 1 erläutert.

## Schritt fünf: Inhalte mit Inhalten erhalten <a name="five"></a>

Denken Sie daran, dass wir vor einiger Zeit `README` Dateien erstellt haben? Nun, es ist Zeit, es zu schreiben. Denken wir zurück an Aufgabe 1, gab es einige spezifische Dinge , die sagten , dass wir eine gute machen `README` - Datei. Erinnerst du dich, was einer von ihnen war? Nur um Ihr Gedächtnis aufzufrischen, waren dies:

* Worum geht es in diesem Projekt und was macht es?
* Warum sollte es die Leute interessieren und warum ist es nützlich?
* Wie kann jemand anfangen, zu dem Projekt beizutragen?
* An wen kann man sich wenden, wenn jemand Hilfe benötigt?
* Ein Link zur Lizenz, den dazugehörigen Richtlinien und dem Verhaltenskodex.
* Eine Beschreibung der Projektstruktur.
* Wer ist beteiligt und welche Rollen haben sie?
* Der aktuelle Status des Projekts.

Öffnen Sie diese Datei in RStudio und fügen Sie nur einige Informationen zu diesem Thema für Ihr Projekt hinzu. Wenn Sie dies für ein tatsächliches Projekt tun, versuchen Sie es nützlich zu machen. Wenn Sie gerade basteln, können Sie hinzufügen, was Sie wollen.

Denken Sie daran, dass Ihre `README` Datei im Markdown-Format (.md) vorliegt. Um eine Auffrischung über einige der einfachen Syntax-Markdown-Funktionen zu erhalten, lesen Sie das [handliche Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/markdown.png?raw=true" width="600px"/>
</p>

<p align="center"><i>Screenshot davon, wie dieses Modul während der Entwicklung in Markdown aussieht. Meta.</i></p>

  


## Schritt sechs: Eine mutige Verpflichtung <a name="six"></a>

OK, jetzt solltest du eine schön bearbeitete `README` Datei haben. Jetzt werden wir dies mit Git für das Projekt "festschreiben". Dies entspricht im Wesentlichen dem Speichern dieser Version Ihres Projekts, wobei aufgezeichnet wird, welche Änderungen vorgenommen wurden. Aufeinanderfolgende Commits erstellen einen Verlauf, der zu einem späteren Zeitpunkt überprüft werden kann, sodass Sie sicher arbeiten können.

Hierfür gibt es verschiedene Möglichkeiten.

1. Gehen Sie zu **Tools> Versionskontrolle> Commit**
2. Im Umgebungsfenster von RStudio sollte sich eine neue Registerkarte "Git" befinden. Praktisch.
3. In Ihrem Konsolenfenster sollte sich jetzt ein neues 'Terminal' befinden, über das Sie Git-Befehlszeilen ausführen können.

Bleiben wir vorerst bei der zweiten Option. Dieser Git-Bereich zeigt Ihnen, welche Dateien geändert wurden, und enthält Schaltflächen für die wichtigsten Git-Befehle, die wir zuvor gesehen haben.

Wählen Sie im Git-Fenster die Datei `README` , die automatisch angezeigt werden soll, wenn Sie Änderungen daran vorgenommen haben. Auf diese Weise wird diese Datei zum Staging-Bereich hinzugefügt. Dies entspricht in etwa dem Platz, den Sie vor dem Speichern für Ihre Arbeit benötigen. Klicken Sie auf "Übernehmen" und ein neues Fenster sollte sich öffnen.

Hier haben Sie die Möglichkeit, Ihre Änderungen zu überprüfen und eine nette Commit-Nachricht zu schreiben. Geben Sie einen kurzen, aber informativen Text über die Änderungen ein, die Sie an dieser Version oder an Ihrem Schnappschuss vorgenommen haben. Sie möchten, dass dies genügend Informationen sind, damit Sie oder andere Personen wissen, warum Sie dieses Commit durchgeführt haben und welche Änderungen damit verbunden sind. Dies sind wie Sicherheitsnetze für Ihr Projekt, falls Sie aus irgendeinem Grund zurückgreifen müssen.

> **Pro-Tipp**: Hier sehen Sie eine Liste aller Änderungen, die Sie seit Ihrem letzten Commit vorgenommen haben. Ältere entfernte Linien sind rot und neu hinzugefügte Linien sind grün. Überprüfen Sie diese nochmals, um sicherzustellen, dass Sie die gewünschten Änderungen vorgenommen haben. Dies ist sehr hilfreich, um Tippfehler, fehlerhafte Bearbeitungen und andere kleine Fehler zu erkennen, die Sie möglicherweise versehentlich eingeführt haben. Sicherheit zuerst.

**Hinweis** Wenn Sie farbenblind sind und nicht sehen können, welche Zeilen hinzugefügt oder entfernt wurden, können Sie die Zeilennummern in den beiden Spalten links im Fenster als Richtlinie verwenden. Hierbei kennzeichnet die Nummer in der ersten Spalte die ältere Version und die Nummer in der zweiten Spalte die neue Version.

Wenn Sie nun auf "Übernehmen" klicken, wird ein weiteres Fenster geöffnet, in dem angezeigt wird, wie viele Dateien Sie geändert haben und wie viele Zeilen in dieser Datei Sie geändert haben. Mach das kleine Fenster zu.

  


## Schritt sieben: DRÜCKEN! <a name="seven"></a>

Klicken Sie oben rechts im neuen Fenster auf die Schaltfläche *Push*. Ein neues Fenster öffnet sich. Dabei werden die in Ihrem lokalen Repository geänderten Dateien mit der Datei `README` in die Online-Version des Projekts auf GitHub synchronisiert.

Verwenden Sie dazu in der Shell den folgenden Befehl:

`Git Push -u Ursprungsmaster`

Manchmal werden Sie hier aufgefordert, Ihren Benutzernamen und Ihr Passwort von GitHub hinzuzufügen. Dies sollten Sie tun, wenn Sie dazu aufgefordert werden.

Schließe das Fenster und das nächste. Gehen Sie auf GitHub zu Ihrem Projekt, aktualisieren Sie es und überprüfen Sie, ob die Datei `README` in all ihrem neu bearbeiteten Glanz noch vorhanden ist. Sie sollten die Commit-Nachricht, die Sie gemacht haben, auch neben der Datei sehen.

  


**OPTIONAL ADVANCED / AWESOME STEP**

Okay, du hast gerade ein paar Inhalte in dein erstes Repo gepusht, großartig! Lassen Sie es uns nun für ein reales Projekt in die Praxis umsetzen. Wie die, an der du gerade teilnimmst. Probieren wir das mal aus:

1. Gehen Sie zum Repository für dieses Projekt auf [GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source)

2. Verzweigen Sie das Repository in Ihr eigenes GitHub-Konto. Die URL dafür sollte lauten: `https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source.git`

3. Rufen Sie RStudio auf, gehen Sie zu **Datei> Neues Projekt**, wählen Sie *Versionskontrolle*, wählen Sie *Git*und fügen Sie dann die gegabelte Repository-URL ein, die Sie in Ihrer Kopie des Repository gefunden haben. Sie haben jetzt Ihre eigene versionierte Kopie dieses gesamten Moduls. Ordentlich. Speichern Sie dies irgendwo auf Ihrem lokalen Computer.

4. Jetzt müssen Sie Git mitteilen, dass eine andere Version dieses Projekts vorhanden ist. Öffnen Sie die *Shell*und geben Sie den folgenden Befehl ein: `git remote add upstream https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source`

5. Was Sie soeben getan haben, war, den ursprünglichen Zweig hier als `vor`, um die Dinge vorerst einfach zu halten. Erstellen Sie nun einen neuen **Zweig** , um Ihre Änderungen an diesem Zweig unabhängig vom Hauptzweig zu dokumentieren. Geben Sie den Befehl ein: `git checkout -b vorschlagsänderungen master`

6. Sie haben soeben einen neuen Zweig mit dem Namen `vorgeschlagen-Änderungen` in dem Sie nun alle Inhalte und Dateien nach Herzenslust bearbeiten können. Hoffentlich ist die Struktur dieses Projekts so einfach, dass Sie darin navigieren können. Alle Rohdateien für das MOOC befinden sich im Ordner `content_development` , und dies ist `Task_3.md`.

7. Wenn Sie bis zum Ende von `Task_3.md`scrollen, sollten Sie einen Ort sehen, an dem Sie Ihren Namen und Ihre Zugehörigkeit bearbeiten können. Fügen Sie diese hinzu und führen Sie dann das oben beschriebene Festschreibungsverfahren aus. Wenn Sie noch etwas sehen, das bearbeitet werden muss, können Sie es auch hinzufügen!

8. Jetzt möchten Sie die Änderungen auf den ursprünglichen Zweig zurückschieben. Verwenden Sie in Ihrer *Shell*den folgenden Befehl: `git push origin suggestions-changes`

9. Gehe zurück zu GitHub und finde deine Gabel hier. Klicken Sie auf die kleine grüne Schaltfläche und erstellen Sie eine Pull-Anfrage. Dies ist im Wesentlichen eine Überprüfung, um die in der ursprünglichen Verzweigung für dieses MOOC-Projekt vorgenommenen Änderungen zu integrieren.

10.     Die für das MOOC-Projekt verantwortlichen Eigentümer erhalten nun eine Benachrichtigung, überprüfen diese und bestätigen, ob alles nach Plan verlaufen ist! Wir werden es überprüfen, und wenn alles in Ordnung ist, wird Ihr Name jetzt für alle Ewigkeit als jemand angezeigt, der diese erweiterte Aufgabe abgeschlossen hat.
      

11.     Trinken Sie eine Tasse Tee, Kaffee oder Wein zum Feiern!
      

**HERZLICHE GLÜCKWÜNSCHE**

Sie haben gerade Git in R Studio integriert und Ihre erste Änderung an einem versionskontrollierten Projekt vorgenommen. Ihr Leben wird niemals mehr dasselbe sein, und Ihr Forschungsworkflow wird wahrscheinlich schneller, agiler und kollaborativer sein als je zuvor. Viel Glück beim Zurückgehen auf Word.

Das Tolle ist, dass dies nicht nur für Code verwendet werden muss. Sie können es für Nur-Text-, Markdown-, HTML- und R-Code verwenden. Die Möglichkeiten sind grenzenlos - was Sie gerade gelernt haben, ist eine neue Form des offen kollaborativen Projektmanagements, das für ein enormes Aufgabenspektrum funktioniert.

Ab sofort liegt es an Ihnen! Einige Ratschläge sind:

* Machen Sie häufige Commits. Behandle Git wie deinen Welpen, denn es erfordert ständige und besondere Aufmerksamkeit. Nur hin und wieder auf den Kopf zu klopfen, reicht aus, um die Zufriedenheit zu wahren, aber am glücklichsten ist es, wenn Sie einen dauerhaften Service in Anspruch nehmen.

* Der beste Weg, dies zu tun, besteht darin, jedes Mal ein Commit durchzuführen, wenn Sie an einem bestimmten Problem arbeiten. Beispiel: Schreiben eines Absatzes, Ausführen einer Analyse oder Beheben eines Fehlers.

* Schieben Sie oft. Lassen Sie diese Commits nicht aufbauen, da Sie sonst ein höheres Risiko für Zusammenführungskonflikte eingehen. Angesichts der Tatsache, dass dies Albträume sein können, sollten Sie nur darauf achten, häufig zu pushen.

* Oft ziehen. Wenn andere remote an demselben Projekt arbeiten, möchten Sie über deren Änderungen auf dem Laufenden bleiben. Stellen Sie sicher, dass Ihre Änderungen regelmäßig von GitHub übernommen werden, um sicherzustellen, dass Sie alle synchron sind.

* Experimentieren und erkunden! Diese Aufgabe zerkratzt wirklich nur die Oberfläche, und es gibt viele verschiedene Funktionen, Werkzeuge und Möglichkeiten, wie dies verwendet werden kann. Es liegt wirklich an Ihnen, herauszufinden, wie Sie diese Informationen verwenden können, um Ihren Forschungsworkflow zu verbessern und letztendlich an einer besseren, offeneren und zuverlässigeren Forschung zusammenzuarbeiten!

* Um mehr über Probleme zu erfahren, Zweige, fusionieren Konflikte, ziehen Anfragen und andere fortgeschrittene Aspekte der Verwendung von Git und RStudio, lesen Sie in diesem [ehrfürchtige Führung](http://r-pkgs.had.co.nz/git.html) von Hadley Wickham.

  


**Wissen Sie, wie dieser Inhalt verbessert werden kann?**

Zeit, deine neuen GitHub-Fähigkeiten für einen Testlauf zu nutzen! Alle Inhalte Entwicklung geschieht in erster Linie [hier](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md). Wenn Sie Verbesserungsvorschläge zu Inhalt, Layout oder etwas anderem haben, können Sie diese vornehmen. Nach Überprüfung durch einen Moderator wird sie automatisch Teil des MOOC-Inhalts!

## Liste der Teilnehmer, die die ADVANCED-Version dieser Aufgabe abgeschlossen haben

* Brendan Palmer, CNI-C, University College Cork
* Lisa Matthias, Freie Universität Berlin
* Hollie Marshall, Universität Leicester 
* Eric D. Wilkey, Western University, Kanada
* José-Raúl Canay-Pazos, Universidad de Santiago de Compostela, Spanien
* Encarnación Martínez Álvarez, Spanien
* Alberto Albz Marocchino, Italien
* Iratxe Rubio, Baskisches Zentrum für Klimawandel BC3
* Gabriele Orlandi, Pariser Hochschule für Sozialwissenschaften (EHESS), Frankreich
* Hande Sodacı, Türkei
* Luke W. Johnston, Universität Aarhus, Dänemark
* Philippe Joly, WZB und HU-Berlin
* Paul Griffiths, NCAS und U. Cambridge
* Harin Lee, Goldschmiede, Universität London
* Luis Camacho, Katholische Universität, Peru
* Tom Cridford, Imperial College London
* Nithiya Streethran, Universität von Stavanger 

[![CC0 Public Domain Widmung](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)