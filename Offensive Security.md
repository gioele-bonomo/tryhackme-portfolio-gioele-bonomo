Corso Pre-Sicurezza

# Offensive Security Intro – TryHackMe

Sicurezza offensiva: comprendere le tattiche degli hacker e potenziare le difese del nostro sistema.

Hacking di un sito web:
il sito web in questione è Fakebank:
  Utilizziamo Gobuster per forzare brute force il sito web di FakeBank. Obiettivo-> trovare directory e pagine nascoste. 
  Gobuster prenderà un elenco di potenziali nomi di pagine o directory e proverà ad accedere a un sito web con ciascuno di essi; se la pagina esiste lo segnalerà
  Terminale: digitare: gobuster -u http://fakebank.thm -w wordlist.txt dir -> Utile per trovare pagine potenzialmente nascoste sul sito web
      -u: viene utilizzato per indicare quale sito web stiamo analizzando
      -w: accetta un elenco di parole da scorrere per trovare pagine nascoste
    /bank-transfer (Status: 200)-> numero di pagine presenti nell'elenco delle direcotry (indicate dallo stato 200)
    dal sito: fakebank.thm, aggiungiamo: fakebank.thm/bank-transfer : accederemo al pannello di admin-> inviare e ricevere denaro quando e come si vuole.
Da hacker etici dobbiamo avvisare la banca di questa vulnerabilità.
Se fossi un penetration tester o un consulente per la sicurezza, questo è un esercizio che faresti per le aziende per testare le vulnerabilità
nelle loro applicazioni web e trovare pagine nascoste da esaminare alla ricerca di vulnerabilità.

Penetration Tester - Responsabile dei test sui prodotti tecnologici per individuare vulnerabilità di sicurezza sfruttabili.
Red Teamer - Interpreta il ruolo di un avversario, attaccando un'organizzazione e fornendo feedback dal punto di vista del nemico.
Ingegnere della sicurezza: progetta, monitora e mantieni controlli, reti e sistemi di sicurezza per contribuire a prevenire gli attacchi informatici.
