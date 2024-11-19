La memoria è parzialmente occupata dal SO, mentre lo spazio restante è utilizzato dai programmi per i processi utente.

Durante l'esecuzione i processi DEVONO risiedere in memoria, ma finché sono bloccato o sospesi, allora possono risiedere in una memoria esterna. 
Lo spostamento di un processo si chiama [[Swapping]].

Si può pensare di usare la tecnica del round robin, con swapping successivi, facendo portare avanti più processi insieme, però questo porta un sovraccarico di lavoro (overhead) per la memoria perché anche fare lo swapping occupa spazio e richiede tempo di esecuzione, rendendo questa tecnica poco efficace.

Per usare in modo efficiente la multiprogrammazione occorre avere in memoria più processi, per ridurre i tempo di context switching.
*   [[Allocazione contigua]]
*   [[Allocazione non contigua]]
