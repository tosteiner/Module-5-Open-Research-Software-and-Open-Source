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
- [La comunità Open Source, governance e contributi](#OS_Community)
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

Alcuni ritengono che il movimento OSS rappresenti un movimento controcorrente verso il neoliberismo e la privatizzazione, attraverso la sfida delle norme e dei regolamenti nella costruzione e il riutilizzo delle informazioni e una potenziale trasformazione del capitalismo moderno attraverso la messa a disposizione di software con il minimo sforzo. Vedi [Il movimento software libero / open source: resistenza o cambiamento?](http://www.redalyc.org/html/742/74212712006/) di Panayiota Georgopoulou per ulteriori informazioni su questo argomento.

  


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

Ci sono due campi principali all'interno della comunità del software libero: **movimento software libero**e **movimento OSS**. Entrambi hanno diverse ideologie basate sulle libertà dell'utente e le applicazioni pratiche del software. Spesso, il termine "FLOSS" viene utilizzato per riconciliare questi due campi politici e significa "Software libero / libero e open source"; Libre è francese e spagnolo per "libero" nel contesto della libertà.

Il principio fondamentale del riutilizzo è ciò che distingue l'OSS dal "Software Libero". Il software libero e open source (FOSS) è un termine inclusivo per descrivere software che può essere classificato sia come libero sia come open source. Un buon esempio di FOSS è il sistema operativo [Ubuntu Linux](https://www.ubuntu.com/).

La grande differenza tra il software libero e l'OSS è che il primo deve distribuire versioni aggiornate con la stessa licenza dell'originale, mentre le versioni più recenti di OSS possono essere distribuite con licenze diverse. FOSS combina il meglio di entrambi i mondi.

Queste definizioni sono ora ampiamente adottate, sia dai governi internazionali, sia da alcune grandi organizzazioni come la [Mozilla Foundation](https://www.mozilla.org/en-US/foundation/) e la [Wikimedia Foundation](https://wikimediafoundation.org/wiki/Home). Le principali organizzazioni nello spazio FLOSS includono il [Software Sustainability Institute del Regno Unito](https://www.software.ac.uk/), che produce risorse preziose come le recenti [Guida al deposito dei software per i ricercatori](https://softwaresaved.github.io/software-deposit-guidance/).

### Per singoli progetti

Un tipico progetto open source ha i seguenti tipi di ruoli formali:

- **Autore**: è la persona che ha creato il progetto
- **Proprietario**: la / le persona / i che detiene la proprietà amministrativa sull'organizzazione o sul deposito 
- **Maintainer**: Contributori che sono responsabili per guidare la visione e gestire gli aspetti organizzativi del progetto. (Possono anche essere autori o proprietari del progetto.)
- **Contributori**: l'utente che ha già contribuito al progetto.
- **Membri della comunità**: persone che usano il progetto. Potrebbero essere attivi nelle conversazioni, creare nuovi problemi o esprimere la loro opinione sui futuri miglioramenti del progetto.

In genere, i ruoli vengono resi pubblici tramite il file `README` , un file Contributors o una pagina team separata per il progetto.

  


## Piattaforme e strumenti esistenti per software Open Source <a name="Platforms"></a>

Gli ambienti virtuali e le macchine stanno diventando sempre più popolari come attivatori di flussi di lavoro di ricerca ad alta potenza e molti di questi sono basati su OSS (ad esempio, sistemi operativi, linguaggi di programmazione e framework di elaborazione dati). I servizi più popolari includono [Google Cloud](https://cloud.google.com/compute/) e [Amazon Web Services](https://aws.amazon.com/), che aiutano anche con l'archiviazione del database e la consegna dei contenuti, oltre alla potenza di calcolo. [InsideDNA](https://insidedna.me/) è una piattaforma di calcolo per la ricerca riproducibile in bioinformatica, genomica e scienze della vita.

Come accennato [precedenza](#What_OSS), LibreOffice offre un'alternativa open source a Microsoft Office. I due sono quasi completamente compatibili, solo con diversi formati di file predefiniti. Per i gestori di citazioni, [Zotero](https://www.zotero.org/) è l'alternativa Open Source più popolare a piattaforme proprietarie come Mendeley o EndNote.

[Zotero](https://www.zotero.org/) utilizza il formato BibTeX (pronunciato 'bib-tech'), basato su LaTeX (pronunciato 'lay-tech'), e ha plugin per browser per rendere semplice la gestione delle citazioni. Integrando questo con altri software come LibreOffice, è ora possibile avere un flusso di lavoro di ricerca completamente open source in molti casi.

### GitHub <a name="GitHub"></a>

> Lo sapevate che l'intero progetto è stato costruito come un tentativo comunità aperta e collaborativa in [GitHub](https://github.com/OpenScienceMOOC/)?

[GitHub](https://github.com/) è un popolare sito di hosting per i contenuti software e non software (spesso chiamati "notebook"), con funzionalità aggiuntive per il controllo delle versioni, la gestione e il monitoraggio dei progetti e i servizi di archiviazione. GitHub è basato su OSS [Git](https://git-scm.com/), che consente agli utenti di lavorare in remoto per mantenere, condividere e collaborare su software di ricerca e altri progetti non basati su software.

Il controllo della versione è essenzialmente un processo che prende istantanee dei file in un repository e ne tiene traccia. Registra quando sono state apportate le modifiche, cosa erano e chi le ha fatte. Se più persone lavorano su un file contemporaneamente, vengono rilevate eventuali modifiche sovrapposte e devono essere risolti prima di continuare. Ciò fornisce un processo molto più snello e automatizzato rispetto al salvataggio e alla registrazione manuale delle modifiche man mano che i progetti si sviluppano. Evita anche gli inevitabili elenchi di versioni di file con nome confuse ...

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/xkcd.png?raw=true" width="200" /></p>

<p align="center"><i>GitHub ci aiuta a evitare, er, convenzioni di denominazione dei file non ottimali (fonte: XKCD)</i></p>

  


Una delle funzioni più popolari e utili di GitHub è la [issue tracker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/issues), che viene utilizzata per organizzare lo sviluppo di OSS. Il link sopra ti porta al tracker dei problemi per lo sviluppo di questo modulo! Se pensi che ci sia qualcosa che può essere migliorato o vuoi commentare, chiunque può aggiungere o contribuire a un problema lì!

Altri servizi di hosting di progetti simili includono [BitBucket](https://bitbucket.org/), [GitLab](https://about.gitlab.com/)e [Launchpad](https://launchpad.net/). Se la recente acquisizione di GitHub da parte di Microsoft è un po 'scoraggiante, queste sono ottime alternative.

Tuttavia, sappiamo anche che GitHub può avere una curva di apprendimento piuttosto elevata. Ecco perché il primo compito pratico di questo MOOC ti insegnerà come impostare il tuo primo repository di progetti GitHub!

**[VAI AL COMPITO 1: Costruisci il tuo primo repository GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)**

  


## Software Open Source utilizzato nella ricerca <a name="Research"></a>

Soprattutto nella ricerca scientifica, l'utilizzo e lo sviluppo del software Open Source è diventato praticamente la norma. Esiste una serie di ragioni al di fuori di quelle che si applicano all'accettazione generale dell'OSS, ad esempio da parte di consumatori, industria o governo. Tra questi motivi vi sono:

- Sempre più spesso, gli algoritmi implementati nel software di analisi sono parte integrante dei metodi descritti nelle pubblicazioni accademiche. In quanto tale, è completamente in disaccordo con una rigorosa revisione tra pari se queste implementazioni degli algoritmi sono chiuse agli estranei.

- La collaborazione scientifica spesso si estende su più istituzioni e reti di ricerca distribuite in cui la segretezza e la gerarchia di comando non sono mantenute in un modo che è "necessario" per lo sviluppo a codice chiuso.

- Molte analisi computazionali sono eseguite in ambienti virtualizzati (come infrastrutture "cloud" istituzionali, nazionali o internazionali) e ospitate su server multiutente. Il software commerciale closed-source spesso non consente tale utilizzo.

- Lo sviluppo dell'OSS si basa spesso su volontari. In un momento di limiti di budget per la ricerca scientifica, questo è un chiaro vantaggio.

Per questi e altri motivi, gli strumenti Open Source sono molto usati nella ricerca scientifica. Questo include l'utilizzo in settori in cui molti ricercatori sono sviluppatori amatoriali se stessi e si basano su strumenti quali [R](https://www.r-project.org/) per l'analisi statistica e di scripting, che, negli ultimi dieci anni, ha quasi completamente spostato software commerciale per l'analisi statistica come SPSS o JMP in un molti campi In campi come la bioinformatica, che coinvolgono un sacco di gestione dei file degli output delle piattaforme di sequenziamento del DNA, i linguaggi di scripting generici come [Python](https://www.python.org/) e le librerie comunemente usate su di esso (come [biopython](http://biopython.org)) sono diventati un vitale parte del toolkit di molti ricercatori.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/python.png?raw=true" width="400" /></p>

<p align="center"><i>Pitone</i></p>

  


Strumenti come R e Python sono essenzialmente software per scrivere software. Anche se la programmazione è un'attività sempre più comune tra i ricercatori, certo che no *ogni* scienziato fa questo. Un passo avanti rispetto alla programmazione è il concatenamento di input e output di vari strumenti di analisi in flussi di lavoro più lunghi. Come esempio della genomica, un flusso di lavoro molto comune è quello di iniziare con letture di sequenziamento ad alto throughput e quindi i) eseguire controlli di controllo di qualità di base; ii) mappare le letture rispetto a un genoma di riferimento; iii) identificare i punti in cui i nuovi dati sono in contrasto con il riferimento. Questi passaggi sono eseguiti di routine come un flusso di lavoro in cui un diverso eseguibile Open Source viene eseguito in un ambiente di riga di comando Linux per ciascuno dei tre passaggi. Sebbene questo sia probabilmente non lo sviluppo di software open source, implica l'uso e la produzione di risorse open source (come gli script di shell Linux) per i quali sono applicabili i principi che discutiamo in questo modulo.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/r.png?raw=true" width="200" /></p>

<p align="center"><i>R</i></p>

  


Infine, l'OSS viene utilizzato anche nella ricerca scientifica per ragioni che rispecchiano più da vicino quelle che guidano l'adozione dell'OSS nella società in generale, ovvero che è economico. Ad esempio, gli individui o organizzazioni potrebbero decidere di passare da Microsoft Office a LibreOffice per la scrittura del manoscritto o trasformazione foglio di calcolo perché quest'ultimo è libero (sia come in [**'birra gratis'**](https://www.youtube.com/watch?v=dQw4w9WgXcQ) e 'libertà di parola'). Allo stesso modo, la scelta di passare da ArcGIS a [QGIS](https://www.qgis.org/en/site/) per l'analisi delle informazioni geografiche potrebbe essere suggerita semplicemente da considerazioni sui costi.   


## Guida introduttiva all'OSS - Domande frequenti <a name="FAQ"></a>

**Sto usando X [es. Matlab, STATA, Excel] e voglio passare a qualcosa di più aperto. Quali sono i prossimi passi?**

Anche se utilizzi software proprietario, puoi sempre condividere il tuo codice sorgente / documenti ecc. *Il miglior primo passo è condividere quello che puoi*.

**Grande! Posso inserirli nel mio nuovo repository Github.**

Se questo è abbastanza per te per ora fantastico! Se non per la maggior parte dei software proprietari ci sono equivalenti Open Source. Provalo con uno e guarda cosa ne pensi.

| Chiuso                                                                                                   | Aperto                                                                                                                                                               |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Matlab                                                                                                   | Python, Julia                                                                                                                                                        |
| STATA / SPSS                                                                                             | R                                                                                                                                                                    |
| MS Office                                                                                                | LibreOffice                                                                                                                                                          |
| matematica                                                                                               | JupyterLab                                                                                                                                                           |
| Prova il tuo nuovo [Pull Request -PR-](https://help.github.com/articles/about-pull-requests/) Skills ... | ... aggiungendo il proprio esempio [qui](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md) |

**Freddo! Ma se faccio lo switch, sarò bloccato: ci vorranno anni per imparare un nuovo strumento / senza supporto / con software buggy.**

Buona domanda! La risposta è, dipende. La cosa migliore da fare è trovare qualcuno che ha fatto il passaggio prima e imparare dalla loro esperienza. Oppure fai una ricerca su Google! Alcuni OSS sono molto migliori delle loro controparti chiuse, altri no, quindi vale la pena scegliere con attenzione.

## Fare un buon software per il riutilizzo <a name="Reuse"></a>

La persona più probabile che potrebbe voler riutilizzare il tuo software in futuro è ... tu! Quindi, mentre la condivisione è sempre meglio che non condividere, puoi rendere la tua vita, e quella degli altri, molto più semplice attraverso la documentazione appropriata. La documentazione può includere diverse cose, come l'inclusione di commenti e annotazioni utili nel codice che aiutano a spiegare perché è stata eseguita un'azione particolare, piuttosto che ciò che si intende raggiungere.

Uno degli aspetti più critici di questo è includere un file `README` informativo, che accompagna quasi tutti i progetti OSS, e alcune volte anche più di uno. Può essere una buona pratica includere un tale file in ogni directory, che include un elenco di file, un sommario e qual è lo scopo della directory. Il file `README` è in genere solo testo normale o markdown (di nuovo, come tutti quelli per MOOC!) E può includere informazioni critiche su come installare ed eseguire software, dipendenze e requisiti precedenti, nonché tutorial o esempi.

> **Lo sapevi che ...** Il termine `README` è spesso attribuito alla famosa scena di Alice nel paese delle meraviglie di Lewis Carroll, in cui Alice affronta magie munchies etichettate con "Eat Me" e "Drink Me". Potente.

Lo scopo qui è di fornire informazioni sufficienti per massimizzare il riutilizzo e la riproducibilità dell'ambiente di calcolo, in modo tale che qualcuno senza esperienza con il progetto possa facilmente accedere e riutilizzare il software ([Sandve et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)). Abbassando le barriere all'entrata, aumenti le possibilità che altri possano riutilizzare il tuo lavoro, che è uno degli obiettivi finali dell'OSS ([Ince et al., 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)).

Un'estensione di questo che può aiutare a rendere le cose ancora più facili per il riutilizzo futuro è la tecnologia del "contenitore". I contenitori sono come un ecosistema congelato nel tempo, in cui il codice, i dati, qualsiasi altra dipendenza, sono tutti perfettamente conservati, impacchettati e salvati nelle attuali versioni funzionanti. Ciò significa che chiunque in futuro potrà entrare ed eseguire nuovamente le analisi. In quanto tali, sono generalmente validi per il riutilizzo, ma questo può venire al sacrificio della modifica o della comprensione da parte degli altri, poiché spesso è possibile nascondere molti dettagli all'interno del codice sorgente e delle sue dipendenze. Esempi comuni di implementazione del contenitore nella ricerca includono [Rocker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf) (un contenitore Docker per il linguaggio R), [Binder](https://mybinder.readthedocs.io/en/latest/)e [Code Ocean](https://codeocean.com/).

**Il software sostenibile è un buon software.**

  


## 10 regole semplici per una ricerca computazionale riproducibile

Le 10 regole semplici per rendere più riproducibile la ricerca computazionale, basate su [Sandve et al. (2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF), sono:

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

<p align="center"><i>Infografica adattata da Sandve et al. (2013). Sentiti libero di scaricarlo e stamparlo per tenerlo a portata di mano durante le tue ricerche!</i></p>

  


Se segui questi passaggi, insieme ai processi in [**Task 1**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) e [**Task 2**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), dovresti stare bene!

  


## Licenze open source <a name="Licensing"></a>

Una licenza Open Source è un tipo di licenza progettata specificamente per software e codice che rendono esplicito quali sono le condizioni legali per la condivisione e il riutilizzo. Come accennato [sopra](#What_OSS), l'aggiunta di una licenza adatta è ciò che differenzia pubblicamente software condiviso da OSS. Ad esempio, il ampiamente utilizzato [MATLAB](https://www.mathworks.com/products/matlab.html) è un software proprietario, e [Octave](https://www.gnu.org/software/octave/) è un linguaggio di programmazione alternativa licenza apertamente.

Ci sono attualmente oltre 1.400 licenze Open Source uniche, una complessità nata dalla difficoltà di comprendere le differenze tra le implicazioni legali di diverse licenze.

Alcune delle licenze più comuni includono:

- [Berkeley Software Distribution ("BSD")](https://en.wikipedia.org/wiki/BSD_licenses),
- [Apache](https://www.apache.org/licenses/LICENSE-2.0),
- [MIT-style (Massachusetts Institute of Technology)](https://opensource.org/licenses/MIT), o
- [Licenza pubblica generale GNU ("GPL")](https://www.gnu.org/licenses/gpl-3.0.en.html).

Non hai bisogno di conoscere tutta la verità legale dietro a tutto ciò, ma è bene sapere almeno quali opzioni sono disponibili per te.

Esistono due modi in cui i contributi a un progetto diventano concessi in licenza:

1. *Esplicitamente*, in cui il contributo individuale ha una licenza chiaramente indicata indipendente dal progetto principale; o
2. *Implicitamente*, per cui il contributo rientra nel codice di licenza originale del progetto principale.

Per fortuna, il processo di selezione di una licenza Open Source è relativamente banale, grazie a strumenti intuitivi come [Scegli una licenza](https://choosealicense.com/). Ciascuna di queste licenze consente ad altri utenti di utilizzare, copiare, distribuire e sviluppare il proprio lavoro, spesso assicurando che i creatori siano adeguatamente riconosciuti per il proprio lavoro. Qui, la chiave sta selezionando una licenza appropriata per il tuo lavoro, a seconda di cosa vuoi o non vuoi, altri da fare con esso.

  


## Citazione del software <a name="Citation"></a>

Le citazioni forniscono una delle interazioni più importanti nella ricerca accademica, costituendo la base dei nostri sistemi di riferimento e metrica. Tipicamente, questo viene eseguito grazie all'assistenza di un identificatore univoco permanente come [Digital Object Identifiers](https://en.wikipedia.org/wiki/Digital_object_identifier) (DOI). Un DOI è un identificatore persistente, implementato nel [Handle System](https://en.wikipedia.org/wiki/Handle_System), che soddisfa uno standard comune, a seconda dello scopo, come ad esempio l'identificazione di informazioni accademiche. Tale identificazione è fondamentale per tracciare la genealogia e la provenienza della ricerca, per la riproducibilità, nonché per dare credito appropriato a coloro che hanno creato il software. È importante sottolineare che il software dovrebbe essere considerato un risultato legittimo dalla ricerca accademica e la citazione sta diventando un modo sempre più comune per indicarlo.

Nel 2016, [Smith et al., 2016](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) scritto un documento di ricerca sui principi della citazione del software come parte del FORCE11 Software Citation Working Group. Nello stesso modo in cui vorresti citare il software che hai usato come parte di buone pratiche di ricerca, è importante rendere anche la tua ricerca facilmente percettibile. Quando si cita un software utilizzato per la propria ricerca, è necessario includere almeno:

- Il nome dell'autore (s),
- Titolo del software,
- Numero di versione e
- L'identificatore / locatore univoco (DOI o URL).

I sei principi di citazione software da [. Smith et al, (2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) sono forniti qui:

- **Importanza**: il software dovrebbe essere considerato un prodotto di ricerca legittimo e citabile. Le citazioni del software dovrebbero avere la stessa importanza nella documentazione scolastica come citazioni di altri prodotti di ricerca, come pubblicazioni e dati; dovrebbero essere inclusi nei metadati del lavoro di citazione, ad esempio nell'elenco di riferimento di un articolo di giornale, e non dovrebbero essere omessi o separati. Il software dovrebbe essere citato sulla stessa base di qualsiasi altro prodotto di ricerca come una carta o un libro, vale a dire che gli autori dovrebbero citare l'insieme appropriato di prodotti software proprio mentre citano la serie appropriata di documenti.

- **Credito e attribuzione**: le citazioni software dovrebbero facilitare il conferimento del credito accademico e l'attribuzione normativa e legale a tutti i contributori al software, riconoscendo che uno stile unico o un meccanismo di attribuzione potrebbero non essere applicabili a tutto il software.

- **Identificazione univoca**: una citazione di software dovrebbe includere un metodo di identificazione che sia azionabile dalla macchina, globalmente unico, interoperabile e riconosciuto da almeno una comunità degli esperti di dominio corrispondenti, e preferibilmente da ricercatori pubblici generali.

- **Persistenza**: gli identificatori e i metadati univoci che descrivono il software e la sua disposizione dovrebbero persistere, anche oltre la durata di vita del software che descrivono.

- **Accessibilità**: le citazioni software dovrebbero facilitare l'accesso al software stesso e ai relativi metadati, documentazione, dati e altro materiale necessario sia per le persone che per le macchine per fare un uso consapevole del software di riferimento.

- **Specificità**: le citazioni software dovrebbero facilitare l'identificazione e l'accesso alla versione specifica del software che è stata utilizzata. L'identificazione del software dovrebbe essere specifica come necessario, come l'uso di numeri di versione, numeri di revisione o varianti come piattaforme.

Nota: per le istruzioni su "come rendere il software leggibile", consultare la sezione [**Utilizzo di GitHub e Zenodo**](#GitHub_Zenodo) seguito e [**Attività 2: Collegamento di GitHub e Zenodo**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md).

  


## Utilizzando GitHub e Zenodo <a name="GitHub_Zenodo"></a>

[GitHub](#GitHub) è uno strumento popolare per la gestione dei progetti, la memorizzazione dei contenuti e il controllo della versione. Si noti che GitHub stesso non è OSS. Tuttavia, Git, lo strumento su cui si basa, è. Git è progettato per aiutare a gestire i file del codice sorgente e gli aggiornamenti, per un progetto relativo al software. Tuttavia, può anche essere esteso ad altri progetti non software; per esempio, questo [MOOC](https://github.com/OpenScienceMOOC/)!

Tuttavia, fare ricerche su GitHub è solo il primo passo. È altrettanto importante renderlo persistente e riutilizzabile, motivo per cui avere un identificatore di oggetti digitali (DOI) associato può essere utile. Il modo più semplice per farlo è attraverso un servizio chiamato [Zenodo](https://zenodo.org/), che è un repository multidisciplinare gratuito e open source creato da OpenAIRE e CERN e può essere utilizzato per assegnare un DOI a singoli repository GitHub. C'è un [GitHub Guida](https://guides.github.com/activities/citable-code/) che spiega i dettagli, che coinvolgono il collegamento repository GitHub direttamente a Zenodo in modo che quando gli sviluppatori creano versioni formali per il loro software, Zenodo crea e archivia un tale versione del software.

Non c'è niente di speciale nell'usare Zenodo per la creazione di DOI, tranne il suo **gratuito**; possono anche essere usati altri repository generali, come [DataCite DOI Fabrica](https://doi.datacite.org/), o i propri repository istituzionali come [Caltech's](https://www.library.caltech.edu/news/enhanced-software-preservation-now-available-caltechdata).

Molti ricercatori potrebbero in genere temere di condividere codice incompleto, buggato o imperfetto. Tuttavia, nella comunità OSS, tale pratica di condivisione del codice "raw" è abbastanza comune. La condivisione del codice consente agli altri di riutilizzarlo e migliorarlo, nonché di impegnarsi in modo più approfondito con qualsiasi ricerca ad esso associata. Questo è uno degli aspetti fondamentali della collaborazione tra pari, forse meglio esemplificato dal tradizionale processo di revisione tra pari di manoscritti di ricerca.

L'attività 2 ti guiderà attraverso il processo di collegamento di un repository GitHub a Zenodo per l'archiviazione.

> **Lo sapevi che ...** Tutto il contenuto prodotto per questo MOOC è disponibile come parte di una comunità in [Zenodo](https://zenodo.org/communities/open-science-mooc/)?

**[VAI AL COMPITO 2: Collegamento di GitHub e Zenodo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)**

  


## Collaborare e contribuire attraverso l'Open Source <a name="Collaborating"></a>

Spesso, l'OSS è sviluppato in maniera pubblica, decentralizzata e collaborativa tra più contributori. Lo scopo di questo è di migliorare la diversità e la portata di un progetto e il suo design, al fine di diventare più vantaggioso e sostenibile. Un simile approccio è stato paragonato a un modello di "bazar" di Eric Raymond, uno dei primi sostenitori dell'OSS. Uno dei principali principi guida di questo è quello della **peer production**, che si basa su comunità auto-organizzate per regolare lo sviluppo dei contenuti, coordinata verso un obiettivo o un risultato condiviso.

I progetti OSS fanno molto affidamento sulla collaborazione volontaria, che spesso comporta un flusso costante di nuovi arrivati per diventare produttivi e sostenibili ([Steinmacher et al., 2014](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)). Creare la giusta atmosfera sociale per un progetto e un ambiente di coinvolgimento accogliente, sono spesso fondamentali per collaborazioni di successo in OSS.

  


## Dove andare da qui <a name="Future_OSS"></a>

Si spera che ora si sia arrivati a vedere l'importanza del software come pietra angolare della scienza moderna e l'importanza che l'OSS gioca in questo.

Le **risultati di apprendimento** di questo dovrebbero essere:

1. Sarai ora in grado di definire le caratteristiche dell'OSS e alcuni degli argomenti di impatto etico, legale, economico e di ricerca a favore e contro di esso.

2. Basandoti sugli standard della community, sarai ora in grado di descrivere i requisiti di qualità della condivisione e del riutilizzo del codice aperto.

3. Ora sarai in grado di utilizzare una serie di strumenti di ricerca che utilizzano l'OSS.

4. Ora sarai in grado di trasformare il codice progettato per il loro uso personale in un codice accessibile e riutilizzabile da altri.

5. Gli sviluppatori di software saranno in grado di rendere il loro software interessante e gli utenti del software sapranno come citare il software che usano.

  


**COMPITO BONUS**

Se hai completato [Task 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) e [Task 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), abbiamo anche un **BONUS TASK** per te, se vuoi portare le tue abilità un passo avanti. [Attività 3](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md) vi porterà un passo più in profondità l'integrazione Git in un flusso di lavoro tipico di ricerca, mostrando come integrarlo con R Studio. Si consiglia di aver completato i primi 2 compiti prima di procedere con questo.

Tuttavia, il tuo viaggio Open Source non si ferma qui! Questo era solo l'inizio e ci sono alcune risorse incredibili là fuori se ti piacerebbe fare o saperne di più:

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
    
    *Questi riferimenti qui sono solo l'inizio. Includono alcune delle panoramiche generali più utili del panorama Open Source nella ricerca. Tuttavia, se vuoi trovare qualcosa di più specifico nel tuo campo di ricerca, allora quel percorso è lì per te da esplorare!*
    
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
    
    **Sapere in che modo questo contenuto può essere migliorato?**
    
    È tempo di prendere le tue nuove abilità GitHub per un test-run! Tutto lo sviluppo del contenuto avviene principalmente qui [qui](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md). Se hai un miglioramento suggerito per il contenuto, il layout o qualsiasi altra cosa, puoi realizzarlo e poi diventerà automaticamente parte del contenuto di MOOC dopo la verifica da parte di un moderatore!
    
    [![Dedicato pubblico dominio CC0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)