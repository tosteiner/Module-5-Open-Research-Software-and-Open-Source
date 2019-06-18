---
output:
  html_document: predefinito
  pdf_document: predefinito
---

# Attività 1: come impostare un repository su GitHub

Questo compito è progettato per studenti e ricercatori che desiderano creare il loro primo progetto Open Source (software o non software) su GitHub. GitHub è un posto in cui puoi venire a giocare e sperimentare nuovi flussi di lavoro di ricerca, ed è davvero solo l'inizio per aiutare a preparare il terreno per i tuoi percorsi e le tue idee.

Non dimenticare che puoi partecipare alle discussioni sul nostro open [**Slack channel**](https://osmooc.herokuapp.com/). Per favore, presentati a # module5opensource e raccontaci un po 'di chi sei, del tuo background e di come sei finito qui!

**SI PREGA DI NOTARE** che una registrazione dello schermo per questa attività è disponibile anche tramite [YouTube](https://www.youtube.com/watch?v=AnftV9HBPSc&).

Tempo stimato per il completamento: 30-45 minuti.

Stimare il risparmio di tempo una volta completato: inimmaginabile ..

## Sommario

* [Iniziare](#Getting_started) 
  * [Impostazione di un profilo GitHub](#Profile)
  * [Il linguaggio GitHub](#Language)
  * [Creare un nuovo repository](#Create_new)
* [I passaggi fondamentali](#Foundation) 
  * [Scegliere una licenza](#License)
  * [Creare un file README](#Readme)
  * [Creare linee guida di contribuzione](#Contributing)
  * [Creare un codice di condotta](#Conduct)
  * [Rendi il tuo codice leggibile](#Citation)
* [Mantenere aggiornati i tuoi problemi](#Issues)
* [Elenco di controllo per l'avvio del progetto](#Check-list)

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/Task1.png?raw=true" alt="Task 1 flusso di lavoro" width="600" height="861" style="margin-right: 30px; margin-left: 10px;" onmouseover="this.width='1200'; this.height='1722'" onmouseout="this.width='600'; this.height='861'">
</p>

<p align="center"><i>Il flusso di lavoro per l'attività 1. Tienilo a portata di mano mentre lavori attraverso l'operazione!</i></p>

  


## Iniziare <a name="Getting_started"></a>

Un 'repository' è in realtà solo un nome di fantasia per un progetto su GitHub. GitHub è un luogo online in cui puoi gestire progetti, archiviare file e collaborare apertamente con altri. Tutto ciò è ottenuto utilizzando il controllo della versione per tenere traccia dei progetti man mano che progrediscono. In quanto tale, GitHub è un potente strumento per progetti software e non software.

Una delle cose più importanti da considerare in questa fase iniziale è pensare a come si desidera che la comunità più ampia interagisca con il proprio progetto. Mentre lavori all'aperto, devi assicurarti che gli altri si sentano a loro agio nell'accedere, visualizzare e interagire con il tuo lavoro. Creare un repository in modo da ridurre le barriere all'ingresso e il timore di essere un "outsider" è il primo passo verso il mantenimento di un progetto di successo.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/octocat.png?raw=true" width="150px" height="125px"/>
</p>

<p align="center"><i>Octocat, la piccola mascotte di GitHub</i></p>

  


### Impostazione di un profilo GitHub <a name="Profile"></a>

Per impostare un profilo GitHub, vai semplicemente alla pagina principale e fai clic su [Registrati per GitHub](https://github.com/join). Qui puoi creare il tuo account personale, con nome utente, e-mail e password come standard.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/github_signup.png?raw=true" width="800" /></p>

<p align="center"><i>Iscriviti a GitHub</i></p>

  


Il prossimo passo è impostare un piano personale. Per ora, seleziona semplicemente il piano "Repository pubblici illimitati gratuitamente", a meno che tu non sia preoccupato per la privacy, nel qual caso seleziona il piano privato. Se si intende creare un progetto per un'organizzazione, è possibile selezionare anche questa opzione.

  


### Il linguaggio GitHub <a name="Language"></a>

Questo è probabilmente l'aspetto più confuso e scoraggiante di GitHub. Ecco alcuni dei termini più utilizzati e le loro definizioni:

* **Inizializzazione**: creare un repository vuoto.
* **Checkout**: crea una copia funzionante di un repository locale.
* **Clone**: copia il repository in una directory locale sul tuo computer.
* **Fork**: crea una derivazione personale di un repository per lavorarci in parallelo.
* **Branch**: una versione indipendente e parallela di un repository. Le modifiche non influiscono sul ramo principale.
* **Master**: il ramo principale e predefinito per un repository.
* **Pulisci**: nessun commit in sospeso sul ramo.
* **Fase**: aggiungere gli aggiornamenti pronti per essere assegnati a un ramo.
* **Commit**: una revisione di un repository, come una funzione "salva" con versione.
* **Commit message**: una descrizione delle modifiche che accompagnano un commit.
* **Verifica**: un controllo di stato.
* **Visualizza**: niente a che fare con i cani. Si riferisce a ottenere le ultime modifiche da un repository online senza unirle.
* **Indice**: "albero" che funge da area di sosta.
* **Directory di lavoro**: La 'struttura' in cui sono conservati i file.
* **Capo**: "albero" che indica l'ultimo commit effettuato.
* **Premere**: aggiungere le modifiche apportate alla testa del proprio repository remoto.
* **Unisci**: Combina le modifiche apportate in un ramo con il ramo principale al completamento.
* **Tirare**: aggiornare il repository recuperando e unendo i nuovi commit.
* **Pull request**: Una richiesta per unire un ramo aggiornato nel ramo master.
* **Problema**: miglioramenti, attività o domande suggeriti relativi a un repository.

Meno male! Non preoccuparti di memorizzare *tutti* di questi per ora. Come ogni nuova abilità, la familiarità arriva con l'esperienza.

Probabilmente puoi vedere come alcuni di questi sono abbastanza simili a cose come salvare, copiare, incollare - operazioni standard del flusso di lavoro, ma adattati per un processo di gestione del software. Ci sono anche [altri](https://mirrors.edge.kernel.org/pub/software/scm/git/docs/gitglossary.html) , ma questo dovrebbe essere fatto per iniziare.

Se sei interessato, la maggior parte di questi termini proviene dal sistema [Git sottostante](https://git-scm.com). Git è stato creato per consentire agli sviluppatori di gestire diverse versioni del codice sorgente in modo distribuito, il che è ottimo. Ha un sacco di caratteristiche e la capacità di fare un sacco di roba complessa, scritto da un [ragazzo molto intelligente](https://www.linuxfoundation.org/blog/2015/04/10-years-of-git-an-interview-with-git-creator-linus-torvalds/). Tuttavia, l'interfaccia utente [non è stata progettata pensando ai nuovi utenti](https://xkcd.com/1597/), quindi può essere difficile da imparare.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/git.png?raw=true" width="150px"/>
</p>

<p align="center"><i>Guida imbattibile per l'utilizzo di Git. (Fonte: XKCD)</i></p>

  


### Creare un nuovo repository <a name="Create_new"></a>

Sul tuo profilo GitHub, fai clic su "Crea nuovo repository". Il primo passo è creare un nome come marchio per il tuo progetto. Idealmente, dovrebbe essere memorabile e dare qualche indicazione su ciò che fa il progetto.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/new_repo.png?raw=true" width="800" /></p>

<p align="center"><i>Crea un nuovo repository</i></p>

  


Assicurati di non duplicare nomi, violare altri marchi o nominarli qualsiasi cosa che possa essere considerata offensiva.

  


## I passaggi fondamentali <a name="Foundation"></a>

Qualsiasi repository GitHub richiede 4 elementi chiave per iniziare e iniziare a sviluppare una community di benvenuto:

1. Una licenza Open Source;
2. Un file `README`;
3. Linee guida che contribuiscono; e
4. Un codice di condotta.

Questi sono aspetti critici e le migliori pratiche di qualsiasi progetto per gli utenti per comprendere i loro diritti legali, le loro aspettative, lo scopo del progetto e per migliorare l'esperienza utente complessiva.

Tutti e quattro questi file devono essere conservati nella directory principale del repository del progetto. È convenzione utilizzare i formati di file markdown (`.md`) per la maggior parte di questi file (sebbene il file di licenza sia più spesso di testo semplice (`.txt`)) e in maiuscolo tutti i nomi di file. Invece di spazi nei nomi di file, assicurati di utilizzare i caratteri di sottolineatura `_`.

Quindi dovresti finire con una selezione di file fondamentale come questa:

1. `LICENSE.md`
2. `README.md`
3. `CONTRIBUTING.md`
4. `CODE_OF_CONDUCT.md`

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/foundation.png?raw=true" width="800" /></p>

<p align="center"><i>La struttura di repository di base</i></p>

  


### Scegliere una licenza <a name="License"></a>

La scelta di una licenza appropriata è ciò che differenzia il tuo repository Open Source dal software disponibile pubblicamente. Mentre non sei obbligato a scegliere una licenza, così facendo garantisci che gli altri saranno in grado di modificare, condividere, riutilizzare e sviluppare il tuo progetto all'interno di un quadro legale.

Per iniziare, seleziona [Scegli una licenza](https://choosealicense.com/) per trovare una licenza che meglio si adatta alle tue intenzioni per il repository.

I tre principali tra cui scegliere sono:

* **Licenza MIT**: Una licenza permissiva che consente alle persone di fare tutto ciò che vogliono con il tuo codice purché forniscano un'attribuzione appropriata a te e non ti ritengano responsabile.
* **Licenza Apache 2.0**: autorizzazioni simili alla licenza MIT, ma fornisce anche una concessione esplicita di diritti di brevetto da parte di contributori agli utenti.
* **GNU General Public License (GPL) v3**: una licenza [copyleft](https://en.wikipedia.org/wiki/Copyleft) che richiede a chiunque ridistribuisca il tuo codice, o un'opera derivata, per rendere la fonte disponibile agli stessi termini della licenza originale; fornisce anche una concessione esplicita di diritti di brevetto da parte dei contributori agli utenti.

Per fortuna, quando avvii un nuovo repository su GitHub, ti viene data la possibilità di selezionare una licenza esistente da un menu a discesa. Si dovrebbe sempre (con pochissime eccezioni) utilizzare una licenza esistente, poiché questo è ciò che i potenziali utenti e contributori vedranno prima di scegliere di utilizzare o contribuire al proprio software.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/license.png?raw=true" width="800" /></p>

<p align="center"><i>Scegliere una licenza di esempio</i></p>

  


Se non ne hanno uno desiderato, puoi aggiungerne uno che ti piace manualmente. Per fare ciò, fai semplicemente clic su "Crea nuovo file" nel repository e copia e incolla il testo di una licenza esistente in. Assegna un nome al file come `LICENSE.txt` o `LICENSE.md` per renderlo chiaro e mantienilo nella cartella del repository principale (cioè la radice). Assicurati di aggiungere un messaggio di commit pulito, e il gioco è fatto!

> **Helping hand**: questo MOOC utilizza una diversa combinazione di licenze per il contenuto del codice e il contenuto non di codice. Qui puoi trovare un esempio della licenza</a> MIT che applichiamo per tutto il codice e il software generato come parte della produzione MOOC.</p> </blockquote> 
> 
>   
> 
> 
> ### Creare un file README <a name="Readme"></a>
> 
> Quando si inizializza il nuovo repository, dovrebbe esserci un'opzione per farlo con un file `README`. Proprio come Alice nel paese delle meraviglie, fanno esattamente quello che dicono - forniscono informazioni chiave sul progetto. Questi sono in genere la prima cosa che i collaboratori esterni vedranno al loro arrivo nel repository, quindi renderli informativi e accoglienti è la chiave.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/readme.png?raw=true" width="800" /></p>

<p align="center"><i>Parte del file README per questo modulo</i></p>

> 
>   
> 
> 
> Il file sarà originariamente in formato markdown (`.md`). Questo è un linguaggio di marcatura leggero con un formato di testo normale. Per imparare alcuni markdown di base, vedi [questo cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet). Ma per ora, possiamo semplicemente usare il testo normale.
> 
> Ci sono molte cose che vorrete includere nel vostro file `README`:
> 
> * Di cosa tratta questo progetto e cosa fa.
> * Perché le persone dovrebbero preoccuparsi e perché è utile.
> * Come può qualcuno iniziare a contribuire al progetto.
> * Chi può essere contattato nel caso qualcuno abbia bisogno di aiuto.
> * Un link alla licenza, linee guida di contribuzione e codice di condotta.
> * Una descrizione della struttura del progetto.
> * Chi è coinvolto e quali sono i loro ruoli.
> * Lo stato attuale del progetto.
> 
> > **Pro-tip**: Più avanti man mano che il progetto si sviluppa, potresti aggiungere domande frequenti basate sul feedback della community o un tutorial per aiutare gli utenti a capire come funziona il tuo progetto.
> 
> Ricorda che non tutti quelli che vengono al tuo progetto saranno degli esperti, o capiranno cosa stai facendo e perché. Avere un file `README` ben documentato migliorerà l'esperienza dell'utente per le persone con una gamma di conoscenze pregresse.
> 
> Quando il file `README` è incluso nella directory root, GitHub lo visualizzerà automaticamente nella home page del tuo repository. Questo significa che è la prima cosa che le persone vedono spesso, quindi fallo contare!
> 
> > **Helping hand**: Qui puoi trovare il `file README` usato per questo modulo [MOOC](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/README.md). Ciò include informazioni sullo stato, le motivazioni, i risultati dell'apprendimento, il team di sviluppo, i documenti chiave e la licenza per aiutare. Puoi copiare e adattare questa struttura per i tuoi progetti, se necessario.
> 
>   
> 
> 
> ### Creare linee guida di contribuzione <a name="Contributing"></a>
> 
> Le linee guida di contribuzione sono progettate per comunicare ai potenziali contributori una breve guida su come interagire con il progetto e la comunità. Vuoi essere sicuro di essere accogliente e indicare che sei desideroso di coinvolgere i partecipanti con il tuo progetto. Ogni volta che un partecipante apre una nuova richiesta di pull o crea un nuovo problema, vedrà un link al tuo file di contribuzione.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/contributing.png?raw=true" width="800" /></p>

<p align="center"><i>Parte delle linee guida `CONTRIBUTING` per questo modulo</i></p>

> 
>   
> 
> 
> Seguendo i nomi dei file tutto maiuscolo, il passo successivo è creare un file `CONTRIBUTING`. Fai clic su "Crea nuovo file" e assicurati di salvarlo nel formato di markdown come prima. Questo file dirà agli altri utenti come possono interagire e partecipare al tuo progetto. Questo è il primo passo verso la creazione di una comunità attorno al tuo progetto, quindi rendilo accattivante, conciso e informativo.
> 
> Il file `CONTRIBUTING` dovrebbe includere informazioni su:
> 
> * Che tipo di contributi stai cercando.
> * Come suggerire aggiornamenti o nuove funzionalità.
> * Come interagire con il progetto usando le funzioni di GitHub (es. Il protocollo di richiesta di pull).
> * Come presentare una segnalazione di bug o creare un problema.
> * L'obiettivo finale, la visione o la roadmap per il progetto.
> * Come contattare i responsabili del progetto.
> * Collegamenti a qualsiasi documentazione o sito Web esterno.
> 
> > **Pro-suggerimento**: prendi in considerazione di iniziare con una breve nota di ringraziamento per le persone che hanno il tempo di prendere in considerazione di contribuire - hanno fatto clic sul file per saperne di più! Se ci sono altri metodi di riconoscimento che hai in mente, assicurati di includerli anche qui.
> 
> Qui, in sostanza, stai cercando di incoraggiare le persone a offrirsi volontariamente per far progredire il tuo progetto. Assicurati di essere accogliente e amichevole, e sii preciso su come le persone possono impegnarsi. Durante la scrittura di questo, assicurati di pensarci dal punto di vista dell'utente: come puoi semplificarti la vita quando invii richieste di pull e apri i problemi per rendere l'intero progetto più fluido.
> 
> > **Helping hand**: Le [linee guida di contribuzione](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CONTRIBUTING.md) per questo modulo MOOC includono alcune cose molto specifiche: un'introduzione all'utilizzo di Git e GitHub, suggerimenti per iniziare, informazioni di contatto, come modificare il contenuto e problemi di repor, un collegamento ai `File README` e informazioni sul contenuto e sugli stili di codice preferiti. Sentiti libero di copiare e adattare questo per il tuo progetto, se necessario.
> 
>   
> 
> 
> ### Creare un codice di condotta <a name="Conduct"></a>
> 
> Un codice di condotta è importante per stabilire le regole di base per il comportamento previsto e la partecipazione per i contributori del progetto ed è un documento facilmente referenziato per dimostrare che il team del progetto prende sul serio i dialoghi costruttivi. Pertanto, è un elemento critico per creare e mantenere una comunità sana che si impegna in modo costruttivo e produttivo all'interno di un'atmosfera sociale positiva.
> 
> Un codice di condotta non solo fornisce aspettative di comportamento, ma descrive anche a chi si applicano tali aspettative, quando si applicano, che cosa fare nel caso in cui si verifichi una violazione del codice e quali saranno le azioni da intraprendere. Come tale, i punti di contatto devono essere chiariti nel codice di condotta. In genere, questo dovrebbe essere in un modo privato come un indirizzo email.
> 
> > **Suggerimento**: se è necessario segnalare una violazione alla persona che riceve tali rapporti, assicurarsi di includere un'opzione per contattare una parte secondaria.
> 
> Per aggiungere un codice di condotta, puoi creare il tuo da zero aggiungendo un nuovo file di markdown o utilizzare modelli esistenti come il [Contributor Covenant](https://contributor-covenant.org/). Assegna un nome al tuo file `CODE_OF_CONDUCT.md`e assicurati che sia visibile nel `file README`.
> 
> > **Helping hand**: Questo MOOC ha anche un [Code of Conduct](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CODE_OF_CONDUCT.md) basato sul Covenant del Collaboratore. Come puoi vedere, include informazioni sugli standard di comportamento previsti, le responsabilità di coloro che vivono nella comunità e l'applicazione del CoC, compresi i dettagli di contatto. Sentiti libero di riutilizzare e adattare questo al tuo progetto come meglio credi.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/code_of_conduct.png?raw=true" width="800" /></p>

<p align="center"><i>Parte del file CODICE DI CONDOTTA per questo modulo, basato sul Patto del Collaboratore</i></p>

> 
>   
> 
> 
> Assicurarsi di applicare il codice di condotta è importante, poiché dimostra che non solo apprezzi il codice, ma rispetti l'influenza che ha sulla tua comunità. È importante trattare ogni membro della comunità con il rispetto, la cortesia e l'importanza che meritano. Se si verifica una violazione o se un recidivo compie violazioni costanti, è meglio fare riferimento alla [Guida all'Open Source](https://opensource.guide/code-of-conduct/#enforcing-your-code-of-conduct) per vedere come applicare il codice di condotta.
> 
>   
> 
> 
> ### Rendi il tuo codice leggibile <a name="Citation"></a>
> 
> Se si vuole rendere il codice citabile fin dall'inizio, è necessario memorizzare i metadati necessari per una citazione fin dall'inizio, con la creazione di un `[codemeta.json](https://codemeta.github.io)` file o un `[CITATION.cff](https: //citation-file-format.github.io)` file. Entrambe permetteranno agli strumenti attualmente in fase di sviluppo di creare automaticamente le informazioni sulle citazioni, piuttosto che chiedervi di digitarle in un modulo successivo.
> 
> Se sei interessato, [cite.research-software.org](https://cite.research-software.org) fornisce ulteriori informazioni di base sulla citazione del software nel mondo accademico.
> 
>   
> 
> 
> ## Mantenere aggiornati i tuoi problemi <a name="Issues"></a>
> 
> I problemi non sono necessariamente problemi con un progetto, ma anche suggerimenti per il miglioramento, cose da sviluppare in futuro, commenti e feedback sul progetto da elaborare. Possono essere condivisi apertamente e discussi con i contributori secondo necessità, un po 'come un forum.
> 
> Se sei un lead di progetto, è importante mantenere un elenco di problemi che chiariscono ai contributori quali aspetti del progetto richiedono attenzione. È anche importante impegnarsi con il maggior numero possibile di problemi dagli altri in modo positivo, per dimostrare che prendi sul serio i loro contributi.
> 
> Gli elementi chiave per le questioni includono:
> 
> * Un titolo informativo e una descrizione;
> * Etichette / tag con codifica a colori per aiutare a categorizzare e filtrare;
> * Pietre miliari per associare questioni con caratteristiche specifiche o fasi del progetto;
> * Gli assegnatari indicano chi è responsabile di lavorare su un problema;
> * Commenti per fornire feedback.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/issues.png?raw=true" width="800" /></p>

<p align="center"><i>Il tracker dei problemi per il progetto Open Scholarship Strategy</i></p>

> 
>   
> 
> 
> All'interno dei problemi è possibile utilizzare le @ menzioni per notificare ad altri contitolari il problema e ottenere le persone giuste impegnate in modo efficace. GitHub ha un sistema interno di notifiche, proprio come Facebook o Twitter, e può anche inviare e-mail alle persone citate nel tracker dei problemi. Questo può essere personalizzato per le persone all'interno delle impostazioni dell'utente.
> 
>   
> 
> 
> ## Lista di controllo per l'avvio del tuo progetto <a name="Checklist"></a>
> 
> Quindi ora sei pronto per lanciare il tuo progetto, iniziare a pubblicizzarlo e ottenere contributi! Prima di continuare, assicurati di avere:
> 
> * [] Il progetto ha un nome memorabile e informativo
> * [] Project ha un file `LICENSE` che è una copia esatta di una licenza Open Source
> * [] Documentazione completa che include `README`, `CONTRIBUTING`e `CODE_OF_CONDUCT`
> * [] Il progetto ha almeno un problema chiaramente etichettato
> * [] Qualsiasi codice incluso in questa fase è chiaramente strutturato e annotato
> 
> **CONGRATULAZIONI!**
> 
> Ora hai lanciato un progetto di ricerca Open Source! Speriamo che, da qui in poi, il tuo lavoro agirà a beneficio della comunità più ampia, creerà nuove collaborazioni e creerà nuove e fantastiche opportunità per tutti voi. Prova a pensare ai modi in cui queste abilità possono essere applicate ai progetti futuri, e come potrebbero averle aiutato in passato.
> 
> D'ora in poi, dipende da te! Alcuni consigli sono:
> 
> * Scrivi codice pulito;
> * Avere un progetto ben strutturato;
> * Commetti frequenti con messaggi puliti;
> * Mantenere i progetti ben documentati;
> * Avere chiare linee guida contribuenti;
> * Sfrutta la descrizione e le funzioni di tag;
> * Non biforcare il repository di qualcun altro a meno che non si intenda lavorare su di essi;
> * Assicurati di contribuire anche ai progetti di altre persone.
> 
> **Sapere in che modo questo contenuto può essere migliorato?**
> 
> È tempo di prendere le tue nuove abilità GitHub per un test-run! Tutto lo sviluppo del contenuto avviene principalmente qui [qui](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md). Se hai un miglioramento suggerito per il contenuto, il layout o qualsiasi altra cosa, puoi realizzarlo e poi diventerà automaticamente parte del contenuto di MOOC dopo la verifica da parte di un moderatore!
> 
> [![Dedicato pubblico dominio CC0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)