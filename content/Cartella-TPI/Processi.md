I processi sono composti da 2 parti:
	-**CODICE**: Istruzioni da eseguire.
	-**DATI DEL PROGRAMMA** : 
		- variabili globali, allocate nella RAM nell’area dati globali 
		- variabili locali e non locali memorizzate in uno stack 
		- variabili temporanee introdotte dal compilatore (tra cui PC o IP) caricate nei registri del processore 
		- variabili allocate dinamicamente durante l’esecuzione, memorizzate in un heap*

Un programma in esecuzione può avere più istanze di sé stesso caricate in RAM, quindi processi generati dallo stesso codice allo stesso momento in esecuzione.

L'insieme dei dati di un processo di chiama **Contesto del processo**.

Si dividono in:
	- **Indipendenti**: Il processo viene portato avanti senza bisogno di scambiare dati con gli altri.
	- **Cooperanti**: Il processo, per proseguire con la sua esecuzione, necessità di ricevere dei dati da un altro processo in esecuzione.
	- **Competitori**: Il processo deve accedere ad una stessa risorsa a cui deve accedere anche un altro, quindi si ostacolano.


<big>Stati dei processi</big>
	Ogni processo si trova una situazione diversa rispetto alla CPU: 
	Gli stati possono essere:
		- new: Processo appena creato e caricato in RAM.
		- ready: Pronto all'esecuzione se ha tutte le risorse necessarie alla sua evoluzione.
		-  running: La CPU sta eseguendo il programma, quindi gli è assegnato il processore.
		- waiting: Quando manca una risorsa per poter evolvere, quindi attendo un I/O per proseguire.
		- terminated: Processo terminato e l'SO può liberare le risorse a cui aveva accesso.

Quando un processo viene creato, gli viene assegnato un identificatore, chiamato Process Identifier (PID) e viene inserito nella RL, ready list. Quando viene spostato dalla RL alla CPU, ci sono 3 motivi per cui può terminare. Termina la sua esecuzione, termina il tempo concesso dalla CPU o gli manca una risorsa, per cui viene spostato nella Waiting list.

Al processo viene conferito un Process Descriptor o Process Control Block, che contiene:
	PID (process intentifier)
	Stato Corrente
	Program Counter
	Registri
	Priorità
	Puntatori alla memoria del Processo
	Puntatori alle Risorse allocate