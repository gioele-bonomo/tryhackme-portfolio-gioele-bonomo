Principi di sicurezza

Innanzitutto conoscere il nostro avversario è fondamentale per poter conoscere i suoi attacchi e iniziare a implementare controlli di sicurezza appropriati. impedire a un bambino di accedere al vostro computer portatile? O state cercando di proteggere un computer portatile che contiene progetti tecnici del valore di milioni di dollari? 

è impossibile raggiungere una sicurezza perfetta

Per valutare la sicurezza di un sistema, è necessario pensare in termini di triade della sicurezza: riservatezza, integrità e disponibilità (CIA).

Confidentiality: Riservatezza: garantisce che solo le persone o i destinatari previsti possano accedere ai dati.
Integrity: L'integrità ha lo scopo di garantire che i dati non possano essere alterati; inoltre, siamo in grado di rilevare qualsiasi alterazione, se si verifica.
Availability: disponibilità ha lo scopo di garantire che il sistema o il servizio sia disponibile quando necessario.
Autenticità : autentico significa non fraudolento o contraffatto. L'autenticità consiste nel garantire che il documento/file/dato provenga dalla fonte dichiarata.
Utilità : l'utilità si concentra sull'utilità delle informazioni. Ad esempio, un utente potrebbe aver perso la chiave di decrittazione per accedere a un laptop con un archivio crittografato. Sebbene l'utente abbia ancora il laptop con i suoi dischi intatti, non può accedervi. In altre parole, sebbene ancora disponibili, le informazioni sono in una forma non utile, ovvero priva di utilità.
Possesso : questo elemento di sicurezza richiede che proteggiamo le informazioni da furti, copie o controlli non autorizzati. Ad esempio, un aggressore potrebbe rubare un'unità di backup, il che significa che perdiamo il possesso delle informazioni finché ne è in possesso. In alternativa, l'aggressore potrebbe riuscire a crittografare i nostri dati utilizzando un ransomware; anche in questo caso, la perdita del possesso dei dati.

Parkeriano Esagono
Nel 1998, Donn Parker propose l'Esagono Parkeriano, un insieme di sei elementi di sicurezza. Essi sono:

Disponibilità
Utilità
Integrità
Autenticità
Riservatezza
Possesso

THM{CIA_TRIAD}


DAD:
La sicurezza di un sistema viene attaccata attraverso diversi mezzi. Può trattarsi della divulgazione di dati segreti, dell'alterazione o della distruzione di dati.
Disclosure : La divulgazione è l'opposto della riservatezza. In altre parole, la divulgazione di dati riservati costituirebbe un attacco alla riservatezza.
Alteration: L'alterazione è l'opposto dell'integrità. Ad esempio, l'integrità di un assegno è indispensabile.
Destruction/Denial: Distruzione/Negazione è l'opposto di Disponibilità.

DAD opposto di CIA


Modelli di sicurezza
come possiamo creare un sistema che garantisca una o più funzioni di sicurezza? La risposta risiede nell'utilizzo di modelli di sicurezza

Modello Bell-LaPadula: raggiungere la riservatezza:

	Proprietà di sicurezza semplice: un soggetto con un livello di sicurezza inferiore non può leggere un oggetto con un livello di sicurezza superiore. (no read up)

	Proprietà di sicurezza Star: un soggetto con un livello di sicurezza più elevato non può scrivere su un oggetto con un livello di sicurezza inferiore (no write down):  impedisce la divulgazione di informazioni sensibili a un soggetto con un livello di sicurezza inferiore

	Proprietà di sicurezza discrezionale:  matrice di accesso per consentire operazioni di lettura e scrittura:

Soggetti	Oggetto A		Oggetto B
Soggetto 1	Scrivere		Nessun accesso
Soggetto 2	Lettura/scrittura	Leggere

È possibile condividere informazioni riservate con persone con un'autorizzazione di sicurezza più elevata (scrivere in alto) e ricevere informazioni riservate da persone con un'autorizzazione di sicurezza inferiore (leggere in basso).
non è stato progettato per gestire la condivisione di file.


Il modello di integrità di Biba: raggiungere l'integrità

	Proprietà di integrità semplice : questa proprietà è definita "no read down"; un soggetto con integrità più elevata non dovrebbe leggere da un oggetto con integrità più bassa.

	Proprietà di integrità della stella : questa proprietà è definita "nessuna scrittura"; un soggetto con integrità inferiore non dovrebbe scrivere su un oggetto con integrità superiore.

leggi, scrivi". Questa regola è in contrasto con il modello Bell-LaPadula, e ciò non dovrebbe sorprendere, poiché il primo si concentra sulla riservatezza, mentre il secondo sull'integrità.
non gestisce le minacce interne (minacce interne).

Il modello Clark-Wilson: mira a raggiungere l'integrità:

	Elemento dati vincolato (CDI) : si riferisce al tipo di dati di cui vogliamo preservare l'integrità.
	Elemento dati non vincolato (UDI) : si riferisce a tutti i tipi di dati oltre a CDI, come input utente e di sistema.
	Procedure di trasformazione (TP) : queste procedure sono operazioni programmate, come lettura e scrittura, e dovrebbero mantenere l'integrità dei CDI.
	Procedure di verifica dell'integrità (IVP) : queste procedure controllano e garantiscono la validità dei CDI.

Flag: THM{SECURITY_MODELS}




Defence in depth: sicurezza multilivello: creazione di un sistema di sicurezza a più livelli
cassetto chiuso a chiave: sicurezza a più livelli: cassetto chiuso a chiave, la stanza interessata chiusa a chiave, la porta principale dell'appartamento chiusa a chiave, il cancello del palazzo chiuso a chiave e potreste anche voler aggiungere qualche telecamera di sicurezza






Norme ISO/IEC 19249
SO/IEC 19249:2017 Tecnologia dell'informazione - Tecniche di sicurezza - Catalogo dei principi di architettura e progettazione per prodotti, sistemi e applicazioni sicuri 
Obiettivo->fornire una panoramica più approfondita di ciò che le organizzazioni internazionali intendono insegnare in merito ai principi di sicurezza.

5 principi architettonici:


1)Separazione dei domini: ogni insieme di componenti (applicazioni, dati o altre risorse) correlati è raggruppato come un'unica entità. Ogni entità avrà il proprio dominio e le verrà assegnato un insieme comune di attributi di sicurezza
	Esempio: livelli di privilegio kernel x86 -> eseguito nell'anello 0 (livello con privilegi più elevato)
		 applicazioni in modalità utente -> eseguite nel livello 3 (privilegi meno elevati)-> separazione inclusa nel modello di Goguen-Meseguer
2) Stratificazione: quando un sistema è strutturato in molti livelli o layer astratti, diventa possibile imporre policy di sicurezza a diversi livelli
	esempio: modello OSI con i 7 livelli di networking: ogni livello-> fornisce servizio specifico al livello superiore. Questa stratificazione impone policy di sicurezza e valida facilmente il corretto funzionamento del sistema.
		 operazioni su disco: un programmatore di solito utilizza le funzioni di lettura e scrittura su disco fornite dal linguaggio di programmazione di alto livello scelto. Il linguaggio di programmazione nasconde le chiamate di sistema di basso livello e le presenta come metodi più intuitivi. La stratificazione è correlata alla Difesa in Profondità.
3)Incapsulamento: OOP, nascondiamo le implementazioni di basso livello e impediamo la manipolazione diretta dei dati in un oggetto fornendo metodi specifici a tale scopo.
	Esempio: se si dispone di un oggetto orologio, si fornirebbe un metodo increment()invece di consentire all'utente di accedere direttamente alla secondsvariabile.
	Obiettivo: impedire valori non validi per e variabili.	
	Contesto più grande: si utilizzerebbero interfacce di programmazione applicativa (API) appropriate che l'applicazione utilizzerebbe per accedere al db.
4)Ridondanza: garantisce disponibilità e integrità.
	esempio: Si consideri il caso di un server hardware con due alimentatori integrati: se uno dei due si guasta, il sistema continua a funzionare. 
		 Si consideri una configurazione RAID 5 con tre unità: se un'unità si guasta, i dati rimangono disponibili utilizzando le due unità rimanenti. 
		 Inoltre, se i dati vengono modificati in modo improprio su uno dei dischi, la modifica verrebbe rilevata tramite la parità, garantendo l'integrità dei dati.
5)Virtualizzazione: condivisione di un singolo set di hardware tra più sistemi operativi. La virtualizzazione offre funzionalità di sandboxing che migliorano i limiti di sicurezza, la detonazione sicura e l'individuazione di programmi dannosi.
		

5 principi di progettazione:


1)Privilegio minimo: in base alla necessità, in base alla necessità di sapere -> Chi può accedere a cosa?
	Insegna che dovresti concedere il minimo numero di permessi a chiunque per svolgere il proprio compito, e nient'altro:
		se un utente ha bisogno di poter visualizzare un documento, dovresti concedergli i diritti di lettura ma non quelli di scrittura.
2)Minimizzazione della superficie di attacco: ogni sistema presenta vulnerabilità che un aggressore potrebbe sfruttare per comprometterlo.
	Rischi che dovremmo minimizzare. Ad esempio, uno dei passaggi per rafforzare un sistema Linux , disabiliteremmo qualsiasi servizio non necessario.
3)Validazione centralizzata dei parametri : molte minacce sono dovute al fatto che il sistema riceve input, soprattutto dagli utenti.
	Input non validi -> utilizzabili per sfruttare vulnerabilità del sistema: come il diniego di servizio e l'esecuzione di codice da remoto.
		Convalida dei parametri: passaggio necessario per garantire il corretto stato del sistema. dovrebbe essere centralizzata all'interno di una libreria o di un sistema.
4)Servizi di sicurezza generali centralizzati :  dovremmo puntare a centralizzare tutti i servizi di sicurezza (creare Server->centralizzato per l'autenticazione)
5)Preparazione alla gestione di errori ed eccezioni: ogni volta che sviluppiamo un sistema, dovremmo tenere presente che errori ed eccezioni si verificano e si verificheranno.
	Esempio: applicazione di shopping: un cliente potrebbe tentare di effettuare un ordine per un articolo esaurito. Un database potrebbe sovraccaricarsi e smettere di rispondere a un'applicazione web. Questo principio insegna che i sistemi dovrebbero essere progettati per essere a prova di errore; ad esempio, se un firewall si blocca, dovrebbe bloccare tutto il traffico invece di consentirlo. Inoltre, dovremmo fare attenzione che i messaggi di errore non trasmettano informazioni che consideriamo riservate, come ad esempio il dump di contenuto di memoria contenente informazioni relative ad altri clienti.



Zero Trust vs Trust ma Verifica

-Fidati ma verifica: dovremmo sempre verificare anche quando ci fidiamo di un'entità e del suo comportamento.
	La verifica di solito richiede l'impostazione di meccanismi di log adeguati; la verifica indica l'analisi dei log per assicurarsi che tutto sia normale.
	non è possibile verificare tutto; basti pensare al lavoro necessario per esaminare tutte le azioni intraprese da una singola entità, come le pagine Internet visitate da un singolo utente. Ciò richiede meccanismi di sicurezza automatizzati, come proxy , rilevamento delle intrusioni e sistemi di prevenzione delle intrusioni.

-Fiducia Zero: fiducia come una vulnerabilità, si rivolge alle minacce interne-> zero trust cerca di eliminarla: Non fidarti mai, verifica sempre!
	 ogni entità vista come avversaria.
	 Zero Trust non concede fiducia a un dispositivo in base alla sua posizione o proprietà.
	 Autenticazione e autorizzazione sono necessarie prima di accedere a qualsiasi risorsa : MICROSEGMENTAZIONE -> progettazione in cui un segmento di rete può avere dimensioni pari a quelle di un singolo host (comunicazione tra gli host richiede autenticazione, liste di controllo degli accessi e altri requisiti di sicurezza).


Threat vs Risk:

Vulnerability: Vulnerabilità : vulnerabile significa suscettibile ad attacchi o danni. Nella sicurezza informatica, una vulnerabilità è una debolezza.
Threat: Minaccia : una minaccia è un potenziale pericolo associato a questa debolezza o vulnerabilità.
Risk: Rischio : il rischio riguarda la probabilità che un agente della minaccia sfrutti una vulnerabilità e il conseguente impatto sull'azienda.

showroom con porte e finestre in vetro standard presenta una debolezza, o vulnerabilità (vetro)-> rischio che porte e finestre in vetro possano essere rotte -> I proprietari dello showroom dovrebbero valutare attentamente il rischio , ovvero la probabilità che una porta o una finestra in vetro si rompa e il conseguente impatto sull'attività.

Lavori per un ospedale che utilizza un particolare sistema di database per archiviare tutte le cartelle cliniche. Un giorno, seguendo le ultime notizie sulla sicurezza, scopri che il sistema di database utilizzato non solo è vulnerabile, ma che è stato rilasciato anche un codice exploit funzionante proof-of-concept; il codice exploit rilasciato indica che la minaccia è reale. Con questa consapevolezza, devi valutare il rischio risultante e decidere i passi successivi.
