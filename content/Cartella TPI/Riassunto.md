Gestione della memoria fisica (RAM) e quella virtuale (HDD).

I processi sono divisi in pagine con dimensione fissa, scandita dal SO.
Per caricarli in memoria, vengono create le pagine fisiche e logiche, per tenere traccia dei frame liberi su cui caricare il programma.
Per fare questo ci si avvale di un bit di validità che determina se nella cella è caricato un processo.

Nella tabella dei frame ci sono: Indirizzo del frame fisico, ID del processo e bit di validità(in questo ordine).

La tabella delle pagine logiche deve essere grande quanto il numero di processi che deve ospitare, al suo interno ci sono: indirizzo del frame fisico, bit di validità.

ESERCIZIO DI INSERIMENTO: Carico nella RAM il processo B2 dall'HDD, quindi nella tabella logica scrivo nella posizione che aveva nel HDD, l'indice della tabella delle pagine fisiche e impostare il Bit di Validità ad 1.
Nella tabella dei Frame, il bit di validità diventa 1 nello stesso indice che aveva nella RAM, inserendo l'indirizzo del processo in Ram l'ID del processo in HDD.

Ind proc RAM |    ID proc HDD
750                 |         ID_B2


ESERCIZIO DI SEGMENTAZIONE: Creo la tabella dei segmenti della grandezza del numero dei processi nell' HDD, formata da 2 colonne : indirizzo base della RAM e limite del segmento.
Tabella:
1 |  250   | 100
2 |  150   | 100
3 |  500   | 150
4 |  1600 | 100

ESERCIZIO DI FITTING: Con P1 e P2 già inseriti, inserire:
P3 nella prima cella libera in grado di contenerlo.(first)
P4 nella più grande possibile.(worst)
P5 nella prima cella disponibile in grado di contenerlo dopo l'ulitmo processo inserito (next).


Domande teoriche:
