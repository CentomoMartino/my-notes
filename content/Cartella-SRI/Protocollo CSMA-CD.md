Protocollo per reti WiFi che rileva le possibili collisioni prima che si verifichino.

Si divide in 2 fasi:
CSMA: Rileva la portante (segnale continuo trasmesso su tutto il canale) e se il canale è libero inizia la trasmissione, altrimenti attraverso un tempo casuale, si rimette in ascolto per verificare la libertà della portante.

CD:  Rileva la collisione se per caso ci fosse stata una collisione tra  2 dispositivi , aspetta un tempo casuale per rimettersi in ascolto della portante e verificare che sia libero per ritrasmettere il messaggio.

COME SUCCEDE LA COLLISIONE?
	Se i dispositivi valutano la portante come libera e trasmettono contemporaneamente un messaggio, questi 2 vanno a sovrapporsi e sommare i propri valori, ottenendo risultati sfalsati o impossibili, ad esempio A = 1, B = 1, si ottiene che il messaggio finale sarà 2, una tensione troppo alta.

Il segnale emesso quando avviene una collisione si chiama Jam (Marmellata).

Se il canale è libero manda un RTS (Request To Send) ed aspetta un CTS (Clear To Send). Una volta mandato il CTS tutte le macchine perdono la possibilità di comunicare per lasciare libero il canale. Se il canale è occupato, imposta un contatore casuale che allo scadere verifica lo stato del canale.