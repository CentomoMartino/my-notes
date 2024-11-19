I processi sono caricati in memoria uno dopo l'altro senza spazi liberi.
Memoria a partizione fissa:  E' possibile solo se la memoria è determinata da delle partizioni fisse che contengono i processi.

2 Opzioni: 
Partizione fissa
Partizione Variabile

PARTIZIONE FISSA

Le partizioni hanno una dimensione che non varia con il tempo. Ogni partizione può eseguire solo 1 processo intero e viene aggiunto alla coda della partizione più piccola che lo possa contenere.

* <small>Frammentazione esterna: Partizioni troppo piccole per memorizzare job di grandi dimensioni.</small>
* <small>Frammentazione interna: Quando una partizione è piena, i programmi in coda possono essere eseguiti in una partizione più grande.</small>

PARTIZIONE VARIABILE

Le partizioni hanno una dimensione variabile in grandezza e numero di partizioni, unendo i blocchi di partizione.

Diverse strategie:

* <small>First-fit: Il gestore cerca la prima zona libera dove far entrare il processo.</small>

* <small>Best-fit: Il gestore scandisce una tabella di partizioni e sceglie la zona più piccola disponibile.</small>

* <small>Worst-fit: Sceglie la zona libera più grande.</small>

* <small>Next-fit: Cerca il prima spazio libero partendo dall'ultimo processo allocato.</small>