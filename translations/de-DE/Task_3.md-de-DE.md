---
output:
  html_document: Standard
  pdf_document: Standard
---

# Aufgabe 3: So integrieren Sie Git in R Studio

Diese Aufgabe richtet sich an Studenten und Forscher, die ein Versionskontrollsystem in einem standardmäßigen R-basierten Workflow implementieren möchten. Dies kann auf eine Reihe von Aufgaben in den Bereichen Softwareentwicklung, Datenanalyse und Projektmanagement angewendet werden. Ihr zukünftiges Forschungsunternehmen wird sich bei Ihnen für die Bequemlichkeit bedanken.

Don't forget you can join in the discussions over at our open [**Slack channel**](https://osmooc.herokuapp.com/). Bitte stellen Sie sich unter # module5opensource vor und erzählen Sie uns, wer Sie sind, welchen Hintergrund Sie haben und wie Sie hier gelandet sind!

Geschätzte Bearbeitungszeit: 30 Minuten

Geschätzte Zeitersparnis nach Abschluss: Praktisch unendlich

**NOTE** A video guide version of this task is now available on [YouTube](https://www.youtube.com/watch?v=Q-6jfjSAspA).

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

Congratulations on making it this far! If you're reading this, you've survived pull requests, web-hooks, and can probably even tell us know what the F in FOSS stands for (*not* Frustration...) Hopefully, you have overcome any scepticism or reluctance towards the benefits of GitHub and Open Source Software, and are ready to take the next step.

Before starting this Task, please make sure you have already completed [Task 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [Task 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), so that you are more familiar with GitHub and some standard Open Source practices.

This task will teach you how to integrate the version control software, Git, with the popular coding environment, RStudio. And yes, it is Git as in gif or God, not Jit as in the wrong way of pronouncing things.

If you are one of those researchers who thinks that having code spread across multiple hard-drives that are waiting to break, Dropbox, Google Drive, or any other non-specialist software, this task is just for you. If you have ever experienced the mind-numbing process of having multiple 'final' versions of a paper bouncing between different co-authors, this is also for you.

All of us are guilty of these sorts of things once in a while, but there are ways to do it that are better for you, future you, and those who might benefit from your work.

  


### Git bekommen <a name="Git"></a>

So, what is Git, and how is it different to GitHub? Git is a version control system, which enables you to save and track time-stamped copies of your work throughout the development process. It also works with non-code items too, like this MOOC, the majority of which was written in markdown in RStudio, and integrated with a Git/GitHub workflow.

This is important, as all research goes through changes and sometimes we want to know what those things were. Did you delete some text that you now think is important? Version control will save that for you. Did your code work perfectly in the past, but is now buggy beyond belief? Version control. It's a great way to avoid that chaotic state where you have multiple copies of the same file, but without a stupid and annoying file naming convention. `FINAL_Revised_2.2_supervisor_edits_ver1.7_scream.txt` will be a thing of the past.

GitHub is the platform that allows you to seamlessly share code from your workspace (e.g., laptop) to be hosted in an online space. So, sort of like the public interface to GitHub. The advantages of Git/GitHub are:

1. Sie können Kopien aller Ihrer Arbeiten im Laufe der Zeit aufbewahren.
2. Sie können die Arbeit anhand verschiedener Kopien im Laufe der Zeit vergleichen, um Fehler oder Fehler zu erkennen.
3. Andere Personen können offen mit Ihrer Arbeit zusammenarbeiten.
4. Sie haben sowohl eine lokale als auch eine Online-Kopie Ihrer Arbeit, die synchron bleiben.
5. Es ist völlig transparent, wer einen Beitrag geleistet hat, warum und wann er geleistet wurde. und
6. Sie können mehrere Personen gleichzeitig an einem Projekt arbeiten lassen.

While this was primarily designed for source code, it should be instantly obvious how this becomes a powerful tool for virtually all research workflows.

  


### RStudio <a name="Rstudio"></a>

RStudio is a popular coding environment for researchers who use the statistical programming language, R. It comes with a text editor, so you don't have to install another and switch between. It also includes a graphical user interface (GUI) to Git and GitHub, which we will be using here.

Isn't it nice when brilliant Open Source tools integrate seamlessly like that. This should help to make your daily use of Git much simpler.

If at any point you need to install new packages for R, simply use the following command:

`install.packages("PACKAGE NAME", dependencies = TRUE)`

Replacing `PACKAGE NAME` with the, er, package name. Some examples you can play with that might come in useful include `knitr`, `devtools` or `ggplot2`.

  


## Schritt eins: Laden Sie alle Dinge herunter <a name="one"></a>

1. Sie sollten bereits ein GitHub-Konto haben, wenn Sie die vorherigen Aufgaben ausgeführt haben. Wenn nicht, [anmelden](https://github.com/). Kostenlose unbegrenzte Repositories für alle!
2. Laden Sie die neueste Version von [R](https://www.r-project.org/)herunter und installieren Sie sie. Auch für [Mac](https://cloud.r-project.org/) und [Linux](https://cloud.r-project.org/bin/linux/)verfügbar.
3. Laden Sie die neueste Version von [Rstudio](https://www.rstudio.com/products/rstudio/#Desktop)herunter und installieren Sie sie. Oh, hey, sieht nach Open Source aus! Swish.
4. Laden Sie die neueste Version von [Git](https://gitforwindows.org/)herunter und installieren Sie sie. **Stellen Sie sicher, dass Sie während der Installation "Git von der Windows-Eingabeaufforderung verwenden" auswählen.**

> **Pro-Tipp**: Um alle R-Pakete in einem zu aktualisieren, führen Sie einfach den folgenden Code `update.packages aus (ask = FALSE, checkBuilt = TRUE)`

For now, just choose all the usual default options for each install. Depending on which Operating System (e.g., Mac, Windows, Linux), this might be different for each of you. For now, and for the rest of this task, we're going to stick with doing things the easy-ish Windows way (but also provide some instructions for using the command line).

For Linux or Debian users, simply use the following command to install Git:

`sudo apt-get install git-core`

For Mac users, [this link](http://git-scm.com/download/mac), or purchase a new laptop with a different operating system.

If you want, you can also download the [local version of GitHub](https://desktop.github.com/) and use it through the simple GUI. It's available on Windows and Mac and Linux, and can make your life a little easier, especially if you want to use a different platform to RStudio.

> **Pro-Tipp:** Sie sehen, wenn Sie Git installieren: "Git Bash als Shell für Git-Projekte verwenden?" Hier können Sie über die Befehlszeile von außerhalb von RStudio auf Git zugreifen. Es ist ein mächtiges Tier. Probieren Sie die folgenden zwei Befehle aus, um zu beginnen:

`git config --global user.name 'YOUR USERNAME'`   
`git config --global user.email 'YOUR EMAIL'`   


## Schritt zwei: Konfigurieren Sie Git in RStudio <a name="two"></a>

Right, that's the easy bit done. Next, go into RStudio, and in the tabs at the top go to Go to **Tools > Global Options > Git/SVN**. SVN is just another version control system like Git, and we don't need to worry about that here.

In the place where it says *Git executable*, add the pathway here to the git.exe file that you just downloaded in the previous step. Make sure the box here that says **Enable version control interface for RStudio projects** is ticked. This now has tied version control to future projects in RStudio, to provide a really powerful additional dimension to collaborative or solo work.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/git_svn.png?raw=true" width="400px"/>
</p>

<p align="center"><i>The Global Options window inside RStudio</i></p>

  


Next, hit the button in this window that says *Create RSA Key*, This is a private key that is used for authentication between different systems, and saves you from having to type in your password over and over. Here, it will pop up a new window with a public key, that you want to copy to your clipboard.

Head over to GitHub, go to your profile settings, and the *SSH and GPG keys* tab. Click *New SSH key*. Here, paste in the key from RStudio, and call it something imaginative like 'RStudio'.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/ssh_key.png?raw=true" width="800px"/>
</p>

<p align="center"><i>Inside GitHub where you will want to enter the key you just generated in RStudio</i></p>

  


OK, now hold on to your butts, we're going into the command line. Don’t worry if you’ve never used the shell before because it’s quite similar to using R, or any other coding system. The main difference here though is that instead of calling functions like in R, you call commands.

So back in RStudio, go to **Tools > Shell**, and it will open up a command prompt window. If you already played with the Git Bash above, you should have done this step already. Enter the following two commands:

`git config --global user.name 'YOUR USERNAME'`   
`git config --global user.email 'YOUR EMAIL'`   


Hopefully it does not have to be said to substitute in your own GitHub username and email here. You can access this at any point just by finding the 'Shell' within Windows. Or, if you right click on any folder on your Desktop that is linked to a GitHub repo, you can open up the Shell instantly and Bash away.

What this stage has done is configure Git, which is software that runs on your desktop, to GitHub, which is a repository website.

Restart R Studio. Whew, that was tough. Next.

  


## Schritt drei: Warum habe ich das gerade getan? <a name="three"></a>

OK, hold your breathe, we're going to pause here just to learn some basic Git commands. Some of the key ones you could do with learning are:

* **Add**: Hierüber senden Sie Dateien an den Staging-Bereich, bevor Sie festgeschrieben werden.

* **Commit** Dies ist wie das 'Speichern' Ihrer Arbeit durch Erstellen einer neuen Version oder Kopie.

* **Push**: So senden Sie Dateien aus Ihrem lokalen Projekt an das Online-Repository.

* **Pull**: So bringen Sie Dateien aus Ihrem Online-Repository in Ihr lokales Projekt.

Back in RStudio, type in the following into the *Terminal*, or by opening up a new Shell:

`git add .`

It won't actually do anything for now, but in the future will add all files in your current working directory (that's what the `.` does) to staging ready for a commit.

  


## Schritt vier: Die perfekte Ehe zwischen Git und R <a name="four"></a>

Now, in Task 1, you should have learned how to build your very first GitHub repository. If you haven't done that, we can wait here while you go and do that. If you have already, or have an existing GitHub repository, we can move on.

So, you should have a repository on GitHub, complete with a `README` file, a `LICENSE` file and some other bits and bobs.

What we are going to do now, is integrate that repository with Git. Steady now.

1. Gehen Sie zunächst zu **Projekt> Projekt erstellen> Versionskontrolle> Git**.
2. Zurück auf GitHub sollten Sie ein bisschen sehen, wo es eine https: // URL gibt. Dies ist der Link zu Ihrem Repository und bietet Ihnen die Möglichkeit, es auf Ihrem Desktop zu klonen. Kopieren Sie zunächst diesen Link, wechseln Sie zurück zu RStudio und fügen Sie ihn wie angegeben in die 'Repository-URL' ein.
3. Geben Sie dem Projekt einen Verzeichnisnamen wie test, Jim oder was auch immer Sie möchten.
4. Suchen Sie als Nächstes auf Ihrem Desktop nach dem Ort, an dem das Projekt gespeichert werden soll, dh nach dem Unterverzeichnis.
5. Klicken Sie auf "Projekt erstellen" und lassen Sie die Magie erledigen!

What you just did was tell RStudio to associate a new project in R with specific repository on GitHub.

## **Schritt vier: Alternative**

If you still haven't built your first repository on GitHub, we can do something slightly different here. In RStudio, click *New project* and then *New Directory*. Call it what you want and change the directory as needed, make sure to tick *Create a git repository*, and then click *Create Project*. This creates an `.Rproj` file, which you can manage in the usual way through RStudio, including adding `README.md`and `LICENSE.md` files as discussing in Task 1.

## Schritt fünf: Inhalte mit Inhalten erhalten <a name="five"></a>

Remember that `README` file we created a while back? Well, it's time to write it. Thinking back to Task 1, there were some specific things that we said make a good `README` file. Do you remember what any of them were? Just to refresh your memory, these were:

* Worum geht es in diesem Projekt und was macht es?
* Warum sollte es die Leute interessieren und warum ist es nützlich?
* Wie kann jemand anfangen, zu dem Projekt beizutragen?
* An wen kann man sich wenden, wenn jemand Hilfe benötigt?
* Ein Link zur Lizenz, den dazugehörigen Richtlinien und dem Verhaltenskodex.
* Eine Beschreibung der Projektstruktur.
* Wer ist beteiligt und welche Rollen haben sie?
* Der aktuelle Status des Projekts.

So, in RStudio, open that file try adding just a bit of information about this for your project. If you are doing this for an actual project, try and make it useful. If you are just tinkering for now, you can add what you want.

Remember that your `README` file is in markdown (.md) format. For a refresher on some of the simple syntax markdown uses, check this [handy cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/markdown.png?raw=true" width="600px"/>
</p>

<p align="center"><i>Screenshot of what this module looks in markdown, during development. Meta.</i></p>

  


## Schritt sechs: Eine mutige Verpflichtung <a name="six"></a>

OK, so now you should have a nicely edited `README` file. Now we are going to 'commit' this to the project using Git. This is basically the equivalent of saving this version of your project, with a record of what changes were made. Successive commits produce a history that can be examined at a later time, allowing you to work with confidence.

There are a few ways of doing this.

1. Gehen Sie zu **Tools> Versionskontrolle> Commit**
2. Im Umgebungsfenster von RStudio sollte sich eine neue Registerkarte "Git" befinden. Praktisch.
3. In Ihrem Konsolenfenster sollte sich jetzt ein neues 'Terminal' befinden, über das Sie Git-Befehlszeilen ausführen können.

Let's just stick with the second option for now. This Git pane shows you which files have been changed and includes buttons for the most important Git commands we saw earlier.

Select the `README` file in the Git window, which should show up automatically if you have made any edits to it. This adds that file to the 'staging' area, which is sort of like the pre-saving space for your work. Click 'Commit' and a new window should pop up.

Here, you have a chance to review your changes, and write a nice commit message. Type in something brief, but informative about the changes that you have made in this version or snapshot of your work. You want this to be enough information so that if you or someone else looks back on it, you'll know why you made this commit and the changes associated with it. These are like safety nets for your project in case you need to fall back for some reason.

> **Pro-Tipp**: Hier sehen Sie eine Liste aller Änderungen, die Sie seit Ihrem letzten Commit vorgenommen haben. Ältere entfernte Linien sind rot und neu hinzugefügte Linien sind grün. Überprüfen Sie diese nochmals, um sicherzustellen, dass Sie die gewünschten Änderungen vorgenommen haben. This is really helpful for spotting typos, stray edits, and any other little mistakes you might have accidentally introduced. Sicherheit zuerst.

**Note** If you are colour-blind and can't see which lines have been added or removed, you can use the line numbers in the two columns on the left of the window as a guide. Here, the number in the first column identifies the older version, and the number in the second column identifies the new version.

Now when you click 'Commit', another window will pop up, telling you how many files you have changed and the number of lines within that file you have changed. Close that little window down.

  


## Schritt sieben: DRÜCKEN! <a name="seven"></a>

Click the *Push* button in the top right of the new window. A new window will pop up now. What this is doing is synchronising the files changed on your local repository with the `README` file to the online version of the project on GitHub.

To do this from the Shell, use the following command:

`git push -u origin master`

Some times here you will be prompted to add your username and password from GitHub, which you should do if asked.

Close that window down, and the next one. Go to your project on GitHub, refresh, and check that the `README` file is still there in all its newly edited glory. You should see the commit message you made next to the file too.

  


**OPTIONAL ADVANCED/AWESOME STEP**

Alright, so you just pushed some content to your first repo, awesome! Now let's put it into practice for a real project. Like, the one you are participating in right now. Let's try this out:

1. Go to the repository for this project on [GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source)

2. Verzweigen Sie das Repository in Ihr eigenes GitHub-Konto. Die URL dafür sollte lauten: `https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source.git`

3. Head into RStudio, go to **File > New Project**, choose *Version Control*, select *Git*, and then paste the forked repository URL found in your copy of the repository. Sie haben jetzt Ihre eigene versionierte Kopie dieses gesamten Moduls. Ordentlich. Speichern Sie dies irgendwo auf Ihrem lokalen Computer.

4. Jetzt müssen Sie Git mitteilen, dass eine andere Version dieses Projekts vorhanden ist. Öffnen Sie die *Shell*und geben Sie den folgenden Befehl ein: `git remote add upstream https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source`

5. Was Sie soeben getan haben, war, den ursprünglichen Zweig hier als `vor`, um die Dinge vorerst einfach zu halten. Now, create a new **branch** to document your changes to this independent of the main branch. Enter the command: `git checkout -b proposed-changes master`

6. You just created a new branch called `proposed-changes` where you can now edit all of the content and files to your heart's delight. Hopefully, the structure of this project is simple enough for you to navigate around. All of the raw files for the MOOC can be found in the `content_development` folder, and this is `Task_3.md`.

7. If you scroll to the bottom of `Task_3.md`, you should see a place where you can edit in your name and affiliation. Add these in, and then go through the commit procedure detailed above. If you see anything else that needs editing too, feel free to add them in too!

8. Now, you want to push the changes back to the original branch. Use the following command in your *Shell*: `git push origin proposed-changes`

9. Go back to GitHub and find your fork here. Click the little green button, and create a pull request. This is essentially a review to integrate the changes made into the original branch for this MOOC project.

10.     The owners in charge of the MOOC project will now get a notification of this, review it, and confirm it if everything went to plan! We will review it, and if it all went okay, your name will now appear for all eternity as someone who completed this advanced task.
      

11.     Have a cup of tea, coffee, or wine to celebrate!
      

**CONGRATULATIONS**

You just integrated Git with R Studio, and made your first change to a version controlled project. Your life will now never be the same, and your research workflow will probably be more rapid, agile, and collaborative than ever. Good luck going back to Word.

The great thing is that this doesn't have to just be used for code. You can use it for plain text, markdown, html, and, well, R code. The possibilities are limitless - what you have just learned is a new form of openly collaborative project management that works for an enormous range of tasks.

From now on, it is all up to you! Some advice is to:

* Make frequent commits. Treat Git like your puppy, in that it requires constant and special attention. Just a pat on the head every now and then is enough to keep it satisfied, but it'll be happiest with sustained servicing.

* The best way to do this is to make a commit each time you work on a specific problem. For example, writing a paragraph, running an analysis, or fixing a bug.

* Push often. Don't let those commits build up, otherwise you run more risk of getting into merge conflicts. Seeing as these can be the stuff of nightmares, just make sure to push often.

* Pull often. If others are working remotely on the same project, you will want to stay up to date with their changes. Make sure to frequently pull in their changes from GitHub to make sure you are all in sync.

* Experiment and explore! This task really only scratches the surface, and there are many different functions, tools, and ways this can be used. Really, it is up to you to find out how to use this information to improve your research workflow, and ultimately collaborate on better, more open and reliable research!

* To learn more about issues, branches, merge conflicts, pull requests, and other advanced aspects of using Git and RStudio, check out this [awesome guide](http://r-pkgs.had.co.nz/git.html) by Hadley Wickham.

  


**Know a way this content can be improved?**

Time to take your new GitHub skills for a test-run! All content development primarily happens [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md). If you have a suggested improvement to the content, layout, or anything else, you can make it and then it will automatically become part of the MOOC content after verification from a moderator!

## List of participants who completed the ADVANCED version of this task

* Brendan Palmer,CRF-C, University College Cork
* Lisa Matthias, Freie Universität Berlin
* Hollie Marshall, University of Leicester 
* Eric D. Wilkey, Western University, Canada
* José-Raúl Canay-Pazos, Universidade de Santiago de Compostela, Spain
* Encarnación Martínez Álvarez, Spain
* Alberto Albz Marocchino, Italy
* Iratxe Rubio, Basque Centre for Climate Change BC3
* Gabriele Orlandi, Paris School of Advanced Studies in Social Sciences (EHESS), France
* Hande Sodacı, Turkey
* Luke W. Johnston, Aarhus University, Denmark
* Philippe Joly, WZB and HU-Berlin
* Paul Griffiths, NCAS and U. Cambridge
* Harin Lee, Goldsmiths, University of London
* Luis Camacho, Catholic University, Perú
* Tom Cridford, Imperial College London
* Nithiya Streethran, University of Stavanger 

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)