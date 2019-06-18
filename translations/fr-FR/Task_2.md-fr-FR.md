---
output:
  html_document: défaut
  pdf_document: défaut
---

# Tâche 2: Comment rendre votre code citable à l'aide de GitHub et Zenodo

Cette tâche est conçue pour les étudiants et les chercheurs qui souhaitent créer et réutiliser des projets / référentiels basés sur GitHub dans la littérature académique.

N'oubliez pas que vous pouvez participer aux discussions sur notre open channel [**Slack channel**](https://osmooc.herokuapp.com/). Présentez-vous à l'adresse # module5opensource, et dites-nous un peu qui vous êtes, votre parcours, et comment vous vous êtes retrouvés ici!

Durée estimée: 45 à 60 minutes.

## Table des matières

- [Avant-propos](#Foreword)
- [Configurer un dépôt GitHub](#Setup)
- [Choisissez votre dépôt GitHub](#Choose)
- [Se connecter à Zenodo](#Login)
- [Autoriser GitHub à se connecter à Zenodo](#Authorise)
- [Sélectionnez le référentiel à archiver](#Archive)
- [Vérifier les paramètres du référentiel](#Check)
- [Créer une nouvelle version](#Release)
- [Obtenir un DOI](#DOI)
- [Liste de contrôle pour citer votre projet](#Checklist)
- [Ressources supplémentaires](#Resources)

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/Task2.png?raw=true" alt="Flux de travail de la tâche 2" width="600" height="861" style="margin-right: 30px; margin-left: 10px;" onmouseover="this.width='1200'; this.height='1722'" onmouseout="this.width='600'; this.height='861'">
</p>

<p align="center"><i>Le flux de travail pour la tâche 2. Conservez-le à portée de la main pendant que vous accomplissez cette tâche!</i></p>

  


## Avant-propos <a name="Foreword"></a>

Bien que l’intégration de GitHub et de Zenodo facilite aujourd’hui le travail avec ces outils (janvier 2019), il est important de souligner qu’il existe des alternatives à GitHub (Gitlab, Bitbucket, ...) et à Zenodo (d’autres dépôts pourraient demandez à vos collègues). Par exemple, vous pouvez utiliser Gitlab et télécharger manuellement chaque nouvelle version dans le référentiel de votre université, en obtenant un DOI. Les principes (travailler avec un système de contrôle de version en ligne et archiver les versions majeures dans un référentiel fournissant un identifiant unique persistant) peuvent être appliqués dans différents flux de travail.

## Configurer un dépôt GitHub <a name="Setup"></a>

> **Conseil**: veillez à inclure un fichier LICENSE et README dans votre référentiel. Cela indiquera aux gens le but du projet et comment ils peuvent s’y engager à l’avenir.

Découvrez comment mettre en place un référentiel GitHub dans cette autre guide [Tâche 1: Construire un référentiel GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) qui fait également partie du «Module 5: Open Software Recherche et Open Source.

## Choisissez votre dépôt GitHub <a name="Choose"></a>

Une fois sur votre page de listes de projets GitHub à l'adresse [github.com](https://github.com) accédez à l'onglet "Référentiels". Sélectionnez le référentiel que vous souhaitez archiver et ouvrez-le.

  


## Se connecter à Zenodo <a name="Login"></a>

Maintenant dirigez-vous vers [zenodo.org](https://zenodo.org). Zenodo est une plate-forme sur laquelle vous pouvez archiver en permanence votre code et d'autres éléments de projet. Pour ce faire, Zenodo attribue aux projets un identificateur d'objet numérique</strong> (DOI) **, ce qui contribue également à rendre le travail plus rentable. Cela diffère de GitHub, qui agit comme un endroit où le travail réel d’un projet a lieu, plutôt que son archivage à long terme. Sur GitHub, le contenu peut être modifié, supprimé, réécrit et irréversiblement, ce qui le rend un peu inquiétant d'être utilisé à des fins de référencement plus durables. Zenodo offre plus de sécurité et de permanence pour les résultats de recherche.</p>

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/zenodo.png?raw=true" width="800" /></p>

<p align="center"><i>Inscrivez-vous à Zenodo</i></p>

  


Si vous avez déjà un compte Zenodo, c'est facile. Sinon, suivez les étapes pour en créer un - vous pouvez même vous connecter en utilisant votre compte GitHub ou votre profil ORCID pour simplifier les choses, car Zenodo a une intégration intégrée. Cela pourrait être plus facile que de créer un autre compte et profil de recherche.

  


## Autoriser GitHub à se connecter à Zenodo <a name="Authorise"></a>

Sur le site Web Zenodo, autorisez-le à se connecter à votre compte GitHub dans la section "[utilisant GitHub](https://zenodo.org/account/settings/github/)". Ici, Zenodo vous redirigera vers GitHub pour demander les autorisations d'utilisation de "[Webhooks](https://developer.github.com/webhooks/)" sur vos référentiels. Vous souhaitez autoriser Zenodo ici avec les autorisations nécessaires pour créer ces liens.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/zenodo_github.png?raw=true" width="800" /></p>

<p align="center"><i>Autoriser Zenodo à se connecter à GitHub</i></p>

  


Si vous essayez de donner à Zenodo l'accès à un référentiel organisationnel, vous (ou un administrateur) devez vous assurer que Zenodo dispose des autorisations nécessaires pour accéder à des tiers. GitHub enverra un email d'autorisation qui doit être confirmé. À ce stade, dans les paramètres de votre référentiel sur GitHub, vous devez également vous assurer que le référentiel est défini sur "public" et non sur privé.

  


## Sélectionnez le référentiel à archiver <a name="Archive"></a>

Si vous en êtes à ce stade, cela signifie que Zenodo est désormais autorisé à configurer les Webhooks du référentiel dont il a besoin pour archiver le référentiel et lui envoyer un DOI. Pour ce faire, sur le site Web Zenodo, accédez à la page</a> liste des référentiels GitHub et cliquez simplement sur le bouton "on" situé en regard de votre référentiel.</p>

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/enabled_repos.png?raw=true" width="800" /></p>

<p align="center"><i>Activer la conservation des référentiels GitHub individuels dans Zenodo</i></p>

  


## Vérifier les paramètres du référentiel <a name="Check"></a>

Vous avez maintenant configuré un nouveau Webhook entre Zenodo et votre référentiel. Dans GitHub, cliquez sur les paramètres de votre référentiel, puis sur l'onglet Webhooks dans le menu de gauche. Cela devrait afficher le nouveau Webhook de Zenodo configuré pour Zenodo. Notez que la liste des Webhook peut prendre un peu de temps à s’afficher.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/webhooks.png?raw=true" width="800" /></p>

<p align="center"><i>Vérifiez que les webhooks sont activés pour votre référentiel GitHub. Exemple ici en utilisant la stratégie Open Scholarship</i></p>

  


## Créer une nouvelle version <a name="Release"></a>

La première fois que vous archivez un référentiel, on parle de «première version». Chaque fois que vous créez et archivez une nouvelle version de ce référentiel, vous créez une nouvelle version. Cela peut être suivi dans l'onglet 'releases' de votre dépôt sur GitHub (en haut au centre).

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/first_release.png?raw=true" width="800" /></p>

<p align="center"><i>Vérifiez que la première version du référentiel a réussi. Exemple ici en utilisant la stratégie Open Scholarship</i></p>

  


Pour la première version archivée de votre référentiel, cliquez sur "Créer une nouvelle version" dans Zenodo. Remplissez le formulaire et donnez quelques détails sur ce que le communiqué implique. Pour la première version, assurez-vous de l'appeler v1.0.0, comme il est d'usage.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/create_release.png?raw=true" width="800" /></p>

<p align="center"><i>Créer une nouvelle version. Exemple ici utilisant la stratégie Open Scholarship, pour laquelle une première version existe déjà</i></p>

  


Enfin, cliquez sur "Publier le communiqué" et vos archives seront publiées et versionnées sur GitHub.

Pour voir votre communiqué sur Zenodo, vous devez visiter l’onglet [Upload](https://zenodo.org/deposit). Pour terminer l'archivage, quelques précisions supplémentaires sont nécessaires sur Zenodo.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/upload_release.png?raw=true" width="800" /></p>

<p align="center"><i>Vérifiez que la nouvelle version a été téléchargée. Exemple présenté ici à l'aide de la stratégie de bourses ouvertes</i></p>

  


## Obtenir un DOI <a name="DOI"></a>

C'est ce que l'on appelle parfois "frapper" DOI et qui nécessite quelques informations supplémentaires sur le référentiel de Zenodo. Sur Zenodo, cliquez sur l’onglet [Upload](https://zenodo.org/deposit) du menu principal. Le référentiel que vous venez de télécharger devrait y figurer. Faites défiler la page et remplissez les informations supplémentaires si nécessaire. Les champs obligatoires sont signalés par un astérisque rouge, puis cliquez sur "Publier".

**Remarque**: Ce n'est que lorsque ces informations supplémentaires auront été ajoutées que votre DOI deviendra opérationnel. Cela peut également prendre un peu de temps pour que le DOI devienne actif. Exemple de DOI présenté ci-dessous (pour la stratégie de bourses ouvertes).

> **Astuce**: copiez l'URL de la DOI dans le fichier README de votre dépôt GitHub pour faciliter la réticulation, et présentez un badge DOI en surbrillance pour que les utilisateurs puissent voir et utiliser votre DOI. Vous ne devez le faire qu’une fois avec votre première version DOI car elle agit en tant que «concept DOI» et est liée à toutes les versions ultérieures de DOI.

[![EST CE QUE JE](https://zenodo.org/badge/DOI/10.5281/zenodo.1323437.svg)](https://doi.org/10.5281/zenodo.1323437)

L’intégration GitHub / Zenodo va maintenant assigner un DOI à chaque version / édition d’un référentiel de projet. Cela permet aux utilisateurs de faire référence à des versions spécifiques de projets et de les citer. En outre, la liste des auteurs pour la citation est automatiquement déterminée par les noms de compte utilisateur GitHub utilisés par le référentiel - cela signifie que personne ne sera laissé pour compte. Les détails de l'auteur peuvent être modifiés ultérieurement sur Zenodo. Les DOI utilisées dans Zenodo sont enregistrées via le service [DataCite](https://www.datacite.org/).

> **Astuce**: Créez une version "lisible par l'homme" de cette citation dans le fichier README de votre projet. Cela sera utile aux chercheurs qui ne sont peut-être pas familiers avec l'utilisation de DOI pour créer des citations, et il sera plus facile pour d'autres de citer votre logiciel et de reconnaître votre travail. Un exemple de ceci pourrait être: Jon Tennant. (2018, 30 juillet). Fondations pour le développement d'une stratégie de bourses ouvertes: Première version officielle (version 1.2). Zenodo. <http://doi.org/10.5281/zenodo.1323437>

**TOUTES NOS FÉLICITATIONS!!**

Votre référentiel GitHub est maintenant archivé dans Zenodo et avec une DOI pouvant être versionnée pour refléter les mises à jour de la version du référentiel au fil du temps. Vous devriez pouvoir voir les détails à ce sujet sur la page GitHub Zenodo de votre référentiel. Cela signifie également que vos projets archivés peuvent être récupérés par d'autres services d'indexation et moteurs de recherche utilisant également des DOI.

Fournir des archives à long terme et un DOI pour votre travail est nécessaire pour que les autres puissent le citer correctement, car cela fournit des métadonnées de base. Pour Open Science, il est important de pouvoir citer le logiciel que vous utilisez dans votre recherche, et ce flux de travail intégré permet cela, conformément aux meilleures pratiques en matière de citation de recherche. De plus, cette pratique est importante pour que la norme des logiciels (et des projets connexes) devienne la norme des autres résultats de recherche.

> **Conseil**: votre recherche est-elle financée par une subvention de l’UE? Vous pouvez désormais connecter directement votre projet archivé à votre subvention en mettant à jour la section des métadonnées des subventions dans l'enregistrement Zenodo du projet. Cela contribue massivement à augmenter sa découvrabilité!

  


## Liste de contrôle pour citer votre projet <a name="Checklist"></a>

Vous disposez maintenant d’un référentiel GitHub archivé de manière durable dans Zenodo, prêt à être réutilisé et cité! Avant de continuer, assurez-vous que vous avez:

- [] Lié votre projet GitHub à Zenodo. Si vous voyez une copie complète de votre référentiel GitHub dans Zenodo, tout fonctionne.
- [] La configuration intégrée de Zenodo et GitHub fonctionne bien. Par exemple, indiquez tous les noms d’auteurs et le titre du projet correct dans Zenodo. Sinon, ou si les auteurs ont juste des pseudonymes, vous pouvez modifier ces détails dans Zenodo.
- [] Le projet a une première version, avec un DOI. Vous devriez avoir un DOI affiché sur la page de vos projets Zenodo. Ce premier DOI s'appelle le «concept DOI» et constitue le lien principal entre tous les DOI de versions ultérieures. Copiez ce lien DOI et intégrez-le dans la page LISEZMOI de vos projets GitHub. Vous avez terminé!

### Ressources supplémentaires <a name="Resources"></a>

[Rendre votre code citable](https://guides.github.com/activities/citable-code/) - Guides GitHub.

**Connaissez-vous un moyen d'améliorer ce contenu?**

Il est temps de tester vos nouvelles compétences GitHub! Tout développement de contenu passe principalement par [ici](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md). Si vous avez une suggestion d'amélioration à apporter au contenu, à la présentation ou à quelque chose d'autre, vous pouvez le créer et il sera automatiquement intégré au contenu du MOOC après vérification par un modérateur!

[![Dédicace du domaine public CC0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)