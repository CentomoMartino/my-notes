Il Data Layer è il secondo livello del modello ISO/OSI e si occupa della correzione degli errori e regola il flusso dei dati.

Il livello 2 fornisce gli indirizzi MAC usati per il trasporto del Frame; questi sono l'indirizzo del mittente e destinatario, contenuti nell'header.
Verifica che la trasmissione sia attiva ed agibile, con la fase di handshake (stretta di mano), un messaggio che determina l'inizio della trasmissione.
Il ricevente, valuta che il messaggio sia corretto e nel caso chiede di reinviarlo.
Il flusso dei dati non deve superare quello che il dispositivo ricevente è in grado di elaborare.
Il protocollo deve essere in grado di chiudere la comunicazione in modo ordinato.

FRAMING: Un messaggio di livello 2, prende il nome di frame, con questa procedura si "imbusta" nel pacchetto che arriva dal livello superiore una header e un trailer, che contiene i controlli necessari per L'APERTURA, MANTENIMENTO e CHIUSURA della comunicazione.
Il frame viene mandato al livello fisico che tramette il frame come sequenza di bit; il ricevente prende l'informazione e la passa al data layer, che riconosce l'inizio e il termine della trama.
Per avere una comunicazione più sicura, si usano dei formati standard di impacchettamento del frame.
Uno di questi è il conteggio dei caratteri: all'inizio di ogni frame è inserito un numero che ne determina la lunghezza. *5* 1234.

Un altro metodo è quello con il flag di inizio e fine. All'inizio e alla fine di ogni messaggio si mette un flag che il ricevente riesce a riconoscere e capire dove inizia e finisce un messaggio.
In questo modo, la comunicazione inizia e termina sempre con la sequenza 01111110; questo causa il problema che questa sequenza puù essere parte del messaggio da inviare, quindi se il dispositivo rileva una sequenza di 6 bit uguali ad 1, inserisce uno 0 dopo il quinto.

<big>Controllo degli errori</big>
é possibile che in una comunicazione, un messaggio venga perduto o duplicato, oppure che arrivi un messaggio errato; quindi si usano delle tecniche di error recovery.
Alcuni protocolli inviano del bit di ridondanza, che vengono creati sulla base del frame, quindi se ci sono delle incongruenze allora vengono rimandati (ARQ - Automatic Repeat and Request) usando le tecniche di "Go back n" oppure "selective repeat".

Controllo di parità: Il frame viene suddiviso per caratteri, e ogni lettera viene codificata in bit, se i numeri 1 sono pari allora risulta 0, nel caso siano dispari è 1.

COMUNICAZIONI: 
Half-duplex: I dispositivi possono inviare e ricevere messaggi, ma non contemporaneamente.
Full-duplex: Entrambi i dispositivi possono riceve e inviare messaggi contemporaneamente, gli switch ethernet sono preimpostati con la modalità full-duplex.

Le reti LAN e WLAN, sono ad accesoo multiplo, quindi sono collegati più di 2 dispositivi.
Per queste connessioni ci sono 2 tipi di metodi di accesso:
Accesso basato sul meccanismo di contesa:
	Tutti i nodi sono in half-duplex e si contendono il supporto. Si usano procedure specifiche che sono:
		Carrier Sense Multiple Access/Collision Detection (CSMA/CD)
		Carrier Sense Multiple Access/Collision Avoidance (CSMA/CA).
Accesso Controllato:
	Usa un token che viene dato a turno ad ogni dispositivo che può inviare messaggi solo durante il suo turno.

CSMA/CD: Si basa su 2 principi fondamentali:
Ascoltare prima di parlare e
Se qualcuno inizia a pralre, smetto di parlare.
CSMA: Rileva la portante e verifica che sia libero per far iniziare la comunicazione.
CD: Rileva la collisione, quando una stazione inizia la trasmissione rimane comunque in ascolto per varificare di essere l'unica che sta parlando. Nel caso qualcun'altro inizi, allora si ferma e aspetta un tempo casuale prima di rimettersi in ascolto.

Frame Ethernet: La dimensione minima è 64 byte, la massima 1518 byte. In questo frame sono compresi gli indirizzi MAC del destinatario, mittente, il dato e il FCS (Frame Check Sequence).
I frame troppo piccoli (runt frame) o troppo grandi (jumbo/baby giant) vengono rifiutati perchè sono risultati di collisioni.

In una area coperta dal WiFi si vanno a sovrapporre le aree di comptetenza per non lasciare buchi in mezzo. Per far avvenire una comunicazione all'interno della rete allora i dispositivi devono avere lo stesso SSID.
Il wireless funziona con le onde radio, che quando incontrano un ostacolo, fanno passare una parte di onde attraverso, mentre un'altra parte viene riflessa, ciò causa perdite di potenza.

Con il Protocollo CSMA/CA, la collisione non viene rilevata, ma viene prevenuta. Il dispositivo rileva il canale e valuta se è libero, e invia un RTS(Request to Send) per richiedere la parola, e se gli viene concessa con un CTS(Clear to Send), comincia la trasmissione. Se il canale è occupato aspetta un tempo random prima di verificare di nuovo il canale.
Questo previene il problema del Terminale Nascosto, che si trova quando l'area di rilevamento di un dispotivio è troppo piccola per rilevarne un altro e non vedendosi, non sanno quando 1 dei 2 sta comunicando. Per questo interviene un Access Point che regola la trasmissione, dando il CTS solo ad 1 dei 2.

Il frame trasmesso tramite una rete WiFi, ha dentro di sè anche il MAC del router e dell'AP del destinatario e del mittente.