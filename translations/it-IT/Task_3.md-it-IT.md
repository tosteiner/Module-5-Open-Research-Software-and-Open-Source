---
output:
  html_document: predefinito
  pdf_document: predefinito
---

# Attività 3: Come integrare Git con R Studio

Questo compito è progettato per studenti e ricercatori che desiderano implementare un sistema di controllo della versione all'interno di un flusso di lavoro basato su R standard. Questo può essere applicato a una serie di attività di sviluppo software, analisi dei dati e gestione dei progetti. Il tuo io di ricerca futuro ti ringrazierà per la convenienza.

Non dimenticare che puoi partecipare alle discussioni sul nostro open [**Slack channel**](https://osmooc.herokuapp.com/). Per favore, presentati a # module5opensource e raccontaci un po 'di chi sei, del tuo background e di come sei finito qui!

Tempo stimato per il completamento: 30 minuti

Stimare il risparmio di tempo una volta completato: virtualmente infinito

**NOTA** Una versione di guida video di questa attività è ora disponibile su [YouTube](https://www.youtube.com/watch?v=Q-6jfjSAspA).

## Sommario

* [Iniziare](#Getting_started) 
  * [Idiota](#Git)
  * [Studio R](#Rstudio)
* [Fase uno: scarica tutte le cose](#one)
* [Passo 2: Configura Git all'interno di RStudio](#two)
* [Fase tre: Perché l'ho fatto?](#three)
* [Fase quattro: il matrimonio perfetto tra Git e R](#four)
* [Fase 5: ottenere contenuti con contenuti](#five)
* [Passo sei: un impegno coraggioso](#six)
* [Punto sette: PREMERE!](#seven)

## Iniziare <a name="Getting_started"></a>

Congratulazioni per averlo fatto così lontano! Se stai leggendo questo, sei sopravvissuto alle richieste di pull, ai web-hook e probabilmente puoi anche dirci cosa è la F in FOSS (*non* Frustration ...) Spero che tu abbia superato qualsiasi scetticismo o riluttanza verso i benefici di GitHub e del software Open Source e sono pronti a fare il passo successivo.

Prima di iniziare questa attività, assicurati di aver già completato [Attività 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) e [Attività 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), in modo da avere più familiarità con GitHub e alcune pratiche standard Open Source.

Questo task ti insegnerà come integrare il software di controllo della versione, Git, con il popolare ambiente di codifica, RStudio. E sì, è Git come in gif o Dio, non Jit come nel modo sbagliato di pronunciare le cose.

Se sei uno di quei ricercatori che pensano che il codice si diffonda su più dischi rigidi in attesa di interruzione, Dropbox, Google Drive o qualsiasi altro software non specialistico, questo compito è solo per te. Se hai mai sperimentato il processo di intorpidimento di avere più versioni "finali" di una carta che rimbalza tra diversi co-autori, questo è anche per te.

Tutti noi siamo colpevoli di questo genere di cose una volta ogni tanto, ma ci sono modi per farlo che sono migliori per te, per te e per quelli che potrebbero trarre beneficio dal tuo lavoro.

  


### Ottenere Git <a name="Git"></a>

Allora, cos'è Git, e in che modo è diverso da GitHub? Git è un sistema di controllo della versione, che consente di salvare e tracciare copie con timbratura del proprio lavoro durante il processo di sviluppo. Funziona anche con elementi non di codice, come questo MOOC, la maggior parte dei quali è stata scritta in markdown in RStudio e integrata con un flusso di lavoro Git / GitHub.

Questo è importante, poiché tutte le ricerche passano attraverso i cambiamenti ea volte vogliamo sapere quali fossero queste cose. Hai eliminato del testo che ora ritieni sia importante? Il controllo della versione lo salverà per te. Il tuo codice ha funzionato perfettamente nel passato, ma ora è bacato oltre ogni immaginazione? Controllo della versione È un ottimo modo per evitare lo stato caotico in cui si hanno più copie dello stesso file, ma senza una convenzione di denominazione dei file stupida e fastidiosa. `FINAL_Revised_2.2_supervisor_edits_ver1.7_scream.txt` sarà una cosa del passato.

GitHub è la piattaforma che ti consente di condividere facilmente il codice dal tuo spazio di lavoro (ad es. Laptop) per essere ospitato in uno spazio online. Quindi, è come l'interfaccia pubblica di GitHub. I vantaggi di Git / GitHub sono:

1. Puoi tenere copie di tutto il tuo lavoro nel tempo;
2. Puoi confrontare il lavoro attraverso diverse copie nel tempo, il che aiuta a individuare bug o errori;
3. Altre persone possono collaborare apertamente con il tuo lavoro;
4. Disponi di una copia locale e online del tuo lavoro che rimane sincronizzata;
5. È completamente trasparente su chi ha dato un contributo, perché lo hanno fatto e quando; e
6. Puoi avere più persone che lavorano sullo stesso progetto contemporaneamente in parallelo.

Anche se questo è stato progettato principalmente per il codice sorgente, dovrebbe essere immediatamente ovvio come questo diventa un potente strumento per praticamente tutti i flussi di lavoro di ricerca.

  


### RStudio <a name="Rstudio"></a>

RStudio è un popolare ambiente di codifica per i ricercatori che usano il linguaggio di programmazione statistica, R. Viene fornito con un editor di testo, quindi non è necessario installarne un altro e passare da uno all'altro. Include anche un'interfaccia utente grafica (GUI) per Git e GitHub, che utilizzeremo qui.

Non è bello quando i brillanti strumenti Open Source si integrano perfettamente in questo modo. Questo dovrebbe aiutare a rendere il tuo uso quotidiano di Git molto più semplice.

Se in qualsiasi momento è necessario installare nuovi pacchetti per R, è sufficiente utilizzare il seguente comando:

`install.packages ("PACKAGE NAME", dipendencies = TRUE)`

Sostituire `PACKAGE NAME` con il, er, nome del pacchetto. Alcuni esempi con cui puoi giocare sono utili come `knitr`, `devtools` o `ggplot2`.

  


## Fase uno: scarica tutte le cose <a name="one"></a>

1. Dovresti già avere un account GitHub se hai seguito le attività precedenti. Altrimenti, [iscriviti qui](https://github.com/). Repository illimitati gratuiti per tutti!
2. Scarica e installa l'ultima versione di [R](https://www.r-project.org/). Disponibile anche per [Mac](https://cloud.r-project.org/) e [Linux](https://cloud.r-project.org/bin/linux/).
3. Scarica e installa l'ultima versione di [Rstudio](https://www.rstudio.com/products/rstudio/#Desktop). Oh, hey, sembra Open Source! Swish.
4. Scarica e installa l'ultima versione di [Git](https://gitforwindows.org/). **Assicurati di selezionare "Usa Git dal prompt dei comandi di Windows" durante l'installazione.**

> **Pro-tip**: per aggiornare tutti i pacchetti R in uno, è sufficiente eseguire il seguente codice `update.packages (ask = FALSE, checkBuilt = TRUE)`

Per ora, basta scegliere tutte le solite opzioni predefinite per ogni installazione. A seconda del sistema operativo (ad esempio, Mac, Windows, Linux), questo potrebbe essere diverso per ognuno di voi. Per ora, e per il resto di questo compito, continueremo a fare le cose con semplicità in Windows (ma forniamo anche alcune istruzioni per usare la riga di comando).

Per utenti Linux o Debian, usa semplicemente il seguente comando per installare Git:

`sudo apt-get install git-core`

Per utenti Mac, [questo collegamento](http://git-scm.com/download/mac)o acquistare un nuovo laptop con un sistema operativo diverso.

Se lo desideri, puoi anche scaricare la versione locale [di GitHub](https://desktop.github.com/) e utilizzarla attraverso la semplice interfaccia grafica. È disponibile su Windows, Mac e Linux e può semplificarti la vita, soprattutto se desideri utilizzare una piattaforma diversa per RStudio.

> **Suggerimento:** Si vede quando si installa Git che dice 'Usa Git Bash come shell per i progetti Git?' Questo è il posto dove puoi usare la riga di comando per accedere a Git da RStudio. È una bestia potente. Prova i seguenti due comandi per iniziare:

`git config --global user.name 'YOUR USERNAME'`   
`git config --global user.email 'YOUR EMAIL'`   


## Passo 2: Configura Git all'interno di RStudio <a name="two"></a>

Giusto, questo è un po 'facile. Successivamente, vai in RStudio, e nelle schede in alto vai su Vai a **Strumenti> Opzioni globali> Git / SVN**. SVN è solo un altro sistema di controllo della versione come Git, e non dobbiamo preoccuparci di questo qui.

Nel punto in cui è indicato *Git eseguibile*, aggiungere il percorso qui al file git.exe appena scaricato nel passaggio precedente. Assicurati che la casella qui che dice **Abilita l'interfaccia di controllo della versione per i progetti RStudio** sia selezionata. Questo ha ora legato il controllo della versione ai progetti futuri in RStudio, per fornire una dimensione aggiuntiva davvero potente al lavoro collaborativo o da solista.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/git_svn.png?raw=true" width="400px"/>
</p>

<p align="center"><i>La finestra delle opzioni globali all'interno di RStudio</i></p>

  


Successivamente, premi il pulsante in questa finestra che dice *Crea RSA Key*, Questa è una chiave privata che viene utilizzata per l'autenticazione tra diversi sistemi e ti evita di dover digitare la tua password più e più volte. Qui, si aprirà una nuova finestra con una chiave pubblica, che si desidera copiare negli Appunti.

Vai su GitHub, vai alle impostazioni del tuo profilo e la scheda *SSH e GPG*. Fare clic su *Nuovo tasto SSH*. Qui, incolla la chiave da RStudio e chiamala qualcosa di fantasioso come "RStudio".

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/ssh_key.png?raw=true" width="800px"/>
</p>

<p align="center"><i>All'interno di GitHub dove vuoi inserire la chiave che hai appena generato in RStudio</i></p>

  


OK, ora tieni le tue cicche, stiamo andando nella riga di comando. Non preoccuparti se non hai mai usato la shell prima perché è abbastanza simile all'utilizzo di R o di qualsiasi altro sistema di codifica. La differenza principale qui è che invece di chiamare funzioni come in R, si chiamano comandi.

Quindi, tornando in RStudio, vai su **Strumenti> Shell**, e si aprirà una finestra del prompt dei comandi. Se hai già giocato con Git Bash sopra, avresti dovuto fare già questo passo. Inserisci i seguenti due comandi:

`git config --global user.name 'YOUR USERNAME'`   
`git config --global user.email 'YOUR EMAIL'`   


Speriamo che non sia necessario sostituirlo con il tuo nome utente GitHub ed e-mail qui. Puoi accedervi in qualsiasi momento trovando la 'Shell' in Windows. Oppure, se si fa clic con il pulsante destro del mouse su una qualsiasi cartella sul desktop collegata a un repository GitHub, è possibile aprire immediatamente Shell e Bash away.

Ciò che questa fase ha fatto è configurare Git, che è un software che gira sul desktop, a GitHub, che è un sito web di repository.

Riavvia R Studio. Wow, è stato difficile. Il prossimo.

  


## Fase tre: Perché l'ho fatto? <a name="three"></a>

OK, tieni il fiato, ci fermeremo qui solo per imparare alcuni comandi Git di base. Alcuni di quelli che potresti fare con l'apprendimento sono:

* **Aggiungi**: qui è dove si inviano i file all'area di staging prima di essere impegnati.

* **Commit** È come "salvare" il tuo lavoro creando una nuova versione o copia.

* **Push**: questo è il modo in cui si inviano i file dal progetto locale al repository online.

* **Pull**: questo è il modo in cui ottieni i file dal tuo repository online al tuo progetto locale.

Tornando in RStudio, digita quanto segue nel *Terminal*o aprendo una nuova shell:

`aggiungi git.`

Non sarà in realtà fare nulla per ora, ma in futuro si aggiungerà tutti i file nella directory di lavoro corrente (che è ciò che il `.` fa) per mettere in scena pronto per un commit.

  


## Fase quattro: il matrimonio perfetto tra Git e R <a name="four"></a>

Ora, nell'Attività 1, dovresti aver imparato come costruire il tuo primo repository GitHub. Se non lo hai fatto, possiamo aspettare qui mentre tu vai e farlo. Se hai già o hai un repository GitHub esistente, possiamo andare avanti.

Quindi, dovresti avere un repository su GitHub, completo di un file `README` , un file `LICENSE` e alcuni altri bit e bob.

Quello che faremo ora è integrare quel repository con Git. Stabile ora.

1. In primo luogo, andare su **Progetto> Crea progetto> Controllo versione> Git**.
2. Tornando su GitHub, dovresti vedere un po 'dove c'è un https: // URL. Questo è il link al tuo repository e ti dà la possibilità di clonarlo sul desktop. Per ora basta copiare quel link, tornare a RStudio e incollarlo nell'URL del repository come indicato.
3. Assegna al progetto un nome di directory, ad esempio prova, Jim o qualsiasi altra cosa desideri.
4. Successivamente, cerca il posto sul desktop in cui desideri che questo progetto sia attivo, la sua sottodirectory.
5. Fai clic su "Crea progetto" e lascia che la magia sia fatta!

Quello che hai appena fatto è stato dire a RStudio di associare un nuovo progetto in R con repository specifico su GitHub.

## **Fase quattro: alternativa**

Se non hai ancora creato il tuo primo repository su GitHub, possiamo fare qualcosa di leggermente diverso qui. In RStudio, fare clic su *Nuovo progetto* e quindi *Nuovo elenco*. Chiamalo come desideri e modifica la directory secondo necessità, assicurati di selezionare *Crea un repository git*, quindi fai clic su *Crea progetto*. Questo crea un file `.Rproj` , che puoi gestire nel solito modo tramite RStudio, inclusa l'aggiunta di `README.md`e `LICENSE.md` come discusso nell'Attività 1.

## Fase 5: ottenere contenuti con contenuti <a name="five"></a>

Ricorda che il file `README` stato creato qualche tempo fa? Bene, è il momento di scriverlo. Ripensando al compito 1, c'erano alcune cose specifiche che abbiamo detto di fare un buon `file README`. Ti ricordi cosa erano tutti? Solo per rinfrescare la tua memoria, questi erano:

* Di cosa tratta questo progetto e cosa fa.
* Perché le persone dovrebbero preoccuparsi e perché è utile.
* Come può qualcuno iniziare a contribuire al progetto.
* Chi può essere contattato nel caso qualcuno abbia bisogno di aiuto.
* Un link alla licenza, linee guida di contribuzione e codice di condotta.
* Una descrizione della struttura del progetto.
* Chi è coinvolto e quali sono i loro ruoli.
* Lo stato attuale del progetto.

Quindi, in RStudio, apri quel file prova ad aggiungere solo un po 'di informazioni su questo per il tuo progetto. Se stai facendo questo per un progetto reale, prova a renderlo utile. Se stai solo armeggiando per ora, puoi aggiungere quello che vuoi.

Ricorda che il tuo `file README` è nel formato markdown (.md). Per un aggiornamento su alcuni degli usi di markdown della sintassi semplice, controlla questo [pratico cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/markdown.png?raw=true" width="600px"/>
</p>

<p align="center"><i>Screenshot di ciò che questo modulo appare in markdown, durante lo sviluppo. Meta.</i></p>

  


## Passo sei: un impegno coraggioso <a name="six"></a>

OK, quindi ora dovresti avere un file `README` ben modificato. Ora stiamo per "impegnarlo" nel progetto usando Git. Questo è sostanzialmente l'equivalente di salvare questa versione del tuo progetto, con una registrazione di quali modifiche sono state apportate. I commit successivi generano una cronologia che può essere esaminata in un secondo momento, consentendo di lavorare con sicurezza.

Ci sono alcuni modi per farlo.

1. Vai a **Strumenti> Controllo versione> Conferma**
2. Nel pannello di ambiente in RStudio, dovrebbe esserci una nuova scheda 'Git'. Maneggevole.
3. Nel pannello della console, ora dovrebbe esserci un nuovo 'Terminale', da cui è possibile eseguire le righe di comando Git.

Rimaniamo solo con la seconda opzione per ora. Questo pannello Git mostra quali file sono stati modificati e include pulsanti per i comandi Git più importanti che abbiamo visto in precedenza.

Seleziona il file `README` nella finestra di Git, che dovrebbe apparire automaticamente se hai apportato delle modifiche ad esso. Questo aggiunge il file all'area 'staging', che è un po 'come lo spazio di pre-salvataggio per il tuo lavoro. Fai clic su "Conferma" e dovrebbe apparire una nuova finestra.

Qui hai la possibilità di rivedere le tue modifiche e scrivere un bel messaggio di commit. Digitare qualcosa di breve, ma informativo sulle modifiche apportate in questa versione o istantanea del proprio lavoro. Vuoi che questo sia abbastanza informazioni in modo che se tu o qualcun altro lo guardi indietro, saprai perché hai fatto questo commit e le modifiche ad esso associate. Queste sono come reti di sicurezza per il tuo progetto nel caso in cui hai bisogno di cadere indietro per qualche motivo.

> **Pro-tip**: qui vedrai un elenco di tutte le modifiche apportate dall'ultimo commit. Le linee rimosse più vecchie sono in rosso e le righe aggiunte di recente sono in verde. Doppio controllo per assicurarti che le modifiche che hai apportato siano quelle che avevi intenzione di realizzare. Questo è veramente utile per individuare errori di battitura, modifiche vaganti e qualsiasi altro piccolo errore che potresti aver introdotto per sbaglio. La sicurezza prima.

**Nota** Se sei daltonico e non riesci a vedere quali linee sono state aggiunte o rimosse, puoi usare come guida i numeri di riga nelle due colonne sulla sinistra della finestra. Qui, il numero nella prima colonna identifica la versione precedente e il numero nella seconda colonna identifica la nuova versione.

Ora quando fai clic su "Conferma", verrà visualizzata un'altra finestra che ti indicherà quanti file sono stati modificati e il numero di righe all'interno di quel file che hai modificato. Chiudi quella piccola finestra in basso.

  


## Punto sette: PREMERE! <a name="seven"></a>

Fai clic sul pulsante *Premi* nella parte in alto a destra della nuova finestra. Una nuova finestra si aprirà ora. Ciò che sta facendo è sincronizzare i file modificati sul repository locale con il file `README` nella versione online del progetto su GitHub.

Per fare ciò da Shell, utilizzare il seguente comando:

`git push -u origine master`

Alcune volte qui ti verrà richiesto di aggiungere nome utente e password da GitHub, che dovresti fare se richiesto.

Chiudi quella finestra in basso e quella successiva. Vai al tuo progetto su GitHub, aggiorna e controlla che il file `README` sia ancora lì in tutta la sua gloria appena modificata. Dovresti vedere anche il messaggio di commit che hai fatto accanto al file.

  


**PASSAGGIO AVANZATO AVANZATO / IMPRESSIONANTE**

Bene, quindi hai semplicemente spinto alcuni contenuti al tuo primo repo, fantastico! Ora mettiamola in pratica per un vero progetto. Come, a quello a cui stai partecipando in questo momento. Proviamo questo:

1. Vai al repository per questo progetto su [GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source)

2. Porta il repository al tuo account GitHub. L'URL per questo dovrebbe essere: `https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source.git`

3. Andare in RStudio, andare su **File> Nuovo progetto**, selezionare *Version Control*, selezionare *Git*e quindi incollare l'URL del repository biforcato trovato nella copia del repository. Ora hai la tua copia con versione di questo intero modulo. Neat. Salvalo da qualche parte sul tuo computer locale.

4. Ora, devi dire a Git che esiste una versione diversa di questo progetto. Apri la *Shell*e inserisci il comando: `git remote add upstream https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source`

5. Quello che hai appena fatto è stato il nome del ramo originale qui `upstream`, solo per mantenere le cose semplici per ora. Ora crea un nuovo **ramo** per documentare le tue modifiche a questo indipendente dal ramo principale. Immettere il comando: `git checkout -b proposed-changes master`

6. Hai appena creato un nuovo ramo chiamato `proposte-modifiche` dove ora puoi modificare tutto il contenuto e i file per la gioia del tuo cuore. Si spera che la struttura di questo progetto sia abbastanza semplice da permetterti di navigare. Tutti i file raw per il MOOC possono essere trovati nella cartella `content_development` , e questo è `Task_3.md`.

7. Se scorri fino alla fine di `Task_3.md`, dovresti vedere un luogo in cui puoi modificare il tuo nome e la tua affiliazione. Aggiungi questi in, e poi passa attraverso la procedura di commit sopra descritta. Se vedi qualcos'altro che richiede anche la modifica, sentiti libero di aggiungerli anche tu!

8. Ora, vuoi riportare le modifiche al ramo originale. Usa il seguente comando nel tuo *Shell*: `origine push git proposte-modifiche`

9. Torna a GitHub e trova la tua forchetta qui. Fai clic sul piccolo pulsante verde e crea una richiesta di pull. Questa è essenzialmente una recensione per integrare le modifiche apportate al ramo originale per questo progetto MOOC.

10.     I proprietari responsabili del progetto MOOC riceveranno una notifica di questo, lo esamineranno e lo confermeranno se tutto è andato per piano! Lo esamineremo e, se tutto andrà bene, il tuo nome apparirà per l'eternità come qualcuno che ha completato questa attività avanzata.
      

11.     Fai una tazza di tè, caffè o vino per festeggiare!
      

**CONGRATULAZIONI**

Hai appena integrato Git con R Studio e hai apportato le tue prime modifiche a un progetto controllato in versione. La tua vita non sarà più la stessa e il tuo flusso di lavoro di ricerca sarà probabilmente più rapido, agile e collaborativo che mai. Buona fortuna per tornare a Word.

La cosa bella è che questo non deve essere usato solo per il codice. Puoi usarlo per testo semplice, markdown, html e, beh, codice R. Le possibilità sono infinite: ciò che hai appena imparato è una nuova forma di gestione del progetto apertamente collaborativa che funziona per una vasta gamma di compiti.

D'ora in poi, dipende da te! Alcuni consigli sono:

* Fai frequenti commit. Tratta Git come il tuo cucciolo, in quanto richiede un'attenzione costante e speciale. Basta una pacca sulla testa ogni tanto è sufficiente per mantenerlo soddisfatto, ma sarà più felice con una manutenzione costante.

* Il modo migliore per farlo è quello di fare un commit ogni volta che lavori su un problema specifico. Ad esempio, scrivere un paragrafo, eseguire un'analisi o correggere un bug.

* Spingi spesso. Non lasciare che quei commit si accumulino, altrimenti corri più rischi di entrare in conflitti di fusione. Visto che questi possono essere roba da incubi, assicurati di spingere spesso.

* Tirare spesso. Se altri stanno lavorando in remoto sullo stesso progetto, vorrai rimanere aggiornato con le loro modifiche. Assicurati di inserire frequentemente le loro modifiche da GitHub per assicurarti di essere tutti sincronizzati.

* Sperimenta ed esplora! Questo compito si limita a graffiare la superficie e ci sono molte funzioni, strumenti e modi in cui può essere usato. In realtà, spetta a te scoprire come utilizzare queste informazioni per migliorare il tuo flusso di lavoro di ricerca e, infine, collaborare per una ricerca migliore, più aperta e affidabile!

* Per ulteriori informazioni su problemi, rami, si fondono i conflitti, tirare le richieste, e altri aspetti avanzati di utilizzare Git e RStudio, check out questa [guida eccezionale](http://r-pkgs.had.co.nz/git.html) da Hadley Wickham.

  


**Sapere in che modo questo contenuto può essere migliorato?**

È tempo di prendere le tue nuove abilità GitHub per un test-run! Tutto lo sviluppo del contenuto avviene principalmente qui [qui](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md). Se hai un miglioramento suggerito per il contenuto, il layout o qualsiasi altra cosa, puoi realizzarlo e poi diventerà automaticamente parte del contenuto di MOOC dopo la verifica da parte di un moderatore!

## Elenco dei partecipanti che hanno completato la versione AVANZATA di questa attività

* Brendan Palmer, CRF-C, University College Cork
* Lisa Matthias, Freie Universität Berlin
* Hollie Marshall, Università di Leicester 
* Eric D. Wilkey, Western University, Canada
* José-Raúl Canay-Pazos, Universidade de Santiago de Compostela, Spagna
* Encarnación Martínez Álvarez, Spagna
* Alberto Albz Marocchino, Italia
* Iratxe Rubio, Centro basco per il cambiamento climatico BC3
* Gabriele Orlandi, Scuola di Studi Avanzati in Scienze Sociali di Parigi (EHESS), Francia
* Hande Sodaci, Turchia
* Luke W. Johnston, Università di Aarhus, Danimarca
* Philippe Joly, WZB e HU-Berlin
* Paul Griffiths, NCAS e U. Cambridge
* Harin Lee, Goldsmiths, Università di Londra
* Luis Camacho, Università Cattolica, Perù
* Tom Cridford, Imperial College London
* Nithiya Streethran, Università di Stavanger 

[![Dedicato pubblico dominio CC0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)