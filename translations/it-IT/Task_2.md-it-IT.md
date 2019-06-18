---
output:
  html_document: predefinito
  pdf_document: predefinito
---

# Attività 2: Come rendere il tuo codice citabile usando GitHub e Zenodo

Questo compito è progettato per studenti e ricercatori che desiderano creare e riutilizzare progetti / repository basati su GitHub nella letteratura accademica.

Non dimenticare che puoi partecipare alle discussioni sul nostro open [**Slack channel**](https://osmooc.herokuapp.com/). Per favore, presentati a # module5opensource e raccontaci un po 'di chi sei, del tuo background e di come sei finito qui!

Tempo stimato per il completamento: 45-60 minuti.

## Sommario

- [Prefazione](#Foreword)
- [Configurare un repository GitHub](#Setup)
- [Scegli il tuo repository GitHub](#Choose)
- [Accedi a Zenodo](#Login)
- [Autorizza GitHub a connettersi con Zenodo](#Authorise)
- [Seleziona il repository da archiviare](#Archive)
- [Controlla le impostazioni del repository](#Check)
- [Crea una nuova versione](#Release)
- [Ottenere un DOI](#DOI)
- [Lista di controllo per la citazione del tuo progetto](#Checklist)
- [Risorse addizionali](#Resources)

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/Task2.png?raw=true" alt="Task 2 flusso di lavoro" width="600" height="861" style="margin-right: 30px; margin-left: 10px;" onmouseover="this.width='1200'; this.height='1722'" onmouseout="this.width='600'; this.height='861'">
</p>

<p align="center"><i>Il flusso di lavoro per l'attività 2. Tienilo a portata di mano mentre lavori attraverso l'operazione!</i></p>

  


## Prefazione <a name="Foreword"></a>

Sebbene l'integrazione di GitHub e Zenodo rendano davvero più facile lavorare con questi strumenti al giorno d'oggi (gennaio 2019), è importante sottolineare che esistono alternative a GitHub (Gitlab, Bitbucket, ...) e alternative a Zenodo (Altri repository potrebbero sii più adatto alla tua comunità, potresti chiedere ai tuoi colleghi). Ad esempio, si può lavorare con Gitlab e caricare manualmente ogni nuova versione nel proprio archivio universitario, ottenendo un DOI. I principi (lavorando con un sistema di controllo delle versioni online e archiviando le versioni principali in un repository che fornisce un identificatore univoco persistente) possono essere applicati in diversi flussi di lavoro.

## Configurare un repository GitHub <a name="Setup"></a>

> **Pro-tip**: assicurati di includere un LICENSE e un file README nel tuo repository. Ciò indicherà alle persone lo scopo del progetto e come potranno interagire con esso in futuro.

Scopri come impostare un repository GitHub in quest'altra guida [Compito 1: Costruire un repository GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) che è anche parte del 'Modulo 5: Open Research Software e Open Source'.

## Scegli il tuo repository GitHub <a name="Choose"></a>

Una volta sulla tua pagina di annunci del progetto GitHub su [github.com](https://github.com) vai alla scheda 'Archivi'. Seleziona il repository che desideri archiviare e aprilo.

  


## Accedi a Zenodo <a name="Login"></a>

Ora vai su [zenodo.org](https://zenodo.org). Zenodo è una piattaforma in cui puoi archiviare in modo permanente il tuo codice e altri elementi del progetto. Zenodo lo fa assegnando ai progetti un **Digital Object Identifier** (DOI), che aiuta anche a rendere il lavoro più interessante. Questo è diverso da GitHub, che funge da luogo in cui avviene il lavoro effettivo su un progetto, piuttosto che dall'archiviazione a lungo termine di esso. In GitHub, il contenuto può essere modificato, cancellato, riscritto e modificato in modo irreversibile, il che rende un po 'preoccupante l'utilizzo per scopi di riferimento duraturi. Zenodo offre maggiore sicurezza e permanenza per i risultati della ricerca.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/zenodo.png?raw=true" width="800" /></p>

<p align="center"><i>Iscriviti a Zenodo</i></p>

  


Se hai già un account Zenodo, questo è facile. In caso contrario, segui i passaggi per crearne uno: puoi anche accedere utilizzando il tuo account GitHub o il tuo profilo ORCID per semplificare le cose, dato che Zenodo ha un'integrazione integrata per esso. Questo potrebbe essere più semplice rispetto alla creazione di un altro account e profilo di ricerca.

  


## Autorizza GitHub a connettersi con Zenodo <a name="Authorise"></a>

Sul sito Web di Zenodo autorizzalo a connettersi al tuo account GitHub nella sezione '[Utilizzo di GitHub](https://zenodo.org/account/settings/github/)'. Qui, Zenodo ti reindirizzerà a GitHub per chiedere le autorizzazioni per usare "[webhooks](https://developer.github.com/webhooks/)" sui tuoi repository. Vuoi autorizzare Zenodo qui con i permessi necessari per formare quei link.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/zenodo_github.png?raw=true" width="800" /></p>

<p align="center"><i>Autorizza Zenodo a connettersi con GitHub</i></p>

  


Se stai tentando di concedere a Zenodo l'accesso a un repository organizzativo, l'utente (o un amministratore) dovrà assicurarsi che a Zenodo siano concesse le autorizzazioni di accesso di terze parti. GitHub invierà un'email di autorizzazione che deve essere confermata. A questo punto, nelle impostazioni del tuo repository su GitHub, devi anche assicurarti che il repository sia impostato su "public", non privato.

  


## Seleziona il repository da archiviare <a name="Archive"></a>

Se si è arrivati a questo punto, ciò significa che Zenodo è ora autorizzato a configurare i webhook di repository di cui ha bisogno per archiviare il repository e rilasciarlo come DOI. Per fare ciò, sul sito Web di Zenodo accedere al repository [GitHub che elenca la pagina](https://zenodo.org/account/settings/github/) e fare semplicemente clic sul pulsante "on" accanto al proprio repository.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/enabled_repos.png?raw=true" width="800" /></p>

<p align="center"><i>Abilita i singoli repository GitHub da conservare in Zenodo</i></p>

  


## Controlla le impostazioni del repository <a name="Check"></a>

Ora hai impostato un nuovo webhook tra Zenodo e il tuo repository. In GitHub, fai clic sulle impostazioni per il tuo repository e sulla scheda Webhooks nel menu a sinistra. Questo dovrebbe mostrare il nuovo webhook Zenodo configurato per Zenodo. Nota, potrebbe essere necessario un po 'di tempo prima che l'elenco del webhook venga visualizzato.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/webhooks.png?raw=true" width="800" /></p>

<p align="center"><i>Verifica che i webhook siano abilitati per il tuo repository GitHub. Esempio qui usando la Open Scholarship Strategy</i></p>

  


## Crea una nuova versione <a name="Release"></a>

La prima volta che archivi un repository è noto come "prima versione". Ogni volta che crei una nuova versione di quel repository e la archivi, crei una nuova versione. Questo può essere tracciato nella scheda "releases" del tuo repository su GitHub (in alto al centro).

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/first_release.png?raw=true" width="800" /></p>

<p align="center"><i>Verifica che la prima versione del repository abbia avuto successo. Esempio qui usando la Open Scholarship Strategy</i></p>

  


Per la prima versione archiviata del tuo repository, fai clic su "Crea una nuova versione" di nuovo in Zenodo. Compila il modulo e fornisci alcuni dettagli su ciò che la liberatoria comporta. Per la prima versione, assicurati di chiamarla v1.0.0, come è prassi normale.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/create_release.png?raw=true" width="800" /></p>

<p align="center"><i>Crea una nuova versione. Esempio qui usando la Open Scholarship Strategy, per la quale esiste già una prima versione</i></p>

  


Infine, fai clic su "pubblica versione" e il tuo archivio sarà pubblicato e versionato su GitHub.

Per visualizzare la tua versione su Zenodo devi visitare la scheda [Carica](https://zenodo.org/deposit). Per completare l'archiviazione sono necessari alcuni dettagli su Zenodo.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/upload_release.png?raw=true" width="800" /></p>

<p align="center"><i>Verifica che la nuova versione sia stata caricata. Esempio qui mostrato usando la Open Scholarship Strategy</i></p>

  


## Ottenere un DOI <a name="DOI"></a>

A volte questo viene chiamato "zecca" DOI e richiede un paio di bit extra di informazioni sul repository su Zenodo. Su Zenodo, fai clic sulla scheda [Carica](https://zenodo.org/deposit) nel menu principale e il repository appena caricato dovrebbe essere lì. Scorri la pagina verso il basso e inserisci le informazioni aggiuntive secondo necessità, i campi obbligatori sono contrassegnati da un asterisco rosso, quindi fai clic su "Pubblica".

**Nota**: solo dopo che queste informazioni aggiuntive sono state aggiunte, il tuo DOI diventerà attivo. Potrebbe anche volerci un po 'di tempo prima che il DOI diventi attivo. Esempio DOI mostrato di seguito (per la Open Scholarship Strategy di nuovo).

> **Pro-tip**: Copia l'URL per il DOI nel file README per il repository GitHub per rendere ancora più semplice il cross-link, oltre a presentare un badge DOI chiaro e chiaro per consentire agli utenti di vedere e utilizzare il tuo DOI. Hai solo bisogno di farlo una volta con il tuo primo rilascio DOI in quanto agisce come un "concetto DOI" ed è collegato a tutti i successivi DOI di rilascio.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1323437.svg)](https://doi.org/10.5281/zenodo.1323437)

L'integrazione GitHub / Zenodo ora assegnerà un DOI a ciascuna versione / rilascio di un repository di progetto. Ciò consente agli utenti di fare riferimento e citare versioni specifiche dei progetti. Inoltre, l'elenco degli autori per la citazione è determinato automaticamente dai nomi degli account utente GitHub usati dal repository, il che significa che nessuno viene lasciato fuori. I dettagli dell'autore possono essere modificati in seguito su Zenodo. I DOI utilizzati in Zenodo sono registrati tramite il servizio [DataCite](https://www.datacite.org/).

> **Pro-tip**: Crea una versione "leggibile" di questa citazione nel file README del tuo progetto. Ciò sarà utile per i ricercatori che potrebbero non avere familiarità con l'uso di DOI per creare citazioni e rendere più facile per gli altri citare il tuo software e riconoscere il tuo lavoro. Un esempio di questo potrebbe essere: Jon Tennant. (2018, 30 luglio). Fondamenti per Open Scholarship Strategy Development: prima versione ufficiale (versione 1.2). Zenodo. <http://doi.org/10.5281/zenodo.1323437>

**CONGRATULAZIONI!!**

Il tuo repository GitHub è ora archiviato in Zenodo e con un DOI che può essere versionato per riflettere gli aggiornamenti della versione del repository nel tempo. Dovresti essere in grado di vedere i dettagli di questo nella pagina di Zenodo di GitHub per il tuo repository. Ciò significa anche che i tuoi progetti archiviati possono essere raccolti da altri servizi di indicizzazione e motori di ricerca che utilizzano anche le DOI.

È necessario fornire un archivio a lungo termine e un DOI per il tuo lavoro affinché altri possano citarlo correttamente, in quanto fornisce metadati di citazione di base. Per Open Science, è importante essere in grado di citare il software che si utilizza nella ricerca e questo flusso di lavoro integrato consente che ciò accada, in linea con le migliori pratiche per la citazione di ricerca. Inoltre, questa pratica è importante per elevare lo standard del software (e dei progetti correlati) a quello dello standard di altri risultati di ricerca.

> **Suggerimento**: la tua ricerca è finanziata da una sovvenzione UE? Ora puoi collegare direttamente il tuo progetto archiviato alla tua sovvenzione aggiornando la sezione di sovvenzione dei metadati sul record Zenodo del progetto. Questo aiuta enormemente ad aumentare la sua rilevabilità!

  


## Lista di controllo per la citazione del tuo progetto <a name="Checklist"></a>

Così ora hai un repository GitHub archiviato in modo sostenibile in Zenodo pronto per essere riutilizzato e citato! Prima di continuare, assicurati di avere:

- [] Collegato il tuo progetto GitHub a Zenodo. Se vedi una copia completa del tuo repository GitHub in Zenodo, allora le cose stanno funzionando.
- [] La configurazione integrata di Zenodo e GitHub funziona bene. Ad esempio, tutti i nomi degli autori e il titolo del progetto corretto si riferiscono a Zenodo. In caso contrario, o se gli autori hanno solo soprannomi, puoi modificare questi dettagli in Zenodo.
- [] Il progetto ha una prima versione, con un DOI. Dovresti visualizzare un DOI sulla pagina dei tuoi progetti Zenodo. Questo primo DOI è chiamato "concetto DOI" ed è il DOI principale che collega a tutte le successive DOI di rilascio. Copia questo link DOI e incorporalo nella pagina README dei progetti GitHub. Hai finito!

### Risorse addizionali <a name="Resources"></a>

[Rendi il tuo codice leggibile](https://guides.github.com/activities/citable-code/) - GitHub Guides.

**Sapere in che modo questo contenuto può essere migliorato?**

È tempo di prendere le tue nuove abilità GitHub per un test-run! Tutto lo sviluppo del contenuto avviene principalmente qui [qui](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md). Se hai un miglioramento suggerito per il contenuto, il layout o qualsiasi altra cosa, puoi realizzarlo e poi diventerà automaticamente parte del contenuto di MOOC dopo la verifica da parte di un moderatore!

[![Dedicato pubblico dominio CC0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)