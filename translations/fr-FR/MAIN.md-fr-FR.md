---
output:
  html_document: défaut
  pdf_document: défaut
---

# Module 5: Logiciel de recherche ouvert et Open Source

## Table des matières

- [introduction](#Introduction)
- [Qu'est-ce qu'un logiciel Open Source?](#What_OSS)
- [Principes des logiciels Open Source](#Principles)
- [The Open Source community and its governance](#OS_Community)
- [Plateformes et outils existants pour les logiciels Open Source](#Platforms)
- [Logiciel Open Source utilisé dans la recherche](#Research)
- [Premiers pas avec l'OSS - FAQ](#FAQ)
- [Faire un bon logiciel pour la réutilisation](#Reuse)
- [Licence Open Source](#Licensing)
- [Citation du logiciel](#Citation)
- [Utiliser GitHub et Zenodo](#GitHub_Zenodo)
- [Collaborer via Open Source](#Collaborating)
- [Où aller en partant d'ici](#Future_OSS)

**VEUILLEZ NOTER** qu’une version audio de ce document est disponible au téléchargement via [Soundcloud](https://soundcloud.com/open-science-mooc/module-5-open-source-and-open-research-software) et [YouTube](https://www.youtube.com/watch?v=BHrOEmKk5zM).

## introduction <a name="Introduction"></a>

Bienvenue au **Module 5** du MOOC Open Science: **Logiciels de recherche ouverts et Open Source**.

Ce module a été développé [à l’air libre](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source) grâce à la collaboration d’une équipe internationale de [afficianados](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/README.md#development-team-)Open Source. Tout ce que vous voyez ici a été développé au grand jour grâce à un retour interactif et à la collaboration de la communauté. Il comprend une série de vidéos, des infographies, des lectures au format texte et des tâches pratiques pour que vous puissiez vous mordre à la gorge.

N'oubliez pas que vous pouvez participer aux discussions sur notre open channel [**Slack channel**](https://osmooc.herokuapp.com/). Présentez-vous à l'adresse # module5opensource, et dites-nous un peu qui vous êtes, votre parcours, et comment vous vous êtes retrouvés ici!

### A qui s'adresse ce module?

Ce module est conçu principalement pour les chercheurs en informatique des cycles supérieurs et supérieurs, ainsi que pour les scientifiques en herbe en matière de données et tout autre chercheur utilisant un code ou un logiciel analytique. Dans un environnement de recherche moderne, cela concerne quasiment quiconque utilise un ordinateur pour son travail.

> "Un article sur le résultat informatique est une publicité, pas une bourse. La bourse actuelle est l’environnement logiciel complet, le code et les données qui ont produit le résultat. "- J. Buckheit et DL Donoho, 1995.

Les logiciels et les technologies sous-tendent une grande partie de la recherche moderne, qui est maintenant presque inévitablement computationnelle - d'une manière ou d'une autre - moteurs de recherche, plateformes de réseaux sociaux, logiciels d'analyse et publication numérique. De ce fait, il existe une demande sans cesse croissante pour des logiciels Open Source plus sophistiqués, associée à une volonté croissante des chercheurs de collaborer ouvertement sur de nouveaux outils.

La puissance de l’Open Source réside dans le fait qu’il réduit les obstacles à la collaboration et à l’adoption, permettant ainsi aux idées et aux technologies de se répandre plus rapidement. Ce module présentera les outils nécessaires à la transformation d'un logiciel en un outil accessible à tous et réutilisé par d'autres

<img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/open_research_software_open_source.png?raw=true" width="800" />

<p align="center"><i>Image de Patrick Hochstenbach (CC0 1.0 Universal)</i></p>

  


### **Objectifs d'apprentissage spécifiques à ce module**:

1. Apprenez les caractéristiques du logiciel ouvert. comprendre les **arguments d'impacts éthiques, juridiques, économiques et de recherche pour et contre le logiciel libre**et mieux comprendre les exigences de qualité du code ouvert.

2. Etre capable de transformer un code créé pour un usage personnel en un code ouvert, accessible aux autres.

3. Utilisez des logiciels (outils) utilisant un contenu ouvert et encourageant une collaboration plus large.

  


## Qu'est-ce qu'un logiciel Open Source? <a name="What_OSS"></a>

Pratiquement tous les flux de travaux de recherche scientifique modernes reposent sur une gamme d’outils logiciels, fonctionnant soit sur différents jeux de données, avec des paramètres différents, et s’appliquent de manière itérative (science des données) science informatique). Le logiciel Open Source (OSS) est un logiciel informatique dans lequel le code source complet est disponible sous une licence spécifique qui permet à d'autres utilisateurs d'accéder à ce code, de le visualiser, de le modifier et de le redistribuer à quelque fin que ce soit. Comme OSS nécessite une telle licence, elle reste généralement gratuite par défaut. Cette licence explicite est également ce qui différencie les logiciels libres du logiciel libre. Réutiliser les logiciels libres pour l'analyse, la simulation et la visualisation à des fins de recherche est généralement plus facile et plus flexible que les logiciels propriétaires. Souvent, que nous le sachions ou non, nous utilisons déjà le logiciel libre dans le cadre de nos propres processus de recherche.

Les logiciels libres s'inscrivent dans le schéma plus large de la science ouverte, car ils contribuent à rendre l'ensemble de l'environnement de recherche, y compris le logiciel qui a produit les résultats de la recherche, entièrement accessible et réutilisable. En tant que tel, il constitue un composant nécessaire pour les meilleures pratiques ([Jiménez et al., 2018](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Jim%C3%A9nez%20et%20al.%2C%202018.pdf)) et pour la répétabilité et la reproductibilité de la recherche (à la fois personnellement et par d'autres), ainsi que d'autres composants, tels que le partage de données ([Stodden, 2010](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Stodden%2C%202010.pdf))

Dans certains cas, le partage du code source peut même être conditionnel à l'acceptation des manuscrits de recherche associés ([Shamir et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Shamir%20et%20al.%2C%202013.pdf)). Il est également généralement admis que l'impact sur la recherche augmente ([Vandwalle, 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Vandewalle%2C%202012.pdf)).

Certains des avantages communs pour les développeurs incluent:

- Augmentation de la loyauté et de l'autonomisation des développeurs;

- Réduction des coûts des services et du marketing;

- Amélioration de l'image de marque des services et des produits;

- Production de logiciels de haute qualité à moindre coût;

- Flexibilité et innovation rapide;

- Personnalisation et intégration modulaire;

- Fiabilité et indépendance accrues; et

- Basé sur des standards ouverts disponibles pour tout le monde.

En tant que tels, les principaux avantages pour les chercheurs (utilisateurs) sont notamment: **des coûts moins élevés**, **une transparence accrue**, **une sécurité et une stabilité accrues**, **aucun «fournisseur» avec un contrôle accru de l'utilisateur**et **une qualité globale supérieure**. De plus, le partage de logiciels libres permet aux chercheurs de se voir attribuer un crédit, par exemple par le biais de la citation directe de logiciels [(Smith et al., 2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf).

Les logiciels OSS couramment utilisés comprennent le navigateur Internet [Mozilla Firefox](https://www.mozilla.org/en-US/firefox/) et la suite [bureautique complète LibreOffice](https://www.libreoffice.org/). LibreOffice est similaire au célèbre Microsoft Office, comprenant un traitement de texte, un gestionnaire de tableur et un logiciel de présentation de diapositives, mais il est totalement gratuit et à code source ouvert.

Certains considèrent que le mouvement des logiciels libres représente un contre-mouvement au néolibéralisme et à la privatisation, en défiant les règles et les normes en matière de construction et de réutilisation de l'information, et une transformation potentielle du capitalisme moderne en rendant les logiciels abondamment disponibles avec un effort minimal. See [The free/open source software movement: Resistance or change?](https://doi.org/10.15448/1984-7289.2009.1.5569) by Panayiota Georgopoulou for more on this topic.

  


## Principes des logiciels Open Source <a name="Principles"></a>

L’initiative [Open Source](https://opensource.org/), l’un des pionniers de l’OSS, propose la définition [suivante](https://en.wikipedia.org/wiki/The_Open_Source_Definition#Definition):

*Ne vous inquiétez pas, vous n'avez pas besoin de mémoriser tout cela, mais il est bon de connaître les principes sur lesquels repose le logiciel libre.*

- **Free Redistribution**: La licence n'empêche aucune partie de vendre ou de céder le logiciel en tant que composant d'une distribution globale de logiciels contenant des programmes de plusieurs sources différentes. La licence ne nécessite pas de redevance ni d’autres frais pour cette vente.
    
    - **Code source**: le programme doit inclure le code source et doit permettre la distribution dans le code source ainsi que sous une forme compilée. Lorsqu'une certaine forme de produit n'est pas distribuée avec le code source, il doit exister un moyen bien connu d'obtenir le code source sans dépasser un coût de reproduction raisonnable, de préférence un téléchargement gratuit via Internet. Le code source doit être la forme préférée dans laquelle un programmeur modifierait le programme. Le code source délibérément obfusqué n'est pas autorisé. Les formulaires intermédiaires tels que la sortie d'un pré-processeur ou d'un traducteur ne sont pas autorisés.
    
    - **Travaux dérivés**: La licence doit autoriser les modifications et les travaux dérivés, et leur permettre d'être distribués dans les mêmes conditions que la licence du logiciel d'origine.
    
    - **Intégrité du code source de l'auteur**: La licence peut empêcher la distribution du code source sous une forme modifiée uniquement si elle permet la distribution de "fichiers de correctif" avec le code source afin de modifier le programme au moment de la compilation. La licence doit explicitement autoriser la distribution de logiciels construits à partir de code source modifié. La licence peut exiger que les œuvres dérivées portent un nom ou un numéro de version différent de celui du logiciel original.
    
    - **Pas de discrimination à l'égard de personnes ou de groupes**: La licence ne doit pas discriminer contre une personne ou un groupe de personnes.
    
    - **Pas de discrimination contre les domaines d'activité**: La licence ne doit empêcher quiconque de faire usage du programme dans un domaine d'activité spécifique. Par exemple, cela ne doit pas empêcher le programme d'être utilisé dans une entreprise ou d'être utilisé pour la recherche génétique.
    
    - **Distribution de la licence**: Les droits attachés au programme doivent s'appliquer à tous ceux à qui le programme est redistribué sans qu'il soit nécessaire d'exécuter une licence supplémentaire par ces parties.
    
    - **licence ne doit pas être spécifique à un produit**: Les droits attachés au programme ne doivent pas dépendre de son appartenance à une distribution de logiciel particulière. Si le programme est extrait de cette distribution et utilisé ou distribué selon les termes de la licence du programme, toutes les parties auxquelles le programme est redistribué devraient bénéficier des mêmes droits que ceux concédés avec la distribution de logiciel d'origine.
    
    - **licence ne doit pas restreindre d'autres logiciels**: La licence ne doit pas imposer de restrictions aux autres logiciels distribués avec le logiciel sous licence. Par exemple, la licence ne doit pas exiger que tous les autres programmes distribués sur le même support soient des logiciels à source ouverte.
    
    - **licence doit être neutre du point de vue de la technologie**: Aucune disposition de la licence ne peut être basée sur une technologie ou un style d'interface individuel.

Maintenant, tout cela pourrait être un peu complexe à retenir. Cependant, il peut être résumé comme *rendant un logiciel aussi réutilisable que possible pour les travaux futurs, tout en étant librement disponible*

  


## Une liste de contrôle Open Source

Un certain nombre de plates-formes et d'outils existants prennent en charge le logiciel libre et la collaboration. [Open Science Training Handbook](https://open-science-training-handbook.gitbook.io/book/) fournit une liste de contrôle à utiliser pour évaluer le degré d'ouverture des logiciels de recherche existants, sur la base de la définition Open Source ci-dessus:

- [] Le logiciel est-il disponible pour être téléchargé et installé?

- [] Le logiciel peut-il être facilement installé sur différentes plates-formes?

- [] Le logiciel a-t-il des conditions d'utilisation?

- [] Le code source est-il disponible pour inspection?

- [] L’historique complet du code source est-il consultable dans un historique des versions accessible au public?

- [] Les dépendances du logiciel (matériel et logiciel) sont-elles décrites correctement? Ces dépendances ne nécessitent-elles qu'un effort raisonnablement minimal pour obtenir et utiliser?

Vérifiez, vérifiez, vérifiez, c'est fait! Simples.

  


## La communauté Open Source et sa gouvernance <a name="OS_Community"></a>

There are two main camps within the free/libre and open source software (FLOSS) community: The **free software movement**, and the **open source software movement** (OSS). Les deux ont des idéologies différentes basées sur les libertés des utilisateurs et les applications pratiques des logiciels. The term 'FLOSS' is used as a overaching neutral term to refer to both; libre being French and Spanish for 'free' in the context of freedom.

In a similar way that people active in the open science movement are heterogeneous in their assumptions and aims, different opinions exist in the FLOSS community as well. Recalling module 1, two of the schools of thought in open science were the *Pragmatic school* and the *Democratic school*. While the former is driven by the assumption that research could be more efficient if scientists worked together, the latter wants to set straight an unequal distribution of knowledge. They probably both end up sharing their research, but each with different intentions.

This is roughly comparable to the OSS and the free software movement: The latter evolved around 1983 to protect what they call the four essential freedoms of a program's user. These include the freedom to run, copy, distribute, study, change and improve a program. Software that respects these freedoms with an appropriate license is considered 'free'. The four freedoms are seen as vital for a society as a whole in the sense that they only enable sharing, cooperation and ultimately freedom in general. In this sense the free software movement is a social movement that creates an ethical imperative.

The open source software movement, which splintered off in 1998, focuses on the practical advantages and does not campaign for principles. It is concerned with developing high-quality software, for which everyone's ability to obtain, modify and contribute back the source code is considered highly beneficial.

Among multiple conclusions they arrive at, access to a program's source code is a shared one. Software thus may be considered *free*, *open source*, or both, according to agreed-on definitions by the Free Software Foundation ([FSF](https://www.gnu.org/philosophy/free-sw.html)) and the Open Source Initiative ([OSI](https://opensource.org/osd)). The FSF argues that free software is a subset of OSS, with only a [fraction](https://www.gnu.org/philosophy/free-open-overlap.html) being open source but nonfree.

Thus, highlighting a particular license status of software in use—open source or free—is mostly about different philosophies, not about software not having the other status as well. Each movement has its share of problems explaining their term: *free* means more than being gratis and *open source* means more than having access to the source code. The [FSF](https://www.gnu.org/philosophy/open-source-misses-the-point.html) and the European counterpart [FSFE](https://fsfe.org/documents/whyfs.html) provide more information on this topic.

### Pour des projets individuels

A typical open source project has the following types of formal roles:

- **Auteur**: C'est la personne qui a créé le projet
- **Propriétaire**: la personne qui a la propriété administrative sur l'organisation ou le référentiel 
- **Mainteneurs**: contributeurs qui sont responsables de la vision et des aspects organisationnels du projet (Ils peuvent également être auteurs ou propriétaires du projet.)
- **Contributeurs**: l'utilisateur qui a déjà contribué au projet.
- **Membres de la communauté**: Personnes qui utilisent le projet. Ils peuvent être actifs dans des conversations, créer de nouveaux problèmes ou exprimer leur opinion sur les améliorations futures du projet.

Typically, roles are made public through either the `README` file, a Contributors file, or a separate team page for the project.

  


## Plateformes et outils existants pour les logiciels Open Source <a name="Platforms"></a>

Virtual environments and machines are becoming increasingly popular as high-powered research workflow enablers, and many of these are built upon OSS (e.g., operating systems, programming languages, and data processing frameworks). Popular services include [Google Cloud](https://cloud.google.com/compute/) and [Amazon Web Services](https://aws.amazon.com/), which also assist with database storage and content delivery, as well as computational power. [InsideDNA](https://insidedna.me/) is a computing platform for reproducible research in bioinformatics, genomics and the life sciences.

As mentioned [above](#What_OSS), LibreOffice provides an Open Source alternative to Microsoft Office. The two are almost completely compatible, just with different default file formats. For citation managers, [Zotero](https://www.zotero.org/) is the most popular Open Source alternative to proprietary platforms such as Mendeley or EndNote.

[Zotero](https://www.zotero.org/) uses the BibTeX (pronounced 'bib-tech') format, based on LaTeX (pronounced 'lay-tech'), and has browser plugins to make citation management simple. By integrating this with other software such as LibreOffice, it is now possible to have a fully Open Source research workflow in many cases.

### GitHub <a name="GitHub"></a>

> Saviez-vous que tout ce projet a été conçu comme un effort communautaire ouvert et collaboratif dans [GitHub](https://github.com/OpenScienceMOOC/)?

[GitHub](https://github.com/) is a popular hosting site for both software and non-software content (often called 'notebooks'), with added capabilities for version control, project management and tracking, and storage services. GitHub is built on top of the OSS [Git](https://git-scm.com/), which enables users to work remotely to maintain, share, and collaborate on research software and other non-software based projects.

Version control is essentially a process that takes snapshots of the files in a repository, and tracks modifications to them. It records when the changes were made, what they were, and who did them. If several people are working on one file at once, any overlapping changes are detected, and must be resolved prior to continuing. This provides a much more streamlined and automated process than manually saving and recording changes as projects develop. It also avoids the inevitable lists of confusing named file versions...

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/xkcd.png?raw=true" width="200" /></p>

<p align="center"><i>GitHub helps us to avoid, er, sub-optimal file naming conventions (source: XKCD)</i></p>

  


One of the more popular and useful functions of GitHub is the [issue tracker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/issues), which is used to organise OSS development. The above link takes you to the issue tracker for the development of this module! If you think there is something here that can improved, or you want to comment on, anyone can add or contribute to an issue there!

Other similar project hosting services include [BitBucket](https://bitbucket.org/), [GitLab](https://about.gitlab.com/), and [Launchpad](https://launchpad.net/). If the recent acquisition of GitHub by Microsoft is a bit off-putting to you, these are great alternatives.

However, we also know that GitHub can have quite a high learning curve. Which is why the first practical task for this MOOC will teach you how to set up your first GitHub project repository!

**[GO TO TASK 1: Building your first GitHub repository](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)**

  


## Logiciel Open Source utilisé dans la recherche <a name="Research"></a>

Especially in scientific research, Open Source Software usage and development has become practically the norm. There's a number of reasons for this beyond those that apply to the general acceptance of OSS by, for example, consumers, industry, or government. Among these reasons are:

- Les algorithmes mis en œuvre dans les logiciels d'analyse font de plus en plus partie des méthodes décrites dans les publications savantes. En tant que tel, il est totalement contraire à un examen par les pairs rigoureux si ces implémentations d'algorithmes sont fermées aux étrangers.

- La collaboration scientifique s'étend le plus souvent à plusieurs institutions et réseaux de recherche distribués où le secret et la hiérarchie de commandement ne sont pas maintenus de manière «nécessaire» au développement en source fermée.

- De nombreuses analyses informatiques sont exécutées dans des environnements virtualisés (comme des infrastructures «cloud» institutionnelles, nationales ou internationales) et hébergées sur des serveurs multi-utilisateurs. Les logiciels commerciaux à source fermée interdisent souvent une telle utilisation.

- Le développement de logiciels libres repose souvent sur des volontaires. À une époque de contraintes budgétaires pour la recherche scientifique, il s'agit d'un avantage certain.

For these and other reasons, Open Source tools are very commonly used in scientific research. This includes usage in fields where many researchers are amateur developers themselves and rely on tools such as [R](https://www.r-project.org/) for statistical analysis and scripting, which, in the last decade, has almost completely displaced commercial software for statistical analysis such as SPSS or JMP in a lot of fields. In fields such as bioinformatics, that involve a lot of file handling of the outputs of DNA sequencing platforms, general purpose scripting languages such as [Python](https://www.python.org/) and commonly used libraries built on top of it (such as [biopython](http://biopython.org)) have become a vital part of the toolkit of many researchers.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/python.png?raw=true" width="400" /></p>

<p align="center"><i>Python</i></p>

  


Tools such as R and Python are essentially software for writing software. Although programming is an increasingly common activity among researchers, of course not *every* scientist does this. One step away from programming is the chaining together of the inputs and outputs of various analysis tools in longer workflows. As an example from genomics, a very common workflow is to start out with high-throughput sequencing reads and then i) do basic quality control checks; ii) map the reads against a reference genome; iii) identify the points where the new data are at variance with the reference. These steps are routinely executed as a workflow where a different Open Source executable is run in a Linux command-line environment for each of the three steps. Although this is arguably not quite open source software development, it does involve the usage and production of open source artifacts (such as Linux shell scripts) for which the principles that we discuss in this module are applicable.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/r.png?raw=true" width="200" /></p>

<p align="center"><i>R</i></p>

  


Lastly, OSS is also used in scientific research for reasons that more closely mirror those that drive the adoption of OSS in wider society, namely that it is cheap. For example, individuals or organizations might decide to switch from Microsoft Office to LibreOffice for manuscript writing or spreadsheet processing because the latter is free (both as in [**'free beer'**](https://www.youtube.com/watch?v=dQw4w9WgXcQ) and 'free speech'). Likewise, the choice to switch from ArcGIS to [QGIS](https://www.qgis.org/en/site/) for the analysis of geographic information might be prompted simply by cost considerations.   


## Premiers pas avec l'OSS - FAQ <a name="FAQ"></a>

**I'm using X[e.g. Matlab,STATA,Excel] and I want to transition to something more open. What are the next steps?**

Even if you are using proprietary software, you can usually still share your source code/documents etc. *The best first step is sharing whatever you can*.

**Great! I can put them in my new github repo.**

If that's enough for you for now great! If not for most pieces of proprietary software there are Open Source equivalents. Have a go with one and see what you think.

| Fermé                                                                                                   | Ouvrir                                                                                                                                                            |
| ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Matlab                                                                                                  | Julia en python                                                                                                                                                   |
| STATA / SPSS                                                                                            | R                                                                                                                                                                 |
| MS Office                                                                                               | LibreOffice                                                                                                                                                       |
| Mathematica                                                                                             | JupyterLab                                                                                                                                                        |
| Max/MSP                                                                                                 | PureData                                                                                                                                                          |
| Test out your new [Pull Request -PR-](https://help.github.com/articles/about-pull-requests/) Skills ... | ... by adding your own example [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md) |

**Cool! But if I make the switch will I be stuck: taking ages to learn a new tool/ without support /with buggy software.**

Good question! The answer is it depends. The best thing to do is find someone who's made the switch before and learn from their experience. Or just do a Google search! Some OSS is much better than their closed counterparts, some aren't, so it's worth choosing carefully.

## Faire un bon logiciel pour la réutilisation <a name="Reuse"></a>

The most likely person who might want to re-use your software in the future is...you! So while sharing is always better than not sharing, you can make your own life, and that of others, much easier through appropriate documentation. Documentation can include several things, such as including helpful comments and annotations in the code that help to explain why a particular action was performed, rather than what it is intended to achieve.

One of the most critical aspects of this is including an informative `README` file, that accompanies almost every OSS project, and some times even more than one. It can be a good practice to include one such file in every directory, that includes a list of files, a table of contents, and what the purpose of the directory is. The `README` file is typically just plain text or markdown (again, such as all of the ones for the MOOC!), and can include critical information for how to install and run software, previous dependencies and requirements, as well as tutorials or examples.

> **Saviez-vous que…** Le terme `README` est parfois attribué de façon ludique à la célèbre scène de Alice Carroll dans Alice au pays des merveilles, dans laquelle Alice affronte des bouffées magiques portant l'inscription «Eat Me» et «Drink Me». Puissant.

The purpose here is to provide sufficient information to maximise the re-use and reproducibility of the computational environment, such that someone with no experience with the project can easily access and re-use the software ([Sandve et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)). By lowering the barriers to entry, you increase the chances of others being able to re-use your work, which is one of the ultimate goals of OSS ([Ince et al., 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)).

An extension of this that can help to make things even easier for future re-use is 'container' technology. Containers are like an ecosystem frozen in time, where the code, the data, any other dependencies, are all perfectly preserved, packaged and saved in the present functioning versions. This means that anyone in the future any one can come in and run the analyses again. As such, they are generally good for re-use, but this can come at the sacrifice of modification or understanding by others, as often a lot of details can be hidden within the source code and its dependencies. Common examples of container implementation in research include [Rocker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf) (a Docker container for the R language), [Binder](https://mybinder.readthedocs.io/en/latest/), and [Code Ocean](https://codeocean.com/).

**Sustainable software is good software.**

  


## 10 règles simples pour une recherche informatique reproductible

The 10 simple rules for making computational research more reproducible, based on [Sandve et al., (2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF), are:

1. Pour chaque résultat, gardez une trace de la façon dont il a été produit.
2. Évitez les étapes de manipulation manuelle des données.
3. Archivez les versions exactes de tous les programmes externes utilisés.
4. Contrôle de version de tous les scripts personnalisés.
5. Enregistrez tous les résultats intermédiaires, si possible dans des formats normalisés.
6. Pour les analyses incluant le caractère aléatoire, notez les graines aléatoires sous-jacentes.
7. Toujours stocker les données brutes derrière les parcelles.
8. Générez des résultats d'analyse hiérarchique, ce qui permet d'inspecter des couches de détails croissants
9. Reliez les déclarations textuelles aux résultats sous-jacents.
10. Fournissez un accès public aux scripts, aux exécutions et aux résultats.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/simple_rules.png?raw=true" width="800" /></p>

<p align="center"><i>Infographic adapted from Sandve et al., (2013). Feel free to download this and print it out to keep handy during your research!</i></p>

  


If you follow these steps, along with the processes in [**Task 1**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [**Task 2**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), you should be fine!

  


## Licence Open Source <a name="Licensing"></a>

An Open Source license is a type of license designed specifically for software and code that make it explicit what the legal conditions for sharing and re-use are. As mentioned [above](#What_OSS), the addition of a suitable license is what differentiates publicly shared software from OSS. For example, the widely used [MATLAB](https://www.mathworks.com/products/matlab.html) is proprietary software, and [Octave](https://www.gnu.org/software/octave/) is an openly licensed alternative programming language.

There are currently more than 1,400 unique Open Source licenses, a complexity born from the difficulty in understanding the differences between the legal implications across different license.

Some of the more common licenses include:

- [Berkeley Software Distribution ("BSD")](https://en.wikipedia.org/wiki/BSD_licenses),
- [Apache](https://www.apache.org/licenses/LICENSE-2.0),
- [style MIT (Massachusetts Institute of Technology)](https://opensource.org/licenses/MIT), ou
- [Licence publique générale GNU ("GPL")](https://www.gnu.org/licenses/gpl-3.0.en.html).

You don't need to know all the legal itty gritty behind all of these, but it is good to at least know what options are avaiilable to you.

There are two ways in which contributions to a project become licensed:

1. *explicitement*, où la contribution individuelle a une licence clairement indiquée, indépendante du projet principal; ou
2. *Implicitement*: la contribution relève du code de licence d'origine du projet principal.

Thankfully, the process of selecting an Open Source license is relatively trivial, thanks to user-friendly tools such as [Choose A License](https://choosealicense.com/) or [Public License Selector](https://ufal.github.io/public-license-selector/). Each of these licenses allows other users to use, copy, distribute, and build upon your work, often while ensuring that the creators are appropriately recognised for their work. Here, the key is selecting an appropriate license for your work, depending on what you want, or do not want, others to do with it.

  


## Citation du logiciel <a name="Citation"></a>

Citations provide one of the most important interactions in scholarly research, forming the basis of our referencing and metrics systems. Typically, this is performed thanks to the assistance of a permanent unique identifier such as a [Digital Object Identifiers](https://en.wikipedia.org/wiki/Digital_object_identifier) (DOI). A DOI is a persistent identifier, implemented in the [Handle System](https://en.wikipedia.org/wiki/Handle_System), that meets a common standard, depending on the purpose, such as for identifying academic information. Such identification is critical for tracking the genealogy and provenance of research, for reproducibility, as well as for giving appropriate credit to those who have created the software. Importantly, software should be considered a legitimate output from scholarly research, and citation is becoming an increasingly common way to indicate that.

In 2016, [Smith et al., 2016](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) wrote a research paper about the principles of software citation as part of the FORCE11 Software Citation Working Group. In the same way that you would want to cite software that you have used as part of good research practices, it is important to make your research easily citable too. When citing any software used for your own research, you should include at minimum:

- Le nom de l'auteur,
- Titre du logiciel,
- Numéro de version, et
- Identifiant / localisateur unique (DOI ou URL).

The six principles of software citation by [Smith et al., (2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) are provided here:

- **Importance**: Les logiciels doivent être considérés comme un produit légitime et citable de la recherche. Les citations de logiciels doivent avoir la même importance dans la documentation scientifique que les citations d’autres produits de recherche, tels que des publications et des données; ils doivent être inclus dans les métadonnées de la citation, par exemple dans la liste de référence d'un article de revue, et ne doivent pas être omis ni séparés. Les logiciels doivent être cités sur les mêmes bases que tout autre produit de recherche, tel qu'un article ou un livre, c'est-à-dire que les auteurs doivent citer l'ensemble approprié de produits logiciels, tout comme ils citent l'ensemble approprié d'articles.

- **Crédit et attribution**: Les citations de logiciels devraient faciliter l’octroi de crédits savants et d’attribution normative et légale à tous les contributeurs au logiciel, tout en reconnaissant qu’un même style ou mécanisme d’attribution peut ne pas s’appliquer à tous les logiciels.

- **Identification unique**: une citation logicielle doit inclure une méthode d’identification pouvant être actionnée par une machine, globalement unique, interopérable et reconnue par au moins une communauté des experts de domaine correspondants, et de préférence par des chercheurs du grand public.

- **Persistance**: les identifiants uniques et les métadonnées décrivant le logiciel et leur disposition doivent rester inchangés, même au-delà de la durée de vie du logiciel qu'ils décrivent.

- **Accessibilité**: les citations de logiciel devraient faciliter l’accès au logiciel lui-même et aux métadonnées, documentation, données et autres éléments nécessaires, nécessaires à la fois aux utilisateurs et aux machines pour une utilisation informée du logiciel référencé.

- **Spécificité**: Les citations de logiciels devraient faciliter l'identification et l'accès à la version spécifique du logiciel utilisé. L'identification du logiciel doit être aussi spécifique que nécessaire, par exemple en utilisant des numéros de version, des numéros de révision ou des variantes telles que des plates-formes.

Note: For instructions on 'how to make your software citable' see the section [**Using GitHub and Zenodo**](#GitHub_Zenodo) below and [**Task 2: Linking GitHub and Zenodo**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md).

  


## Utiliser GitHub et Zenodo <a name="GitHub_Zenodo"></a>

[GitHub](#GitHub) is a popular tool for project management, content storage, and version control. Note that GitHub itself is not OSS. However, Git, the tool which it is based on, is. Git is designed to help manage the source code files, and the updates to them, for a software-related project. However, it can also be extended to other non-software projects; for example, this [MOOC](https://github.com/OpenScienceMOOC/)!

However, getting research onto GitHub is just the first step. It is equally important to make it persistent and re-usable, which is why having a Digital Object Identifier (DOI) associated with it can be useful. The simplest way to do this is through a service called [Zenodo](https://zenodo.org/), which is a free and open source multi-disciplinary repository created by OpenAIRE and CERN, and can be used to assign a DOI to individual GitHub repositories. There is a [GitHub Guide](https://guides.github.com/activities/citable-code/) that explains the details, which involve linking GitHub repositories directly through to Zenodo so that when developers create formal releases for their software, Zenodo creates and archives a that version of the software.

There's nothing special about using Zenodo for creating DOIs, other than its **free of cost**; other general repositories can also be used, such as [DataCite DOI Fabrica](https://doi.datacite.org/), or your own institutional repositories such as [Caltech's](https://www.library.caltech.edu/news/enhanced-software-preservation-now-available-caltechdata).

A lot of researchers might typically be afraid of sharing code which is incomplete, buggy, or imperfect. However, in the OSS community, such a practice of sharing 'raw' code is fairly commonplace. Sharing code openly enables others to re-use and improve it, as well as to engage in a deeper way with any research associated with it. This is one of the fundamental aspects of peer-collaboration, perhaps best exemplified by the traditional process of research manuscript peer review.

Task 2 will guide you through the process of linking a GitHub repository to Zenodo for archiving.

> **saviez-vous ...** ensemble du contenu produit pour ce MOOC est disponible dans le cadre d'une communauté située dans [Zenodo](https://zenodo.org/communities/open-science-mooc/)?

**[GO TO TASK 2: Linking GitHub and Zenodo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)**

  


## Collaborer et contribuer via Open Source <a name="Collaborating"></a>

Often, OSS is developed in a public, decentralised, collaborative manner between multiple contributors. The purpose of this is to enhance the diversity and scope of a project and its design, in order to become more beneficial and sustainable. Such an approach was famously likened to a 'bazaar' model by Eric Raymond, an early OSS proponent. One of the major guiding principles of this is that of **peer production**, which relies on self-organised communities to regulate the development of content, co-ordinated towards a shared goal or outcome.

OSS projects rely heavily on volunteer collaboration, which often entails a constant flux of newcomers in order to become productive and sustainable ([Steinmacher et al., 2014](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)). Creating the right social atmosphere for a project, and a welcoming engagement environment, are often critical to successful collaboraitons in OSS.

  


## Où aller en partant d'ici <a name="Future_OSS"></a>

Hopefully now you have come to see the importance of software as a cornerstone of modern science, and the importance that OSS plays in this.

The **learning outcomes** from this should be:

1. Vous allez maintenant être en mesure de définir les caractéristiques du logiciel libre, ainsi que certains des arguments d’impact éthique, juridique, économique et de recherche pour et contre celui-ci.

2. Sur la base des normes de la communauté, vous pourrez maintenant décrire les exigences de qualité liées au partage et à la réutilisation de code ouvert.

3. Vous pourrez désormais utiliser une gamme d’outils de recherche utilisant les logiciels libres.

4. Vous allez maintenant pouvoir transformer le code conçu pour leur usage personnel en code accessible et réutilisable par d'autres.

5. Les développeurs de logiciels seront en mesure de rendre leur logiciel citable et les utilisateurs de logiciels sauront comment citer les logiciels qu'ils utilisent.

  


**BONUS TASK**

If you have completed [Task 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [Task 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), we also have a **BONUS TASK** for you, if you want to take your skills a step further. [Task 3](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md) will take you a step deeper into integrating Git into a typical research workflow by showing you how to integrate it with R Studio. It is recommended that you have completed the first 2 tasks before proceeding with this one.

However, your Open Source journey does not stop here! This was just the beginning, and there are some incredible resources out there if you would like to do or learn more:

- Si vous vous sentez particulièrement inspiré par cela, vous pouvez approuver le [Manifeste Code de la science](http://sciencecodemanifesto.org/), qui est basé sur les cinq principes de code, le droit d' auteur, la citation, le crédit et curation.

- Pour lancer et développer votre propre projet, le programme [Open Source Guides](https://opensource.guide/) propose une gamme de guides pratiques et de compétences pour vous aider à lancer et faire avancer vos projets de logiciel libre.

- Pour un aperçu détaillé des flux de recherche basés sur des logiciels libres, le guide [Open Science, Open Data, Open Source](https://pfern.github.io/OSODOS/gitbook/) de Pedro L. Fernandes et Rutger A. Vos est l’une des principales ressources en ligne.

- Des revues plus formalisées existent également pour les articles logiciels, notamment [Le Journal de Open Research Software](https://openresearchsoftware.metajnl.com/) et [Le Journal du Logiciel Open Source](https://joss.theoj.org/). Une liste de ces sites est également [disponible](https://www.software.ac.uk/which-journals-should-i-publish-my-software).

- [PLOS Open Source Toolkit](https://channels.plos.org/open-source-toolkit) constitue un forum mondial pour la recherche et les applications matérielles et logicielles Open Source.

- [NumFOCUS](http://www.numfocus.org) est une organisation à but non lucratif qui soutient et promeut des logiciels scientifiques novateurs et open source de classe mondiale. Parmi les projets qu'ils parrainent, citons:
    
    - [Initiatives Jythy Notebook](http://ipython.org) IPython</a> et .</p></li> 
        
        - [rOpenSci](http://ropensci.org), qui promeut l'environnement statistique open source R pour une recherche transparente et reproductible.
        
        - Pour acquérir plus d'expérience pratique des logiciels libres, la communauté [Software Carpentry](https://software-carpentry.org/) organise régulièrement des ateliers pour améliorer les compétences informatiques en laboratoire ([Wilson et al., 2017](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Wilson%20et%20al.%2C%202017.pdf)).</ul></li> </ul> 
        
          
        
        
        ### Lectures complémentaires <a name="Reading"></a>
        
        *These references here are just the beginning. They include some of the most useful general overviews of the Open Source landscape in research. However, if you want to be find something more specific to your own research field, then that path is there for you to explore!*
        
        - L'avenir de la recherche dans le développement de logiciels libres / à sources ouvertes [(Scacchi, 2010)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Scacchi%2C%202010.pdf).
        
        - La méthode scientifique en pratique: la reproductibilité en sciences informatiques [(Stodden, 2010)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Stodden%2C%202010.pdf).
        
        - Le cas des programmes informatiques ouverts [(Ince et al., 2012)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf).
        
        - Questions d'actualité et tendances de la recherche sur les communautés de logiciels libres [(Martinez-Torres et Diaz-Fernandez, 2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Martinez-Torres%20and%20Diaz-Fernandez%2C%202013.pdf).
        
        - Dix règles simples pour une recherche informatique reproductible [(Sandve et al., 2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF).
        
        - Une revue systématique de la littérature sur les obstacles rencontrés par les nouveaux arrivants pour les projets de logiciels libres [(Steinmacher et al., 2014)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf).
        
        - Partage des connaissances dans les communautés de logiciels open source: motivations et gestion [(Iskoujina et Roberts, 2015)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Iskoujina%20and%20Roberts%2C%202015.pdf).
        
        - Principes de citation de logiciel [(Smith et al., 2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf).
        
        - Une introduction à Rocker: les conteneurs Docker pour R [(Boettiger et Eddelbuettel, 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf).
        
        - Bonnes pratiques en informatique scientifique [(Wilson et al., 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Wilson%20et%20al.%2C%202017.pdf).
        
        - Quatre recommandations simples pour encourager les meilleures pratiques dans les logiciels de recherche [(Jiménez et al., 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Jim%C3%A9nez%20et%20al.%2C%202018.pdf).
        
          
        
        
        ### Équipe de développement <a name="Development_team"></a>
        
        - [Alex Morley](https://twitter.com/alex__morley), Open Sourceror, Université d'Oxford, Royaume-Uni.
        - [Kevin Moerman](https://twitter.com/KMMoerman), Open Sourceror, MIT, États-Unis.
        - [Tania Allard](https://twitter.com/ixek), Open Sourceress, Data Enchantress, Université de Leeds, Royaume-Uni.
        - [Simon Worthington](https://twitter.com/mrchristian99), libérateur de livre, TIB, Allemagne.
        - [Paola Masuzzo](https://twitter.com/pcmasuzzo), Batman Open Source, Italie.
        - [Ivo Grigorov](https://twitter.com/OAforClimate), Robin Open Source, Danemark.
        - [Rutger Vos](https://twitter.com/rvosa), Open Sourceror, Centre de biodiversité Naturalis, Pays-Bas.
        - [Julien Colomb](https://twitter.com/j_colomb), Open Ninja, Berlin.
        - [Jon Tennant](https://twitter.com/protohedgehog), Dinosaure Whisperer.
        
        **Know a way this content can be improved?**
        
        Time to take your new GitHub skills for a test-run! All content development primarily happens [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md). If you have a suggested improvement to the content, layout, or anything else, you can make it and then it will automatically become part of the MOOC content after verification from a moderator!
        
        [![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)