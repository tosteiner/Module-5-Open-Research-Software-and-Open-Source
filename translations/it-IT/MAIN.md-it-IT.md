---
output:
  html_document: predefinito
  pdf_document: predefinito
---

# Modulo 5: Open Research Software e Open Source

## Sommario

- [introduzione](#Introduction)
- [Cos'è il software Open Source](#What_OSS)
- [Principi del software Open Source](#Principles)
- [The Open Source community and its governance](#OS_Community)
- [Piattaforme e strumenti esistenti per software Open Source](#Platforms)
- [Software Open Source utilizzato nella ricerca](#Research)
- [Guida introduttiva all'OSS - Domande frequenti](#FAQ)
- [Fare un buon software per il riutilizzo](#Reuse)
- [Licenze open source](#Licensing)
- [Citazione del software](#Citation)
- [Utilizzando GitHub e Zenodo](#GitHub_Zenodo)
- [Collaborazione tramite Open Source](#Collaborating)
- [Dove andare da qui](#Future_OSS)

**SI PREGA DI NOTARE** che una versione audio di questo è disponibile per il download tramite [Soundcloud](https://soundcloud.com/open-science-mooc/module-5-open-source-and-open-research-software) e [YouTube](https://www.youtube.com/watch?v=BHrOEmKk5zM).

## introduzione <a name="Introduction"></a>

Benvenuti su **Modulo 5** del MOOC Open Science: **Open Research Software e Open Source**.

Questo modulo è stato sviluppato [in open](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source) attraverso la collaborazione di un team internazionale di [esperti di Open Source](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/README.md#development-team-). Tutto ciò che vedi qui è stato sviluppato all'aria aperta attraverso il feedback interattivo e la collaborazione della più ampia comunità. Comprende una serie di video, infografiche, letture testuali e attività pratiche per farti affondare i denti.

Non dimenticare che puoi partecipare alle discussioni sul nostro open [**Slack channel**](https://osmooc.herokuapp.com/). Per favore, presentati a # module5opensource e raccontaci un po 'di chi sei, del tuo background e di come sei finito qui!

### Per chi è questo modulo?

Questo modulo è progettato principalmente per i ricercatori computazionali a livello di laurea e di laurea, così come i ricercatori di dati in erba e qualsiasi altro ricercatore che utilizza codice analitico o software. In un moderno ambiente di ricerca, questo copre praticamente chiunque usi un computer per il lavoro.

> "Un articolo sul risultato computazionale è la pubblicità, non la borsa di studio. La vera borsa di studio è l'intero ambiente software, codice e dati, che ha prodotto il risultato. "- J. Buckheit e DL Donoho, 1995.

Il software e la tecnologia sono alla base di molte ricerche moderne, che ora sono quasi inevitabilmente computazionali in un modo o nell'altro: motori di ricerca, piattaforme di social networking, software analitico e editoria digitale. Con questo, c'è una domanda sempre crescente di software Open Source più sofisticato, accompagnato da una crescente disponibilità per i ricercatori a collaborare apertamente a nuovi strumenti.

Il potere dell'open source sta nel fatto che riduce gli ostacoli alla collaborazione e all'adozione, consentendo quindi a idee e tecnologie di diffondersi più rapidamente. Questo modulo introdurrà gli strumenti necessari necessari per trasformare il software in qualcosa che possa essere accessibile e riutilizzato apertamente da altri.

<img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/open_research_software_open_source.png?raw=true" width="800" />

<p align="center"><i>Immagine di Patrick Hochstenbach (CC0 1.0 Universal)</i></p>

  


### **Obiettivi di apprendimento specifici per questo modulo**:

1. Impara le caratteristiche del software aperto; comprendere le **argomenti impatto etico, giuridico, economico, e di ricerca a favore e contro Software Open Source**, e capire meglio i requisiti di qualità di codice aperto.

2. Essere in grado di trasformare il codice creato per uso personale in un codice aperto che è accessibile da altri.

3. Utilizza software (strumenti) che utilizza i contenuti aperti e incoraggia una più ampia collaborazione.

  


## Cos'è il software Open Source <a name="What_OSS"></a>

Praticamente tutti i moderni flussi di lavoro di ricerca scientifica si basano su una serie di strumenti software, operanti su set di dati diversi, con parametri diversi, applicati iterativamente in vari modi (scienza dei dati) o operanti su diversi input e utilizzando modelli e metodi per predire alcuni stati di output ( scienza computazionale). Open Source Software (OSS) è un software per computer in cui il codice sorgente completo è disponibile con una licenza specifica che consente ad altri utenti di accedere, visualizzare, modificare e ridistribuire quel codice per qualsiasi scopo. Poiché l'OSS richiede tale licenza, in genere rimane gratuita per impostazione predefinita. Questa licenza esplicita è anche ciò che distingue l'OSS dal software libero. Anche il riutilizzo dell'OSS per l'analisi, la simulazione e la visualizzazione per la ricerca è in genere più semplice e flessibile rispetto al software proprietario. Spesso, che lo sappiamo o no, stiamo già utilizzando l'OSS come parte dei nostri flussi di lavoro di ricerca.

L'OSS si inserisce nel più ampio schema di Open Science in quanto contribuisce a rendere l'intero ambiente di ricerca, compreso il software che ha prodotto i risultati della ricerca, completamente accessibile e riutilizzabile. Come tale, costituisce una componente necessaria per le migliori pratiche ([Jiménez et al., 2018](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Jim%C3%A9nez%20et%20al.%2C%202018.pdf)) e la ripetibilità e riproducibilità della ricerca (sia personalmente che da altri), insieme ad altre componenti, come la condivisione di dati ([Stodden, 2010)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Stodden%2C%202010.pdf)).

In alcuni casi, la condivisione del codice sorgente può anche essere subordinata all'accettazione dei manoscritti di ricerca associati ([Shamir et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Shamir%20et%20al.%2C%202013.pdf)). Generalmente viene percepito anche come un aumento dell'impatto della ricerca ([Vandwalle, 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Vandewalle%2C%202012.pdf)).

Alcuni dei vantaggi comuni per gli sviluppatori includono:

- Maggiore fidelizzazione e empowerment dello sviluppatore;

- Minori costi di servizi e marketing;

- Aumento del marchio di servizi e prodotti;

- Produzione di software di alta qualità a costi inferiori;

- Flessibilità e innovazione rapida;

- Personalizzazione e integrazione modulare;

- Maggiore affidabilità e indipendenza; e

- Basato su standard aperti disponibili per tutti.

Di conseguenza, i principali vantaggi per i ricercatori (utenti) includono **costi inferiori**, **maggiore trasparenza**, **maggiore sicurezza e stabilità**, **nessun 'blocco' del fornitore con un maggiore controllo dell'utente**e **qualità generale in generale**. Inoltre, la condivisione dell'OSS consente ai ricercatori di ricevere credito per i loro sforzi, ad esempio attraverso la citazione diretta del software [(Smith et al., 2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf).

Comunemente utilizzato OSS include il [Mozilla Firefox](https://www.mozilla.org/en-US/firefox/) browser internet e il [LibreOffice](https://www.libreoffice.org/) suite per l'ufficio completa. LibreOffice è simile al popolare Microsoft Office, incluso un word processor, un gestore di fogli di calcolo e un software di presentazione di diapositive, ma è completamente gratuito e Open Source.

Alcuni ritengono che il movimento OSS rappresenti un movimento controcorrente verso il neoliberismo e la privatizzazione, attraverso la sfida delle norme e dei regolamenti nella costruzione e il riutilizzo delle informazioni e una potenziale trasformazione del capitalismo moderno attraverso la messa a disposizione di software con il minimo sforzo. See [The free/open source software movement: Resistance or change?](https://doi.org/10.15448/1984-7289.2009.1.5569) by Panayiota Georgopoulou for more on this topic.

  


## Principi del software Open Source <a name="Principles"></a>

Il [Open Source Initiative](https://opensource.org/), uno dei pionieri della OSS, offre la seguente [Definizione](https://en.wikipedia.org/wiki/The_Open_Source_Definition#Definition):

*Non ti preoccupare, non è necessario memorizzare tutto questo, ma è bene conoscere i principi da cui l'OSS proviene.*

- **Ridistribuzione gratuita**: la licenza non limiterà a nessuna parte la vendita o la cessione del software come componente di una distribuzione software aggregata contenente programmi provenienti da fonti diverse. La licenza non richiede un compenso o altra commissione per tale vendita.
    
    - **Codice sorgente**: il programma deve includere il codice sorgente e deve consentire la distribuzione nel codice sorgente e nel modulo compilato. Laddove una qualche forma di prodotto non è distribuita con il codice sorgente, ci deve essere un mezzo ben pubblicizzato per ottenere il codice sorgente per non più di un ragionevole costo di riproduzione preferibilmente, scaricando via Internet gratuitamente. Il codice sorgente deve essere la forma preferita in cui un programmatore dovrebbe modificare il programma. Il codice sorgente deliberatamente offuscato non è consentito. Non sono ammesse forme intermedie come l'output di un preprocessore o di un traduttore.
    
    - **Opere derivate**: la licenza deve consentire modifiche e opere derivate e deve consentirne la distribuzione agli stessi termini della licenza del software originale.
    
    - **Integrità del codice sorgente dell'autore**: la licenza può limitare la distribuzione del codice sorgente in forma modificata solo se la licenza consente la distribuzione di "file patch" con il codice sorgente allo scopo di modificare il programma al momento della compilazione. La licenza deve consentire esplicitamente la distribuzione di software creato da un codice sorgente modificato. La licenza potrebbe richiedere che i lavori derivati portino un nome o un numero di versione diverso dal software originale.
    
    - **Nessuna discriminazione contro persone o gruppi**: la licenza non deve discriminare alcuna persona o gruppo di persone.
    
    - **Nessuna discriminazione nei confronti di Field of Endeavour**: la licenza non deve impedire a nessuno di utilizzare il programma in uno specifico campo di attività. Ad esempio, potrebbe non limitare il programma a essere utilizzato in un'azienda o essere utilizzato per la ricerca genetica.
    
    - **Distribuzione della licenza**: i diritti connessi al programma devono essere applicati a tutti coloro a cui il programma viene ridistribuito senza la necessità di eseguire una licenza aggiuntiva da parte di tali parti.
    
    - **licenza non deve essere specifica per un prodotto**: i diritti associati al programma non devono dipendere dal fatto che il programma faccia parte di una particolare distribuzione software. Se il programma viene estratto da tale distribuzione e utilizzato o distribuito nei termini della licenza del programma, tutte le parti a cui il programma viene ridistribuito dovrebbero avere gli stessi diritti garantiti in concomitanza con la distribuzione del software originale.
    
    - **licenza non deve limitare altro software**: la licenza non deve porre restrizioni ad altri software distribuiti insieme al software con licenza. Ad esempio, la licenza non deve insistere sul fatto che tutti gli altri programmi distribuiti sullo stesso supporto debbano essere software open source.
    
    - **licenza deve essere tecnologia-neutrale**: Nessuna disposizione della licenza può essere basata su una singola tecnologia o stile di interfaccia.

Ora, tutto questo potrebbe essere un po 'complesso da ricordare. Tuttavia, può essere riassunto come *rendendo il software più riutilizzabile possibile per i lavori futuri, pur essendo disponibile gratuitamente*.

  


## Una lista di controllo open source

Esistono numerose piattaforme e strumenti esistenti che supportano l'OSS e la collaborazione. Il manuale [Open Science Training Handbook](https://open-science-training-handbook.gitbook.io/book/) fornisce una checklist da utilizzare per valutare l''apertura' del software di ricerca esistente, basato sulla Definizione Open Source sopra:

- [] Il software è disponibile per il download e l'installazione?

- [] Il software può essere facilmente installato su piattaforme diverse?

- [] Il software ha delle condizioni sull'uso?

- [] Il codice sorgente è disponibile per l'ispezione?

- [] La cronologia completa del codice sorgente è disponibile per l'ispezione attraverso una cronologia delle versioni disponibile pubblicamente?

- [] Le dipendenze del software (hardware e software) sono descritte correttamente? Queste dipendenze richiedono solo uno sforzo ragionevolmente minimo per ottenere e utilizzare?

Controlla, controlla, controlla, fatto! Semplici.

  


## La comunità Open Source e il suo governo <a name="OS_Community"></a>

There are two main camps within the free/libre and open source software (FLOSS) community: The **free software movement**, and the **open source software movement** (OSS). Entrambi hanno diverse ideologie basate sulle libertà dell'utente e le applicazioni pratiche del software. The term 'FLOSS' is used as a overaching neutral term to refer to both; libre being French and Spanish for 'free' in the context of freedom.

In a similar way that people active in the open science movement are heterogeneous in their assumptions and aims, different opinions exist in the FLOSS community as well. Recalling module 1, two of the schools of thought in open science were the *Pragmatic school* and the *Democratic school*. While the former is driven by the assumption that research could be more efficient if scientists worked together, the latter wants to set straight an unequal distribution of knowledge. They probably both end up sharing their research, but each with different intentions.

This is roughly comparable to the OSS and the free software movement: The latter evolved around 1983 to protect what they call the four essential freedoms of a program's user. These include the freedom to run, copy, distribute, study, change and improve a program. Software that respects these freedoms with an appropriate license is considered 'free'. The four freedoms are seen as vital for a society as a whole in the sense that they only enable sharing, cooperation and ultimately freedom in general. In this sense the free software movement is a social movement that creates an ethical imperative.

The open source software movement, which splintered off in 1998, focuses on the practical advantages and does not campaign for principles. It is concerned with developing high-quality software, for which everyone's ability to obtain, modify and contribute back the source code is considered highly beneficial.

Among multiple conclusions they arrive at, access to a program's source code is a shared one. Software thus may be considered *free*, *open source*, or both, according to agreed-on definitions by the Free Software Foundation ([FSF](https://www.gnu.org/philosophy/free-sw.html)) and the Open Source Initiative ([OSI](https://opensource.org/osd)). The FSF argues that free software is a subset of OSS, with only a [fraction](https://www.gnu.org/philosophy/free-open-overlap.html) being open source but nonfree.

Thus, highlighting a particular license status of software in use—open source or free—is mostly about different philosophies, not about software not having the other status as well. Each movement has its share of problems explaining their term: *free* means more than being gratis and *open source* means more than having access to the source code. The [FSF](https://www.gnu.org/philosophy/open-source-misses-the-point.html) and the European counterpart [FSFE](https://fsfe.org/documents/whyfs.html) provide more information on this topic.

### Per singoli progetti

A typical open source project has the following types of formal roles:

- **Autore**: è la persona che ha creato il progetto
- **Proprietario**: la / le persona / i che detiene la proprietà amministrativa sull'organizzazione o sul deposito 
- **Maintainer**: Contributori che sono responsabili per guidare la visione e gestire gli aspetti organizzativi del progetto. (Possono anche essere autori o proprietari del progetto.)
- **Contributori**: l'utente che ha già contribuito al progetto.
- **Membri della comunità**: persone che usano il progetto. Potrebbero essere attivi nelle conversazioni, creare nuovi problemi o esprimere la loro opinione sui futuri miglioramenti del progetto.

Typically, roles are made public through either the `README` file, a Contributors file, or a separate team page for the project.

  


## Piattaforme e strumenti esistenti per software Open Source <a name="Platforms"></a>

Virtual environments and machines are becoming increasingly popular as high-powered research workflow enablers, and many of these are built upon OSS (e.g., operating systems, programming languages, and data processing frameworks). Popular services include [Google Cloud](https://cloud.google.com/compute/) and [Amazon Web Services](https://aws.amazon.com/), which also assist with database storage and content delivery, as well as computational power. [InsideDNA](https://insidedna.me/) is a computing platform for reproducible research in bioinformatics, genomics and the life sciences.

As mentioned [above](#What_OSS), LibreOffice provides an Open Source alternative to Microsoft Office. The two are almost completely compatible, just with different default file formats. For citation managers, [Zotero](https://www.zotero.org/) is the most popular Open Source alternative to proprietary platforms such as Mendeley or EndNote.

[Zotero](https://www.zotero.org/) uses the BibTeX (pronounced 'bib-tech') format, based on LaTeX (pronounced 'lay-tech'), and has browser plugins to make citation management simple. By integrating this with other software such as LibreOffice, it is now possible to have a fully Open Source research workflow in many cases.

### GitHub <a name="GitHub"></a>

> Lo sapevate che l'intero progetto è stato costruito come un tentativo comunità aperta e collaborativa in [GitHub](https://github.com/OpenScienceMOOC/)?

[GitHub](https://github.com/) is a popular hosting site for both software and non-software content (often called 'notebooks'), with added capabilities for version control, project management and tracking, and storage services. GitHub is built on top of the OSS [Git](https://git-scm.com/), which enables users to work remotely to maintain, share, and collaborate on research software and other non-software based projects.

Version control is essentially a process that takes snapshots of the files in a repository, and tracks modifications to them. It records when the changes were made, what they were, and who did them. If several people are working on one file at once, any overlapping changes are detected, and must be resolved prior to continuing. This provides a much more streamlined and automated process than manually saving and recording changes as projects develop. It also avoids the inevitable lists of confusing named file versions...

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/xkcd.png?raw=true" width="200" /></p>

<p align="center"><i>GitHub helps us to avoid, er, sub-optimal file naming conventions (source: XKCD)</i></p>

  


One of the more popular and useful functions of GitHub is the [issue tracker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/issues), which is used to organise OSS development. The above link takes you to the issue tracker for the development of this module! If you think there is something here that can improved, or you want to comment on, anyone can add or contribute to an issue there!

Other similar project hosting services include [BitBucket](https://bitbucket.org/), [GitLab](https://about.gitlab.com/), and [Launchpad](https://launchpad.net/). If the recent acquisition of GitHub by Microsoft is a bit off-putting to you, these are great alternatives.

However, we also know that GitHub can have quite a high learning curve. Which is why the first practical task for this MOOC will teach you how to set up your first GitHub project repository!

**[GO TO TASK 1: Building your first GitHub repository](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)**

  


## Software Open Source utilizzato nella ricerca <a name="Research"></a>

Especially in scientific research, Open Source Software usage and development has become practically the norm. There's a number of reasons for this beyond those that apply to the general acceptance of OSS by, for example, consumers, industry, or government. Among these reasons are:

- Sempre più spesso, gli algoritmi implementati nel software di analisi sono parte integrante dei metodi descritti nelle pubblicazioni accademiche. In quanto tale, è completamente in disaccordo con una rigorosa revisione tra pari se queste implementazioni degli algoritmi sono chiuse agli estranei.

- La collaborazione scientifica spesso si estende su più istituzioni e reti di ricerca distribuite in cui la segretezza e la gerarchia di comando non sono mantenute in un modo che è "necessario" per lo sviluppo a codice chiuso.

- Molte analisi computazionali sono eseguite in ambienti virtualizzati (come infrastrutture "cloud" istituzionali, nazionali o internazionali) e ospitate su server multiutente. Il software commerciale closed-source spesso non consente tale utilizzo.

- Lo sviluppo dell'OSS si basa spesso su volontari. In un momento di limiti di budget per la ricerca scientifica, questo è un chiaro vantaggio.

For these and other reasons, Open Source tools are very commonly used in scientific research. This includes usage in fields where many researchers are amateur developers themselves and rely on tools such as [R](https://www.r-project.org/) for statistical analysis and scripting, which, in the last decade, has almost completely displaced commercial software for statistical analysis such as SPSS or JMP in a lot of fields. In fields such as bioinformatics, that involve a lot of file handling of the outputs of DNA sequencing platforms, general purpose scripting languages such as [Python](https://www.python.org/) and commonly used libraries built on top of it (such as [biopython](http://biopython.org)) have become a vital part of the toolkit of many researchers.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/python.png?raw=true" width="400" /></p>

<p align="center"><i>Python</i></p>

  


Tools such as R and Python are essentially software for writing software. Although programming is an increasingly common activity among researchers, of course not *every* scientist does this. One step away from programming is the chaining together of the inputs and outputs of various analysis tools in longer workflows. As an example from genomics, a very common workflow is to start out with high-throughput sequencing reads and then i) do basic quality control checks; ii) map the reads against a reference genome; iii) identify the points where the new data are at variance with the reference. These steps are routinely executed as a workflow where a different Open Source executable is run in a Linux command-line environment for each of the three steps. Although this is arguably not quite open source software development, it does involve the usage and production of open source artifacts (such as Linux shell scripts) for which the principles that we discuss in this module are applicable.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/r.png?raw=true" width="200" /></p>

<p align="center"><i>R</i></p>

  


Lastly, OSS is also used in scientific research for reasons that more closely mirror those that drive the adoption of OSS in wider society, namely that it is cheap. For example, individuals or organizations might decide to switch from Microsoft Office to LibreOffice for manuscript writing or spreadsheet processing because the latter is free (both as in [**'free beer'**](https://www.youtube.com/watch?v=dQw4w9WgXcQ) and 'free speech'). Likewise, the choice to switch from ArcGIS to [QGIS](https://www.qgis.org/en/site/) for the analysis of geographic information might be prompted simply by cost considerations.   


## Guida introduttiva all'OSS - Domande frequenti <a name="FAQ"></a>

**I'm using X[e.g. Matlab,STATA,Excel] and I want to transition to something more open. What are the next steps?**

Even if you are using proprietary software, you can usually still share your source code/documents etc. *The best first step is sharing whatever you can*.

**Great! I can put them in my new github repo.**

If that's enough for you for now great! If not for most pieces of proprietary software there are Open Source equivalents. Have a go with one and see what you think.

| Chiuso                                                                                                  | Aperto                                                                                                                                                            |
| ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Matlab                                                                                                  | Python, Julia                                                                                                                                                     |
| STATA / SPSS                                                                                            | R                                                                                                                                                                 |
| MS Office                                                                                               | LibreOffice                                                                                                                                                       |
| matematica                                                                                              | JupyterLab                                                                                                                                                        |
| Max/MSP                                                                                                 | PureData                                                                                                                                                          |
| Test out your new [Pull Request -PR-](https://help.github.com/articles/about-pull-requests/) Skills ... | ... by adding your own example [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md) |

**Cool! But if I make the switch will I be stuck: taking ages to learn a new tool/ without support /with buggy software.**

Good question! The answer is it depends. The best thing to do is find someone who's made the switch before and learn from their experience. Or just do a Google search! Some OSS is much better than their closed counterparts, some aren't, so it's worth choosing carefully.

## Fare un buon software per il riutilizzo <a name="Reuse"></a>

The most likely person who might want to re-use your software in the future is...you! So while sharing is always better than not sharing, you can make your own life, and that of others, much easier through appropriate documentation. Documentation can include several things, such as including helpful comments and annotations in the code that help to explain why a particular action was performed, rather than what it is intended to achieve.

One of the most critical aspects of this is including an informative `README` file, that accompanies almost every OSS project, and some times even more than one. It can be a good practice to include one such file in every directory, that includes a list of files, a table of contents, and what the purpose of the directory is. The `README` file is typically just plain text or markdown (again, such as all of the ones for the MOOC!), and can include critical information for how to install and run software, previous dependencies and requirements, as well as tutorials or examples.

> **Lo sapevi che ...** Il termine `README` è spesso attribuito alla famosa scena di Alice nel paese delle meraviglie di Lewis Carroll, in cui Alice affronta magie munchies etichettate con "Eat Me" e "Drink Me". Potente.

The purpose here is to provide sufficient information to maximise the re-use and reproducibility of the computational environment, such that someone with no experience with the project can easily access and re-use the software ([Sandve et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)). By lowering the barriers to entry, you increase the chances of others being able to re-use your work, which is one of the ultimate goals of OSS ([Ince et al., 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)).

An extension of this that can help to make things even easier for future re-use is 'container' technology. Containers are like an ecosystem frozen in time, where the code, the data, any other dependencies, are all perfectly preserved, packaged and saved in the present functioning versions. This means that anyone in the future any one can come in and run the analyses again. As such, they are generally good for re-use, but this can come at the sacrifice of modification or understanding by others, as often a lot of details can be hidden within the source code and its dependencies. Common examples of container implementation in research include [Rocker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf) (a Docker container for the R language), [Binder](https://mybinder.readthedocs.io/en/latest/), and [Code Ocean](https://codeocean.com/).

**Sustainable software is good software.**

  


## 10 regole semplici per una ricerca computazionale riproducibile

The 10 simple rules for making computational research more reproducible, based on [Sandve et al., (2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF), are:

1. Per ogni risultato, tieni traccia di come è stato prodotto.
2. Evitare passaggi di manipolazione dei dati manuali.
3. Archiviare le versioni esatte di tutti i programmi esterni utilizzati.
4. La versione controlla tutti gli script personalizzati.
5. Registra tutti i risultati intermedi, quando possibile in formati standardizzati.
6. Per le analisi che includono la casualità, nota i semi casuali sottostanti.
7. Memorizza sempre i dati grezzi dietro i grafici.
8. Genera output di analisi gerarchica, consentendo di ispezionare strati di dettagli crescenti.
9. Connetti le dichiarazioni testuali ai risultati sottostanti.
10. Fornire accesso pubblico a script, esecuzioni e risultati.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/simple_rules.png?raw=true" width="800" /></p>

<p align="center"><i>Infographic adapted from Sandve et al., (2013). Feel free to download this and print it out to keep handy during your research!</i></p>

  


If you follow these steps, along with the processes in [**Task 1**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [**Task 2**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), you should be fine!

  


## Licenze open source <a name="Licensing"></a>

An Open Source license is a type of license designed specifically for software and code that make it explicit what the legal conditions for sharing and re-use are. As mentioned [above](#What_OSS), the addition of a suitable license is what differentiates publicly shared software from OSS. For example, the widely used [MATLAB](https://www.mathworks.com/products/matlab.html) is proprietary software, and [Octave](https://www.gnu.org/software/octave/) is an openly licensed alternative programming language.

There are currently more than 1,400 unique Open Source licenses, a complexity born from the difficulty in understanding the differences between the legal implications across different license.

Some of the more common licenses include:

- [Berkeley Software Distribution ("BSD")](https://en.wikipedia.org/wiki/BSD_licenses),
- [Apache](https://www.apache.org/licenses/LICENSE-2.0),
- [MIT-style (Massachusetts Institute of Technology)](https://opensource.org/licenses/MIT), o
- [Licenza pubblica generale GNU ("GPL")](https://www.gnu.org/licenses/gpl-3.0.en.html).

You don't need to know all the legal itty gritty behind all of these, but it is good to at least know what options are avaiilable to you.

There are two ways in which contributions to a project become licensed:

1. *Esplicitamente*, in cui il contributo individuale ha una licenza chiaramente indicata indipendente dal progetto principale; o
2. *Implicitamente*, per cui il contributo rientra nel codice di licenza originale del progetto principale.

Thankfully, the process of selecting an Open Source license is relatively trivial, thanks to user-friendly tools such as [Choose A License](https://choosealicense.com/) or [Public License Selector](https://ufal.github.io/public-license-selector/). Each of these licenses allows other users to use, copy, distribute, and build upon your work, often while ensuring that the creators are appropriately recognised for their work. Here, the key is selecting an appropriate license for your work, depending on what you want, or do not want, others to do with it.

  


## Citazione del software <a name="Citation"></a>

Citations provide one of the most important interactions in scholarly research, forming the basis of our referencing and metrics systems. Typically, this is performed thanks to the assistance of a permanent unique identifier such as a [Digital Object Identifiers](https://en.wikipedia.org/wiki/Digital_object_identifier) (DOI). A DOI is a persistent identifier, implemented in the [Handle System](https://en.wikipedia.org/wiki/Handle_System), that meets a common standard, depending on the purpose, such as for identifying academic information. Such identification is critical for tracking the genealogy and provenance of research, for reproducibility, as well as for giving appropriate credit to those who have created the software. Importantly, software should be considered a legitimate output from scholarly research, and citation is becoming an increasingly common way to indicate that.

In 2016, [Smith et al., 2016](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) wrote a research paper about the principles of software citation as part of the FORCE11 Software Citation Working Group. In the same way that you would want to cite software that you have used as part of good research practices, it is important to make your research easily citable too. When citing any software used for your own research, you should include at minimum:

- Il nome dell'autore (s),
- Titolo del software,
- Numero di versione e
- L'identificatore / locatore univoco (DOI o URL).

The six principles of software citation by [Smith et al., (2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) are provided here:

- **Importanza**: il software dovrebbe essere considerato un prodotto di ricerca legittimo e citabile. Le citazioni del software dovrebbero avere la stessa importanza nella documentazione scolastica come citazioni di altri prodotti di ricerca, come pubblicazioni e dati; dovrebbero essere inclusi nei metadati del lavoro di citazione, ad esempio nell'elenco di riferimento di un articolo di giornale, e non dovrebbero essere omessi o separati. Il software dovrebbe essere citato sulla stessa base di qualsiasi altro prodotto di ricerca come una carta o un libro, vale a dire che gli autori dovrebbero citare l'insieme appropriato di prodotti software proprio mentre citano la serie appropriata di documenti.

- **Credito e attribuzione**: le citazioni software dovrebbero facilitare il conferimento del credito accademico e l'attribuzione normativa e legale a tutti i contributori al software, riconoscendo che uno stile unico o un meccanismo di attribuzione potrebbero non essere applicabili a tutto il software.

- **Identificazione univoca**: una citazione di software dovrebbe includere un metodo di identificazione che sia azionabile dalla macchina, globalmente unico, interoperabile e riconosciuto da almeno una comunità degli esperti di dominio corrispondenti, e preferibilmente da ricercatori pubblici generali.

- **Persistenza**: gli identificatori e i metadati univoci che descrivono il software e la sua disposizione dovrebbero persistere, anche oltre la durata di vita del software che descrivono.

- **Accessibilità**: le citazioni software dovrebbero facilitare l'accesso al software stesso e ai relativi metadati, documentazione, dati e altro materiale necessario sia per le persone che per le macchine per fare un uso consapevole del software di riferimento.

- **Specificità**: le citazioni software dovrebbero facilitare l'identificazione e l'accesso alla versione specifica del software che è stata utilizzata. L'identificazione del software dovrebbe essere specifica come necessario, come l'uso di numeri di versione, numeri di revisione o varianti come piattaforme.

Note: For instructions on 'how to make your software citable' see the section [**Using GitHub and Zenodo**](#GitHub_Zenodo) below and [**Task 2: Linking GitHub and Zenodo**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md).

  


## Utilizzando GitHub e Zenodo <a name="GitHub_Zenodo"></a>

[GitHub](#GitHub) is a popular tool for project management, content storage, and version control. Note that GitHub itself is not OSS. However, Git, the tool which it is based on, is. Git is designed to help manage the source code files, and the updates to them, for a software-related project. However, it can also be extended to other non-software projects; for example, this [MOOC](https://github.com/OpenScienceMOOC/)!

However, getting research onto GitHub is just the first step. It is equally important to make it persistent and re-usable, which is why having a Digital Object Identifier (DOI) associated with it can be useful. The simplest way to do this is through a service called [Zenodo](https://zenodo.org/), which is a free and open source multi-disciplinary repository created by OpenAIRE and CERN, and can be used to assign a DOI to individual GitHub repositories. There is a [GitHub Guide](https://guides.github.com/activities/citable-code/) that explains the details, which involve linking GitHub repositories directly through to Zenodo so that when developers create formal releases for their software, Zenodo creates and archives a that version of the software.

There's nothing special about using Zenodo for creating DOIs, other than its **free of cost**; other general repositories can also be used, such as [DataCite DOI Fabrica](https://doi.datacite.org/), or your own institutional repositories such as [Caltech's](https://www.library.caltech.edu/news/enhanced-software-preservation-now-available-caltechdata).

A lot of researchers might typically be afraid of sharing code which is incomplete, buggy, or imperfect. However, in the OSS community, such a practice of sharing 'raw' code is fairly commonplace. Sharing code openly enables others to re-use and improve it, as well as to engage in a deeper way with any research associated with it. This is one of the fundamental aspects of peer-collaboration, perhaps best exemplified by the traditional process of research manuscript peer review.

Task 2 will guide you through the process of linking a GitHub repository to Zenodo for archiving.

> **Lo sapevi che ...** Tutto il contenuto prodotto per questo MOOC è disponibile come parte di una comunità in [Zenodo](https://zenodo.org/communities/open-science-mooc/)?

**[GO TO TASK 2: Linking GitHub and Zenodo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)**

  


## Collaborare e contribuire attraverso l'Open Source <a name="Collaborating"></a>

Often, OSS is developed in a public, decentralised, collaborative manner between multiple contributors. The purpose of this is to enhance the diversity and scope of a project and its design, in order to become more beneficial and sustainable. Such an approach was famously likened to a 'bazaar' model by Eric Raymond, an early OSS proponent. One of the major guiding principles of this is that of **peer production**, which relies on self-organised communities to regulate the development of content, co-ordinated towards a shared goal or outcome.

OSS projects rely heavily on volunteer collaboration, which often entails a constant flux of newcomers in order to become productive and sustainable ([Steinmacher et al., 2014](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)). Creating the right social atmosphere for a project, and a welcoming engagement environment, are often critical to successful collaboraitons in OSS.

  


## Dove andare da qui <a name="Future_OSS"></a>

Hopefully now you have come to see the importance of software as a cornerstone of modern science, and the importance that OSS plays in this.

The **learning outcomes** from this should be:

1. Sarai ora in grado di definire le caratteristiche dell'OSS e alcuni degli argomenti di impatto etico, legale, economico e di ricerca a favore e contro di esso.

2. Basandoti sugli standard della community, sarai ora in grado di descrivere i requisiti di qualità della condivisione e del riutilizzo del codice aperto.

3. Ora sarai in grado di utilizzare una serie di strumenti di ricerca che utilizzano l'OSS.

4. Ora sarai in grado di trasformare il codice progettato per il loro uso personale in un codice accessibile e riutilizzabile da altri.

5. Gli sviluppatori di software saranno in grado di rendere il loro software interessante e gli utenti del software sapranno come citare il software che usano.

  


**BONUS TASK**

If you have completed [Task 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [Task 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), we also have a **BONUS TASK** for you, if you want to take your skills a step further. [Task 3](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md) will take you a step deeper into integrating Git into a typical research workflow by showing you how to integrate it with R Studio. It is recommended that you have completed the first 2 tasks before proceeding with this one.

However, your Open Source journey does not stop here! This was just the beginning, and there are some incredible resources out there if you would like to do or learn more:

- Se ti senti particolarmente ispirato da questo, puoi sostenere il Manifesto</a>codice scientifico , che si basa sui cinque principi di codice, copyright, citazione, credito e cura.</p></li> 
    
    - Per avviare e sviluppare il tuo progetto, il programma [Open Source Guides](https://opensource.guide/) offre una serie di guide pratiche e abilità per aiutarti a lanciare e far progredire i tuoi progetti OSS.
    
    - Per uno sguardo dettagliato ai flussi di lavoro di ricerca basati su OSS, la guida a [Open Science, Open Data, Open Source](https://pfern.github.io/OSODOS/gitbook/) di Pedro L. Fernandes e Rutger A. Vos è una delle migliori risorse online.
    
    - Esistono anche sedi di riviste più formalizzate per articoli basati su software, tra cui [The Journal of Open Research Software](https://openresearchsoftware.metajnl.com/) e [The Journal of Open Source Software](https://joss.theoj.org/). Un elenco di tali luoghi è anche disponibile [](https://www.software.ac.uk/which-journals-should-i-publish-my-software).
    
    - [PLOS Open Source Toolkit](https://channels.plos.org/open-source-toolkit) fornisce un forum globale per la ricerca e l'applicazione di hardware e software Open Source.
    
    - [NumFOCUS](http://www.numfocus.org) è un'organizzazione non profit che supporta e promuove software scientifico open source di livello mondiale e innovativo. Alcuni dei progetti che sponsorizzano includono:
        
        - [Iniziative IPython](http://ipython.org) e [Jupyter Notebook](https://jupyter.org).
        
        - [rOpenSci](http://ropensci.org), che promuove l'ambiente statistico R open source per ricerche trasparenti e riproducibili.
        
        - Per acquisire più esperienza con OSS, la comunità [Software Carpentry](https://software-carpentry.org/) tiene seminari regolari per migliorare le capacità di calcolo basate sul laboratorio ([Wilson et al., 2017](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Wilson%20et%20al.%2C%202017.pdf)).</ul> 
    
      
    
    
    ### Ulteriori letture <a name="Reading"></a>
    
    *These references here are just the beginning. They include some of the most useful general overviews of the Open Source landscape in research. However, if you want to be find something more specific to your own research field, then that path is there for you to explore!*
    
    - Il futuro della ricerca nello sviluppo di software libero / open source [(Scacchi, 2010)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Scacchi%2C%202010.pdf).
    
    - Il metodo scientifico in pratica: riproducibilità nelle scienze computazionali [(Stodden, 2010)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Stodden%2C%202010.pdf).
    
    - Il caso dei programmi per computer aperti [(Ince et al., 2012)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf).
    
    - Problemi attuali e tendenze di ricerca sulle comunità di software open source [(Martinez-Torres e Diaz-Fernandez, 2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Martinez-Torres%20and%20Diaz-Fernandez%2C%202013.pdf).
    
    - Dieci semplici regole per la ricerca computazionale riproducibile [(Sandve et al., 2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF).
    
    - Una revisione sistematica della letteratura sugli ostacoli incontrati dai nuovi arrivati nei progetti di software open source [(Steinmacher et al., 2014)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf).
    
    - Condivisione della conoscenza nelle comunità di software open source: motivazione e gestione [(Iskoujina e Roberts, 2015)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Iskoujina%20and%20Roberts%2C%202015.pdf).
    
    - Principi di citazione del software [(Smith et al., 2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf).
    
    - Un'introduzione a Rocker: contenitori Docker per R [(Boettiger e Eddelbuettel, 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf).
    
    - Buone pratiche nel calcolo scientifico [(Wilson et al., 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Wilson%20et%20al.%2C%202017.pdf).
    
    - Quattro semplici raccomandazioni per incoraggiare le migliori pratiche nel software di ricerca [(Jiménez et al., 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Jim%C3%A9nez%20et%20al.%2C%202018.pdf).
    
      
    
    
    ### Team di sviluppo <a name="Development_team"></a>
    
    - [Alex Morley](https://twitter.com/alex__morley), Open Sourceror, Università di Oxford, Regno Unito.
    - [Kevin Moerman](https://twitter.com/KMMoerman), Open Sourceror, MIT, USA.
    - [Tania Allard](https://twitter.com/ixek), Open Sourceress, Data Enchantress, Università di Leeds, Regno Unito.
    - [Simon Worthington](https://twitter.com/mrchristian99), Liberazionista del libro, TIB, Germania.
    - [Paola Masuzzo](https://twitter.com/pcmasuzzo), Open Source Batman, Italia.
    - [Ivo Grigorov](https://twitter.com/OAforClimate), Open Source Robin, Danimarca.
    - [Rutger Vos](https://twitter.com/rvosa), Open Sourceror, Naturalis Biodiversity Centre, Paesi Bassi.
    - [Julien Colomb](https://twitter.com/j_colomb), Open Ninja, Berlino.
    - [Jon Tennant](https://twitter.com/protohedgehog), Dinosaur Whisperer.
    
    **Know a way this content can be improved?**
    
    Time to take your new GitHub skills for a test-run! All content development primarily happens [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md). If you have a suggested improvement to the content, layout, or anything else, you can make it and then it will automatically become part of the MOOC content after verification from a moderator!
    
    [![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)