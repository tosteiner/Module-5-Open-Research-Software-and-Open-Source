---
output:
  html_document: défaut
  pdf_document: défaut
---

# Tâche 3: Comment intégrer Git à R Studio

Cette tâche est conçue pour les étudiants et les chercheurs qui souhaitent implémenter un système de contrôle de version dans un flux de travail standard basé sur R. Ceci peut être appliqué à une gamme de tâches de développement logiciel, d'analyse de données et de gestion de projet. Vos recherches futures vous remercieront pour la commodité.

N'oubliez pas que vous pouvez participer aux discussions sur notre open channel [**Slack channel**](https://osmooc.herokuapp.com/). Présentez-vous à l'adresse # module5opensource, et dites-nous un peu qui vous êtes, votre parcours, et comment vous vous êtes retrouvés ici!

Durée estimée: 30 minutes

Estimez le gain de temps une fois terminé: pratiquement infini

**REMARQUE** Une version de guide vidéo de cette tâche est maintenant disponible sur [YouTube](https://www.youtube.com/watch?v=Q-6jfjSAspA).

## Table des matières

* [Commencer](#Getting_started) 
  * [Git](#Git)
  * [R Studio](#Rstudio)
* [Première étape: télécharger toutes les choses](#one)
* [Deuxième étape: configurer Git dans RStudio](#two)
* [Troisième étape: Pourquoi est-ce que je viens de faire ça?](#three)
* [Quatrième étape: le mariage parfait entre Git et R](#four)
* [Cinquième étape: obtenir du contenu avec le contenu](#five)
* [Sixième étape: un engagement courageux](#six)
* [Septième étape: PUSH!](#seven)

## Commencer <a name="Getting_started"></a>

Félicitations pour aller si loin! Si vous lisez ceci, vous avez survécu aux demandes de tirage, aux Web-hooks et pouvez probablement même nous dire ce que signifie le F dans FOSS (*pas* frustration ...). Espérons que vous ayez surmonté tout scepticisme ou réticence vers les avantages de GitHub et du logiciel Open Source, et sont prêts à passer à l’étape suivante.

Avant de commencer cette tâche, veuillez vous assurer que vous avez déjà terminé [Tâche 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) et [Tâche 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)afin de vous familiariser davantage avec GitHub et certaines pratiques Open Source standard.

Cette tâche vous apprendra comment intégrer le logiciel de contrôle de version, Git, à l'environnement de codage populaire, RStudio. Et oui, c'est Git comme dans gif ou Dieu, pas Jit comme une mauvaise façon de prononcer les choses.

Si vous êtes un de ces chercheurs qui pensent que le code doit être réparti sur plusieurs disques durs en attente de rupture, Dropbox, Google Drive ou tout autre logiciel non spécialisé, cette tâche est pour vous. Si vous avez déjà expérimenté le processus ahurissant de disposer de plusieurs versions «finales» d'un document qui rebondit entre différents co-auteurs, c'est également pour vous.

Nous sommes tous coupables de ce genre de choses de temps en temps, mais il existe des moyens de le faire qui sont meilleurs pour vous, votre avenir et ceux qui pourraient bénéficier de votre travail.

  


### Obtenir Git <a name="Git"></a>

Alors, qu'est-ce que Git et en quoi est-il différent de GitHub? Git est un système de contrôle de version qui vous permet de sauvegarder et de suivre des copies horodatées de votre travail tout au long du processus de développement. Il fonctionne également avec des éléments non codés, comme ce MOOC dont la majorité a été écrite sous forme de markdown dans RStudio et intégrée à un flux de travail Git / GitHub.

Ceci est important, car toutes les recherches évoluent et nous voulons parfois savoir ce qu’il en était. Avez-vous supprimé du texte que vous considérez maintenant comme important? Le contrôle de version vous permettra d’économiser cela. Votre code a-t-il parfaitement fonctionné dans le passé, mais est-il maintenant impossible de croire? Contrôle de version. C'est un excellent moyen d'éviter cet état chaotique où vous avez plusieurs copies du même fichier, mais sans convention de dénomination stupide et ennuyeuse. `FINAL_Revised_2.2_supervisor_edits_ver1.7_scream.txt` sera une chose du passé.

GitHub est la plate-forme qui vous permet de partager en toute transparence le code de votre espace de travail (un ordinateur portable, par exemple) pour qu'il soit hébergé dans un espace en ligne. Donc, un peu comme l’interface publique vers GitHub. Les avantages de Git / GitHub sont:

1. Vous gardez des copies de tout votre travail dans le temps;
2. Vous pouvez comparer le travail à travers différentes copies dans le temps, ce qui permet de repérer des bugs ou des erreurs;
3. D'autres personnes peuvent collaborer ouvertement avec votre travail.
4. Vous avez une copie locale et une copie en ligne de votre travail qui restent synchronisées;
5. Il est totalement transparent de savoir qui a apporté une contribution, pourquoi et quand; et
6. Vous pouvez avoir plusieurs personnes travaillant sur le même projet à la fois en parallèle.

Bien que cela ait été principalement conçu pour le code source, il devrait être immédiatement évident de voir comment cela devient un puissant outil pour pratiquement tous les flux de travaux de recherche.

  


### RStudio <a name="Rstudio"></a>

RStudio est un environnement de codage populaire pour les chercheurs utilisant le langage de programmation statistique R. Il est fourni avec un éditeur de texte. Vous n'avez donc pas besoin d'en installer un autre ni de basculer entre eux. Il inclut également une interface utilisateur graphique (GUI) pour Git et GitHub, que nous allons utiliser ici.

N’est-ce pas agréable lorsque de brillants outils Open Source s’intègrent parfaitement comme ça Cela devrait vous aider à simplifier votre utilisation quotidienne de Git.

Si à un moment quelconque vous devez installer de nouveaux packages pour R, utilisez simplement la commande suivante:

`install.packages ("NOM DU PAQUET", dependencies = TRUE)`

Remplacer `PACKAGE NAME` par le, er, nom du package. Certains exemples avec lesquels vous pouvez jouer et qui pourraient s'avérer utiles incluent `knitr`, `devtools` ou `ggplot2`.

  


## Première étape: télécharger toutes les choses <a name="one"></a>

1. Vous devriez déjà avoir un compte GitHub maintenant si vous avez suivi les tâches précédentes. Sinon, [signe ici](https://github.com/). Dépôts illimités gratuits pour tous!
2. Téléchargez et installez la dernière version de [R](https://www.r-project.org/). Egalement disponible pour [Mac](https://cloud.r-project.org/) et [Linux](https://cloud.r-project.org/bin/linux/).
3. Téléchargez et installez la dernière version de [Rstudio](https://www.rstudio.com/products/rstudio/#Desktop). Oh, hé, ça a l'air Open Source! Bruissement.
4. Téléchargez et installez la dernière version de [Git](https://gitforwindows.org/). **Assurez-vous de sélectionner “Utiliser Git à partir de l'invite de commande Windows” lors de l'installation.**

> **Astuce**: pour mettre à jour tous vos paquets R en un, exécutez simplement le code suivant `update.packages (ask = FALSE, checkBuilt = TRUE)`

Pour l'instant, il suffit de choisir toutes les options par défaut habituelles pour chaque installation. Selon le système d'exploitation utilisé (Mac, Windows, Linux, par exemple), cela peut être différent pour chacun d'entre vous. Pour l'instant, et pour le reste de cette tâche, nous allons continuer à faire les choses à la manière la plus simple possible de Windows (mais nous fournirons également quelques instructions pour utiliser la ligne de commande).

Pour les utilisateurs Linux ou Debian, utilisez simplement la commande suivante pour installer Git:

`sudo apt-get install git-core`

Pour les utilisateurs de Mac, [ce lien](http://git-scm.com/download/mac), ou achetez un nouvel ordinateur portable avec un système d'exploitation différent.

Si vous le souhaitez, vous pouvez également télécharger la version [locale de GitHub](https://desktop.github.com/) et l'utiliser via la simple interface graphique. Disponible sur Windows, Mac et Linux, il peut vous simplifier la vie, surtout si vous souhaitez utiliser une plate-forme différente de RStudio.

> **Astuce:** Lors de l’installation de Git, vous voyez «Utiliser Git Bash comme shell pour les projets Git? C’est à cet endroit que vous pouvez utiliser la ligne de commande pour accéder à Git depuis l’extérieur de RStudio. C'est une bête puissante. Essayez les deux commandes suivantes pour commencer:

`git config --global user.name 'VOTRE NOM D'UTILISATEUR'`   
`git config --global user.email 'VOTRE EMAIL'`   


## Deuxième étape: configurer Git dans RStudio <a name="two"></a>

Bon, c'est la partie facile faite. Ensuite, allez dans RStudio, et dans les onglets en haut, allez à Aller à **Outils> Options globales> Git / SVN**. SVN est juste un autre système de contrôle de version comme Git, et nous n’avons pas à nous en préoccuper ici.

À l'endroit où il est indiqué *exécutable Git*, ajoutez le chemin ici au fichier git.exe que vous venez de télécharger à l'étape précédente. Assurez-vous que la case **Activer l'interface de contrôle de version pour les projets RStudio** est cochée. Cela a maintenant lié le contrôle de version aux projets futurs dans RStudio, afin de fournir une dimension supplémentaire vraiment puissante au travail collaboratif ou solo.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/git_svn.png?raw=true" width="400px"/>
</p>

<p align="center"><i>La fenêtre Options globales à l'intérieur de RStudio</i></p>

  


Ensuite, cliquez sur le bouton dans cette fenêtre qui dit *Créer RSA Key*, Ceci est une clé privée qui est utilisé pour l' authentification entre les différents systèmes, et vous évite d'avoir à taper votre mot de passe à plusieurs reprises. Ici, une nouvelle fenêtre contenant une clé publique que vous souhaitez copier dans votre presse-papiers s’ouvrira.

Rendez -vous sur GitHub, allez à vos paramètres de profil, et le *SSH et les clés GPG* onglet. Cliquez sur *New SSH key*. Ici, collez la clé de RStudio et appelez-la de manière imaginative telle que "RStudio".

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/ssh_key.png?raw=true" width="800px"/>
</p>

<p align="center"><i>Dans GitHub où vous voulez entrer la clé que vous venez de générer dans RStudio</i></p>

  


OK, maintenant, tiens tes fesses, nous allons dans la ligne de commande. Ne vous inquiétez pas si vous n'avez jamais utilisé le shell auparavant, car il ressemble beaucoup à l'utilisation de R ou de tout autre système de codage. La principale différence ici cependant est qu’au lieu d’appeler des fonctions comme dans R, vous appelez des commandes.

De retour dans RStudio, allez à **Outils> Shell**et une fenêtre d’invite de commande s’ouvrira. Si vous avez déjà joué avec le Git Bash ci-dessus, vous devriez déjà avoir fait cette étape. Entrez les deux commandes suivantes:

`git config --global user.name 'VOTRE NOM D'UTILISATEUR'`   
`git config --global user.email 'VOTRE EMAIL'`   


Espérons qu'il ne soit pas nécessaire de dire de substituer votre nom d'utilisateur et votre email GitHub ici Vous pouvez y accéder à tout moment simplement en trouvant le «shell» dans Windows. Ou, si vous cliquez avec le bouton droit de la souris sur n’importe quel dossier de votre bureau lié à un dépôt GitHub, vous pouvez ouvrir le shell instantanément et l’écarter.

Au cours de cette étape, vous avez configuré Git, un logiciel exécuté sur votre bureau, avec GitHub, un site Web de référentiel.

Redémarrez R Studio. Ouf, c'était dur. Suivant.

  


## Troisième étape: Pourquoi est-ce que je viens de faire ça? <a name="three"></a>

OK, retiens ton souffle, nous allons faire une pause ici pour apprendre quelques commandes de base de Git. Voici quelques exemples clés que vous pouvez utiliser pour apprendre:

* **Ajouter**: C'est ici que vous envoyez des fichiers dans la zone de transfert avant d'être validés.

* **Commit** Cela revient à "enregistrer" votre travail en créant une nouvelle version ou une copie.

* **Push**: Voici comment vous envoyez des fichiers de votre projet local au référentiel en ligne.

* **Pull**: C’est ainsi que vous récupérez les fichiers de votre référentiel en ligne vers votre projet local.

De retour dans RStudio, tapez ce qui suit dans le *Terminal*ou en ouvrant un nouveau shell:

`git add.`

Il ne fera quoi que ce soit pour l' instant, mais à l'avenir ajoutera tous les fichiers dans votre répertoire de travail courant (c'est ce que le `.` ) vers les mettant en scène prêt pour une livraison .

  


## Quatrième étape: le mariage parfait entre Git et R <a name="four"></a>

Maintenant, dans la tâche 1, vous devriez avoir appris à construire votre tout premier référentiel GitHub. Si vous ne l'avez pas fait, nous pouvons attendre ici pendant que vous y allez. Si vous avez déjà un référentiel GitHub ou en possédez un, nous pouvons continuer.

Donc, vous devriez avoir un référentiel sur GitHub, avec un fichier `README` , un fichier `LICENSE` et quelques autres bits et bobs.

Ce que nous allons faire maintenant, c'est intégrer ce référentiel à Git. Stable maintenant.

1. Tout d’abord, allez à **Projet> Créer un projet> Contrôle de version> Git**.
2. De retour sur GitHub, vous devriez voir un peu où il y a une URL https: //. C'est le lien vers votre référentiel, et cela vous donne la possibilité de le cloner sur votre bureau. Pour l'instant, copiez simplement ce lien, revenez à RStudio et collez-le dans "l'URL du référentiel" comme indiqué.
3. Donnez au projet un nom de répertoire, tel que test, Jim ou ce que vous voulez.
4. Ensuite, recherchez l'emplacement de votre projet sur votre bureau, son sous-répertoire.
5. Cliquez sur 'Créer un projet' et laissez la magie se faire!

Vous venez de dire à RStudio d’associer un nouveau projet R avec un référentiel spécifique sur GitHub.

## **Quatrième étape: alternative**

Si vous n'avez toujours pas construit votre premier référentiel sur GitHub, nous pouvons faire quelque chose de légèrement différent ici. Dans RStudio, cliquez sur *New project* , puis sur *New Directory*. Appelez-le comme vous le souhaitez et modifiez le répertoire selon vos besoins, cochez la case *Créer un référentiel git*, puis cliquez sur *Create Project*. Cela crée un fichier `.Rproj` , que vous pouvez gérer de manière habituelle via RStudio, notamment en ajoutant `fichiers README.md`et `LICENSE.md` comme indiqué dans la tâche 1.

## Cinquième étape: obtenir du contenu avec le contenu <a name="five"></a>

Rappelez-vous que `fichier LISEZMOI` que nous avons créé il y a longtemps? Eh bien, il est temps de l'écrire. En repensant à la tâche 1, nous avons dit que certaines choses spécifiques constituent un bon fichier `README`. Vous souvenez-vous de ce qu'ils étaient? Juste pour vous rafraîchir la mémoire, voici:

* De quoi parle ce projet et que fait-il?
* Pourquoi les gens devraient-ils s'en préoccuper et pourquoi est-ce utile?
* Comment peut-on commencer à contribuer au projet?
* Qui peut être contacté au cas où quelqu'un aurait besoin d'aide?
* Un lien vers la licence, les directives de contribution et le code de conduite.
* Une description de la structure du projet.
* Qui est impliqué et quels sont leurs rôles.
* Le statut actuel du projet.

Donc, dans RStudio, ouvrez ce fichier, essayez d’ajouter quelques informations à ce sujet pour votre projet. Si vous faites cela pour un projet réel, essayez de le rendre utile. Si vous ne faites que bricoler pour le moment, vous pouvez ajouter ce que vous voulez.

N'oubliez pas que votre fichier `README` est au format Markdown (.md). Pour un rappel sur quelques utilisations simples de la syntaxe markdown, consultez cette feuille de triche [pratique](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/markdown.png?raw=true" width="600px"/>
</p>

<p align="center"><i>Capture d'écran de ce que ce module regarde dans Markdown, pendant le développement. Méta.</i></p>

  


## Sixième étape: un engagement courageux <a name="six"></a>

OK, vous devriez maintenant avoir un fichier `README` bien édité. Nous allons maintenant «engager» ceci dans le projet en utilisant Git. En gros, cela équivaut à enregistrer cette version de votre projet, avec un enregistrement des modifications apportées. Les commits successifs produisent une histoire qui peut être examinée ultérieurement, ce qui vous permet de travailler en toute confiance.

Il y a plusieurs façons de le faire.

1. Allez à **Outils> Contrôle de version> Valider**
2. Dans le volet environnement de RStudio, il devrait y avoir un nouvel onglet "Git". Pratique.
3. Dans le volet de votre console, il devrait maintenant y avoir un nouveau "Terminal", avec lequel vous pouvez exécuter les lignes de commande Git.

Restons juste avec la deuxième option pour le moment. Cette sous-fenêtre Git vous indique quels fichiers ont été modifiés et inclut des boutons pour les commandes Git les plus importantes que nous avons vues précédemment.

Sélectionnez le fichier `README` dans la fenêtre Git, qui devrait s'afficher automatiquement si vous l'avez modifié. Cela ajoute ce fichier à la zone de "stockage intermédiaire", ce qui est un peu comme l'espace de pré-économie pour votre travail. Cliquez sur 'Commit' et une nouvelle fenêtre devrait apparaître.

Ici, vous avez la possibilité de passer en revue vos modifications et d’écrire un message de validation intéressant. Tapez quelque chose de bref, mais informatif sur les modifications que vous avez apportées dans cette version ou un instantané de votre travail. Vous souhaitez que ces informations soient suffisantes pour que, si vous ou une autre personne pouvez y revenir, vous sachiez pourquoi vous avez effectué ce commit et les modifications qui y sont associées. Ce sont comme des filets de sécurité pour votre projet au cas où vous auriez besoin de vous retirer pour une raison quelconque.

> **Pro-tip**: Ici, vous verrez une liste de tous les changements que vous avez effectués depuis votre dernier commit Les anciennes lignes supprimées sont en rouge et les lignes nouvellement ajoutées sont en vert. Vérifiez-les deux fois pour vous assurer que les modifications que vous avez apportées sont celles que vous aviez l'intention de faire. Ceci est vraiment utile pour repérer les fautes de frappe, les modifications perdues et toute autre petite erreur que vous pourriez avoir accidentellement introduite. La sécurité d'abord.

**Remarque** Si vous êtes daltonien et que vous ne voyez pas quelles lignes ont été ajoutées ou supprimées, vous pouvez utiliser les numéros de ligne des deux colonnes à gauche de la fenêtre. Ici, le numéro de la première colonne identifie l'ancienne version et le numéro de la deuxième colonne identifie la nouvelle version.

Maintenant, lorsque vous cliquez sur 'Valider', une autre fenêtre apparaîtra, vous indiquant le nombre de fichiers que vous avez modifiés et le nombre de lignes que vous avez modifiées. Fermez cette petite fenêtre.

  


## Septième étape: PUSH! <a name="seven"></a>

Cliquez sur le bouton *Push* en haut à droite de la nouvelle fenêtre. Une nouvelle fenêtre apparaîtra maintenant. Cela permet de synchroniser les fichiers modifiés sur votre référentiel local avec le fichier `README` avec la version en ligne du projet sur GitHub.

Pour ce faire à partir du shell, utilisez la commande suivante:

`git push -u origine master`

Quelques fois ici, vous serez invité à ajouter votre nom d'utilisateur et mot de passe de GitHub, que vous devriez faire si demandé.

Fermez cette fenêtre et la suivante. Accédez à votre projet sur GitHub, actualisez et vérifiez que le fichier `README` est toujours présent dans toute sa gloire. Vous devriez également voir le message de validation que vous avez créé à côté du fichier.

  


**ÉTAPE OPTIONNELLE AVANCÉE / IMPRESSIONNANTE**

Bon, alors vous venez de placer du contenu dans votre premier dépôt, génial! Maintenant, mettons cela en pratique pour un vrai projet. Par exemple, celui auquel vous participez actuellement. Essayons ceci:

1. Accédez au référentiel de ce projet sur [GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source)

2. Ajoutez le référentiel à votre propre compte GitHub. L'URL pour cela devrait être: `https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source.git`

3. Rendez-vous dans RStudio, accédez à **Fichier> Nouveau projet**, choisissez *Version Control*, sélectionnez *Git*, puis collez l'URL du référentiel créé dans votre copie du référentiel. Vous avez maintenant votre propre copie versionnée de tout ce module. Soigné. Enregistrez ceci quelque part sur votre ordinateur local.

4. Maintenant, vous devez dire à Git qu’une version différente de ce projet existe. Ouvrez le *Shell*et entrez la commande: `git ajouter à distance en amont https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source`

5. Ce que vous venez de faire, c’est de nommer la branche originale ici `amont`, histoire de simplifier les choses. Maintenant, créez une nouvelle branche **** pour documenter vos modifications indépendamment de la branche principale. Entrez la commande: `git checkout -b propose-changements maître`

6. Vous venez de créer une nouvelle branche appelée `changes-changes proposés` où vous pouvez maintenant modifier tout le contenu et les fichiers à votre guise. Espérons que la structure de ce projet est suffisamment simple pour vous permettre de naviguer. Tous les fichiers bruts du MOOC se trouvent dans le dossier `content_development` , il s’agit de `Task_3.md`.

7. Si vous faites défiler la liste vers le bas `Task_3.md`, vous devriez voir un endroit où vous pouvez modifier votre nom et votre affiliation. Ajoutez-les, puis suivez la procédure de validation décrite ci-dessus. Si vous voyez autre chose à éditer, n'hésitez pas à l'ajouter!

8. Maintenant, vous voulez repousser les modifications dans la branche d'origine. Utilisez la commande suivante dans votre *Shell*: `origine proposée par git push-changes`

9. Retournez sur GitHub et trouvez votre fourche ici. Cliquez sur le petit bouton vert et créez une demande de tirage. Il s’agit essentiellement d’une revue visant à intégrer les modifications apportées à la branche originale de ce projet MOOC.

10.     Les propriétaires en charge du projet MOOC vont maintenant recevoir une notification à ce sujet, l'examiner et le confirmer si tout se passe bien! Nous allons l'examiner et si tout s'est bien passé, votre nom apparaîtra pour toute l'éternité en tant que personne qui a effectué cette tâche avancée.
      

11.     Prenez une tasse de thé, café ou vin pour célébrer!
      

**TOUTES NOS FÉLICITATIONS**

Vous venez d'intégrer Git à R Studio et apportez votre première modification à un projet contrôlé par la version. Votre vie ne sera plus jamais la même et votre flux de travail de recherche sera probablement plus rapide, plus agile et plus collaboratif que jamais. Bonne chance pour revenir à Word.

La grande chose est que cela ne doit pas simplement être utilisé pour le code. Vous pouvez l'utiliser pour du texte brut, du balisage, du code HTML et, bien, du code R. Les possibilités sont illimitées. Ce que vous venez d’apprendre est une nouvelle forme de gestion de projet ouvertement collaborative qui fonctionne pour un très grand nombre de tâches.

A partir de maintenant, tout dépend de vous! Un conseil est de:

* Faites des commits fréquents. Traitez Git comme votre chiot, car il nécessite une attention constante et particulière. Juste une tape sur la tête de temps en temps est suffisant pour le satisfaire, mais ce sera plus heureux avec un entretien prolongé.

* La meilleure façon de le faire est de faire un commit à chaque fois que vous travaillez sur un problème spécifique. Par exemple, écrire un paragraphe, exécuter une analyse ou réparer un bogue.

* Poussez souvent. Ne laissez pas ces commits s'accumuler, sinon vous courez plus de risques d'entrer dans des conflits de fusion. Étant donné que cela peut faire l’objet de cauchemars, veillez à pousser souvent.

* Tirez souvent. Si d'autres personnes travaillent à distance sur le même projet, vous voudrez rester au courant de leurs modifications. Veillez à extraire fréquemment leurs modifications de GitHub pour vous assurer que vous êtes tous synchronisés.

* Expérimentez et explorez! En réalité, cette tâche ne fait qu'effleurer la surface, et il existe de nombreuses fonctions, outils et méthodes d'utilisation. En réalité, il vous appartient de découvrir comment utiliser ces informations pour améliorer votre flux de travail de recherche et enfin collaborer à une recherche de meilleure qualité, plus ouverte et fiable!

* Pour en savoir plus sur les problèmes, les branches, conflits de fusion, tirer les demandes, et d' autres aspects avancés de l' utilisation de Git et rstudio, consultez ce [awesome guide](http://r-pkgs.had.co.nz/git.html) par Hadley Wickham.

  


**Connaissez-vous un moyen d'améliorer ce contenu?**

Il est temps de tester vos nouvelles compétences GitHub! Tout développement de contenu passe principalement par [ici](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md). Si vous avez une suggestion d'amélioration à apporter au contenu, à la présentation ou à quelque chose d'autre, vous pouvez le créer et il sera automatiquement intégré au contenu du MOOC après vérification par un modérateur!

## Liste des participants ayant terminé la version AVANCÉE de cette tâche

* Brendan Palmer, CRF-C, Université College Cork
* Lisa Matthias, université libre de Berlin
* Hollie Marshall, Université de Leicester 
* Eric D. Wilkey, Université Western, Canada
* José-Raúl Canay-Pazos, Université de Saint-Jacques-de-Compostelle, Espagne
* Encarnación Martínez Álvarez, Espagne
* Alberto Albz Marocchino, Italie
* Iratxe Rubio, Centre basque pour le changement climatique BC3
* Gabriele Orlandi, École supérieure de sciences sociales de Paris (EHESS), France
* Hande Sodacı, Turquie
* Luke W. Johnston, Université d’Aarhus, Danemark
* Philippe Joly, WZB et HU-Berlin
* Paul Griffiths, NCAS et U. Cambridge
* Harin Lee, Goldsmiths, Université de Londres
* Luis Camacho, Université catholique, Pérou
* Tom Cridford, Imperial College de Londres
* Nithiya Streethran, Université de Stavanger 

[![Dédicace du domaine public CC0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)