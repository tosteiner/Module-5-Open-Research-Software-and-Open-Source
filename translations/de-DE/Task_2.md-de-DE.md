---
output:
  html_document: Standard
  pdf_document: Standard
---

# Aufgabe 2: Wie Sie Ihren Code mit GitHub und Zenodo zitierbar machen

Diese Aufgabe richtet sich an Studenten und Forscher, die GitHub-basierte Projekte / Repositories in der wissenschaftlichen Literatur erstellen und wiederverwenden möchten.

Vergiss nicht, dass du in unserem offenen [**Slack Channel**](https://osmooc.herokuapp.com/)mitdiskutieren kannst. Bitte stellen Sie sich unter # module5opensource vor und erzählen Sie uns, wer Sie sind, welchen Hintergrund Sie haben und wie Sie hier gelandet sind!

Geschätzte Zeit bis zur Fertigstellung: 45-60 Minuten.

## Inhaltsverzeichnis

- [Vorwort](#Foreword)
- [Richten Sie ein GitHub-Repository ein](#Setup)
- [Wählen Sie Ihr GitHub-Repository](#Choose)
- [Loggen Sie sich bei Zenodo ein](#Login)
- [Autorisieren Sie GitHub, um eine Verbindung mit Zenodo herzustellen](#Authorise)
- [Wählen Sie das zu archivierende Repository aus](#Archive)
- [Überprüfen Sie die Repository-Einstellungen](#Check)
- [Erstellen Sie eine neue Version](#Release)
- [Einen DOI bekommen](#DOI)
- [Checkliste für das Zitieren Ihres Projekts](#Checklist)
- [Zusätzliche Ressourcen](#Resources)

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/Task2.png?raw=true" alt="Task 2-Workflow" width="600" height="861" style="margin-right: 30px; margin-left: 10px;" onmouseover="this.width='1200'; this.height='1722'" onmouseout="this.width='600'; this.height='861'">
</p>

<p align="center"><i>Der Workflow für Aufgabe 2. Halten Sie dies bereit, während Sie die Aufgabe abarbeiten!</i></p>

  


## Vorwort <a name="Foreword"></a>

Obwohl die Integration von GitHub und Zenodo die Arbeit mit diesen Tools heutzutage (Januar 2019) wirklich erleichtert, ist es wichtig zu betonen, dass es Alternativen zu GitHub (Gitlab, Bitbucket, ...) und zu Zenodo (Andere Repositorys) gibt besser zu Ihrer Community passen, fragen Sie vielleicht Ihre Kollegen). Beispielsweise kann man mit Gitlab arbeiten und jede neue Version manuell in Ihr Universitätsrepository hochladen, um einen DOI zu erhalten. Die Prinzipien (online mit einem Versionskontrollsystem arbeiten und Hauptversionen in einem Repository archivieren, das eine persistente eindeutige Kennung bereitstellt) können in verschiedenen Workflows angewendet werden.

## Richten Sie ein GitHub-Repository ein <a name="Setup"></a>

> **Pro-Tipp**: Stellen Sie sicher, dass Sie eine LIZENZ- und README-Datei in Ihr Repository aufnehmen. Dies zeigt den Menschen den Zweck des Projekts und wie sie sich in Zukunft damit beschäftigen können.

Weitere Informationen zum Einrichten eines GitHub-Repositorys finden Sie in diesem anderen Handbuch. [Aufgabe 1: Erstellen eines GitHub-Repositorys](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) das auch Teil von 'Modul 5: Open Research Software und Open Source' ist.

## Wählen Sie Ihr GitHub-Repository <a name="Choose"></a>

Gehen Sie auf der Seite mit den GitHub-Projektlisten unter [github.com](https://github.com) zur Registerkarte "Repositorys". Wählen Sie das Repository aus, das Sie archivieren möchten, und öffnen Sie es.

  


## Loggen Sie sich bei Zenodo ein <a name="Login"></a>

Gehen Sie jetzt zu [zenodo.org](https://zenodo.org). Zenodo ist eine Plattform, auf der Sie Ihren Code und andere Projektelemente dauerhaft archivieren können. Zenodo weist dazu den Projekten einen **Digital Object Identifier** (DOI) zu, was ebenfalls dazu beiträgt, die Arbeit zitierfähiger zu machen. Dies unterscheidet sich von GitHub, das als Ort für die eigentliche Arbeit an einem Projekt dient, anstatt es langfristig zu archivieren. Bei GitHub können Inhalte geändert, gelöscht, umgeschrieben und irreversibel geändert werden, was die Verwendung für längerfristige Referenzierungszwecke ein wenig erschwert. Zenodo bietet mehr Sicherheit und Beständigkeit für Forschungsergebnisse.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/zenodo.png?raw=true" width="800" /></p>

<p align="center"><i>Melden Sie sich bei Zenodo an</i></p>

  


Wenn Sie bereits ein Zenodo-Konto haben, ist dies ganz einfach. Wenn nicht, folgen Sie den Schritten, um einen zu erstellen. Sie können sich sogar mit Ihrem GitHub-Konto oder ORCID-Profil anmelden, um die Dinge zu vereinfachen, da Zenodo eine integrierte Integration dafür hat. Dies ist möglicherweise einfacher, als ein weiteres Forschungskonto und -profil zu erstellen.

  


## Autorisieren Sie GitHub, um eine Verbindung mit Zenodo herzustellen <a name="Authorise"></a>

Autorisieren Sie es auf der Zenodo-Website, um eine Verbindung zu Ihrem GitHub-Konto im Abschnitt "[Using GitHub](https://zenodo.org/account/settings/github/)" herzustellen. Hier leitet Zenodo Sie zu GitHub weiter, um nach Berechtigungen für die Verwendung von "[Webhooks](https://developer.github.com/webhooks/)" in Ihren Repositorys zu fragen. Sie möchten Zenodo hier mit den Berechtigungen autorisieren, die zum Bilden dieser Links erforderlich sind.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/zenodo_github.png?raw=true" width="800" /></p>

<p align="center"><i>Autorisieren Sie Zenodo, um eine Verbindung mit GitHub herzustellen</i></p>

  


Wenn Sie Zenodo Zugriff auf ein Organisationsrepository gewähren möchten, müssen Sie (oder ein Administrator) sicherstellen, dass Zenodo Zugriffsberechtigungen von Drittanbietern erteilt werden. GitHub sendet eine Autorisierungs-E-Mail, die bestätigt werden muss. Zu diesem Zeitpunkt müssen Sie in den Einstellungen Ihres Repositorys auf GitHub auch sicherstellen, dass das Repository auf "öffentlich" und nicht auf "privat" eingestellt ist.

  


## Wählen Sie das zu archivierende Repository aus <a name="Archive"></a>

Wenn Sie so weit gekommen sind, bedeutet dies, dass Zenodo jetzt berechtigt ist, die Repository-Webhooks zu konfigurieren, die zum Archivieren des Repositorys und Ausstellen eines DOI erforderlich sind. Um dies zu tun, auf der Zenodo Website navigieren Sie zur [GitHub - Repository - Eintrag Seite](https://zenodo.org/account/settings/github/) und klicken Sie einfach auf ‚on‘ Taste neben dem Repository.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/enabled_repos.png?raw=true" width="800" /></p>

<p align="center"><i>Aktivieren Sie einzelne GitHub-Repositorys, um sie in Zenodo beizubehalten</i></p>

  


## Überprüfen Sie die Repository-Einstellungen <a name="Check"></a>

Jetzt haben Sie einen neuen Webhook zwischen Zenodo und Ihrem Repository eingerichtet. Klicken Sie in GitHub auf die Einstellungen für Ihr Repository und auf die Registerkarte Webhooks im Menü auf der linken Seite. Daraufhin sollte der neue Zenodo-Webhook angezeigt werden, der für Zenodo konfiguriert wurde. Beachten Sie, dass es einige Zeit dauern kann, bis die Webhook-Liste angezeigt wird.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/webhooks.png?raw=true" width="800" /></p>

<p align="center"><i>Stellen Sie sicher, dass Webhooks für Ihr GitHub-Repository aktiviert sind. Beispiel hier mit der Open Scholarship Strategy</i></p>

  


## Erstellen Sie eine neue Version <a name="Release"></a>

Das erste Mal, dass Sie ein Repository archivieren, wird als "erstes Release" bezeichnet. Jedes Mal, wenn Sie eine neue Version dieses Repository erstellen und archivieren, erstellen Sie eine neue Version. Dies kann in der Registerkarte "Veröffentlichungen" für Ihr Repository auf GitHub (oben in der Mitte) verfolgt werden.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/first_release.png?raw=true" width="800" /></p>

<p align="center"><i>Überprüfen Sie, ob das erste Release des Repository erfolgreich war. Beispiel hier mit der Open Scholarship Strategy</i></p>

  


Klicken Sie für die erste archivierte Version Ihres Repositorys in Zenodo auf "Neue Version erstellen". Füllen Sie das Formular aus und machen Sie Angaben zu den Folgen der Veröffentlichung. Vergewissern Sie sich, dass Sie das erste Release wie üblich v1.0.0 nennen.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/create_release.png?raw=true" width="800" /></p>

<p align="center"><i>Erstellen Sie eine neue Version. Beispiel hier unter Verwendung der Open Scholarship Strategy, für die bereits ein erstes Release existiert</i></p>

  


Klicken Sie abschließend auf "Veröffentlichung veröffentlichen". Ihr Archiv wird auf GitHub veröffentlicht und versioniert.

Um Ihre Version auf Zenodo anzuzeigen, müssen Sie den Tab [Upload](https://zenodo.org/deposit) besuchen. Um die Archivierung abzuschließen, sind einige weitere Details zu Zenodo erforderlich.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/upload_release.png?raw=true" width="800" /></p>

<p align="center"><i>Überprüfen Sie, ob die neue Version hochgeladen wurde. Beispiel hier gezeigt mit der Open Scholarship Strategy</i></p>

  


## Einen DOI bekommen <a name="DOI"></a>

Dies wird manchmal als DOI-Prägung bezeichnet und erfordert einige zusätzliche Informationen über das Repository in Zenodo. Auf Zenodo klicken Sie auf den [Hochladen](https://zenodo.org/deposit) Registerkarte im Hauptmenü, und die neu hochgeladen Repository sollte es sein. Scrollen Sie auf der Seite nach unten und geben Sie die erforderlichen zusätzlichen Informationen ein. Erforderliche Felder sind mit einem roten Sternchen markiert. Klicken Sie anschließend auf "Veröffentlichen".

**Hinweis**: Erst nachdem diese zusätzlichen Informationen hinzugefügt wurden, wird Ihr DOI live. Es kann auch eine kurze Zeit dauern, bis der DOI aktiv wird. Beispiel DOI unten (wieder für die Open Scholarship Strategy).

> **Pro-Tipp**: Kopieren Sie die URL für das DOI in die README-Datei für Ihr GitHub-Repo, um das Vernetzen noch einfacher zu machen. Außerdem wird ein klar hervorgehobenes DOI-Abzeichen angezeigt, damit Benutzer Ihr DOI sehen und verwenden können. Sie müssen dies nur einmal mit Ihrem ersten Release-DOI tun, da es als Konzept-DOI fungiert und mit allen nachfolgenden Release-DOIs verknüpft ist.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1323437.svg)](https://doi.org/10.5281/zenodo.1323437)

Die GitHub / Zenodo-Integration weist jetzt jeder Version / Release eines Projekt-Repositorys eine DOI zu. Auf diese Weise können Benutzer auf bestimmte Versionen von Projekten verweisen und diese zitieren. Außerdem wird die Liste der Autoren für das Zitat automatisch durch die vom Repository verwendeten GitHub-Benutzerkontonamen bestimmt - dies bedeutet, dass niemand ausgelassen wird. Die Details zum Autor können später in Zenodo bearbeitet werden. In Zenodo verwendete DOIs werden über den [DataCite](https://www.datacite.org/) Dienst registriert.

> **Pro-Tipp**: Erstellen Sie eine für Menschen lesbare Version dieses Zitats in der README-Datei Ihres Projekts. Dies ist hilfreich für Forscher, die mit der Verwendung von DOIs zum Erstellen von Zitaten möglicherweise nicht vertraut sind, und erleichtert anderen das Zitieren Ihrer Software und das Bestätigen Ihrer Arbeit. Ein Beispiel hierfür könnte sein: Jon Tennant. (2018, 30. Juli). Grundlagen für die Entwicklung einer offenen Stipendienstrategie: Erste formelle Veröffentlichung (Version 1.2). Zenodo. <http://doi.org/10.5281/zenodo.1323437>

**HERZLICHE GLÜCKWÜNSCHE!!**

Ihr GitHub-Repository ist jetzt in Zenodo archiviert und verfügt über eine DOI, die versioniert werden kann, um Aktualisierungen der Repository-Version im Laufe der Zeit widerzuspiegeln. Sie sollten Details dazu auf der GitHub Zenodo-Seite für Ihr Repository sehen können. Dies bedeutet auch, dass Ihre archivierten Projekte von anderen Indexdiensten und Suchmaschinen, die ebenfalls DOIs verwenden, abgerufen werden können.

Die Bereitstellung eines Langzeitarchivs und einer DOI für Ihre Arbeit ist erforderlich, damit andere Benutzer diese ordnungsgemäß zitieren können, da hiermit grundlegende Zitiermetadaten bereitgestellt werden. Für Open Science ist es wichtig, in der Lage zu sein, die Software zu zitieren, die Sie für Ihre Forschung verwenden, und dieser integrierte Workflow ermöglicht dies in Übereinstimmung mit den Best Practices für Forschungszitate. Darüber hinaus ist diese Praxis wichtig, um den Standard von Software (und verwandten Projekten) auf den Standard anderer Forschungsergebnisse anzuheben.

> **Pro-Tipp**: Wird Ihre Forschung durch ein EU-Stipendium finanziert? Jetzt können Sie Ihr archiviertes Projekt direkt mit Ihrem Grant verbinden, indem Sie den Grant-Abschnitt der Metadaten im Zenodo-Datensatz des Projekts aktualisieren. Dies trägt massiv zur Erhöhung der Auffindbarkeit bei!

  


## Checkliste für das Zitieren Ihres Projekts <a name="Checklist"></a>

Jetzt haben Sie ein nachhaltig archiviertes GitHub-Repository in Zenodo, das wiederverwendet und zitiert werden kann! Bevor Sie fortfahren, stellen Sie sicher, dass Sie:

- [] Verknüpfte dein GitHub-Projekt mit Zenodo. Wenn Sie in Zenodo eine vollständige Kopie Ihres GitHub-Repository sehen, funktioniert es.
- [] Das in Zenodo und GitHub integrierte Setup funktioniert gut. Lassen Sie beispielsweise alle Autorennamen und den korrekten Projekttitel zu Zenodo gelangen. Wenn nicht, oder wenn Autoren nur Spitznamen haben, können Sie diese Details in Zenodo bearbeiten.
- [] Project hat eine erste Veröffentlichung mit einem DOI. Auf Ihrer Zenodo-Projektseite sollte ein DOI angezeigt werden. Dieser erste DOI wird als "Konzept-DOI" bezeichnet und ist der Master-DOI, der mit allen nachfolgenden Release-DOIs verknüpft ist. Kopieren Sie diesen DOI-Link und binden Sie ihn in die README-Seite Ihres GitHub-Projekts ein. Sie sind fertig!

### Zusätzliche Ressourcen <a name="Resources"></a>

[Zitierfähig machen](https://guides.github.com/activities/citable-code/) - GitHub Guides.

**Wissen Sie, wie dieser Inhalt verbessert werden kann?**

Zeit, deine neuen GitHub-Fähigkeiten für einen Testlauf zu nutzen! Alle Inhalte Entwicklung geschieht in erster Linie [hier](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md). Wenn Sie Verbesserungsvorschläge zu Inhalt, Layout oder etwas anderem haben, können Sie diese vornehmen. Nach Überprüfung durch einen Moderator wird sie automatisch Teil des MOOC-Inhalts!

[![CC0 Public Domain Widmung](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)