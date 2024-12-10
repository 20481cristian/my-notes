## Concetti Chiave del CSMA/CA

Il **CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance)** è un protocollo di accesso al mezzo utilizzato nelle reti **WLAN**, come definito dallo standard IEEE 802.11. Il suo obiettivo principale è **evitare collisioni** prima che si verifichino, poiché il rilevamento delle collisioni è difficile nelle reti wireless.

**Ecco i punti fondamentali del funzionamento del CSMA/CA:**

- **Ascolta prima di parlare (Carrier Sense):** una stazione che desidera trasmettere verifica prima se il canale è libero.
- **Attesa se occupato:** se il canale è occupato, la stazione attende un periodo di tempo casuale (DIFS - Distributed Interframe Space) prima di riprovare.
- **Richiesta di invio (RTS) e autorizzazione (CTS):** per diminuire il **problema del terminale nascosto**, la stazione mittente invia un pacchetto RTS (Request to Send) e attende un CTS (Clear To Send) dalla stazione ricevente prima di trasmettere i dati.
- **Trasmissione dati:** la trasmissione inizia dopo un breve intervallo SIFS (Short Interframe Space).
- **Conferma (ACK):** la stazione ricevente invia un ACK per confermare la corretta ricezione dei dati.

**Vantaggi di CSMA/CA:**

- **Riduzione delle collisioni:** il meccanismo RTS/CTS e i tempi di attesa (DIFS, SIFS) contribuiscono a prevenire collisioni, migliorando l'efficienza della rete.
- **Gestione del terminale nascosto:** RTS/CTS previene collisioni causate da stazioni che non possono sentirsi a vicenda.
- **Supporto per diverse velocità di dati e tecnologie di trasmissione:** lo standard IEEE 802.11 prevede diverse versioni (a, b, g, n, ac) con velocità di dati più elevate e tecnologie di trasmissione migliorate.

**Ulteriori informazioni da considerare:**

- **Point Coordination Function (PCF):** un meccanismo opzionale centralizzato che utilizza il polling per allocare l'accesso al mezzo, utile per traffico sensibile al ritardo.
- **Tipi di frame 802.11:** frame di dati, frame di controllo e frame di gestione.
- **Efficienza e throughput:** CSMA/CA può subire una riduzione dell'efficienza con un aumento del numero di stazioni e del traffico di rete.