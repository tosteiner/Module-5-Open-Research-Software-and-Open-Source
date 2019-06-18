---
output:
  html_document: défaut
  pdf_document: défaut
---

# Tâche 1: Comment configurer un référentiel sur GitHub

Cette tâche est conçue pour les étudiants et les chercheurs qui souhaitent créer leur premier projet Open Source (logiciel ou non logiciel) sur GitHub. GitHub est un endroit où vous pouvez jouer et expérimenter de nouveaux flux de travail de recherche. Ce n’est vraiment qu’un début pour vous aider à préparer le terrain pour vos propres voies et idées.

N'oubliez pas que vous pouvez participer aux discussions sur notre open channel [**Slack channel**](https://osmooc.herokuapp.com/). Présentez-vous à l'adresse # module5opensource, et dites-nous un peu qui vous êtes, votre parcours, et comment vous vous êtes retrouvés ici!

**VEUILLEZ NOTER** qu’un enregistrement d’écran pour cette tâche est également disponible via [YouTube](https://www.youtube.com/watch?v=AnftV9HBPSc&).

Durée estimée: 30 à 45 minutes.

Estimez le gain de temps une fois terminé: inimaginable ..

## Table des matières

* [Commencer](#Getting_started) 
  * [Configurer un profil GitHub](#Profile)
  * [Le langage GitHub](#Language)
  * [Création d'un nouveau référentiel](#Create_new)
* [Les étapes fondamentales](#Foundation) 
  * [Choisir une licence](#License)
  * [Création d'un fichier README](#Readme)
  * [Création de directives contributives](#Contributing)
  * [Créer un code de conduite](#Conduct)
  * [Rendre votre code citable](#Citation)
* [Garder vos problèmes à jour](#Issues)
* [Check-list pour le lancement de votre projet](#Check-list)

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/Task1.png?raw=true" alt="Flux de travail de la tâche 1" width="600" height="861" style="margin-right: 30px; margin-left: 10px;" onmouseover="this.width='1200'; this.height='1722'" onmouseout="this.width='600'; this.height='861'">
</p>

<p align="center"><i>Le flux de travail pour la tâche 1. Conservez-le à portée de la main pendant que vous accomplissez cette tâche!</i></p>

  


## Commencer <a name="Getting_started"></a>

Un 'référentiel' n'est en réalité qu'un nom de fantaisie pour un projet sur GitHub. GitHub est un endroit en ligne où vous pouvez gérer des projets, stocker des fichiers et collaborer ouvertement avec d'autres. Tout cela est réalisé en utilisant le contrôle de version pour suivre les projets au fur et à mesure de leur avancement. En tant que tel, GitHub est un outil puissant pour les projets logiciels et non logiciels.

L'une des choses les plus importantes à prendre en compte à ce stade précoce est de réfléchir à la manière dont vous souhaitez que la communauté élargie interagisse avec votre projet. Pendant que vous travaillez à l'air libre, vous voulez vous assurer que les autres se sentent à l'aise pour accéder à votre travail, le regarder et le partager. La mise en place d'un référentiel de manière à réduire les barrières à l'entrée et la peur d'être un «étranger» constituent la première étape vers la réussite du projet.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/octocat.png?raw=true" width="150px" height="125px"/>
</p>

<p align="center"><i>Octocat, la petite mascotte de GitHub</i></p>

  


### Configurer un profil GitHub <a name="Profile"></a>

Pour configurer un profil GitHub, rendez-vous simplement sur la page principale et cliquez sur [Inscrivez-vous pour GitHub](https://github.com/join). Ici, vous pouvez créer votre compte personnel, avec un nom d'utilisateur, un email et un mot de passe en standard.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/github_signup.png?raw=true" width="800" /></p>

<p align="center"><i>Inscrivez-vous à GitHub</i></p>

  


La prochaine étape consiste à établir un plan personnel. Pour l'instant, sélectionnez simplement le plan "Référentiels publics illimités gratuitement", à moins que vous ne craigniez pour la confidentialité, auquel cas sélectionnez le plan privé. Si vous souhaitez configurer un projet pour une organisation, vous pouvez également sélectionner cette option.

  


### Le langage GitHub <a name="Language"></a>

C'est peut-être l'aspect le plus déroutant et déroutant de GitHub. Voici certains des termes les plus couramment utilisés et leurs définitions:

* **Initialiser**: Créez un référentiel vide.
* **Checkout**: Créez une copie de travail d'un référentiel local.
* **Clone**: Copiez le référentiel dans un répertoire local de votre ordinateur.
* **Fourchette**: Créez une ramification personnelle d'un référentiel pour travailler dessus en parallèle.
* **Branche**: Une version indépendante et parallèle d'un référentiel. Les modifications n'affectent pas la branche principale.
* **Master**: branche principale et par défaut d'un référentiel.
* **Nettoyer**: Aucune validation en attente sur la branche.
* **Étape**: Ajoutez des mises à jour prêtes à être validées dans une branche.
* **Commit**: Révision d'un référentiel, semblable à une fonction "enregistrer" versionnée.
* **Message de validation**: description des modifications accompagnant une validation.
* **Check**: une vérification de statut.
* **Fetch**: Rien à voir avec les chiens. Désigne obtenir les dernières modifications d'un référentiel en ligne sans les fusionner.
* **Index**: L'arbre qui sert de zone de transit.
* **Répertoire de travail**: L'arborescence dans laquelle les fichiers sont conservés.
* **Head**: L'arbre qui indique les derniers commits effectués.
* **Push**: Ajoutez les modifications validées à la tête de votre référentiel distant.
* **Fusion**: Combinaison des modifications apportées dans une branche avec la branche principale à la fin.
* **Pull**: Mettez à jour votre référentiel en récupérant et en fusionnant les derniers commits.
* **Demande d'extraction**: demande de fusion d'une branche mise à jour dans la branche principale.
* **Problème**: Améliorations, tâches ou questions suggérées relatives à un référentiel.

Ouf! Ne vous inquiétez pas de la mémorisation de *tout* pour le moment. Comme toute nouvelle compétence, la familiarité vient avec l'expérience.

Vous pouvez probablement voir en quoi certaines d'entre elles sont assez similaires à des opérations telles que sauvegarder, copier, coller - des opérations de flux de travail standard, mais adaptées à un processus de gestion de logiciel. Il y a un [un peu plus](https://mirrors.edge.kernel.org/pub/software/scm/git/docs/gitglossary.html) aussi, mais cela devrait faire pour commencer.

Si vous êtes intéressé, la plupart de ces termes proviennent du système sous-jacent [Git](https://git-scm.com). Git a été conçu pour permettre aux développeurs de gérer différentes versions du code source de manière distribuée, ce qui est excellent. Il a beaucoup de fonctionnalités et la capacité de faire beaucoup de choses complexes, écrit par un [gars très intelligent](https://www.linuxfoundation.org/blog/2015/04/10-years-of-git-an-interview-with-git-creator-linus-torvalds/). Cependant, l'interface utilisateur [n'a pas été conçue pour les nouveaux utilisateurs](https://xkcd.com/1597/)et peut donc être difficile à apprendre.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/git.png?raw=true" width="150px"/>
</p>

<p align="center"><i>Guide imbattable pour utiliser Git. (Source: XKCD)</i></p>

  


### Création d'un nouveau référentiel <a name="Create_new"></a>

Sur votre profil GitHub, cliquez sur "Créer un nouveau référentiel". La première étape consiste à créer un nom en tant que marque de votre projet. Idéalement, cela devrait être mémorable et donner une indication de ce que le projet fait.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/new_repo.png?raw=true" width="800" /></p>

<p align="center"><i>Créer un nouveau référentiel</i></p>

  


Veillez à ne pas dupliquer les noms, à ne pas porter atteinte à d’autres marques, ou à ne rien nommer d’offensif.

  


## Les étapes fondamentales <a name="Foundation"></a>

Tout référentiel GitHub nécessite 4 éléments clés pour démarrer et commencer à développer une communauté accueillante:

1. Une licence Open Source;
2. Un fichier `README`;
3. Directives contributives; et
4. Un code de conduite.

Ce sont des aspects critiques et les meilleures pratiques de tout projet permettant aux utilisateurs de comprendre leurs droits, leurs attentes, l'objectif du projet et d'améliorer l'expérience globale de l'utilisateur.

Ces quatre fichiers doivent être conservés dans le répertoire racine du référentiel de votre projet. Il est courant d’utiliser des formats de fichier de démarquage (`.md`) pour la plupart de ces fichiers (bien que le fichier de licence soit le plus souvent en texte brut (`.txt`)) et de mettre en majuscule tous les noms de fichiers. Au lieu d'espaces dans les noms de fichiers, veillez à utiliser des traits de soulignement `_`.

Donc, vous devriez vous retrouver avec une sélection de fichier fondamentale comme ceci:

1. `LICENCE.md`
2. `LISEZMOI.md`
3. `CONTRIBUTING.md`
4. `CODE_OF_CONDUCT.md`

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/foundation.png?raw=true" width="800" /></p>

<p align="center"><i>La structure de base du référentiel</i></p>

  


### Choisir une licence <a name="License"></a>

Choisir une licence appropriée est ce qui différenciera votre référentiel Open Source des logiciels disponibles au public. Bien que vous ne soyez pas obligé de choisir une licence, vous garantissez ainsi que d'autres personnes pourront modifier, partager, réutiliser et développer votre projet dans un cadre légal.

Pour commencer, vous voulez cocher [Choisissez Une licence](https://choosealicense.com/) pour trouver la licence qui convient le mieux à vos intentions pour le référentiel.

Les trois principaux choix sont:

* **Licence MIT**: Une licence permissive qui permet aux utilisateurs de faire ce qu’ils veulent avec votre code, à condition qu’elle vous attribue les attributions appropriées et ne vous engage pas à la responsabilité.
* **Apache License 2.0**: autorisations similaires à la licence MIT, mais fournit également une concession expresse de droits de brevet des contributeurs aux utilisateurs.
* **Licence publique générale GNU (GPL) v3**: Licence [copyleft](https://en.wikipedia.org/wiki/Copyleft) qui oblige toute personne qui redistribue votre code, ou un travail dérivé, de rendre la source disponible sous les mêmes conditions que la licence originale; fournit également une concession expresse de droits de brevet des contributeurs aux utilisateurs.

Heureusement, lorsque vous démarrez un nouveau référentiel sur GitHub, vous avez la possibilité de sélectionner une licence existante dans un menu déroulant. Vous devriez toujours (à de très rares exceptions près) utiliser une licence existante, car c’est ce que les utilisateurs potentiels et les contributeurs verront avant d’utiliser ou de contribuer à votre logiciel.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/license.png?raw=true" width="800" /></p>

<p align="center"><i>Choisir un exemple de licence</i></p>

  


S'ils n'en ont pas un que vous voulez, vous pouvez en ajouter un que vous aimez manuellement. Pour ce faire, cliquez simplement sur "Créer un nouveau fichier" dans le référentiel, puis copiez et collez un texte de licence existant dans. Nommez le fichier sous la forme `LICENSE.txt` ou `LICENSE.md` pour le rendre clair et conservez-le dans le dossier du référentiel principal (la racine). Assurez-vous d'ajouter un message de validation propre et vous avez terminé!

> **Coup de main**: Ce MOOC utilise une combinaison différente de licences pour le contenu de code et le contenu sans code. Vous trouverez ici un exemple de la licence [MIT](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/LICENSE.md) que nous appliquons pour tout code et logiciel généré dans le cadre de la production de MOOC.

  


### Création d'un fichier README <a name="Readme"></a>

Lorsque vous initialisez votre nouveau référentiel, vous devez avoir la possibilité de le faire avec un fichier `README`. Comme Alice au pays des merveilles, ils font exactement ce qu'ils disent - fournissent des informations clés sur le projet. C’est généralement la première chose que les contributeurs extérieurs verront lorsqu’ils se rendront dans votre référentiel. Il est donc essentiel de les informer et de les accueillir.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/readme.png?raw=true" width="800" /></p>

<p align="center"><i>Une partie du fichier README pour ce module</i></p>

  


Le fichier sera initialement au format Markdown (`.md`). C'est un langage de balisage léger avec un format de texte brut. Pour apprendre quelques démarques de base, voir [cette feuille de triche](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet). Mais pour l'instant, nous pouvons simplement utiliser du texte brut.

Il y a plusieurs choses que vous voudrez inclure dans votre fichier `README`:

* De quoi parle ce projet et que fait-il?
* Pourquoi les gens devraient-ils s'en préoccuper et pourquoi est-ce utile?
* Comment peut-on commencer à contribuer au projet?
* Qui peut être contacté au cas où quelqu'un aurait besoin d'aide?
* Un lien vers la licence, les directives de contribution et le code de conduite.
* Une description de la structure du projet.
* Qui est impliqué et quels sont leurs rôles.
* Le statut actuel du projet.

> **Astuce**: Plus tard, au fur et à mesure du développement de votre projet, vous voudrez peut-être ajouter une FAQ basée sur les commentaires de la communauté ou un tutoriel pour aider les utilisateurs à comprendre le fonctionnement de votre projet.

N'oubliez pas que tout le monde qui participe à votre projet ne sera pas un expert ou ne comprendra pas ce que vous faites et pourquoi. Avoir un fichier `README` bien documenté améliorera l'expérience utilisateur pour les personnes possédant une gamme de connaissances antérieures.

Lorsque le fichier `README` est inclus dans le répertoire racine, GitHub l'affichera automatiquement sur la page d'accueil de votre référentiel. Cela signifie que c'est la première chose que les gens verront souvent, alors faites en sorte que ça compte!

> **Coup de main**: Vous trouverez ici le fichier `README` utilisé pour ce module [MOOC](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/README.md). Cela inclut des informations sur le statut, la justification, les résultats d'apprentissage, l'équipe de développement, les documents clés et la licence pour aider. Vous pouvez copier et adapter cette structure pour vos propres projets selon vos besoins.

  


### Création de directives contributives <a name="Contributing"></a>

Les directives de contribution sont conçues pour communiquer aux contributeurs potentiels un bref guide sur la manière de s’engager dans votre projet et votre communauté. Vous voulez vous assurer d’être accueillant et indiquer que vous souhaitez que les participants s’engagent dans votre projet. Lorsqu'un participant ouvre une nouvelle demande d'extraction ou crée un nouveau problème, il voit un lien vers votre fichier de contribution.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/contributing.png?raw=true" width="800" /></p>

<p align="center"><i>Une partie des directives `CONTRIBUTING` pour ce module</i></p>

  


En ce qui concerne les noms de fichiers en majuscules, l’étape suivante consiste à créer un fichier `CONTRIBUTING`. Cliquez sur 'Créer un nouveau fichier' et assurez-vous de l'enregistrer au format markdown comme auparavant. Ce fichier indiquera aux autres utilisateurs comment ils peuvent s’impliquer et participer à votre projet. Il s’agit du premier pas vers la création d’une communauté autour de votre projet. Rendez-le donc engageant, concis et informatif.

Le fichier `CONTRIBUTING` doit contenir des informations sur:

* Quel type de contributions que vous recherchez.
* Comment suggérer des mises à jour ou de nouvelles fonctionnalités.
* Comment interagir avec le projet en utilisant les fonctions de GitHub (par exemple, le protocole de requête d'extraction).
* Comment déposer un rapport de bogue ou créer un problème.
* L'objectif ultime, la vision ou la feuille de route du projet.
* Comment contacter les responsables du projet.
* Liens vers toute documentation externe ou sites Web.

> **Astuce**: Envisagez de commencer par une brève note de remerciement aux personnes qui prennent le temps d’envisager de contribuer - elles ont cliqué sur le fichier pour en savoir plus après tout! Si vous envisagez d'autres méthodes de reconnaissance, assurez-vous de les inclure également ici.

Ici, vous essayez essentiellement d'encourager les gens à donner de leur temps pour faire avancer votre projet. Assurez-vous d'être accueillant et amical, et précisez comment les gens peuvent s'engager. Lorsque vous écrivez cela, assurez-vous de penser à cela du point de vue de l'utilisateur. Comment leur simplifier la vie en soumettant des demandes d'extraction et en ouvrant des problèmes pour rendre l'ensemble du projet plus fluide.

> **Coup de main**: Les [directives contribuants](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CONTRIBUTING.md) pour ce module MOOC comprennent des choses très spécifiques: une introduction à l' utilisation de Git et GitHub, des conseils pour la mise en route, des informations de contact, comment modifier le contenu et les questions RAPPOR, un lien vers le `Fichier README` et informations sur le contenu préféré et les styles de code. N'hésitez pas à copier et à adapter cela à votre propre projet selon vos besoins.

  


### Créer un code de conduite <a name="Conduct"></a>

Un code de conduite est important pour définir les règles de base du comportement et de la participation attendus des contributeurs au projet. Il constitue un document facilement référencé pour montrer que votre équipe de projet prend au sérieux les dialogues constructifs. Par conséquent, il s'agit d'un élément essentiel pour la création et le maintien d'une communauté en santé qui s'engage de manière constructive et productive dans une atmosphère sociale positive.

Un code de conduite non seulement définit les attentes en matière de comportement, mais décrit également à qui ces attentes s'appliquent, lorsqu'elles s'appliquent, que faire en cas d'infraction au code et quelles en seront les actions. En tant que tels, les points de contact doivent être clairement définis dans le code de conduite. En règle générale, cela doit être privé, par exemple une adresse électronique.

> **Astuce**: Si une violation de la personne qui reçoit ces informations doit être signalée, veillez à inclure une option permettant de contacter une partie secondaire.

Pour ajouter un code de conduite, vous pouvez créer le vôtre en ajoutant un nouveau fichier de démarques, ou utiliser des modèles existants tels que le covenant [contributeur](https://contributor-covenant.org/). Nommez votre fichier `CODE_OF_CONDUCT.md`et assurez-vous qu'il est visible dans le fichier `README`.

> **Coup de main**: Ce MOOC a également un [Code de conduite](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CODE_OF_CONDUCT.md) basé sur le Pacte des donateurs. Comme vous pouvez le constater, il comprend des informations sur les normes de comportement attendues, les responsabilités des membres de la communauté et l'application du code de conduite, y compris les coordonnées. N'hésitez pas à réutiliser et à adapter cela à votre projet comme bon vous semble.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/code_of_conduct.png?raw=true" width="800" /></p>

<p align="center"><i>Partie du fichier CODE OF CONDUCT de ce module, basée sur le covenant du contributeur</i></p>

  


Il est important de veiller à appliquer le code de conduite, car cela montre que non seulement vous le valorisez, mais vous respectez l'influence qu'il a sur votre communauté. Il est important de traiter chaque membre de la communauté avec le respect, la courtoisie et l'importance qu'il mérite. En cas d'infraction ou si un récidiviste commet des infractions systématiques, il est préférable de consulter le [Open Source Guide](https://opensource.guide/code-of-conduct/#enforcing-your-code-of-conduct) pour savoir comment appliquer le code de conduite.

  


### Rendre votre code citable <a name="Citation"></a>

Si vous souhaitez que votre code soit citable dès le début, vous devez stocker les métadonnées nécessaires à une citation depuis le début en créant un fichier `[codemeta.json](https://codemeta.github.io)` ou un fichier `[CITATION.cff](https: //citation-file-format.github.io)` fichier. Les deux permettront aux outils en cours de développement de créer automatiquement des informations de citation, plutôt que de vous demander de les saisir ultérieurement dans un formulaire.

Si vous êtes intéressé, [cite.research-software.org](https://cite.research-software.org) fournit des informations de base supplémentaires sur la citation de logiciels dans les universités.

  


## Garder vos problèmes à jour <a name="Issues"></a>

Les problèmes ne sont pas nécessairement des problèmes avec un projet, mais aussi des suggestions d'amélioration, des éléments à développer dans le futur, ainsi que des commentaires et des remarques sur le projet sur lesquels travailler. Ils peuvent être partagés ouvertement et discutés avec les contributeurs selon les besoins, un peu comme un forum.

Si vous dirigez un projet, il est important de conserver une liste de problèmes qui permettent aux contributeurs de déterminer clairement quels aspects du projet nécessitent une attention particulière. Il est également important de traiter de manière positive le plus grand nombre possible de problèmes, afin de montrer que vous prenez leurs contributions au sérieux.

Les éléments clés des problèmes incluent:

* Un titre informatif et une description;
* Étiquettes / étiquettes codées par couleurs pour aider à classer et filtrer;
* Jalons pour associer des problèmes à des fonctionnalités spécifiques ou à des phases de projet;
* Les cessionnaires indiquent qui est chargé de travailler sur un problème;
* Commentaires pour fournir des commentaires.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/issues.png?raw=true" width="800" /></p>

<p align="center"><i>Le suivi des problèmes pour le projet de stratégie de bourses ouvertes</i></p>

  


Dans les numéros, il est possible d’utiliser @ mentions pour informer les autres intervenants du problème et pour que les bonnes personnes s’impliquent de manière efficace. GitHub a un système interne de notifications, tout comme Facebook ou Twitter, et peut également envoyer des emails aux personnes mentionnées dans le suivi des problèmes. Tout cela peut être personnalisé pour les individus dans les paramètres de l'utilisateur.

  


## Liste de contrôle pour le lancement de votre projet <a name="Checklist"></a>

Alors maintenant, vous êtes prêt à lancer votre projet, commencer à en faire la publicité et à recevoir des contributions! Avant de continuer, assurez-vous que vous avez:

* [] Le projet a un nom mémorable et informatif
* [] Project a un fichier `LICENSE` qui est une copie exacte d'une licence Open Source.
* [] Documentation complète comprenant les fichiers `README`, `CONTRIBUTING`et `CODE_OF_CONDUCT`.
* [] Le projet a au moins un problème clairement identifié
* [] Tout code inclus à cette étape est clairement structuré et annoté

**TOUTES NOS FÉLICITATIONS!**

Vous avez maintenant lancé un projet de recherche Open Source! J'espère qu'à partir de maintenant, votre travail profitera à l'ensemble de la communauté, forgera de nouvelles collaborations et créera de nouvelles et fantastiques opportunités pour vous tous. Essayez de réfléchir à la manière dont ces compétences peuvent être appliquées à de futurs projets et à la manière dont elles auraient pu vous aider dans le passé.

A partir de maintenant, tout dépend de vous! Un conseil est de:

* Écrivez le code propre;
* Avoir un projet bien structuré;
* Faites des commits fréquents avec des messages propres;
* Gardez les projets bien documentés;
* Avoir des directives de contribution claires;
* Utilisez les fonctions de description et de balise;
* Ne divisez pas le référentiel de quelqu'un d'autre à moins que vous n'ayez l'intention de travailler dessus;
* Assurez-vous de contribuer également aux projets des autres.

**Connaissez-vous un moyen d'améliorer ce contenu?**

Il est temps de tester vos nouvelles compétences GitHub! Tout développement de contenu passe principalement par [ici](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md). Si vous avez une suggestion d'amélioration à apporter au contenu, à la présentation ou à quelque chose d'autre, vous pouvez le créer et il sera automatiquement intégré au contenu du MOOC après vérification par un modérateur!

[![Dédicace du domaine public CC0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)