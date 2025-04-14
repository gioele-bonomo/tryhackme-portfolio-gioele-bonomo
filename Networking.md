reti=cose connesse tra di loro.
In informatica il concetto è lo stesso, esteso ai dispositivi tecnologici.

Internet
unica rete gigantesca composta al suo interno da moltissime piccole reti.

ARPANET-> prima iterazione di internet, fine anni 60.
Progetto finanziato dagli USA.
Soltanto nel 89, venne inventato internet come la conosciamo oggi, creando il World WIde Web (WWW)-> diventando archivio per tutte le informazioni.

Internet, composta da iccole reti collegate tra di loro (reti private).
Le reti che collegano le reti private sono le reti pubbliche-> internet

Identificazione dei dispositivi su una rete
Per mantenere ordine in rete, i dispositivi devono essere identificativi che identificabili su una rete.
-Nome (IP)
-Impronte digitali (MAC)

IP: Internet Protocol, insieme di numeri suddivisi in quattro ottetti.
ipv4-> 2^32 indirizzi IP, 4,29mld.
ipv6->2^128 (340 trilioni), nasce per risolvere questo problema

MAC: Media Access Control, numero esadecimale di dodici caratteri dove i primi 6 determinano l'azienda che ha prodotto l'interfaccia di rete, mentre gli ultimi 6 sono un numero univoco.

ipv6-> possono essere falsificati-> spoofing: quando in rete si finge di identificarsi come un altro, utilizzando il proprio MAC.


Simulazione rete wifi pubblica di un hotel
Per utilizzare il servizio di wifi dell'hotel, bisogna pagare.
Abbiamo 2 host, uno che ha pagato (green) e un altro che non ha pagato (red).
Il router consente l'invio dei pacchetti (traffico dati) all'host green, mentre viene negato all'altro host, l'invio dei pacchetti, perchè non ha pagato.

Possiamo però modificare indirizzo MAC del l'host red con quello green, così da camuffarci come l'host green e utilizzare il wifi.

Flag: THM{YOU_GOT_ON_TRYHACKME}

Ping
utilizza pkt ICMP (Internet COntrol Message Protocol) per determinare le prestazioni di una connessione tra dispositgivi, ad esempio se la connessione esiste o è affidabile.

ping-> tempo impiegato dai pkt ICMP per viaggiare tra i dispositivi:
misurazione effettuata utilizzando il pkt di eco ICMP e successivamente la risposta di eco ICMP dal dispositivo di destinazione.

