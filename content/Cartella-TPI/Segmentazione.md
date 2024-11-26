
La memoria centrale è suddivisa secondo la stessa divisione logica dei programmi, dove ogni modulo software svolge una funzione diversa. (es. StampaDati, EstraiDati)

Ad ogni modulo è associato un segmento di memoria centrale di dimensione variabile.

Un segmento è caricato su un frame di uguali dimensioni. I segmenti di un processo possono essere caricati in frame non contigui mentre quelli caricati sono conservati nell'area di swap.

La traduzione degli indirizzi logici in fisici  avviene attraverso la [[Tabella dei segmenti]]

<big>Vantaggi</big>

	- La gestione di strutture di dati dinamiche che crescono e diminuiscono.
	- Viene facilitata la possibilità di condivisione di segmenti tra alcuni               processi.
	- Si semplifica il linking di procedure compilate separatamente.
	- Ogni segmento può avere un diverso tipo di protezione.

