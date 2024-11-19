Obbiettivi:
* Mantenere in memoria solo le parti necessarie
* Gestire ogni volta solo piccole porzioni di memoria
* Non sprecare spazio evitando frammmentazioni
* Poter usare porziani di memoria non contigue per lo stesso programma
* Non dare l'incombenza della suddivisione del programma al programmatore

La memoria fisica viene suddivisa in blocchi di dimensione fissa (Pagine fisiche)
I programmi vengono divisi in blocchi di dimensioni uguali (Pagine logiche).

	Se le pagine logiche sono MINORI delle pagine fisiche:
		Il programma può essere caricato in memoria

	Se le pagine logiche sono MAGGIORI:
		Il programma viene caricato parzialmente

Problema di <big>PAGE FAULT</big>:
	Casistica in cui il processo che deve essere eseguito non trova le infomazioni di esecuzione sulla RAM, e quindi deve essere ricaricato. Viene selezionato il frame più vecchio all'interno della tabella delle pagine fisiche e viene sostituito con la tecnica dello swap-in.

Viene gestito dalla [[MMU]]