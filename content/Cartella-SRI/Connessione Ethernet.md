
Attraverso cavi CROSSOVER DTE/DCE.
Il data layer è il responsabile della trasmissione dei frame tra supporti.

Il layer incapsula i dati dal livello superiore e li INCAPSULA aggiungendo una HEADER (Infomazioni su mittente e destinatario) e un TRAILER.

Con i collegamenti seriali l'accesso è consentito solo tra 2 dispositivi, quindi non si richiedono tecniche di sincronizzazione.

Il router:
		Accetta il frame da un supporto.
		Decapsula  il frame in una PDU di livello 3.
		Ri-incapsula il frame in una PDU di livello 2.
		Invia al prossimo dispositivo il Frame.

La comunicazione in una rete LAN Ehternet segue il seguente protocollo: [[Protocollo CSMA-CD]]



La dimensione minima del frame Ethernet è di 64 byte, fino ad un massimo di 1518.
Include l'inidizzo MAC di destinazione tramite campo FCS (Frame Check Sequence).
I frame di lunghezze maggiri vengono chiamati "Jumbo" o "Baby Gigant".
Campi del frame: [[Campi Frame Ethernet]]