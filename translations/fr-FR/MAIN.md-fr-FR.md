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
- [La communauté Open Source, la gouvernance et les contributions](#OS_Community)
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

Certains considèrent que le mouvement des logiciels libres représente un contre-mouvement au néolibéralisme et à la privatisation, en défiant les règles et les normes en matière de construction et de réutilisation de l'information, et une transformation potentielle du capitalisme moderne en rendant les logiciels abondamment disponibles avec un effort minimal. Voir [Le mouvement du logiciel libre / open source: résistance ou changement?](http://www.redalyc.org/html/742/74212712006/) de Panayiota Georgopoulou pour plus d'informations à ce sujet.

  


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

La communauté du logiciel libre comprend deux camps principaux: le mouvement **du logiciel libre**et le mouvement **OSS**. Les deux ont des idéologies différentes basées sur les libertés des utilisateurs et les applications pratiques des logiciels. Souvent, le terme «FLOSS» est utilisé pour réconcilier ces deux camps politiques et signifie «logiciels libres / libres et logiciels libres»; Libre étant français et espagnol pour «libre» dans le contexte de la liberté.

Le principe de base de la réutilisation est ce qui sépare le logiciel libre du "logiciel libre". Le logiciel libre et Open Source (FOSS) est un terme inclusif qui décrit un logiciel pouvant être classé à la fois comme source libre et à source ouverte. Un bon exemple de FOSS est le système d’exploitation [Ubuntu Linux](https://www.ubuntu.com/).

La grande différence entre les logiciels libres et les logiciels libres réside dans le fait que les premiers doivent distribuer les versions mises à jour sous la même licence que la version originale, alors que les versions les plus récentes peuvent être distribuées sous différentes licences. FOSS combine le meilleur des deux mondes.

Ces définitions sont maintenant largement adoptées par les gouvernements internationaux ainsi que par certaines grandes organisations telles que [Mozilla Foundation](https://www.mozilla.org/en-US/foundation/) et [Wikimedia Foundation](https://wikimediafoundation.org/wiki/Home). Parmi les principales organisations du secteur des logiciels libres, on citera [Software Sustainability Institute](https://www.software.ac.uk/)du Royaume-Uni, qui produit des ressources précieuses telles que leur récent Guide sur le dépôt de [logiciels pour les chercheurs](https://softwaresaved.github.io/software-deposit-guidance/).

### Pour des projets individuels

Un projet Open Source typique comporte les types de rôles formels suivants:

- **Auteur**: C'est la personne qui a créé le projet
- **Propriétaire**: la personne qui a la propriété administrative sur l'organisation ou le référentiel 
- **Mainteneurs**: contributeurs qui sont responsables de la vision et des aspects organisationnels du projet (Ils peuvent également être auteurs ou propriétaires du projet.)
- **Contributeurs**: l'utilisateur qui a déjà contribué au projet.
- **Membres de la communauté**: Personnes qui utilisent le projet. Ils peuvent être actifs dans des conversations, créer de nouveaux problèmes ou exprimer leur opinion sur les améliorations futures du projet.

En règle générale, les rôles sont rendus publics via le fichier `README` , un fichier Contributors ou une page d'équipe distincte pour le projet.

  


## Plateformes et outils existants pour les logiciels Open Source <a name="Platforms"></a>

Les environnements virtuels et les machines sont de plus en plus populaires en tant que facilitateurs de flux de travail de recherche de grande puissance, et beaucoup d'entre eux sont basés sur des logiciels libres (systèmes d'exploitation, langages de programmation et cadres de traitement de données, par exemple). Les services populaires incluent [Google Cloud](https://cloud.google.com/compute/) et [Amazon Web Services](https://aws.amazon.com/), qui aident également au stockage de bases de données et à la fourniture de contenu, ainsi qu’à la puissance de calcul. [InsideDNA](https://insidedna.me/) est une plateforme informatique pour la recherche reproductible en bioinformatique, génomique et sciences de la vie.

Comme mentionné [ci - dessus](#What_OSS), LibreOffice fournit une alternative Open Source à Microsoft Office. Les deux sont presque complètement compatibles, mais avec des formats de fichier par défaut différents. [Zotero](https://www.zotero.org/) est l'alternative Open Source la plus populaire pour les plates-formes propriétaires telles que Mendeley ou EndNote.

[Zotero](https://www.zotero.org/) utilise le format BibTeX (prononcé 'bib-tech'), basé sur LaTeX (prononcé 'lay-tech'), et comporte des plugins de navigateur pour simplifier la gestion des citations. En intégrant cela à d'autres logiciels tels que LibreOffice, il est désormais possible d'avoir un flux de travail de recherche entièrement Open Source dans de nombreux cas.

### GitHub <a name="GitHub"></a>

> Saviez-vous que tout ce projet a été conçu comme un effort communautaire ouvert et collaboratif dans [GitHub](https://github.com/OpenScienceMOOC/)?

[GitHub](https://github.com/) est un site d'hébergement populaire pour le contenu logiciel et non logiciel (souvent appelé «bloc-notes»), avec des fonctionnalités supplémentaires pour le contrôle de version, la gestion et le suivi de projets ainsi que les services de stockage. GitHub est construit sur l'OSS [Git](https://git-scm.com/), qui permet aux utilisateurs de travailler à distance pour gérer, partager et collaborer sur des logiciels de recherche et d'autres projets non logiciels.

Le contrôle de version est essentiellement un processus qui prend des instantanés des fichiers d'un référentiel et enregistre les modifications qui y sont apportées. Il enregistre à quel moment les modifications ont été apportées, ce qu’elles étaient et qui les a effectuées. Si plusieurs personnes travaillent simultanément sur un même fichier, toutes les modifications qui se chevauchent sont détectées et doivent être résolues avant de continuer. Cela fournit un processus beaucoup plus simple et automatisé que la sauvegarde et l'enregistrement manuels des modifications au fur et à mesure de l'avancement des projets. Cela évite également les listes inévitables de versions de fichiers nommés qui prêtent à confusion ...

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/xkcd.png?raw=true" width="200" /></p>

<p align="center"><i>GitHub nous aide à éviter les conventions de nommage des fichiers sous-optimales (source: XKCD)</i></p>

  


L' une des fonctions les plus populaires et les plus utiles de GitHub est le [problème Tracker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/issues), qui est utilisé pour organiser le développement de l' OSS. Le lien ci-dessus vous mène au gestionnaire de problèmes pour le développement de ce module! Si vous pensez que quelque chose ici peut être amélioré, ou si vous souhaitez commenter, tout le monde peut ajouter ou contribuer à un problème!

D'autres services d'hébergement de projet similaires incluent [BitBucket](https://bitbucket.org/), [GitLab](https://about.gitlab.com/)et [Launchpad](https://launchpad.net/). Si l’acquisition récente de GitHub par Microsoft vous dégoûte un peu, c’est une excellente alternative.

Cependant, nous savons également que GitHub peut avoir une courbe d'apprentissage assez longue. C'est pourquoi la première tâche pratique de ce MOOC vous apprendra comment configurer votre premier référentiel de projets GitHub!

**[ALLEZ À LA TÂCHE 1: Construire votre premier référentiel GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)**

  


## Logiciel Open Source utilisé dans la recherche <a name="Research"></a>

En particulier dans la recherche scientifique, l'utilisation et le développement de logiciels Open Source sont devenus pratiquement la norme. Cela s'explique par un certain nombre de raisons autres que celles qui concernent l'acceptation générale du logiciel libre, par exemple les consommateurs, l'industrie ou le gouvernement. Parmi ces raisons sont:

- Les algorithmes mis en œuvre dans les logiciels d'analyse font de plus en plus partie des méthodes décrites dans les publications savantes. En tant que tel, il est totalement contraire à un examen par les pairs rigoureux si ces implémentations d'algorithmes sont fermées aux étrangers.

- La collaboration scientifique s'étend le plus souvent à plusieurs institutions et réseaux de recherche distribués où le secret et la hiérarchie de commandement ne sont pas maintenus de manière «nécessaire» au développement en source fermée.

- De nombreuses analyses informatiques sont exécutées dans des environnements virtualisés (comme des infrastructures «cloud» institutionnelles, nationales ou internationales) et hébergées sur des serveurs multi-utilisateurs. Les logiciels commerciaux à source fermée interdisent souvent une telle utilisation.

- Le développement de logiciels libres repose souvent sur des volontaires. À une époque de contraintes budgétaires pour la recherche scientifique, il s'agit d'un avantage certain.

Pour ces raisons et d'autres, les outils Open Source sont très couramment utilisés dans la recherche scientifique. Cela inclut l'utilisation dans des domaines où de nombreux chercheurs sont des développeurs amateurs et s'appuient sur des outils tels que [R](https://www.r-project.org/) pour l'analyse statistique et l'écriture de scripts, qui, au cours de la dernière décennie, ont presque complètement remplacé les logiciels commerciaux d'analyse statistique tels que SPSS ou JMP. beaucoup de champs. Dans des domaines tels que la bioinformatique, qui impliquent un grand nombre de traitements de fichiers des sorties de plates-formes de séquençage d’ADN, les langages de script à usage général tels que [Python](https://www.python.org/) et les bibliothèques couramment utilisées construits dessus (tels que [biopython](http://biopython.org)) sont devenus indispensables. fait partie de la boîte à outils de nombreux chercheurs.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/python.png?raw=true" width="400" /></p>

<p align="center"><i>Python</i></p>

  


Des outils tels que R et Python sont essentiellement des logiciels d’écriture de logiciels. Bien que la programmation est une activité de plus en plus fréquente chez les chercheurs, bien sûr *tous les* scientifique fait cela. Une étape de la programmation est le chaînage des entrées et des sorties de divers outils d'analyse dans des flux de travail plus longs. À titre d’exemple tiré de la génomique, un flux de travail très courant consiste à commencer par des lectures de séquençage à haut débit, puis i) à effectuer des contrôles de contrôle qualité de base; ii) mapper les lectures sur un génome de référence; iii) identifier les points où les nouvelles données sont en contradiction avec la référence. Ces étapes sont systématiquement exécutées en tant que flux de travail dans lequel un exécutable Open Source différent est exécuté dans un environnement de ligne de commande Linux pour chacune des trois étapes. Bien que ce ne soit pas un développement de logiciel open source, cela implique l'utilisation et la production d'artefacts open source (tels que des scripts shell Linux) auxquels les principes décrits dans ce module sont applicables.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/r.png?raw=true" width="200" /></p>

<p align="center"><i>R</i></p>

  


Enfin, les logiciels libres sont également utilisés dans la recherche scientifique pour des raisons plus proches de celles qui ont motivé l'adoption du logiciel libre dans la société, à savoir qu'il est bon marché. Par exemple, les individus ou les organisations pourraient décider de passer de Microsoft Office à LibreOffice pour l' écriture manuscrite ou le traitement de la feuille de calcul , car ce dernier est libre ( à la fois comme [**« bière gratuite »**](https://www.youtube.com/watch?v=dQw4w9WgXcQ) et « la liberté d' expression »). De même, le choix de passer d'ArcGIS à [QGIS](https://www.qgis.org/en/site/) pour l'analyse d'informations géographiques peut être motivé simplement par des considérations de coût.   


## Premiers pas avec l'OSS - FAQ <a name="FAQ"></a>

**J'utilise X [par exemple Matlab, STATA, Excel] et je souhaite passer à quelque chose de plus ouvert. Quelles sont les prochaines étapes?**

Même si vous utilisez un logiciel propriétaire, vous pouvez toujours partager votre code source / vos documents, etc. *La meilleure première étape consiste à partager ce que vous pouvez*.

**Génial! Je peux les mettre dans mon nouveau dépôt Github.**

Si cela vous suffit pour le moment génial! Si ce n'est pas le cas pour la plupart des logiciels propriétaires, il existe des équivalents Open Source. Essayez-le et voyez ce que vous en pensez.

| Fermé                                                                                                            | Ouvrir                                                                                                                                                                 |
| ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Matlab                                                                                                           | Julia en python                                                                                                                                                        |
| STATA / SPSS                                                                                                     | R                                                                                                                                                                      |
| MS Office                                                                                                        | LibreOffice                                                                                                                                                            |
| Mathematica                                                                                                      | JupyterLab                                                                                                                                                             |
| Testez votre nouvelle demande [Pull -PR-](https://help.github.com/articles/about-pull-requests/) compétences ... | ... en ajoutant votre propre exemple [ici](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md) |

**Cool! Mais si je fais le changement, je serai coincé: cela prendra du temps pour apprendre un nouvel outil / sans support / avec un logiciel buggy.**

Bonne question! La réponse est que cela dépend. La meilleure chose à faire est de trouver quelqu'un qui a déjà changé et d'apprendre de son expérience. Ou faites simplement une recherche sur Google! Certains logiciels libres sont bien meilleurs que leurs homologues fermés, d’autres ne le sont pas;

## Faire un bon logiciel pour la réutilisation <a name="Reuse"></a>

La personne la plus susceptible de vouloir réutiliser votre logiciel à l'avenir est ... vous! Ainsi, bien que partager soit toujours mieux que ne pas partager, vous pouvez rendre votre vie, et celle des autres, beaucoup plus facile grâce à une documentation appropriée. La documentation peut inclure plusieurs éléments, notamment inclure des commentaires et des annotations utiles dans le code, qui permettent d'expliquer pourquoi une action particulière a été effectuée, plutôt que l'objectif recherché.

L'un des aspects les plus critiques de cette opération est notamment l'inclusion d'un fichier `README` informatif, qui accompagne presque tous les projets de logiciel libre, et parfois même plusieurs. Il peut être judicieux d’inclure un tel fichier dans chaque répertoire, qui comprend une liste de fichiers, une table des matières et l’objet du répertoire. Le fichier `README` est généralement du texte brut ou une réduction (à nouveau, comme tous ceux du MOOC!), Et peut contenir des informations critiques sur la procédure d’installation et d’exécution des logiciels, les dépendances et exigences exemples.

> **Saviez-vous que…** Le terme `README` est parfois attribué de façon ludique à la célèbre scène de Alice Carroll dans Alice au pays des merveilles, dans laquelle Alice affronte des bouffées magiques portant l'inscription «Eat Me» et «Drink Me». Puissant.

L'objectif ici est de fournir suffisamment d'informations pour optimiser la réutilisation et la reproductibilité de l'environnement informatique, de sorte qu'une personne n'ayant aucune expérience du projet puisse facilement accéder au logiciel et le réutiliser ([Sandve et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)). En réduisant les barrières à l'entrée, vous augmentez les chances que d'autres personnes puissent réutiliser votre travail, ce qui est l'un des objectifs ultimes du logiciel libre ([Ince et al., 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)).

La technologie des «conteneurs» est une extension de ce qui peut aider à rendre les choses encore plus faciles pour une réutilisation future. Les conteneurs sont comme un écosystème figé dans le temps, où le code, les données et toutes les autres dépendances sont parfaitement conservés, empaquetés et enregistrés dans les versions fonctionnelles actuelles. Cela signifie que n'importe qui dans le futur peut entrer et relancer les analyses. En tant que tels, ils sont généralement bons à réutiliser, mais cela peut venir du sacrifice de la modification ou de la compréhension par d’autres, étant donné que beaucoup de détails peuvent souvent être cachés dans le code source et ses dépendances. Les exemples courants de mise en œuvre de conteneur dans la recherche incluent [Rocker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf) (un conteneur Docker pour le langage R), [Binder](https://mybinder.readthedocs.io/en/latest/)et [Code Ocean](https://codeocean.com/).

**Un logiciel durable est un bon logiciel.**

  


## 10 règles simples pour une recherche informatique reproductible

Les 10 règles simples pour rendre la recherche informatique plus reproductible, basées sur [Sandve et al. (2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF), sont

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

<p align="center"><i>Infographie adapté de Sandve et al. (2013). N'hésitez pas à télécharger ceci et à l'imprimer pour le garder à portée de main lors de vos recherches!</i></p>

  


Si vous suivez ces étapes, ainsi que les processus de [**Tâche 1**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) et [**Tâche 2**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), ça devrait aller!

  


## Licence Open Source <a name="Licensing"></a>

Une licence Open Source est un type de licence spécialement conçu pour les logiciels et les codes, qui explicite les conditions légales de partage et de réutilisation. Comme mentionné [ci - dessus](#What_OSS), l'ajout d'une licence appropriée est ce qui différencie le logiciel publiquement partagé de l' OSS. Par exemple, [MATLAB](https://www.mathworks.com/products/matlab.html) , largement utilisé, est un logiciel propriétaire et [Octave](https://www.gnu.org/software/octave/) est un langage de programmation alternatif sous licence ouverte.

Il existe actuellement plus de 1 400 licences Open Source uniques, une complexité née de la difficulté à comprendre les différences entre les implications juridiques d'une licence à l'autre.

Certaines des licences les plus courantes incluent:

- [Berkeley Software Distribution ("BSD")](https://en.wikipedia.org/wiki/BSD_licenses),
- [Apache](https://www.apache.org/licenses/LICENSE-2.0),
- [style MIT (Massachusetts Institute of Technology)](https://opensource.org/licenses/MIT), ou
- [Licence publique générale GNU ("GPL")](https://www.gnu.org/licenses/gpl-3.0.en.html).

Vous n'avez pas besoin de connaître tous les détails juridiques derrière tout cela, mais il est bon de savoir au moins quelles options vous sont offertes.

Les contributions à un projet sont autorisées sous deux formes:

1. *explicitement*, où la contribution individuelle a une licence clairement indiquée, indépendante du projet principal; ou
2. *Implicitement*: la contribution relève du code de licence d'origine du projet principal.

Heureusement, le processus de sélection d'une licence Open Source est relativement simple, grâce à des outils conviviaux tels que [Choose A License](https://choosealicense.com/). Chacune de ces licences permet à d'autres utilisateurs d'utiliser, de copier, de distribuer et de développer votre travail, souvent en veillant à ce que les créateurs soient reconnus de manière appropriée pour leur travail. Ici, la clé est de choisir une licence appropriée pour votre travail, en fonction de ce que vous voulez ou ne voulez pas que les autres en fassent.

  


## Citation du logiciel <a name="Citation"></a>

Les citations fournissent l’une des interactions les plus importantes dans la recherche scientifique, constituant la base de nos systèmes de référencement et de métriques. En règle générale, cette opération est effectuée à l'aide d'un identifiant unique permanent, tel qu'un [Digital Object Identifiers](https://en.wikipedia.org/wiki/Digital_object_identifier) (DOI). Un DOI est un identifiant persistant, implémenté dans le [Handle System](https://en.wikipedia.org/wiki/Handle_System), qui répond à une norme commune, en fonction de l’objet, par exemple pour identifier des informations académiques. Une telle identification est essentielle pour suivre la généalogie et la provenance de la recherche, pour sa reproductibilité, ainsi que pour attribuer le crédit approprié à ceux qui ont créé le logiciel. Il est important de noter que les logiciels doivent être considérés comme une sortie légitime de la recherche scientifique, et la citation devient un moyen de plus en plus courant d’indiquer cela.

En 2016, [Smith et al., 2016](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) rédigé un document de recherche sur les principes de la citation de logiciels dans le cadre du groupe de travail FORCE11 Software Citation. De la même manière que vous voudriez citer un logiciel que vous avez utilisé dans le cadre de bonnes pratiques de recherche, il est important que votre recherche soit facilement citable. Lorsque vous citez un logiciel utilisé pour vos propres recherches, vous devez inclure au minimum:

- Le nom de l'auteur,
- Titre du logiciel,
- Numéro de version, et
- Identifiant / localisateur unique (DOI ou URL).

Les six principes de citation de logiciel de [Smith et al., (2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) sont fournis ici:

- **Importance**: Les logiciels doivent être considérés comme un produit légitime et citable de la recherche. Les citations de logiciels doivent avoir la même importance dans la documentation scientifique que les citations d’autres produits de recherche, tels que des publications et des données; ils doivent être inclus dans les métadonnées de la citation, par exemple dans la liste de référence d'un article de revue, et ne doivent pas être omis ni séparés. Les logiciels doivent être cités sur les mêmes bases que tout autre produit de recherche, tel qu'un article ou un livre, c'est-à-dire que les auteurs doivent citer l'ensemble approprié de produits logiciels, tout comme ils citent l'ensemble approprié d'articles.

- **Crédit et attribution**: Les citations de logiciels devraient faciliter l’octroi de crédits savants et d’attribution normative et légale à tous les contributeurs au logiciel, tout en reconnaissant qu’un même style ou mécanisme d’attribution peut ne pas s’appliquer à tous les logiciels.

- **Identification unique**: une citation logicielle doit inclure une méthode d’identification pouvant être actionnée par une machine, globalement unique, interopérable et reconnue par au moins une communauté des experts de domaine correspondants, et de préférence par des chercheurs du grand public.

- **Persistance**: les identifiants uniques et les métadonnées décrivant le logiciel et leur disposition doivent rester inchangés, même au-delà de la durée de vie du logiciel qu'ils décrivent.

- **Accessibilité**: les citations de logiciel devraient faciliter l’accès au logiciel lui-même et aux métadonnées, documentation, données et autres éléments nécessaires, nécessaires à la fois aux utilisateurs et aux machines pour une utilisation informée du logiciel référencé.

- **Spécificité**: Les citations de logiciels devraient faciliter l'identification et l'accès à la version spécifique du logiciel utilisé. L'identification du logiciel doit être aussi spécifique que nécessaire, par exemple en utilisant des numéros de version, des numéros de révision ou des variantes telles que des plates-formes.

Remarque: pour savoir comment "rendre votre logiciel citable", reportez-vous à la section [**Utilisation de GitHub et Zenodo**](#GitHub_Zenodo) ci-dessous et [**Tâche 2: Lier GitHub à Zenodo**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md).

  


## Utiliser GitHub et Zenodo <a name="GitHub_Zenodo"></a>

[GitHub](#GitHub) est un outil populaire de gestion de projet, de stockage de contenu et de contrôle de version. Notez que GitHub lui-même n'est pas un logiciel libre. Cependant, l'outil sur lequel il est basé est Git. Git est conçu pour vous aider à gérer les fichiers de code source et leurs mises à jour, pour un projet lié au logiciel. Cependant, il peut également être étendu à d'autres projets non logiciels; par exemple, ce [MOOC](https://github.com/OpenScienceMOOC/)!

Cependant, lancer des recherches sur GitHub n'est que la première étape. Il est également important de le rendre persistant et réutilisable. C'est pourquoi il peut être utile de lui associer un identificateur d'objet numérique (DOI). La manière la plus simple de le faire consiste à utiliser un service appelé [Zenodo](https://zenodo.org/), un référentiel multidisciplinaire gratuit et à source ouverte créé par OpenAIRE et le CERN, et pouvant être utilisé pour affecter un DOI à des référentiels GitHub individuels. Il existe un [Guide GitHub](https://guides.github.com/activities/citable-code/) qui explique les détails, ce qui implique de relier les référentiels GitHub directement à Zenodo. Ainsi, lorsque les développeurs créent des versions officielles de leur logiciel, Zenodo crée et archive cette version du logiciel.

L'utilisation de Zenodo pour créer des DOI n'a rien de spécial, mis à part son **gratuit**; Vous pouvez également utiliser d'autres référentiels généraux, tels que [DataCite DOI Fabrica](https://doi.datacite.org/)ou vos propres référentiels institutionnels, tels que [Caltech's](https://www.library.caltech.edu/news/enhanced-software-preservation-now-available-caltechdata).

De nombreux chercheurs craignent généralement de partager un code incomplet, buggy ou imparfait. Cependant, dans la communauté des logiciels libres, une telle pratique de partage de code «brut» est assez courante. Le partage ouvert de code permet aux autres utilisateurs de le réutiliser et de l'améliorer, ainsi que de s'engager plus profondément dans les recherches qui lui sont associées. C’est l’un des aspects fondamentaux de la collaboration entre pairs, qui est peut-être mieux illustré par le processus traditionnel d’examen par des pairs des manuscrits de recherche.

La tâche 2 vous guidera tout au long du processus de liaison d’un référentiel GitHub à Zenodo pour archivage.

> **saviez-vous ...** ensemble du contenu produit pour ce MOOC est disponible dans le cadre d'une communauté située dans [Zenodo](https://zenodo.org/communities/open-science-mooc/)?

**[ALLEZ À LA TÂCHE 2: Lier GitHub et Zenodo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)**

  


## Collaborer et contribuer via Open Source <a name="Collaborating"></a>

Les logiciels libres sont souvent développés de manière publique, décentralisée et collaborative entre plusieurs contributeurs. Le but est d’accroître la diversité et la portée d’un projet et de sa conception afin de devenir plus bénéfique et durable. Une telle approche a été comparée à un modèle de «bazar» d’Eric Raymond, un des premiers partisans de l’OSS. L'un des principes directeurs majeurs de cette approche est celui de la production **par les pairs**, qui repose sur des communautés auto-organisées pour réguler le développement de contenu, coordonné vers un objectif ou résultat commun.

Les projets OSS reposent largement sur la collaboration de volontaires, ce qui implique souvent un flux constant de nouveaux arrivants afin de devenir productif et durable ([Steinmacher et al., 2014](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)). Créer la bonne atmosphère sociale pour un projet et créer un environnement de participation accueillant sont souvent essentiels au succès des collaborations dans les logiciels libres.

  


## Où aller en partant d'ici <a name="Future_OSS"></a>

J'espère que maintenant vous en êtes venus à comprendre l'importance du logiciel en tant que pierre angulaire de la science moderne et l'importance que joue le logiciel libre dans ce domaine.

Les **résultats d'apprentissage** de ceci devraient être:

1. Vous allez maintenant être en mesure de définir les caractéristiques du logiciel libre, ainsi que certains des arguments d’impact éthique, juridique, économique et de recherche pour et contre celui-ci.

2. Sur la base des normes de la communauté, vous pourrez maintenant décrire les exigences de qualité liées au partage et à la réutilisation de code ouvert.

3. Vous pourrez désormais utiliser une gamme d’outils de recherche utilisant les logiciels libres.

4. Vous allez maintenant pouvoir transformer le code conçu pour leur usage personnel en code accessible et réutilisable par d'autres.

5. Les développeurs de logiciels seront en mesure de rendre leur logiciel citable et les utilisateurs de logiciels sauront comment citer les logiciels qu'ils utilisent.

  


**TÂCHE DE BONUS**

Si vous avez terminé [Tâche 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) et [Tâche 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), nous avons également une Tâche **BONUS** pour vous, si vous souhaitez approfondir vos compétences. [tâche 3](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md) permettra de mieux intégrer Git dans un flux de travail de recherche typique en vous montrant comment l'intégrer à R Studio. Il est recommandé d’avoir terminé les 2 premières tâches avant de procéder à celle-ci.

Cependant, votre parcours Open Source ne s'arrête pas là! Ce n'était que le début, et il existe des ressources incroyables si vous souhaitez faire ou en apprendre davantage:

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
        
        *Ces références ne sont que le début. Ils incluent certains des aperçus généraux les plus utiles du paysage Open Source en recherche. Cependant, si vous voulez trouver quelque chose de plus spécifique à votre propre domaine de recherche, alors ce chemin est là pour vous!*
        
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
        
        **Connaissez-vous un moyen d'améliorer ce contenu?**
        
        Il est temps de tester vos nouvelles compétences GitHub! Tout développement de contenu passe principalement par [ici](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md). Si vous avez une suggestion d'amélioration à apporter au contenu, à la présentation ou à quelque chose d'autre, vous pouvez le créer et il sera automatiquement intégré au contenu du MOOC après vérification par un modérateur!
        
        [![Dédicace du domaine public CC0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)