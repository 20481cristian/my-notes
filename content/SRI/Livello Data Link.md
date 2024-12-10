## Approfondimenti sul Data Link Layer

Il Data Link Layer, o livello di collegamento dati, è il secondo livello del modello OSI e si occupa di fornire un servizio affidabile di trasmissione dati tra due nodi direttamente collegati. Si tratta di un livello sensibile agli errori in quanto il livello fisico non si occupa di gestire o correggere gli errori di trasmissione.

**Le principali funzioni del Data Link Layer includono:**

- **Framing:** suddivisione del flusso di bit proveniente dal livello fisico in frame, ovvero unità di dati di dimensioni definite, per facilitarne la gestione e il controllo.

- **Indirizzamento fisico:** utilizzo di indirizzi MAC (Media Access Control) per identificare univocamente i nodi sulla rete locale e garantire la corretta consegna dei frame.

- **Controllo degli errori:** implementazione di meccanismi per rilevare e correggere gli errori di trasmissione che possono verificarsi sul mezzo fisico.

- **Controllo del flusso:** gestione del flusso di dati tra mittente e ricevente per evitare la saturazione del buffer del ricevente ed eventuali perdite di dati.

- **Accesso al mezzo:** accesso al mezzo di trasmissione condiviso in ambienti multi-accesso come le reti LAN, evitando collisioni tra i dati trasmessi dai diversi nodi.

**Protocolli di controllo del flusso:**

- **Stop-and-wait:** il mittente trasmette un frame e attende l'acknowledgement (ACK) dal ricevente prima di trasmettere il successivo. Questo metodo è semplice ma poco efficiente, soprattutto su collegamenti con elevata latenza.

- **Sliding-window:** il mittente può trasmettere più frame contemporaneamente senza attendere l'ACK per ogni singolo frame. Questo metodo è più efficiente in quanto sfrutta meglio la banda disponibile.

**Protocolli di controllo degli errori:**

- **ARQ (Automatic Repeat Request):** il mittente ritrasmette i frame che non vengono correttamente ricevuti dal ricevente. Esistono diverse varianti di ARQ, come Stop-and-Wait ARQ, Go-Back-N ARQ e Selective Reject ARQ.

**Esempi di protocolli a livello Data Link:**

- **HDLC (High-Level Data Link Control):** protocollo ampiamente utilizzato che definisce diversi tipi di stazioni, configurazioni di collegamento e modalità di trasferimento dati.

- **Ethernet:** famiglia di tecnologie per reti LAN che definisce specifiche per il livello fisico e il livello Data Link.

- **Wi-Fi:** famiglia di tecnologie per reti LAN wireless basate sullo standard IEEE 802.11.

